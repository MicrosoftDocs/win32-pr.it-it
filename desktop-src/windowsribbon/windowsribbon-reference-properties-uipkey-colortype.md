---
title: UI_PKEY_ColorType
description: Identifica la proprietà ColorType dell'interfaccia utente \_ pkey \_ .
ms.assetid: 7eaa9d8b-0c21-487c-9093-79ddffcae131
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313d2a657d889a7c582d86d8f8c9e4ebd2cfd01e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338230"
---
# <a name="ui_pkey_colortype"></a><span data-ttu-id="5abea-103">Interfaccia utente \_ pkey \_ ColorType</span><span class="sxs-lookup"><span data-stu-id="5abea-103">UI\_PKEY\_ColorType</span></span>

<span data-ttu-id="5abea-104">Identifica la proprietà ColorType dell'interfaccia utente \_ pkey \_ .</span><span class="sxs-lookup"><span data-stu-id="5abea-104">Identifies the UI\_PKEY\_ColorType property.</span></span>

```
propertyDescription
   name = UI_PKEY_ColorType
   shellPKey = UI_PKEY_ColorType
   formatID = 00000401-7363-696e-8441798acf5aebb7
   propID = 401
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a><span data-ttu-id="5abea-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="5abea-105">Remarks</span></span>

<span data-ttu-id="5abea-106">L'interfaccia utente \_ pkey \_ ColorType viene usata da un'applicazione per eseguire una query sull'impostazione del colore del controllo [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) .</span><span class="sxs-lookup"><span data-stu-id="5abea-106">UI\_PKEY\_ColorType is used by an application to query color setting of the [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) control.</span></span>

<span data-ttu-id="5abea-107">Il valore della proprietà è dall' [**enumerazione \_ SWATCHCOLORTYPE dell'interfaccia utente**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) .</span><span class="sxs-lookup"><span data-stu-id="5abea-107">The property value is from the [**UI\_SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) enumeration.</span></span>



|                                |                                                                                                                                                                                 |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5abea-108">interfaccia utente \_ SWATCHCOLORTYPE \_ nocolor</span><span class="sxs-lookup"><span data-stu-id="5abea-108">UI\_SWATCHCOLORTYPE\_NOCOLOR</span></span>   | <span data-ttu-id="5abea-109">L'applicazione deve considerare l'impostazione del colore come trasparente.</span><span class="sxs-lookup"><span data-stu-id="5abea-109">Application should treat the color setting as transparent.</span></span> <span data-ttu-id="5abea-110">Viene in genere usato in combinazione con l'impostazione colori **Nessun** colore.</span><span class="sxs-lookup"><span data-stu-id="5abea-110">Typically used in conjunction with the **No color** color setting.</span></span>                                                   |
| <span data-ttu-id="5abea-111">interfaccia utente \_ SWATCHCOLORTYPE \_ automatica</span><span class="sxs-lookup"><span data-stu-id="5abea-111">UI\_SWATCHCOLORTYPE\_AUTOMATIC</span></span> | <span data-ttu-id="5abea-112">L'applicazione deve eseguire una query su [GetSysColor (Color \_ WINDOWTEXT)](/windows/win32/api/winuser/nf-winuser-getsyscolor).</span><span class="sxs-lookup"><span data-stu-id="5abea-112">Application should query [GetSysColor(COLOR\_WINDOWTEXT)](/windows/win32/api/winuser/nf-winuser-getsyscolor).</span></span> <span data-ttu-id="5abea-113">Viene in genere usato in combinazione con l'impostazione colore **automatica** .</span><span class="sxs-lookup"><span data-stu-id="5abea-113">Typically used in conjunction with the **Automatic** color setting.</span></span> |
| <span data-ttu-id="5abea-114">interfaccia utente \_ SWATCHCOLORTYPE \_ RGB</span><span class="sxs-lookup"><span data-stu-id="5abea-114">UI\_SWATCHCOLORTYPE\_RGB</span></span>       | <span data-ttu-id="5abea-115">L'applicazione deve eseguire una query sul [ \_ \_ colore pkey dell'interfaccia utente](windowsribbon-reference-properties-uipkey-color.md) per l'impostazione del colore.</span><span class="sxs-lookup"><span data-stu-id="5abea-115">Application should query [UI\_PKEY\_Color](windowsribbon-reference-properties-uipkey-color.md) for the color setting.</span></span>                                                          |



 

<span data-ttu-id="5abea-116">L'interfaccia utente \_ pkey \_ ColorType viene passata al metodo [**IUICommandHandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) callback quando viene selezionato un campione di colore in un [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span><span class="sxs-lookup"><span data-stu-id="5abea-116">UI\_PKEY\_ColorType is passed to the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) callback method when a color swatch is selected in a [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5abea-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5abea-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5abea-118">Proprietà selezione colori</span><span class="sxs-lookup"><span data-stu-id="5abea-118">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 