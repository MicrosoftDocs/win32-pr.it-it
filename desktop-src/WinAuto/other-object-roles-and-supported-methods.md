---
title: Altri ruoli oggetto e metodi supportati (riferimento all'elemento dell'interfaccia utente MSAA)
description: In questo argomento vengono fornite informazioni sui ruoli degli oggetti che non sono inclusi negli argomenti precedenti per gli elementi dell'interfaccia utente.
ms.assetid: 0c3a3ccf-f02a-4aca-9380-a13774598a19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f3d7fbdbb6dfbf83729f3e1c1d4caa3027f8d51
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729026"
---
# <a name="other-object-roles-and-supported-methods-msaa-ui-element-reference"></a>Altri ruoli oggetto e metodi supportati (riferimento all'elemento dell'interfaccia utente MSAA)

In questo argomento vengono fornite informazioni sui ruoli degli oggetti che non sono inclusi negli argomenti precedenti per gli elementi dell'interfaccia utente. Ogni ruolo di oggetto include un elenco dei metodi e delle proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) supportati per il ruolo dell'oggetto. Mentre altri argomenti documentano i metodi e le proprietà **IAccessible** supportati per gli elementi dell'interfaccia utente, in questo argomento vengono elencati i metodi e le proprietà che possono essere supportati per un particolare ruolo dell'oggetto. Molti degli elementi dell'interfaccia utente che possono avere uno dei ruoli elencati di seguito vengono in genere visualizzati nei browser.

> [!Note]  
> Usare questo argomento come linee guida. Si consiglia vivamente di utilizzare gli strumenti di Microsoft Active Accessibility per verificare il comportamento previsto per un singolo ruolo di un oggetto.

 

Nella tabella seguente sono elencati i ruoli oggetto aggiuntivi Oleacc.dll supportati da.



|                                                                         |                                                           |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [**\_avviso di sistema del ruolo \_**](/windows)                           | [**\_elenco a \_ selezione sistema ruolo**](/windows)       |
| [**\_applicazione di sistema ruolo \_**](/windows)               | [**\_equazione del sistema di ruolo \_**](/windows)       |
| [**\_bordo sistema \_ ruolo**](/windows)                         | [**\_rappresentazione grafica del sistema di ruoli \_**](/windows)         |
| [**\_BUTTONDROPDOWN di sistema ruolo \_**](/windows)         | [**\_HELPBALLOON di sistema ruolo \_**](/windows) |
| [**\_BUTTONDROPDOWNGRID di sistema ruolo \_**](/windows) | [**\_IPAddress sistema \_ ruolo**](/windows)     |
| [**\_BUTTONMENU di sistema ruolo \_**](/windows)                 | [**\_collegamento del sistema ruolo \_**](/windows)               |
| [**\_cella del sistema del ruolo \_**](/windows)                             | [**\_riquadro sistema \_ ruoli**](/windows)               |
| [**\_carattere di sistema ruolo \_**](/windows)                   | [**\_riga sistema \_ ruolo**](/windows)                 |
| [**\_grafico del sistema di ruoli \_**](/windows)                           | [**\_ROWHEADER di sistema ruolo \_**](/windows)     |
| [**\_clock di sistema del ruolo \_**](/windows)                           | [**\_separatore di sistema ruolo \_**](/windows)     |
| [**\_colonna di sistema del ruolo \_**](/windows)                         | [**\_suono del sistema di ruolo \_**](/windows)             |
| [**\_diagramma del sistema di ruoli \_**](/windows)                       | [**\_SPLITBUTTON di sistema ruolo \_**](/windows) |
| [**\_Composizione sistema \_ ruolo**](/windows)                             | [**\_tabella di sistema del ruolo \_**](/windows)             |
| [**\_documento di sistema del ruolo \_**](/windows)                     | [**\_spazio del sistema ruolo \_**](/windows)   |



 

## <a name="role_system_alert"></a>\_avviso di sistema del ruolo \_

