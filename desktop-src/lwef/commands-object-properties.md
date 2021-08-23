---
title: Proprietà dell'oggetto Commands
description: Proprietà dell'oggetto Commands
ms.assetid: 889a56b2-0b6d-4df8-a313-7553371e4413
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11b9e8f8e6e7b44697891cd567fce8ca0f5db13a0142936b5cf48bdb52721392
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716541"
---
# <a name="commands-object-properties"></a>Proprietà dell'oggetto Commands

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Il server supporta le proprietà seguenti per la [**raccolta Commands:**](/windows/desktop/lwef/the-commands-collection-object)

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

Una voce per la [**raccolta Commands**](/windows/desktop/lwef/the-commands-collection-object) può essere visualizzata sia nel menu a comparsa che nella finestra Comandi vocali per un carattere. Per visualizzare questa voce nel menu a comparsa, impostarne la [**proprietà Didascalia.**](caption-property-cmds.md) Per includere la voce nella finestra Comandi vocali, impostarne la [**proprietà VoiceCaption.**](voicecaption-property.md) Per la compatibilità con le versioni precedenti, se non è presente **VoiceCaption,** viene **usata l'impostazione Didascalia.**

La tabella seguente riepiloga in che modo le proprietà di un [**oggetto Commands**](/windows/desktop/lwef/the-commands-collection-object) influiscono sulla presentazione della voce:



| Proprietà Caption                                                                                                                                                                                                                                            | Voice-Caption proprietà | Proprietà Voice | Proprietà Visible | Viene visualizzato nel menu a comparsa del carattere | Viene visualizzato nella finestra Comandi vocali |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------|----------------|------------------|------------------------------------|----------------------------------|
| Sì                                                                                                                                                                                                                                                         | Sì                    | Sì            | Vero             | Sì, usando Didascalia                 | Sì, con VoiceCaption          |
| Sì                                                                                                                                                                                                                                                         | Sì                    | No             | Vero             | Sì, usando Didascalia                 | No                               |
| Sì                                                                                                                                                                                                                                                         | Sì                    | Sì            | False            | No                                 | Sì, con VoiceCaption          |
| Sì                                                                                                                                                                                                                                                         | Sì                    | No             | False            | No                                 | No                               |
| No                                                                                                                                                                                                                                                          | Sì                    | Sì            | True             | No                                 | Sì, con VoiceCaption          |
| No                                                                                                                                                                                                                                                          | Sì                    | Sì            | False            | No                                 | Sì, con VoiceCaption          |
| No                                                                                                                                                                                                                                                          | Sì                    | No             | True             | No                                 | No                               |
| No                                                                                                                                                                                                                                                          | Sì                    | No             | False            | No                                 | No                               |
| Sì                                                                                                                                                                                                                                                         | No1                    | Sì            | Vero             | Sì, usando Didascalia                 | Sì, usando Didascalia               |
| Sì                                                                                                                                                                                                                                                         | No                     | No             | True             | Sì                                | No                               |
| Sì                                                                                                                                                                                                                                                         | No                     | Sì            | False            | No                                 | Sì, usando Didascalia               |
| Sì                                                                                                                                                                                                                                                         | No                     | No             | False            | No                                 | No                               |
| No                                                                                                                                                                                                                                                          | No                     | Sì            | True             | No                                 | No                               |
| No                                                                                                                                                                                                                                                          | No                     | Sì            | False            | No                                 | No                               |
| No                                                                                                                                                                                                                                                          | No                     | No             | True             | No                                 | No                               |
| No                                                                                                                                                                                                                                                          | No                     | No             | False            | No                                 | No                               |
|  Se l'impostazione della proprietà è Null. In alcuni linguaggi di programmazione una stringa vuota potrebbe non essere interpretata come una stringa Null.  Il comando è ancora accessibile dalla voce e viene visualizzato nella finestra Comandi vocali come "(comando non definito)".<br/> |                        |                |                  |                                    |                                  |



 

 

