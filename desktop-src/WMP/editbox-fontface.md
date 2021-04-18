---
title: CASELLA. fontFace
description: L'attributo fontFace specifica o Recupera il tipo di carattere per il testo nel controllo casella di modifica.
ms.assetid: 5fb5e6d2-8535-402e-9ca1-d43e334e94e3
keywords:
- Media Player Windows casella. fontFace
topic_type:
- apiref
api_name:
- EDITBOX.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49c5794da93821db840a48facbba45540da9249a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331589"
---
# <a name="editboxfontface"></a><span data-ttu-id="d8e31-104">CASELLA. fontFace</span><span class="sxs-lookup"><span data-stu-id="d8e31-104">EDITBOX.fontFace</span></span>

<span data-ttu-id="d8e31-105">L'attributo **fontFace** specifica o Recupera il tipo di carattere per il testo nel controllo casella di modifica.</span><span class="sxs-lookup"><span data-stu-id="d8e31-105">The **fontFace** attribute specifies or retrieves the font for text in the edit box control.</span></span>

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a><span data-ttu-id="d8e31-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="d8e31-106">Possible Values</span></span>

<span data-ttu-id="d8e31-107">Questo attributo è una **stringa** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="d8e31-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8e31-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="d8e31-108">Remarks</span></span>

<span data-ttu-id="d8e31-109">Questo attributo può essere il nome di qualsiasi tipo di carattere valido disponibile in Windows.</span><span class="sxs-lookup"><span data-stu-id="d8e31-109">This attribute can be the name of any valid font available in Windows.</span></span> <span data-ttu-id="d8e31-110">Windows Media Player non supporterà l'installazione dei tipi di carattere. Pertanto, scegliere un tipo di carattere che sarà noto nel sistema previsto.</span><span class="sxs-lookup"><span data-stu-id="d8e31-110">Windows Media Player will not support installing fonts, so choose a font that you know will be on the intended system.</span></span>

<span data-ttu-id="d8e31-111">Se il **fontFace** specificato non è disponibile nel sistema dell'utente, il controllo casella di modifica viene impostato sul tipo di carattere di sistema Windows.</span><span class="sxs-lookup"><span data-stu-id="d8e31-111">If the **fontFace** specified is not available on the user's system, the edit box control defaults to the Windows system font.</span></span> <span data-ttu-id="d8e31-112">Il valore predefinito per i sistemi in lingua inglese è "Tahoma".</span><span class="sxs-lookup"><span data-stu-id="d8e31-112">The default value for English-language systems is "Tahoma".</span></span> <span data-ttu-id="d8e31-113">Per i sistemi internazionali, il valore predefinito viene caricato da un file di risorse.</span><span class="sxs-lookup"><span data-stu-id="d8e31-113">For international systems, the default is loaded from a resource file.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8e31-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d8e31-114">Requirements</span></span>



| <span data-ttu-id="d8e31-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8e31-115">Requirement</span></span> | <span data-ttu-id="d8e31-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d8e31-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="d8e31-117">Versione</span><span class="sxs-lookup"><span data-stu-id="d8e31-117">Version</span></span><br/> | <span data-ttu-id="d8e31-118">Windows Media Player per Windows XP o versione successiva</span><span class="sxs-lookup"><span data-stu-id="d8e31-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d8e31-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d8e31-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8e31-120">**Elemento casella**</span><span class="sxs-lookup"><span data-stu-id="d8e31-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="d8e31-121">**CASELLA. fontSize**</span><span class="sxs-lookup"><span data-stu-id="d8e31-121">**EDITBOX.fontSize**</span></span>](editbox-fontsize.md)
</dt> <dt>

[<span data-ttu-id="d8e31-122">**CASELLA. fontStyle**</span><span class="sxs-lookup"><span data-stu-id="d8e31-122">**EDITBOX.fontStyle**</span></span>](editbox-fontstyle.md)
</dt> </dl>

 

 





