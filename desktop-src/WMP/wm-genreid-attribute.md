---
title: Attributo WM/GenreID
description: L'attributo WM/GenreID è un identificatore di genere conforme al tag TCON in ID3v2.
ms.assetid: 9b68f9be-1f02-4b14-b052-90657b8800e3
keywords:
- Media Player Windows per gli attributi WM/GenreID
topic_type:
- apiref
api_name:
- WM/GenreID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d31e54805f778a51f345c84654056391ec4052e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327014"
---
# <a name="wmgenreid-attribute"></a><span data-ttu-id="0c52b-104">Attributo WM/GenreID</span><span class="sxs-lookup"><span data-stu-id="0c52b-104">WM/GenreID Attribute</span></span>

<span data-ttu-id="0c52b-105">L'attributo **WM/GenreID** è un identificatore di genere conforme al tag TCON in id3v2.</span><span class="sxs-lookup"><span data-stu-id="0c52b-105">The **WM/GenreID** attribute is a genre identifier compliant with the TCON tag in ID3v2.</span></span>

## <a name="applies-to"></a><span data-ttu-id="0c52b-106">Si applica a</span><span class="sxs-lookup"><span data-stu-id="0c52b-106">Applies To</span></span>

-   [<span data-ttu-id="0c52b-107">Elementi audio</span><span class="sxs-lookup"><span data-stu-id="0c52b-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="0c52b-108">Attributi di file di Windows Media usati di frequente</span><span class="sxs-lookup"><span data-stu-id="0c52b-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="0c52b-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="0c52b-109">Remarks</span></span>

<span data-ttu-id="0c52b-110">Questo attributo viene archiviato solo nel file multimediale digitale.</span><span class="sxs-lookup"><span data-stu-id="0c52b-110">This attribute is stored only in the digital media file.</span></span>

<span data-ttu-id="0c52b-111">La versione 2 di ID3 è una convenzione di assegnazione di tag originariamente progettata per il formato MP3.</span><span class="sxs-lookup"><span data-stu-id="0c52b-111">ID3 version 2 is a tagging convention that was originally designed for MP3.</span></span> <span data-ttu-id="0c52b-112">Per ulteriori informazioni, vedere il [sito Web dell'organizzazione ID3](https://id3.org/).</span><span class="sxs-lookup"><span data-stu-id="0c52b-112">For more information, see the [ID3 organization's website](https://id3.org/).</span></span>

<span data-ttu-id="0c52b-113">La costante Windows Media Format SDK per questo attributo è g \_ wszGenreID.</span><span class="sxs-lookup"><span data-stu-id="0c52b-113">The Windows Media Format SDK constant for this attribute is g\_wszGenreID.</span></span>

<span data-ttu-id="0c52b-114">Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="0c52b-114">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c52b-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0c52b-115">Requirements</span></span>



| <span data-ttu-id="0c52b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c52b-116">Requirement</span></span> | <span data-ttu-id="0c52b-117">Valore</span><span class="sxs-lookup"><span data-stu-id="0c52b-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c52b-118">Versione</span><span class="sxs-lookup"><span data-stu-id="0c52b-118">Version</span></span><br/> | <span data-ttu-id="0c52b-119">Windows Media Player 9 Series Windows Media Player 10 o versioni successive non supporta questo attributo</span><span class="sxs-lookup"><span data-stu-id="0c52b-119">Windows Media Player 9 Series Windows Media Player 10 or later does not support this attribute</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0c52b-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0c52b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c52b-121">**Riferimento agli attributi**</span><span class="sxs-lookup"><span data-stu-id="0c52b-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





