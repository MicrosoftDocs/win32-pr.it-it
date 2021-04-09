---
title: Proprietà degli oggetti Commands
description: Proprietà degli oggetti Commands
ms.assetid: 889a56b2-0b6d-4df8-a313-7553371e4413
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4493b1e146a011434f7a0324a4008031a575d2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046580"
---
# <a name="commands-object-properties"></a>Proprietà degli oggetti Commands

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Il server supporta le seguenti proprietà per la raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) :

-   [**Didascalia**](caption-property-cmds.md)
-   [**Conteggio**](count-property.md)
-   [**DefaultCommand**](defaultcommand-property.md)
-   [**FontName**](fontname-property.md)
-   [**FontSize**](fontsize-property.md)
-   [**GlobalVoiceCommandsEnabled**](globalvoicecommandsenabled-property.md)
-   [**HelpContextID**](helpcontextid-property.md)
-   [**Visible**](visible-property-cso.md)
-   [**Chiamata vocale**](voice-property.md)
-   [**VoiceCaption**](voicecaption-property.md)

Una voce per la raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) può essere visualizzata sia nel menu a comparsa che nella finestra comandi vocali per un carattere. Per fare in modo che questa voce venga visualizzata nel menu a comparsa, impostare la relativa proprietà [**Caption**](caption-property-cmds.md) . Per includere la voce nella finestra comandi vocali, impostare la relativa proprietà [**VoiceCaption**](voicecaption-property.md) . (Per compatibilità con le versioni precedenti, se non esiste alcun **VoiceCaption**, viene utilizzata l'impostazione del **titolo** )

Nella tabella seguente viene riepilogato il modo in cui le proprietà di un oggetto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) influiscono sulla presentazione della voce:



| Proprietà Caption                                                                                                                                                                                                                                            | Proprietà Voice-Caption | Proprietà Voice | Visible (proprietà) | Viene visualizzato nel menu a comparsa del carattere | Viene visualizzato nella finestra comandi vocali |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------|----------------|------------------|------------------------------------|----------------------------------|
| Sì                                                                                                                                                                                                                                                         | Sì                    | Sì            | Vero             | Sì, uso della didascalia                 | Sì, uso di VoiceCaption          |
| Sì                                                                                                                                                                                                                                                         | Sì                    | No             | Vero             | Sì, uso della didascalia                 | No                               |
| Sì                                                                                                                                                                                                                                                         | Sì                    | Sì            | False            | No                                 | Sì, uso di VoiceCaption          |
| Sì                                                                                                                                                                                                                                                         | Sì                    | No             | False            | No                                 | No                               |
| No                                                                                                                                                                                                                                                          | Sì                    | Sì            | True             | No                                 | Sì, uso di VoiceCaption          |
| No                                                                                                                                                                                                                                                          | Sì                    | Sì            | False            | No                                 | Sì, uso di VoiceCaption          |
| No                                                                                                                                                                                                                                                          | Sì                    | No             | True             | No                                 | No                               |
| No                                                                                                                                                                                                                                                          | Sì                    | No             | False            | No                                 | No                               |
| Sì                                                                                                                                                                                                                                                         | No1                    | Sì            | Vero             | Sì, uso della didascalia                 | Sì, uso della didascalia               |
| Sì                                                                                                                                                                                                                                                         | No                     | No             | True             | Sì                                | No                               |
| Sì                                                                                                                                                                                                                                                         | No                     | Sì            | False            | No                                 | Sì, uso della didascalia               |
| Sì                                                                                                                                                                                                                                                         | No                     | No             | False            | No                                 | No                               |
| No                                                                                                                                                                                                                                                          | No                     | Sì            | True             | No                                 | No                               |
| No                                                                                                                                                                                                                                                          | No                     | Sì            | False            | No                                 | No                               |
| No                                                                                                                                                                                                                                                          | No                     | No             | True             | No                                 | No                               |
| No                                                                                                                                                                                                                                                          | No                     | No             | False            | No                                 | No                               |
|  Se l'impostazione della proprietà è null. In alcuni linguaggi di programmazione è possibile che una stringa vuota non venga interpretata come una stringa null.  Il comando è ancora accessibile tramite voce e viene visualizzato nella finestra dei comandi vocali come "(comando non definito)".<br/> |                        |                |                  |                                    |                                  |



 

 

