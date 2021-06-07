---
title: UI_PKEY_FontProperties_BackgroundColorType
description: Identifica la proprietà \_ FontProperties BackgroundColorType dell'interfaccia \_ \_ utente PKEY.
ms.assetid: d93f4d9f-3d35-4066-be94-f6b6b4302bff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45bbd2056087d584663c8ca716c4021554098dfa
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443822"
---
# <a name="ui_pkey_fontproperties_backgroundcolortype"></a><span data-ttu-id="a1039-103">UI \_ PKEY \_ FontProperties \_ BackgroundColorType</span><span class="sxs-lookup"><span data-stu-id="a1039-103">UI\_PKEY\_FontProperties\_BackgroundColorType</span></span>

<span data-ttu-id="a1039-104">Identifica la proprietà \_ FontProperties BackgroundColorType dell'interfaccia \_ \_ utente PKEY.</span><span class="sxs-lookup"><span data-stu-id="a1039-104">Identifies the UI\_PKEY\_FontProperties\_BackgroundColorType property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_BackgroundColorType
   shellPKey = UI_PKEY_FontProperties_BackgroundColorType
   formatID = 00000311-7363-696e-8441798acf5aebb7
   propID = 311
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a><span data-ttu-id="a1039-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="a1039-105">Remarks</span></span>

<span data-ttu-id="a1039-106">UI PKEY FontProperties BackgroundColorType viene usato da un'applicazione, in combinazione con UI \_ \_ \_ [ \_ PKEY \_ FontProperties \_ BackgroundColor,](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor)per eseguire query nelle impostazioni della raccolta colori **evidenziazione** testo.</span><span class="sxs-lookup"><span data-stu-id="a1039-106">UI\_PKEY\_FontProperties\_BackgroundColorType is used by an application, in conjunction with [UI\_PKEY\_FontProperties\_BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor), to query **Text highlight color** gallery settings.</span></span>

<span data-ttu-id="a1039-107">Il valore della proprietà deriva [**dall'enumerazione \_ SWATCHCOLORTYPE dell'interfaccia**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) utente.</span><span class="sxs-lookup"><span data-stu-id="a1039-107">The property value is from the [**UI\_SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) enumeration.</span></span>

<span data-ttu-id="a1039-108">Il valore predefinito è `UI_SWATCHCOLORTYPE_RGB`.</span><span class="sxs-lookup"><span data-stu-id="a1039-108">The default value is `UI_SWATCHCOLORTYPE_RGB`.</span></span>

<span data-ttu-id="a1039-109">Nella tabella seguente vengono descritti i valori delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="a1039-109">The following table describes the property values.</span></span>



|   <span data-ttu-id="a1039-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a1039-110">Property</span></span>                             |   <span data-ttu-id="a1039-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1039-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | <span data-ttu-id="a1039-112">L'applicazione deve eseguire una query sulla metrica  di sistema appropriata per il valore del colore in genere il colore di sfondo corrente della finestra del tema di Windows recuperato con GetSysColor(COLOR \_ WINDOW).</span><span class="sxs-lookup"><span data-stu-id="a1039-112">Application should query the appropriate system metric for the color value typically the current Windows theme **window background color** that is retrieved with GetSysColor(COLOR\_WINDOW).</span></span>                                                                                                                                                                                                                                                                 |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | <span data-ttu-id="a1039-113">Non supportato da [**FontControl.**](windowsribbon-element-fontcontrol.md)</span><span class="sxs-lookup"><span data-stu-id="a1039-113">Not supported by the [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                |
| `UI_SWATCHCOLORTYPE_RGB`       | <span data-ttu-id="a1039-114">L'applicazione deve eseguire una query [ \_ dell'interfaccia utente PKEY \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) per il valore del colore.</span><span class="sxs-lookup"><span data-stu-id="a1039-114">Application should query [UI\_PKEY\_FontProperties\_BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) for the color value.</span></span> <span data-ttu-id="a1039-115">Il valore del colore [dell'interfaccia utente \_ PKEY \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) viene visualizzato nel pulsante **Colore** evidenziazione testo e selezionato nella raccolta colori **evidenziazione** testo.</span><span class="sxs-lookup"><span data-stu-id="a1039-115">The color value of [UI\_PKEY\_FontProperties\_BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) is displayed on the **Text highlight color** button and selected in the **Text highlight color** gallery.</span></span><br/> |



 

<span data-ttu-id="a1039-116">UI PKEY FontProperties BackgroundColorType viene passato al metodo \_ \_ di callback \_ [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute)  quando viene selezionato un campione di colore in una raccolta colori di evidenziazione del testo [**FontControl.**](windowsribbon-element-fontcontrol.md)</span><span class="sxs-lookup"><span data-stu-id="a1039-116">UI\_PKEY\_FontProperties\_BackgroundColorType is passed to the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) callback method when a color swatch is selected in a [**FontControl**](windowsribbon-element-fontcontrol.md) **Text highlight color** gallery.</span></span>

> [!Note]  
> <span data-ttu-id="a1039-117">È consigliabile che l'applicazione  imposta solo un valore iniziale per il colore di evidenziazione testo e non lo riposiziona quando il cursore viene riposizionato all'interno di un documento.</span><span class="sxs-lookup"><span data-stu-id="a1039-117">It is highly recommended that the application only set an initial **Text highlight color** value and not re-set this value when the cursor is repositioned within a document.</span></span> <span data-ttu-id="a1039-118">L'ultima selezione deve essere mantenuta per evitare la necessità di selezionare nuovamente il colore desiderato.</span><span class="sxs-lookup"><span data-stu-id="a1039-118">The last selection should be maintained to avoid the need to re-select the desired color.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a1039-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a1039-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1039-120">Proprietà del controllo Font</span><span class="sxs-lookup"><span data-stu-id="a1039-120">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="a1039-121">**\_SWATCHCOLORTYPE DELL'INTERFACCIA UTENTE**</span><span class="sxs-lookup"><span data-stu-id="a1039-121">**UI\_SWATCHCOLORTYPE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[<span data-ttu-id="a1039-122">Controllo Font</span><span class="sxs-lookup"><span data-stu-id="a1039-122">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