Per ulteriori informazioni su questo ruolo, vedere [**\_ \_ avviso di sistema dei ruoli**](object-roles.md).

**Proprietà e metodi supportati**

-   ottenere \_ accName
-   ottenere \_ accRole
-   ottenere \_ accState

## <a name="role_system_application"></a>\_applicazione di sistema ruolo \_

Per altre informazioni su questo ruolo, vedere [**\_ \_ applicazione di sistema dei ruoli**](object-roles.md).

**Proprietà e metodi supportati**

-   accHitTest
-   accLocation
-   accNavigate
-   ottenere \_ accChild
-   ottenere \_ accChildCount
-   ottenere \_ accFocus
-   ottenere \_ accHelp
-   ottenere \_ accHelpTopic
-   ottenere \_ accKeyboardShortcut
-   ottenere \_ accName
-   ottenere \_ accParent
-   ottenere \_ accRole
-   ottenere \_ accState

## <a name="role_system_border"></a>\_bordo sistema \_ ruolo

Per ulteriori informazioni su questo ruolo, vedere [**\_ \_ bordo del sistema dei ruoli**](object-roles.md).

**Proprietà e metodi supportati**

-   accHitTest
-   accLocation
-   accNavigate
-   ottenere \_ accRole
-   ottenere \_ accState

## <a name="role_system_buttondropdown"></a>\_BUTTONDROPDOWN di sistema ruolo \_

Per ulteriori informazioni su questo ruolo, vedere [**ruolo del \_ sistema \_ BUTTONDROPDOWN**](object-roles.md).

**Proprietà e metodi supportati**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   ottenere \_ accChild
-   ottenere \_ accChildCount
-   ottenere \_ accDefaultAction
-   ottenere \_ accFocus
-   ottenere \_ accHelp
-   ottenere \_ accHelpTopic
-   ottenere \_ accKeyboardShortcut
-   ottenere \_ accName
-   ottenere \_ accParent
-   ottenere \_ accRole
-   ottenere \_ accState

## <a name="role_system_buttondropdowngrid"></a>\_BUTTONDROPDOWNGRID di sistema ruolo \_

Per ulteriori informazioni su questo ruolo, vedere [**ruolo del \_ sistema \_ BUTTONDROPDOWNGRID**](object-roles.md).

**Proprietà e metodi supportati**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   ottenere \_ accChild
-   ottenere \_ accChildCount
-   ottenere \_ accDefaultAction
-   ottenere \_ accFocus
-   ottenere \_ accHelp
-   ottenere \_ accHelpTopic
-   ottenere \_ accKeyboardShortcut
-   ottenere \_ accName
-   ottenere \_ accParent
-   ottenere \_ accRole
-   ottenere \_ accState

## <a name="role_system_buttonmenu"></a>\_BUTTONMENU di sistema ruolo \_

Per ulteriori informazioni su questo ruolo, vedere [**ruolo del \_ sistema \_ BUTTONMENU**](object-roles.md).

**Proprietà e metodi supportati**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   ottenere \_ accDefaultAction
-   ottenere \_ accFocus
-   ottenere \_ accHelp
-   ottenere \_ accHelpTopic
-   ottenere \_ accKeyboardShortcut
-   ottenere \_ accName
-   ottenere \_ accParent
-   ottenere \_ accRole
-   ottenere \_ accState

## <a name="role_system_cell"></a>\_cella del sistema del ruolo \_

Per ulteriori informazioni su questo ruolo, vedere [**\_ \_ cella del sistema del ruolo**](object-roles.md).

**Proprietà e metodi supportati**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   ottenere \_ accChild
-   ottenere \_ accChildCount
-   ottenere \_ accFocus
-   ottenere \_ accHelp
-   ottenere \_ accHelpTopic
-   ottenere \_ accKeyboardShortcut
-   ottenere \_ accName
-   ottenere \_ accParent
-   ottenere \_ accRole
-   ottenere \_ accState
-   ottenere \_ accValue

## <a name="role_system_character"></a>\_carattere di sistema ruolo \_

