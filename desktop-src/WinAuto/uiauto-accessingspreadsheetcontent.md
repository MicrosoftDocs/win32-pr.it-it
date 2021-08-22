---
title: Accesso al contenuto del foglio di calcolo
description: Questo argomento descrive in che modo Microsoft Automazione interfaccia utente applicazioni client possono accedere al contenuto di un foglio di calcolo.
ms.assetid: F32EFA46-222B-4A4E-9938-10DE0F6A2CA7
keywords:
- client, accesso al contenuto del foglio di calcolo
- client, controlli basati su testo
- client, pattern di controllo foglio di calcolo
- client,pattern di controllo SpreadsheetItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f09d34aeb484da056920a2b77d47ca199e11c00c99832412e9bf007807c49563
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052349"
---
# <a name="accessing-spreadsheet-content"></a>Accesso al contenuto del foglio di calcolo

Un controllo basato su testo che contiene contenuto del foglio di calcolo può consentire ai client di accedere al contenuto supportando i pattern di controllo [Spreadsheet](uiauto-implementingspreadsheet.md) e [SpreadsheetItem.](uiauto-implementingspreadsheetitem.md) Questo argomento descrive in che modo Microsoft Automazione interfaccia utente applicazioni client possono accedere al contenuto di un foglio di calcolo.

Per determinare se un controllo basato su testo supporta i pattern di controllo [Spreadsheet](uiauto-implementingspreadsheet.md) e [SpreadsheetItem,](uiauto-implementingspreadsheetitem.md) recuperare prima di tutto l'interfaccia [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) per il controllo [Automazione interfaccia utente](uiauto-obtainingelements.md).) Chiamare quindi il metodo [**IUIAutomationElement::GetCurrentPattern,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) specificando un identificatore del pattern di controllo [**UIA \_ SpreadsheetPatternId**](uiauto-controlpattern-ids.md) o [**UIA \_ SpreadsheetItemPatternId**](uiauto-controlpattern-ids.md)e una variante che riceve TRUE se il controllo supporta il pattern di controllo specifico.

Per accedere al contenuto del foglio di calcolo, recuperare [**l'interfaccia IUIAutomationSpreadsheetPattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetpattern) chiamando il metodo [**IUIAutomationElement::GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) e specificando [**UIA \_ SpreadsheetPatternId**](uiauto-controlpattern-ids.md) come identificatore del pattern di controllo. Usare quindi il metodo [**IUIAutomationSpreadsheetPattern::GetItemByName**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationspreadsheetpattern-getitembyname) per ottenere [**l'interfaccia IUIAutomationSpreadsheetItem**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetitempattern) per un particolare elemento del foglio di calcolo (in genere una cella). Usare le proprietà e i metodi **dell'interfaccia IUIAutomationSpreadsheetItem** per recuperare la formula per la cella e le eventuali annotazioni associate alla cella. Per altre informazioni sulle annotazioni, vedere [Recupero di annotazioni.](uiauto-usingtextrangeobjects.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Automazione interfaccia utente supporto per il contenuto testuale](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Uso di controlli basati su testo](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 