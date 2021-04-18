---
title: TESTO. fontFace
description: L'attributo fontFace specifica o Recupera il carattere tipografico per il controllo di testo.
ms.assetid: 3b39e245-139a-4361-b678-0f9e962996b7
keywords:
- Media Player di Windows TEXT. fontFace
topic_type:
- apiref
api_name:
- TEXT.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 183b25547e456cb90cac4d2137354679e13d8a96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329426"
---
# <a name="textfontface"></a><span data-ttu-id="d485a-104">TESTO. fontFace</span><span class="sxs-lookup"><span data-stu-id="d485a-104">TEXT.fontFace</span></span>

<span data-ttu-id="d485a-105">L'attributo **fontFace** specifica o Recupera il carattere tipografico per il controllo di testo.</span><span class="sxs-lookup"><span data-stu-id="d485a-105">The **fontFace** attribute specifies or retrieves the typeface for the Text control.</span></span>

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a><span data-ttu-id="d485a-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="d485a-106">Possible Values</span></span>

<span data-ttu-id="d485a-107">Questo attributo è una **stringa** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="d485a-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d485a-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="d485a-108">Remarks</span></span>

<span data-ttu-id="d485a-109">Questo attributo può essere il nome di qualsiasi tipo di carattere valido disponibile in Windows.</span><span class="sxs-lookup"><span data-stu-id="d485a-109">This attribute can be the name of any valid font available on Windows.</span></span> <span data-ttu-id="d485a-110">Windows Media Player non supporterà l'installazione dei tipi di carattere. Pertanto, scegliere un tipo di carattere che sarà noto nel sistema previsto.</span><span class="sxs-lookup"><span data-stu-id="d485a-110">Windows Media Player will not support installing fonts, so choose a font that you know will be on the intended system.</span></span>

<span data-ttu-id="d485a-111">Se il **fontFace** specificato non è disponibile nel sistema dell'utente, per impostazione predefinita il controllo testo è il tipo di carattere di sistema Windows.</span><span class="sxs-lookup"><span data-stu-id="d485a-111">If the **fontFace** specified is not available on the user's system, the Text control defaults to the Windows system font.</span></span>

<span data-ttu-id="d485a-112">Vedere l'attributo [value](text-value.md) per un esempio che illustra la modalità di utilizzo degli attributi dell'elemento di **testo** .</span><span class="sxs-lookup"><span data-stu-id="d485a-112">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="d485a-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d485a-113">Requirements</span></span>



| <span data-ttu-id="d485a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d485a-114">Requirement</span></span> | <span data-ttu-id="d485a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="d485a-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="d485a-116">Versione</span><span class="sxs-lookup"><span data-stu-id="d485a-116">Version</span></span><br/> | <span data-ttu-id="d485a-117">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="d485a-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d485a-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d485a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d485a-119">**Elemento TEXT**</span><span class="sxs-lookup"><span data-stu-id="d485a-119">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="d485a-120">**TESTO. fontSize**</span><span class="sxs-lookup"><span data-stu-id="d485a-120">**TEXT.fontSize**</span></span>](text-fontsize.md)
</dt> </dl>

 

 





