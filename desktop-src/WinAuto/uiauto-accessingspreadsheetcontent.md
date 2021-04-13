---
title: Accesso al contenuto del foglio di calcolo
description: Questo argomento descrive il modo in cui le applicazioni client di automazione interfaccia utente Microsoft possono accedere al contenuto di un foglio di calcolo.
ms.assetid: F32EFA46-222B-4A4E-9938-10DE0F6A2CA7
keywords:
- client, accesso al contenuto del foglio di calcolo
- client, controlli basati su testo
- client, pattern di controllo del foglio di calcolo
- client, pattern di controllo SpreadsheetItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31495086614f34aeff378a8565200fa03f2dad62
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338935"
---
# <a name="accessing-spreadsheet-content"></a>Accesso al contenuto del foglio di calcolo

Un controllo basato su testo che contiene il contenuto del foglio di calcolo può consentire ai client di accedere al contenuto supportando il [foglio di calcolo](uiauto-implementingspreadsheet.md) e i pattern di controllo [SpreadsheetItem](uiauto-implementingspreadsheetitem.md) . Questo argomento descrive il modo in cui le applicazioni client di automazione interfaccia utente Microsoft possono accedere al contenuto di un foglio di calcolo.

Per determinare se un controllo basato su testo supporta il [foglio di calcolo](uiauto-implementingspreadsheet.md) e i pattern di controllo [SpreadsheetItem](uiauto-implementingspreadsheetitem.md) , recuperare prima l'interfaccia [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) per il controllo (vedere [ottenere gli elementi di automazione interfaccia utente](uiauto-obtainingelements.md)). Chiamare quindi il metodo [**IUIAutomationElement:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) , specificando un identificatore del pattern di controllo di [**\_ SpreadsheetPatternId**](uiauto-controlpattern-ids.md) o [**UIA \_ SpreadsheetItemPatternId**](uiauto-controlpattern-ids.md)e una variante che riceve true se il controllo supporta il pattern di controllo specifico.

Per accedere al contenuto del foglio di calcolo, recuperare l'interfaccia [**IUIAutomationSpreadsheetPattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetpattern) chiamando il metodo [**IUIAutomationElement:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) e specificando [**UIA \_ SpreadsheetPatternId**](uiauto-controlpattern-ids.md) come identificatore del pattern di controllo. Usare quindi il metodo [**IUIAutomationSpreadsheetPattern:: GetItemByName**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationspreadsheetpattern-getitembyname) per ottenere l'interfaccia [**IUIAutomationSpreadsheetItem**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetitempattern) per un particolare elemento del foglio di calcolo, in genere una cella. Utilizzare le proprietà e i metodi dell'interfaccia **IUIAutomationSpreadsheetItem** per recuperare la formula per la cella e tutte le annotazioni associate alla cella. Per ulteriori informazioni sulle annotazioni, vedere [recupero di annotazioni.](uiauto-usingtextrangeobjects.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Supporto di automazione interfaccia utente per contenuto testuale](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Utilizzo di controlli basati su testo](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 