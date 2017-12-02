# Material Icons for QML

```
$ git submodule add https://github.com/Adphi/QMLMaterialIcons.git
```

```
$ git submodule init
```

Add to the folder's content to the qml.qrc container.


## Usage Example:
IconButton.qml

```qml
import QtQuick 2.9
import QtQuick.Controls 2.2
import "QMLMaterialIcons" 1.0

ToolButton {
    id: toolButton
    property string icon: ""
    property color color: "white"
    Text {
        anchors.centerIn: parent
        text: toolButton.icon
        font.family: MaterialIcons.icons
        font.pointSize: 24
        opacity: 0.75
        color: toolButton.color
    }
}
```

Then :

main.qml
```qml
import QtQuick 2.9
import QtQuick.Controls 2.2
import QtQuick.Layouts 1.3
import QtQuick.Controls.Material 2.2
import "QMLMaterialIcons" 1.0


ApplicationWindow {
    visible: true
    width: 640
    height: 480
    title: qsTr("QML Material Icons")

    Material.theme: Material.Dark
    Material.primary: "black"
    property color textColor: "white"

    header: ToolBar {
        id: toolBar
        RowLayout {
            anchors.fill: parent

            IconButton {
                id: menuButton
                icon: MaterialIcons.iMenu
                color: "white"
            }

            Text {
                text: qsTr("QML Material Icons")
                color: textColor
                opacity: 0.8
                font.pointSize: 20
                Layout.fillWidth: true
                elide: Label.ElideRight
            }

            IconButton {
                id: moreButton
                icon: MaterialIcons.iMore_vert
                color: "white"
            }
        }
    }

}
```

Enjoy the auto-completion.

https://material.io/icons/
