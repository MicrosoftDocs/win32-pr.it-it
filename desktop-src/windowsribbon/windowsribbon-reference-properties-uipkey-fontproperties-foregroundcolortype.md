---
title: UI_PKEY_FontProperties_ForegroundColorType
description: Identifica la proprietà \_ FontProperties ForegroundColorType dell'interfaccia \_ \_ utente PKEY.
ms.assetid: ab04c0b0-911f-4649-9ce8-5ecd847abf9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f261256a36ee7a387c6c3a695d8c1182898690c2
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444352"
---
# <a name="ui_pkey_fontproperties_foregroundcolortype"></a><span data-ttu-id="1a1d1-103">UI \_ PKEY \_ FontProperties \_ ForegroundColorType</span><span class="sxs-lookup"><span data-stu-id="1a1d1-103">UI\_PKEY\_FontProperties\_ForegroundColorType</span></span>

<span data-ttu-id="1a1d1-104">Identifica la proprietà \_ FontProperties ForegroundColorType dell'interfaccia \_ \_ utente PKEY.</span><span class="sxs-lookup"><span data-stu-id="1a1d1-104">Identifies the UI\_PKEY\_FontProperties\_ForegroundColorType property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_ForegroundColorType
   shellPKey = UI_PKEY_FontProperties_ForegroundColorType
   formatID = 00000310-7363-696e-8441798acf5aebb7
   propID = 310
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a><span data-ttu-id="1a1d1-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="1a1d1-105">Remarks</span></span>

<span data-ttu-id="1a1d1-106">UI PKEY FontProperties ForegroundColorType viene usato da un'applicazione, insieme a \_ \_ UI \_ [ \_ PKEY \_ FontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), per eseguire query **nelle impostazioni della** raccolta colori del testo.</span><span class="sxs-lookup"><span data-stu-id="1a1d1-106">UI\_PKEY\_FontProperties\_ForegroundColorType is used by an application, in conjunction with [UI\_PKEY\_FontProperties\_ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), to query **Text color** gallery settings.</span></span>

<span data-ttu-id="1a1d1-107">Il valore della proprietà deriva [**dall'enumerazione \_ SWATCHCOLORTYPE dell'interfaccia**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) utente.</span><span class="sxs-lookup"><span data-stu-id="1a1d1-107">The property value is from the [**UI\_SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) enumeration.</span></span>

<span data-ttu-id="1a1d1-108">Il valore predefinito è `UI_SWATCHCOLORTYPE_RGB`.</span><span class="sxs-lookup"><span data-stu-id="1a1d1-108">The default value is `UI_SWATCHCOLORTYPE_RGB`.</span></span>

<span data-ttu-id="1a1d1-109">Nella tabella seguente vengono descritti i valori delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="1a1d1-109">The following table describes the property values.</span></span>



|     <span data-ttu-id="1a1d1-110">Valore</span><span class="sxs-lookup"><span data-stu-id="1a1d1-110">Value</span></span>                           |     <span data-ttu-id="1a1d1-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a1d1-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | <span data-ttu-id="1a1d1-112">Non supportato da [**FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="1a1d1-112">Not supported by the [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>                                                                                                                                                                                                                                                                                                                                        |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | <span data-ttu-id="1a1d1-113">L'applicazione deve eseguire una query sulla metrica  di sistema appropriata per il valore del colore in genere il colore corrente del testo del tema di Windows recuperato con GetSysColor(COLOR \_ WINDOWTEXT).</span><span class="sxs-lookup"><span data-stu-id="1a1d1-113">Application should query the appropriate system metric for the color value typically the current Windows theme **text color** that is retrieved with GetSysColor(COLOR\_WINDOWTEXT).</span></span>                                                                                                                                                                                                                                  |
| `UI_SWATCHCOLORTYPE_RGB`       | <span data-ttu-id="1a1d1-114">L'applicazione deve eseguire una query [ \_ PKEY \_ FontProperties \_ ForegroundColor dell'interfaccia](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) utente per il valore del colore.</span><span class="sxs-lookup"><span data-stu-id="1a1d1-114">Application should query [UI\_PKEY\_FontProperties\_ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) for the color value.</span></span> <span data-ttu-id="1a1d1-115">Il valore del colore [dell'interfaccia utente \_ PKEY \_ FontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) viene visualizzato nel pulsante **Colore** testo e selezionato nella **raccolta colori** testo.</span><span class="sxs-lookup"><span data-stu-id="1a1d1-115">The color value of [UI\_PKEY\_FontProperties\_ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) is displayed on the **Text color** button and selected in the **Text color** gallery.</span></span><br/> |



 

<span data-ttu-id="1a1d1-116">Ui PKEY FontProperties ForegroundColorType viene passato al metodo \_ \_ di callback \_ [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute)  quando viene selezionato un campione di colore in una raccolta colori [**FontControl**](windowsribbon-element-fontcontrol.md) Text.</span><span class="sxs-lookup"><span data-stu-id="1a1d1-116">UI\_PKEY\_FontProperties\_ForegroundColorType is passed to the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) callback method when a color swatch is selected in a [**FontControl**](windowsribbon-element-fontcontrol.md) **Text color** gallery.</span></span>

> [!Note]  
> <span data-ttu-id="1a1d1-117">È altamente consigliabile che l'applicazione imposta solo un valore iniziale di colore testo e non ri-impostare questo valore quando il cursore viene riposizionato all'interno di un documento. </span><span class="sxs-lookup"><span data-stu-id="1a1d1-117">It is highly recommended that the application only set an initial **Text color** value and not re-set this value when the cursor is repositioned within a document.</span></span> <span data-ttu-id="1a1d1-118">L'ultima selezione deve essere mantenuta per evitare la necessità di selezionare nuovamente il colore desiderato.</span><span class="sxs-lookup"><span data-stu-id="1a1d1-118">The last selection should be maintained to avoid the need to re-select the desired color.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1a1d1-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1a1d1-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a1d1-120">Proprietà del controllo Font</span><span class="sxs-lookup"><span data-stu-id="1a1d1-120">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="1a1d1-121">**\_SWATCHCOLORTYPE DELL'INTERFACCIA UTENTE**</span><span class="sxs-lookup"><span data-stu-id="1a1d1-121">**UI\_SWATCHCOLORTYPE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[<span data-ttu-id="1a1d1-122">Controllo Carattere</span><span class="sxs-lookup"><span data-stu-id="1a1d1-122">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