Per ulteriori informazioni su questo ruolo, vedere [**Role \_ System \_ character**](object-roles.md).

**Proprietà e metodi supportati**

-   accHitTest
-   accLocation
-   accNavigate
-   ottenere \_ accDescription
-   ottenere \_ accFocus
-   ottenere \_ accKeyboardShortcut
-   ottenere \_ accName
-   ottenere \_ accParent
-   ottenere \_ accRole
-   ottenere \_ accState
-   ottenere \_ accValue

## <a name="role_system_chart"></a>\_grafico del sistema di ruoli \_

Per ulteriori informazioni su questo ruolo, vedere [**il \_ \_ grafico del sistema dei ruoli**](object-roles.md).

**Proprietà e metodi supportati**

-   accHitTest
-   accLocation
-   accNavigate
-   ottenere \_ accChild
-   ottenere \_ accChildCount
-   ottenere \_ accFocus
-   ottenere \_ accHelp
-   ottenere \_ accHelpTopic
-   ottenere \_ accKeyboardShortcut
-   ottenere \_ accName
-   ottenere \_ accParent
-   ottenere \_ accRole
-   ottenere \_ accState

## <a name="role_system_clock"></a>\_clock di sistema del ruolo \_

Per altre informazioni su questo ruolo, vedere [**\_ \_ clock di sistema del ruolo**](object-roles.md).

**Proprietà e metodi supportati**

-   accHitTest
-   accLocation
-   accNavigate
-   ottenere \_ accFocus
-   ottenere \_ accHelp
-   ottenere \_ accHelpTopic
-   ottenere \_ accKeyboardShortcut
-   ottenere \_ accName
-   ottenere \_ accParent
-   ottenere \_ accRole
-   ottenere \_ accState
-   ottenere \_ accValue

## <a name="role_system_column"></a>\_colonna di sistema del ruolo \_

Per ulteriori informazioni su questo ruolo, vedere [**\_ \_ colonna di sistema del ruolo**](object-roles.md).

**Proprietà e metodi supportati**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   ottenere \_ accChild
-   ottenere \_ accChildCount
-   ottenere \_ accFocus
-   ottenere \_ accName
-   ottenere \_ accParent
-   ottenere \_ accRole
-   ottenere \_ accState
-   ottenere \_ accValue

## <a name="role_system_diagram"></a>\_diagramma del sistema di ruoli \_

Per altre informazioni su questo ruolo, vedere [**\_ \_ diagramma di sistema dei ruoli**](object-roles.md).

**Proprietà e metodi supportati**

-   accHitTest
-   accLocation
-   accNavigate
-   ottenere \_ accChild
-   ottenere \_ accChildCount
-   ottenere \_ accFocus
-   ottenere \_ accHelp
-   ottenere \_ accHelpTopic
-   ottenere \_ accKeyboardShortcut
-   ottenere \_ accName
-   ottenere \_ accParent
-   ottenere \_ accRole
-   ottenere \_ accState

## <a name="role_system_dial"></a>\_Composizione sistema \_ ruolo

Per ulteriori informazioni su questo ruolo, vedere la pagina relativa alla [**\_ \_ composizione del sistema di ruoli**](object-roles.md).

**Proprietà e metodi supportati**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   ottenere \_ accDefaultAction
-   ottenere \_ accFocus
-   ottenere \_ accHelp
-   ottenere \_ accHelpTopic
-   ottenere \_ accKeyboardShortcut
-   ottenere \_ accName
-   ottenere \_ accParent
-   ottenere \_ accRole
-   ottenere \_ accState
-   ottenere \_ accValue

## <a name="role_system_document"></a>\_documento di sistema del ruolo \_

Per ulteriori informazioni su questo ruolo, vedere [**il \_ \_ documento di sistema dei ruoli**](object-roles.md).

**Proprietà e metodi supportati**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   ottenere \_ accChild
-   ottenere \_ accChildCount
-   ottenere \_ accFocus
-   ottenere \_ accName
-   ottenere \_ accParent
-   ottenere \_ accRole
-   ottenere \_ accState

