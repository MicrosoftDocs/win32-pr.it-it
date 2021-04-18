---
title: UI_PKEY_FontProperties_ForegroundColorType
description: Identifica la \_ \_ Proprietà ForegroundColorType FontProperties di pkey dell'interfaccia utente \_ .
ms.assetid: ab04c0b0-911f-4649-9ce8-5ecd847abf9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5589e9b21fc7ab0884a3cac51eba114ee77036b3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399282"
---
# <a name="ui_pkey_fontproperties_foregroundcolortype"></a><span data-ttu-id="d4bc0-103">Interfaccia utente \_ pkey \_ FontProperties \_ ForegroundColorType</span><span class="sxs-lookup"><span data-stu-id="d4bc0-103">UI\_PKEY\_FontProperties\_ForegroundColorType</span></span>

<span data-ttu-id="d4bc0-104">Identifica la \_ \_ Proprietà ForegroundColorType FontProperties di pkey dell'interfaccia utente \_ .</span><span class="sxs-lookup"><span data-stu-id="d4bc0-104">Identifies the UI\_PKEY\_FontProperties\_ForegroundColorType property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_ForegroundColorType
   shellPKey = UI_PKEY_FontProperties_ForegroundColorType
   formatID = 00000310-7363-696e-8441798acf5aebb7
   propID = 310
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a><span data-ttu-id="d4bc0-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="d4bc0-105">Remarks</span></span>

<span data-ttu-id="d4bc0-106">L'interfaccia utente \_ pkey \_ FontProperties \_ ForegroundColorType viene usata da un'applicazione, in combinazione con l' [interfaccia utente \_ pkey \_ FontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), per eseguire query sulle impostazioni della raccolta **colori del testo** .</span><span class="sxs-lookup"><span data-stu-id="d4bc0-106">UI\_PKEY\_FontProperties\_ForegroundColorType is used by an application, in conjunction with [UI\_PKEY\_FontProperties\_ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), to query **Text color** gallery settings.</span></span>

<span data-ttu-id="d4bc0-107">Il valore della proprietà è dall' [**enumerazione \_ SWATCHCOLORTYPE dell'interfaccia utente**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) .</span><span class="sxs-lookup"><span data-stu-id="d4bc0-107">The property value is from the [**UI\_SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) enumeration.</span></span>

<span data-ttu-id="d4bc0-108">Il valore predefinito è `UI_SWATCHCOLORTYPE_RGB`.</span><span class="sxs-lookup"><span data-stu-id="d4bc0-108">The default value is `UI_SWATCHCOLORTYPE_RGB`.</span></span>

<span data-ttu-id="d4bc0-109">Nella tabella seguente vengono descritti i valori delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="d4bc0-109">The following table describes the property values.</span></span>



|                                |                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | <span data-ttu-id="d4bc0-110">Non supportato da [**FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="d4bc0-110">Not supported by the [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>                                                                                                                                                                                                                                                                                                                                        |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | <span data-ttu-id="d4bc0-111">L'applicazione deve eseguire una query sulla metrica di sistema appropriata per il valore di colore in genere il colore corrente del **testo** del tema Windows recuperato con GETSYSCOLOR (Color \_ WINDOWTEXT).</span><span class="sxs-lookup"><span data-stu-id="d4bc0-111">Application should query the appropriate system metric for the color value typically the current Windows theme **text color** that is retrieved with GetSysColor(COLOR\_WINDOWTEXT).</span></span>                                                                                                                                                                                                                                  |
| `UI_SWATCHCOLORTYPE_RGB`       | <span data-ttu-id="d4bc0-112">L'applicazione deve eseguire una query sull' [interfaccia utente \_ pkey \_ FontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) per il valore del colore.</span><span class="sxs-lookup"><span data-stu-id="d4bc0-112">Application should query [UI\_PKEY\_FontProperties\_ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) for the color value.</span></span> <span data-ttu-id="d4bc0-113">Il valore del colore dell' [interfaccia utente \_ pkey \_ FontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) viene visualizzato sul pulsante **colore testo** e selezionato nella raccolta **colori testo** .</span><span class="sxs-lookup"><span data-stu-id="d4bc0-113">The color value of [UI\_PKEY\_FontProperties\_ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) is displayed on the **Text color** button and selected in the **Text color** gallery.</span></span><br/> |



 

<span data-ttu-id="d4bc0-114">L'interfaccia utente \_ pkey \_ FontProperties \_ ForegroundColorType viene passata al metodo [**IUICommandHandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) callback quando viene selezionato un campione di colore in una raccolta **colori del testo** [**FontControl**](windowsribbon-element-fontcontrol.md) .</span><span class="sxs-lookup"><span data-stu-id="d4bc0-114">UI\_PKEY\_FontProperties\_ForegroundColorType is passed to the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) callback method when a color swatch is selected in a [**FontControl**](windowsribbon-element-fontcontrol.md) **Text color** gallery.</span></span>

> [!Note]  
> <span data-ttu-id="d4bc0-115">È consigliabile che l'applicazione imposti solo un valore di **colore del testo** iniziale e non imposti nuovamente questo valore quando il cursore viene riposizionato all'interno di un documento.</span><span class="sxs-lookup"><span data-stu-id="d4bc0-115">It is highly recommended that the application only set an initial **Text color** value and not re-set this value when the cursor is repositioned within a document.</span></span> <span data-ttu-id="d4bc0-116">L'ultima selezione deve essere mantenuta per evitare di dover selezionare di nuovo il colore desiderato.</span><span class="sxs-lookup"><span data-stu-id="d4bc0-116">The last selection should be maintained to avoid the need to re-select the desired color.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d4bc0-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d4bc0-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4bc0-118">Proprietà del controllo del tipo di carattere</span><span class="sxs-lookup"><span data-stu-id="d4bc0-118">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="d4bc0-119">**interfaccia utente \_ SWATCHCOLORTYPE**</span><span class="sxs-lookup"><span data-stu-id="d4bc0-119">**UI\_SWATCHCOLORTYPE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[<span data-ttu-id="d4bc0-120">Controllo carattere</span><span class="sxs-lookup"><span data-stu-id="d4bc0-120">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

