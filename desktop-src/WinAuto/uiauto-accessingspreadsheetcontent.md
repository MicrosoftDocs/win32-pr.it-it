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
# <a name="accessing-spreadsheet-content"></a><span data-ttu-id="f5f89-107">Accesso al contenuto del foglio di calcolo</span><span class="sxs-lookup"><span data-stu-id="f5f89-107">Accessing Spreadsheet Content</span></span>

<span data-ttu-id="f5f89-108">Un controllo basato su testo che contiene il contenuto del foglio di calcolo può consentire ai client di accedere al contenuto supportando il [foglio di calcolo](uiauto-implementingspreadsheet.md) e i pattern di controllo [SpreadsheetItem](uiauto-implementingspreadsheetitem.md) .</span><span class="sxs-lookup"><span data-stu-id="f5f89-108">A text-based control that contains spreadsheet content can enable clients to access the content by supporting the [Spreadsheet](uiauto-implementingspreadsheet.md) and [SpreadsheetItem](uiauto-implementingspreadsheetitem.md) control patterns.</span></span> <span data-ttu-id="f5f89-109">Questo argomento descrive il modo in cui le applicazioni client di automazione interfaccia utente Microsoft possono accedere al contenuto di un foglio di calcolo.</span><span class="sxs-lookup"><span data-stu-id="f5f89-109">This topic describes how Microsoft UI Automation client applications can access the content of a spreadsheet.</span></span>

<span data-ttu-id="f5f89-110">Per determinare se un controllo basato su testo supporta il [foglio di calcolo](uiauto-implementingspreadsheet.md) e i pattern di controllo [SpreadsheetItem](uiauto-implementingspreadsheetitem.md) , recuperare prima l'interfaccia [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) per il controllo (vedere [ottenere gli elementi di automazione interfaccia utente](uiauto-obtainingelements.md)). Chiamare quindi il metodo [**IUIAutomationElement:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) , specificando un identificatore del pattern di controllo di [**\_ SpreadsheetPatternId**](uiauto-controlpattern-ids.md) o [**UIA \_ SpreadsheetItemPatternId**](uiauto-controlpattern-ids.md)e una variante che riceve true se il controllo supporta il pattern di controllo specifico.</span><span class="sxs-lookup"><span data-stu-id="f5f89-110">To determine whether a text-based control supports the [Spreadsheet](uiauto-implementingspreadsheet.md) and [SpreadsheetItem](uiauto-implementingspreadsheetitem.md) control patterns, first retrieve the [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) interface for the control (see [Obtaining UI Automation Elements](uiauto-obtainingelements.md).) Next, call the [**IUIAutomationElement::GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) method, specifying a control pattern identifier of [**UIA\_SpreadsheetPatternId**](uiauto-controlpattern-ids.md) or [**UIA\_SpreadsheetItemPatternId**](uiauto-controlpattern-ids.md), and a variant that receives TRUE if the control supports the particular control pattern.</span></span>

<span data-ttu-id="f5f89-111">Per accedere al contenuto del foglio di calcolo, recuperare l'interfaccia [**IUIAutomationSpreadsheetPattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetpattern) chiamando il metodo [**IUIAutomationElement:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) e specificando [**UIA \_ SpreadsheetPatternId**](uiauto-controlpattern-ids.md) come identificatore del pattern di controllo.</span><span class="sxs-lookup"><span data-stu-id="f5f89-111">To access the spreadsheet content, retrieve the [**IUIAutomationSpreadsheetPattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetpattern) interface by calling [**IUIAutomationElement::GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) method and specifying [**UIA\_SpreadsheetPatternId**](uiauto-controlpattern-ids.md) as the control pattern identifier.</span></span> <span data-ttu-id="f5f89-112">Usare quindi il metodo [**IUIAutomationSpreadsheetPattern:: GetItemByName**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationspreadsheetpattern-getitembyname) per ottenere l'interfaccia [**IUIAutomationSpreadsheetItem**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetitempattern) per un particolare elemento del foglio di calcolo, in genere una cella.</span><span class="sxs-lookup"><span data-stu-id="f5f89-112">Next, use the [**IUIAutomationSpreadsheetPattern::GetItemByName**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationspreadsheetpattern-getitembyname) method to get the [**IUIAutomationSpreadsheetItem**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetitempattern) interface for a particular spreadsheet item (typically a cell).</span></span> <span data-ttu-id="f5f89-113">Utilizzare le proprietà e i metodi dell'interfaccia **IUIAutomationSpreadsheetItem** per recuperare la formula per la cella e tutte le annotazioni associate alla cella.</span><span class="sxs-lookup"><span data-stu-id="f5f89-113">Use the properties and methods of the **IUIAutomationSpreadsheetItem** interface to retrieve the formula for the cell, and any annotations associated with the cell.</span></span> <span data-ttu-id="f5f89-114">Per ulteriori informazioni sulle annotazioni, vedere [recupero di annotazioni.](uiauto-usingtextrangeobjects.md)</span><span class="sxs-lookup"><span data-stu-id="f5f89-114">For more information about annotations, see [Retrieving Annotations.](uiauto-usingtextrangeobjects.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="f5f89-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f5f89-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5f89-116">Supporto di automazione interfaccia utente per contenuto testuale</span><span class="sxs-lookup"><span data-stu-id="f5f89-116">UI Automation Support for Textual Content</span></span>](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[<span data-ttu-id="f5f89-117">Utilizzo di controlli basati su testo</span><span class="sxs-lookup"><span data-stu-id="f5f89-117">Working with Text-based Controls</span></span>](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 