## <a name="role_system_droplist"></a>\_elenco a \_ selezione sistema ruolo

Per ulteriori informazioni su questo ruolo, vedere la pagina relativa all' [**\_ \_ elenco**](object-roles.md)a discapito di sistema dei ruoli.

**Proprietà e metodi supportati**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   ottenere \_ accChild
-   ottenere \_ accChildCount
-   ottenere \_ accDefaultAction
-   ottenere \_ accFocus
-   ottenere \_ accHelp
-   ottenere \_ accHelpTopic
-   ottenere \_ accKeyboardShortcut
-   ottenere \_ accName
-   ottenere \_ accParent
-   ottenere \_ accRole
-   ottenere \_ accState

## <a name="role_system_equation"></a>\_equazione del sistema di ruolo \_

Per altre informazioni su questo ruolo, vedere [**\_ \_ equazione del sistema di ruolo**](object-roles.md).

**Proprietà e metodi supportati**

-   accHitTest
-   accLocation
-   accNavigate
-   ottenere \_ accFocus
-   ottenere \_ accName
-   ottenere \_ accParent
-   ottenere \_ accRole
-   ottenere \_ accState
-   ottenere \_ accValue

## <a name="role_system_graphic"></a>\_rappresentazione grafica del sistema di ruoli \_

Per altre informazioni su questo ruolo, vedere [**\_ \_ Graphic System Role**](object-roles.md).

**Proprietà e metodi supportati**

-   accHitTest
-   accLocation
-   accNavigate
-   ottenere \_ accFocus
-   ottenere \_ accHelp
-   ottenere \_ accHelpTopic
-   ottenere \_ accKeyboardShortcut
-   ottenere \_ accName
-   ottenere \_ accParent
-   ottenere \_ accRole
-   ottenere \_ accState

## <a name="role_system_helpballoon"></a>\_HELPBALLOON di sistema ruolo \_

Per ulteriori informazioni su questo ruolo, vedere [**ruolo del \_ sistema \_ HELPBALLOON**](object-roles.md).

**Proprietà e metodi supportati**

-   accHitTest
-   accLocation
-   accNavigate
-   ottenere \_ accChild
-   ottenere \_ accChildCount
-   ottenere \_ accDefaultAction
-   ottenere \_ accName
-   ottenere \_ accParent
-   ottenere \_ accRole
-   ottenere \_ accState
-   ottenere \_ accValue

## <a name="role_system_ipaddress"></a>\_IPAddress sistema \_ ruolo

Per ulteriori informazioni su questo ruolo, vedere [**Role \_ System \_ IPAddress**](object-roles.md).

**Proprietà e metodi supportati**

-   accHitTest
-   accLocation
-   accNavigate
-   ottenere \_ accChild
-   ottenere \_ accChildCount
-   ottenere \_ accFocus
-   ottenere \_ accHelp
-   ottenere \_ accHelpTopic
-   ottenere \_ accKeyboardShortcut
-   ottenere \_ accName
-   ottenere \_ accParent
-   ottenere \_ accRole
-   ottenere \_ accState
-   ottenere \_ accValue

## <a name="role_system_link"></a>\_collegamento del sistema ruolo \_

Per ulteriori informazioni su questo ruolo, vedere [**\_ \_ collegamento del sistema di ruolo**](object-roles.md).

**Proprietà e metodi supportati**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   ottenere \_ accChild
-   ottenere \_ accChildCount
-   ottenere \_ accDefaultAction
-   ottenere \_ accDescription
-   ottenere \_ accFocus
-   ottenere \_ accKeyboardShortcut
-   ottenere \_ accName
-   ottenere \_ accParent
-   ottenere \_ accRole
-   ottenere \_ accState
-   ottenere \_ accValue

## <a name="role_system_pane"></a>\_riquadro sistema \_ ruoli

Per ulteriori informazioni su questo ruolo, vedere [**\_ \_ riquadro sistema ruoli**](object-roles.md).

