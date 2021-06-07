---
title: UI_PKEY_ColorType
description: Identifica la proprietà \_ PKEY \_ ColorType dell'interfaccia utente.
ms.assetid: 7eaa9d8b-0c21-487c-9093-79ddffcae131
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9240d8c816adcf2674efcc2e7428d22b765f542
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443892"
---
# <a name="ui_pkey_colortype"></a><span data-ttu-id="ca705-103">Tipo \_ di colore PKEY \_ dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="ca705-103">UI\_PKEY\_ColorType</span></span>

<span data-ttu-id="ca705-104">Identifica la proprietà \_ PKEY \_ ColorType dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ca705-104">Identifies the UI\_PKEY\_ColorType property.</span></span>

```
propertyDescription
   name = UI_PKEY_ColorType
   shellPKey = UI_PKEY_ColorType
   formatID = 00000401-7363-696e-8441798acf5aebb7
   propID = 401
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a><span data-ttu-id="ca705-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="ca705-105">Remarks</span></span>

<span data-ttu-id="ca705-106">Ui PKEY ColorType viene usato da un'applicazione per eseguire query sull'impostazione del \_ colore del controllo \_ [**DropDownColorPicker.**](windowsribbon-element-dropdowncolorpicker.md)</span><span class="sxs-lookup"><span data-stu-id="ca705-106">UI\_PKEY\_ColorType is used by an application to query color setting of the [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) control.</span></span>

<span data-ttu-id="ca705-107">Il valore della proprietà deriva [**dall'enumerazione \_ SWATCHCOLORTYPE dell'interfaccia**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) utente.</span><span class="sxs-lookup"><span data-stu-id="ca705-107">The property value is from the [**UI\_SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) enumeration.</span></span>



|    <span data-ttu-id="ca705-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ca705-108">Property</span></span>                            |    <span data-ttu-id="ca705-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca705-109">Description</span></span>                                                                                                                                                                             |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca705-110">UI \_ SWATCHCOLORTYPE \_ NOCOLOR</span><span class="sxs-lookup"><span data-stu-id="ca705-110">UI\_SWATCHCOLORTYPE\_NOCOLOR</span></span>   | <span data-ttu-id="ca705-111">L'applicazione deve considerare l'impostazione del colore trasparente.</span><span class="sxs-lookup"><span data-stu-id="ca705-111">Application should treat the color setting as transparent.</span></span> <span data-ttu-id="ca705-112">Usato in genere insieme **all'impostazione Nessun colore.**</span><span class="sxs-lookup"><span data-stu-id="ca705-112">Typically used in conjunction with the **No color** color setting.</span></span>                                                   |
| <span data-ttu-id="ca705-113">UI \_ SWATCHCOLORTYPE \_ AUTOMATIC</span><span class="sxs-lookup"><span data-stu-id="ca705-113">UI\_SWATCHCOLORTYPE\_AUTOMATIC</span></span> | <span data-ttu-id="ca705-114">L'applicazione deve eseguire una query [su GetSysColor(COLOR \_ WINDOWTEXT)](/windows/win32/api/winuser/nf-winuser-getsyscolor).</span><span class="sxs-lookup"><span data-stu-id="ca705-114">Application should query [GetSysColor(COLOR\_WINDOWTEXT)](/windows/win32/api/winuser/nf-winuser-getsyscolor).</span></span> <span data-ttu-id="ca705-115">In genere usato in combinazione con **l'impostazione Del** colore automatico.</span><span class="sxs-lookup"><span data-stu-id="ca705-115">Typically used in conjunction with the **Automatic** color setting.</span></span> |
| <span data-ttu-id="ca705-116">RGB \_ SWATCHCOLORTYPE \_ dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="ca705-116">UI\_SWATCHCOLORTYPE\_RGB</span></span>       | <span data-ttu-id="ca705-117">L'applicazione deve eseguire una query [sul \_ colore PKEY \_ dell'interfaccia](windowsribbon-reference-properties-uipkey-color.md) utente per l'impostazione del colore.</span><span class="sxs-lookup"><span data-stu-id="ca705-117">Application should query [UI\_PKEY\_Color](windowsribbon-reference-properties-uipkey-color.md) for the color setting.</span></span>                                                          |



 

<span data-ttu-id="ca705-118">Ui PKEY ColorType viene passato al metodo \_ \_ di callback [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) quando viene selezionato un campione di colore in [**un controllo DropDownColorPicker.**](windowsribbon-element-dropdowncolorpicker.md)</span><span class="sxs-lookup"><span data-stu-id="ca705-118">UI\_PKEY\_ColorType is passed to the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) callback method when a color swatch is selected in a [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca705-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ca705-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca705-120">Selezione colori proprietà</span><span class="sxs-lookup"><span data-stu-id="ca705-120">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 