---
title: Attributo AlternateSourceURL
description: L'attributo AlternateSourceURL è un localizzatore di risorse uniforme per l'elemento multimediale che funge da alternativa agli attributi DLNASourceURI e SourceURL.
ms.assetid: 2be88d9b-4fd8-4e70-9a4d-114a2bf8b23c
keywords:
- Attributo AlternateSourceURL Windows Media Player
topic_type:
- apiref
api_name:
- AlternateSourceURL Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 574a355dfa862c4db004fa2df942e464934a38ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328126"
---
# <a name="alternatesourceurl-attribute"></a><span data-ttu-id="88fec-104">Attributo AlternateSourceURL</span><span class="sxs-lookup"><span data-stu-id="88fec-104">AlternateSourceURL Attribute</span></span>

<span data-ttu-id="88fec-105">L'attributo **AlternateSourceURL** è un localizzatore di risorse uniforme per l'elemento multimediale che funge da alternativa agli attributi [**DLNASourceURI**](dlnasourceuri-attribute.md) e [**SourceURL**](sourceurl-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="88fec-105">The **AlternateSourceURL** attribute is a uniform resource locator for the media item that serves as an alternative to the [**DLNASourceURI**](dlnasourceuri-attribute.md) and [**SourceURL**](sourceurl-attribute.md) attributes.</span></span>

## <a name="applies-to"></a><span data-ttu-id="88fec-106">Si applica a</span><span class="sxs-lookup"><span data-stu-id="88fec-106">Applies To</span></span>

-   [<span data-ttu-id="88fec-107">**Elementi audio**</span><span class="sxs-lookup"><span data-stu-id="88fec-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="88fec-108">**Elementi foto**</span><span class="sxs-lookup"><span data-stu-id="88fec-108">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="88fec-109">**Elementi della playlist**</span><span class="sxs-lookup"><span data-stu-id="88fec-109">**Playlist Items**</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="88fec-110">**Elementi video**</span><span class="sxs-lookup"><span data-stu-id="88fec-110">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="88fec-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="88fec-111">Remarks</span></span>

<span data-ttu-id="88fec-112">Questo attributo non è disponibile per gli elementi multimediali nella libreria locale dell'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="88fec-112">This attribute is not available for media items in the current user's local library.</span></span> <span data-ttu-id="88fec-113">È disponibile solo per gli elementi multimediali che appartengono a una libreria remota; ovvero una libreria che è stata resa disponibile da un altro utente nella rete domestica.</span><span class="sxs-lookup"><span data-stu-id="88fec-113">It is available only for media items that belong to a remote library; that is, a library that has been made available by another user on the home network.</span></span> <span data-ttu-id="88fec-114">Per determinare se un catalogo multimediale è remoto, chiamare [**IWMPLibrary:: Get \_ Type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span><span class="sxs-lookup"><span data-stu-id="88fec-114">To determine whether a media library is remote, call [**IWMPLibrary::get\_type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span></span>

## <a name="requirements"></a><span data-ttu-id="88fec-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="88fec-115">Requirements</span></span>



| <span data-ttu-id="88fec-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="88fec-116">Requirement</span></span> | <span data-ttu-id="88fec-117">Valore</span><span class="sxs-lookup"><span data-stu-id="88fec-117">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="88fec-118">Versione</span><span class="sxs-lookup"><span data-stu-id="88fec-118">Version</span></span><br/> | <span data-ttu-id="88fec-119">Windows Media Player 12</span><span class="sxs-lookup"><span data-stu-id="88fec-119">Windows Media Player 12</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="88fec-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="88fec-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88fec-121">**Riferimento agli attributi**</span><span class="sxs-lookup"><span data-stu-id="88fec-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