**Proprietà e metodi supportati**

-   accHitTest
-   accLocation
-   accNavigate
-   ottenere \_ accChild
-   ottenere \_ accChildCount
-   ottenere \_ accFocus
-   ottenere \_ accHelp
-   ottenere \_ accHelpTopic
-   ottenere \_ accKeyboardShortcut
-   ottenere \_ accName
-   ottenere \_ accParent
-   ottenere \_ accRole
-   ottenere \_ accState

## <a name="role_system_row"></a>\_riga sistema \_ ruolo

Per ulteriori informazioni su questo ruolo, vedere [**\_ \_ riga di sistema del ruolo**](object-roles.md).

**Proprietà e metodi supportati**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   ottenere \_ accChild
-   ottenere \_ accChildCount
-   ottenere \_ accDescription
-   ottenere \_ accFocus
-   ottenere \_ accName
-   ottenere \_ accParent
-   ottenere \_ accRole
-   ottenere \_ accState
-   ottenere \_ accValue

## <a name="role_system_rowheader"></a>\_ROWHEADER di sistema ruolo \_

Per ulteriori informazioni su questo ruolo, vedere [**ruolo del \_ sistema \_ ROWHEADER**](object-roles.md).

**Proprietà e metodi supportati**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   ottenere \_ accChild
-   ottenere \_ accChildCount
-   ottenere \_ accDefaultAction
-   ottenere \_ accDescription
-   ottenere \_ accFocus
-   ottenere \_ accName
-   ottenere \_ accParent
-   ottenere \_ accRole
-   ottenere \_ accState
-   ottenere \_ accValue

## <a name="role_system_separator"></a>\_separatore di sistema ruolo \_

Per ulteriori informazioni su questo ruolo, vedere [**\_ \_ separatore di sistema dei ruoli**](object-roles.md).

**Proprietà e metodi supportati**

-   accHitTest
-   accLocation
-   ottenere \_ accChild
-   ottenere \_ accChildCount
-   ottenere \_ accParent
-   ottenere \_ accRole
-   ottenere \_ accState

## <a name="role_system_sound"></a>\_suono del sistema di ruolo \_

Per altre informazioni su questo ruolo, vedere [**\_ \_ suono del sistema di ruolo**](object-roles.md).

**Proprietà e metodi supportati**

-   ottenere \_ accDescription
-   ottenere \_ accName
-   ottenere \_ accRole
-   ottenere \_ accState

## <a name="role_system_splitbutton"></a>\_SPLITBUTTON di sistema ruolo \_

Per ulteriori informazioni su questo ruolo, vedere [**ruolo del \_ sistema \_ SPLITBUTTON**](object-roles.md).

**Proprietà e metodi supportati**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   ottenere \_ accDefaultAction
-   ottenere \_ accHelp
-   ottenere \_ accHelpTopic
-   ottenere \_ accKeyboardShortcut
-   ottenere \_ accName
-   ottenere \_ accParent
-   ottenere \_ accRole
-   ottenere \_ accState

## <a name="role_system_table"></a>\_tabella di sistema del ruolo \_

Per altre informazioni su questo ruolo, vedere [**\_ \_ tabella di sistema dei ruoli**](object-roles.md).

**Proprietà e metodi supportati**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   ottenere \_ accChild
-   ottenere \_ accChildCount
-   ottenere \_ accDescription
-   ottenere \_ accFocus
-   ottenere \_ accHelp
-   ottenere \_ accHelpTopic
-   ottenere \_ accKeyboardShortcut
-   ottenere \_ accName
-   ottenere \_ accParent
-   ottenere \_ accRole
-   ottenere \_ accState

## <a name="role_system_whitespace"></a>\_spazio del sistema ruolo \_

Per altre informazioni su questo ruolo, vedere [**\_ \_ spazio del sistema dei ruoli**](object-roles.md).

**Proprietà e metodi supportati**

-   accLocation
-   accSelect
-   ottenere \_ accParent
-   ottenere \_ accRole
-   ottenere \_ accState

 

 