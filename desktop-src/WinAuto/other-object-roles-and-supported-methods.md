---
title: Altri ruoli oggetto e metodi supportati (riferimento agli elementi dell'interfaccia utente MSAA)
description: In questo argomento vengono fornite informazioni sui ruoli oggetto non inclusi negli argomenti precedenti per gli elementi dell'interfaccia utente.
ms.assetid: 0c3a3ccf-f02a-4aca-9380-a13774598a19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4e29a4ef0345513912c8ad08e3a322e01b56bd3245291e9def64a49b35ac22b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052569"
---
# <a name="other-object-roles-and-supported-methods-msaa-ui-element-reference"></a>Altri ruoli oggetto e metodi supportati (riferimento agli elementi dell'interfaccia utente MSAA)

In questo argomento vengono fornite informazioni sui ruoli oggetto non inclusi negli argomenti precedenti per gli elementi dell'interfaccia utente. Ogni ruolo oggetto include un elenco dei metodi e delle proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) supportati per il ruolo oggetto. Mentre altri argomenti documentano i metodi e le proprietà **IAccessible** supportati per gli elementi dell'interfaccia utente, questo argomento elenca i metodi e le proprietà che ci si può aspettare di essere supportati per un particolare ruolo oggetto. Molti degli elementi dell'interfaccia utente che potrebbero avere uno dei ruoli elencati di seguito sono in genere visibili nei browser.

> [!Note]  
> Usare questo argomento come linea guida. È consigliabile usare gli strumenti Microsoft Active Accessibility per verificare il comportamento previsto per un singolo ruolo oggetto.

 

Nella tabella seguente sono elencati i ruoli oggetto aggiuntivi Oleacc.dll supportati.



| &nbsp; |  &nbsp; |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [**AVVISO DEL \_ SISTEMA DEL \_ RUOLO**](/windows)                           | [**ROLE \_ SYSTEM \_ DROPLIST**](/windows)       |
| [**APPLICAZIONE DEL \_ SISTEMA RUOLO \_**](/windows)               | [**EQUAZIONE \_ DEL SISTEMA \_ DI RUOLI**](/windows)       |
| [**BORDO DEL \_ SISTEMA \_ DI RUOLI**](/windows)                         | [**IMMAGINE DEL \_ SISTEMA \_ RUOLO**](/windows)         |
| [**ROLE \_ SYSTEM \_ BUTTONDROPDOWN**](/windows)         | [**GUIDA \_ DEL SISTEMA DEI \_ RUOLIBALLOON**](/windows) |
| [**PULSANTE \_ SISTEMA \_ RUOLODROPDOWNGRID**](/windows) | [**ROLE \_ SYSTEM \_ IPADDRESS**](/windows)     |
| [**ROLE \_ SYSTEM \_ BUTTONMENU**](/windows)                 | [**COLLEGAMENTO SISTEMA \_ \_ RUOLO**](/windows)               |
| [**CELLA \_ DEL SISTEMA \_ RUOLO**](/windows)                             | [**RIQUADRO \_ SISTEMA \_ RUOLO**](/windows)               |
| [**ROLE \_ SYSTEM \_ CHARACTER**](/windows)                   | [**ROLE \_ SYSTEM \_ ROW**](/windows)                 |
| [**ROLE \_ SYSTEM \_ CHART**](/windows)                           | [**ROLE \_ SYSTEM \_ ROWHEADER**](/windows)     |
| [**ROLE \_ SYSTEM \_ CLOCK**](/windows)                           | [**ROLE \_ SYSTEM \_ SEPARATOR**](/windows)     |
| [**ROLE \_ SYSTEM \_ COLUMN**](/windows)                         | [**SUONO \_ DEL SISTEMA DEL \_ RUOLO**](/windows)             |
| [**DIAGRAMMA DEL \_ SISTEMA DI \_ RUOLI**](/windows)                       | [**RUOLO \_ SISTEMA \_ SPLITBUTTON**](/windows) |
| [**ROLE \_ SYSTEM \_ DIAL**](/windows)                             | [**TABELLA \_ DI SISTEMA DEI \_ RUOLI**](/windows)             |
| [**DOCUMENTO \_ DI SISTEMA DEL \_ RUOLO**](/windows)                     | [**SPAZIO \_ VUOTO DEL SISTEMA DI \_ RUOLI**](/windows)   |



 

## <a name="role_system_alert"></a>AVVISO DEL \_ SISTEMA DEL \_ RUOLO

Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ ALERT**](object-roles.md).

**Proprietà e metodi supportati**

-   get \_ accName
-   get \_ accRole
-   get \_ accState

## <a name="role_system_application"></a>APPLICAZIONE DEL \_ SISTEMA RUOLO \_

Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ APPLICATION.**](object-roles.md)

**Proprietà e metodi supportati**

-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_border"></a>BORDO DEL \_ SISTEMA \_ DI RUOLI

Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ BORDER.**](object-roles.md)

**Proprietà e metodi supportati**

-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accRole
-   get \_ accState

