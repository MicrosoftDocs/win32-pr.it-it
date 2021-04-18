---
title: LISTBOX. fontFace
description: L'attributo fontFace specifica o Recupera il tipo di carattere per il controllo casella di riepilogo.
ms.assetid: 15e3180a-6e1e-4654-a0bb-164d66a86a26
keywords:
- Media Player di Windows LISTBOX. fontFace
topic_type:
- apiref
api_name:
- LISTBOX.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82c03c367001b307dd8bd5059ec7e3f4a0b364e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327749"
---
# <a name="listboxfontface"></a><span data-ttu-id="9991d-104">LISTBOX. fontFace</span><span class="sxs-lookup"><span data-stu-id="9991d-104">LISTBOX.fontFace</span></span>

<span data-ttu-id="9991d-105">L'attributo **fontFace** specifica o Recupera il tipo di carattere per il controllo casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="9991d-105">The **fontFace** attribute specifies or retrieves the font for the list box control.</span></span>

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a><span data-ttu-id="9991d-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="9991d-106">Possible Values</span></span>

<span data-ttu-id="9991d-107">Questo attributo è una **stringa** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="9991d-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9991d-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="9991d-108">Remarks</span></span>

<span data-ttu-id="9991d-109">Questo attributo può essere il nome di qualsiasi tipo di carattere valido disponibile in Windows.</span><span class="sxs-lookup"><span data-stu-id="9991d-109">This attribute can be the name of any valid font available in Windows.</span></span> <span data-ttu-id="9991d-110">Windows Media Player non supporterà l'installazione dei tipi di carattere. Pertanto, scegliere un tipo di carattere che sarà noto nel sistema previsto.</span><span class="sxs-lookup"><span data-stu-id="9991d-110">Windows Media Player will not support installing fonts, so choose a font that you know will be on the intended system.</span></span>

<span data-ttu-id="9991d-111">Se il **fontFace** specificato non è disponibile nel sistema dell'utente, l'impostazione predefinita del controllo casella di riepilogo è il tipo di carattere di sistema Windows.</span><span class="sxs-lookup"><span data-stu-id="9991d-111">If the **fontFace** specified is not available on the user's system, the list box control defaults to the Windows system font.</span></span> <span data-ttu-id="9991d-112">Il valore predefinito per i sistemi in lingua inglese è "Tahoma".</span><span class="sxs-lookup"><span data-stu-id="9991d-112">The default value for English-language systems is "Tahoma".</span></span> <span data-ttu-id="9991d-113">Per i sistemi internazionali, il valore predefinito viene caricato da un file di risorse.</span><span class="sxs-lookup"><span data-stu-id="9991d-113">For international systems, the default is loaded from a resource file.</span></span>

## <a name="requirements"></a><span data-ttu-id="9991d-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9991d-114">Requirements</span></span>



| <span data-ttu-id="9991d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9991d-115">Requirement</span></span> | <span data-ttu-id="9991d-116">Valore</span><span class="sxs-lookup"><span data-stu-id="9991d-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="9991d-117">Versione</span><span class="sxs-lookup"><span data-stu-id="9991d-117">Version</span></span><br/> | <span data-ttu-id="9991d-118">Windows Media Player per Windows XP o versione successiva</span><span class="sxs-lookup"><span data-stu-id="9991d-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9991d-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9991d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9991d-120">**LISTBOX (elemento)**</span><span class="sxs-lookup"><span data-stu-id="9991d-120">**LISTBOX Element**</span></span>](listbox-element.md)
</dt> <dt>

[<span data-ttu-id="9991d-121">**LISTBOX. fontSize**</span><span class="sxs-lookup"><span data-stu-id="9991d-121">**LISTBOX.fontSize**</span></span>](listbox-fontsize.md)
</dt> <dt>

[<span data-ttu-id="9991d-122">**LISTBOX. fontStyle**</span><span class="sxs-lookup"><span data-stu-id="9991d-122">**LISTBOX.fontStyle**</span></span>](listbox-fontstyle.md)
</dt> </dl>

 

 





