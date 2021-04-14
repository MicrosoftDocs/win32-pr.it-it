---
title: UI_PKEY_FontProperties_BackgroundColorType
description: Identifica la \_ \_ Proprietà BackgroundColorType FontProperties di pkey dell'interfaccia utente \_ .
ms.assetid: d93f4d9f-3d35-4066-be94-f6b6b4302bff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 568898cb2706eb932ea708f929aa4791f0643c74
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473267"
---
# <a name="ui_pkey_fontproperties_backgroundcolortype"></a><span data-ttu-id="5b0e2-103">Interfaccia utente \_ pkey \_ FontProperties \_ BackgroundColorType</span><span class="sxs-lookup"><span data-stu-id="5b0e2-103">UI\_PKEY\_FontProperties\_BackgroundColorType</span></span>

<span data-ttu-id="5b0e2-104">Identifica la \_ \_ Proprietà BackgroundColorType FontProperties di pkey dell'interfaccia utente \_ .</span><span class="sxs-lookup"><span data-stu-id="5b0e2-104">Identifies the UI\_PKEY\_FontProperties\_BackgroundColorType property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_BackgroundColorType
   shellPKey = UI_PKEY_FontProperties_BackgroundColorType
   formatID = 00000311-7363-696e-8441798acf5aebb7
   propID = 311
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a><span data-ttu-id="5b0e2-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="5b0e2-105">Remarks</span></span>

<span data-ttu-id="5b0e2-106">L'interfaccia utente \_ pkey \_ FontProperties \_ BackgroundColorType viene utilizzata da un'applicazione, insieme all' [interfaccia utente \_ pkey \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor), per eseguire query sulle impostazioni della raccolta **colori di evidenziazione del testo** .</span><span class="sxs-lookup"><span data-stu-id="5b0e2-106">UI\_PKEY\_FontProperties\_BackgroundColorType is used by an application, in conjunction with [UI\_PKEY\_FontProperties\_BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor), to query **Text highlight color** gallery settings.</span></span>

<span data-ttu-id="5b0e2-107">Il valore della proprietà è dall' [**enumerazione \_ SWATCHCOLORTYPE dell'interfaccia utente**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) .</span><span class="sxs-lookup"><span data-stu-id="5b0e2-107">The property value is from the [**UI\_SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) enumeration.</span></span>

<span data-ttu-id="5b0e2-108">Il valore predefinito è `UI_SWATCHCOLORTYPE_RGB`.</span><span class="sxs-lookup"><span data-stu-id="5b0e2-108">The default value is `UI_SWATCHCOLORTYPE_RGB`.</span></span>

<span data-ttu-id="5b0e2-109">Nella tabella seguente vengono descritti i valori delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="5b0e2-109">The following table describes the property values.</span></span>



|                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | <span data-ttu-id="5b0e2-110">L'applicazione deve eseguire una query sulla metrica di sistema appropriata per il valore del colore in genere il **colore di sfondo della finestra** del tema Windows corrente che viene recuperato con GetSysColor (finestra dei colori \_ ).</span><span class="sxs-lookup"><span data-stu-id="5b0e2-110">Application should query the appropriate system metric for the color value typically the current Windows theme **window background color** that is retrieved with GetSysColor(COLOR\_WINDOW).</span></span>                                                                                                                                                                                                                                                                 |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | <span data-ttu-id="5b0e2-111">Non supportato da [**FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="5b0e2-111">Not supported by the [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                |
| `UI_SWATCHCOLORTYPE_RGB`       | <span data-ttu-id="5b0e2-112">L'applicazione deve eseguire una query sull' [interfaccia utente \_ pkey \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) per il valore del colore.</span><span class="sxs-lookup"><span data-stu-id="5b0e2-112">Application should query [UI\_PKEY\_FontProperties\_BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) for the color value.</span></span> <span data-ttu-id="5b0e2-113">Il valore del colore dell' [interfaccia utente \_ pkey \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) viene visualizzato sul pulsante **colore di evidenziazione del testo** e selezionato nella raccolta colori di **evidenziazione del testo** .</span><span class="sxs-lookup"><span data-stu-id="5b0e2-113">The color value of [UI\_PKEY\_FontProperties\_BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) is displayed on the **Text highlight color** button and selected in the **Text highlight color** gallery.</span></span><br/> |



 

<span data-ttu-id="5b0e2-114">L'interfaccia utente \_ pkey \_ FontProperties \_ BackgroundColorType viene passata al metodo [**IUICommandHandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) callback quando viene selezionato un campione di colore in una raccolta **colori di evidenziazione del testo** [**FontControl**](windowsribbon-element-fontcontrol.md) .</span><span class="sxs-lookup"><span data-stu-id="5b0e2-114">UI\_PKEY\_FontProperties\_BackgroundColorType is passed to the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) callback method when a color swatch is selected in a [**FontControl**](windowsribbon-element-fontcontrol.md) **Text highlight color** gallery.</span></span>

> [!Note]  
> <span data-ttu-id="5b0e2-115">È consigliabile che l'applicazione imposti solo un valore di **colore di evidenziazione del testo** iniziale e non imposti nuovamente questo valore quando il cursore viene riposizionato all'interno di un documento.</span><span class="sxs-lookup"><span data-stu-id="5b0e2-115">It is highly recommended that the application only set an initial **Text highlight color** value and not re-set this value when the cursor is repositioned within a document.</span></span> <span data-ttu-id="5b0e2-116">L'ultima selezione deve essere mantenuta per evitare di dover selezionare di nuovo il colore desiderato.</span><span class="sxs-lookup"><span data-stu-id="5b0e2-116">The last selection should be maintained to avoid the need to re-select the desired color.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="5b0e2-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5b0e2-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b0e2-118">Proprietà del controllo del tipo di carattere</span><span class="sxs-lookup"><span data-stu-id="5b0e2-118">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="5b0e2-119">**interfaccia utente \_ SWATCHCOLORTYPE**</span><span class="sxs-lookup"><span data-stu-id="5b0e2-119">**UI\_SWATCHCOLORTYPE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[<span data-ttu-id="5b0e2-120">Controllo carattere</span><span class="sxs-lookup"><span data-stu-id="5b0e2-120">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