## <a name="role_system_buttondropdown"></a>ROLE \_ SYSTEM \_ BUTTONDROPDOWN

Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ BUTTONDROPDOWN**](object-roles.md).

**Proprietà e metodi supportati**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accDefaultAction
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_buttondropdowngrid"></a>PULSANTE \_ SISTEMA \_ RUOLODROPDOWNGRID

Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ BUTTONDROPDOWNGRID**](object-roles.md).

**Proprietà e metodi supportati**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accDefaultAction
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_buttonmenu"></a>ROLE \_ SYSTEM \_ BUTTONMENU

Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ BUTTONMENU**](object-roles.md).

**Proprietà e metodi supportati**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accDefaultAction
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_cell"></a>CELLA \_ DEL SISTEMA \_ RUOLO

Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ CELL**](object-roles.md).

**Proprietà e metodi supportati**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_character"></a>ROLE \_ SYSTEM \_ CHARACTER

Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ CHARACTER**](object-roles.md).

**Proprietà e metodi supportati**

-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accDescription
-   get \_ accFocus
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_chart"></a>ROLE \_ SYSTEM \_ CHART

Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ CHART.**](object-roles.md)

**Proprietà e metodi supportati**

-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_clock"></a>ROLE \_ SYSTEM \_ CLOCK

Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ CLOCK**](object-roles.md).

**Proprietà e metodi supportati**

-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_column"></a>ROLE \_ SYSTEM \_ COLUMN

Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ COLUMN.**](object-roles.md)

**Proprietà e metodi supportati**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accFocus
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_diagram"></a>DIAGRAMMA DEL \_ SISTEMA DI \_ RUOLI

Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ DIAGRAM**](object-roles.md).

**Proprietà e metodi supportati**

-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_dial"></a>ROLE \_ SYSTEM \_ DIAL

Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ DIAL.**](object-roles.md)

**Proprietà e metodi supportati**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accDefaultAction
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_document"></a>DOCUMENTO \_ DI SISTEMA DEL \_ RUOLO

Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ DOCUMENT**](object-roles.md).

**Proprietà e metodi supportati**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accFocus
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_droplist"></a>ROLE \_ SYSTEM \_ DROPLIST

Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ DROPLIST**](object-roles.md).

**Proprietà e metodi supportati**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accDefaultAction
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_equation"></a>EQUAZIONE \_ DEL SISTEMA \_ DI RUOLI

Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ EQUATION**](object-roles.md).

**Proprietà e metodi supportati**

-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accFocus
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_graphic"></a>IMMAGINE DEL \_ SISTEMA \_ RUOLO

Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ GRAPHIC.**](object-roles.md)

**Proprietà e metodi supportati**

-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_helpballoon"></a>GUIDA \_ DEL SISTEMA DEI \_ RUOLIBALLOON

Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ HELPBALLOON**](object-roles.md).

**Proprietà e metodi supportati**

-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accDefaultAction
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_ipaddress"></a>INDIRIZZO \_ IP DEL SISTEMA DEL \_ RUOLO

Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ IPADDRESS**](object-roles.md).

**Proprietà e metodi supportati**

-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accFocus
-   ottenere \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_link"></a>COLLEGAMENTO \_ AL SISTEMA DEL \_ RUOLO

Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ LINK**](object-roles.md).

**Proprietà e metodi supportati**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accDefaultAction
-   get \_ accDescription
-   get \_ accFocus
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_pane"></a>RIQUADRO \_ SISTEMA \_ RUOLO

Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ PANE**](object-roles.md).

**Proprietà e metodi supportati**

-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accFocus
-   ottenere \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_row"></a>ROLE \_ SYSTEM \_ ROW

Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ ROW**](object-roles.md).

**Proprietà e metodi supportati**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accDescription
-   get \_ accFocus
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_rowheader"></a>ROLE \_ SYSTEM \_ ROWHEADER

Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ ROWHEADER**](object-roles.md).

**Proprietà e metodi supportati**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accDefaultAction
-   get \_ accDescription
-   get \_ accFocus
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_separator"></a>SEPARATORE \_ DI SISTEMA DEI \_ RUOLI

Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ SEPARATOR**](object-roles.md).

**Proprietà e metodi supportati**

-   accHitTest
-   accLocation
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_sound"></a>SUONO \_ DEL SISTEMA DEI \_ RUOLI

Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ SOUND**](object-roles.md).

**Proprietà e metodi supportati**

-   get \_ accDescription
-   get \_ accName
-   get \_ accRole
-   get \_ accState

## <a name="role_system_splitbutton"></a>ROLE \_ SYSTEM \_ SPLITBUTTON

Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ SPLITBUTTON**](object-roles.md).

**Proprietà e metodi supportati**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accDefaultAction
-   ottenere \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_table"></a>TABELLA \_ DI SISTEMA DEI \_ RUOLI

Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ TABLE**](object-roles.md).

**Proprietà e metodi supportati**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accDescription
-   get \_ accFocus
-   ottenere \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_whitespace"></a>SPAZIO \_ VUOTO DEL SISTEMA DEI \_ RUOLI

Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ WHITESPACE**](object-roles.md).

**Proprietà e metodi supportati**

-   accLocation
-   accSelect
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

 

 