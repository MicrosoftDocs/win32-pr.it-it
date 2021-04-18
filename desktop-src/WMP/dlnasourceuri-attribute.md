---
title: Attributo DLNASourceURI
description: L'attributo DLNASourceURI è l'URI (Universal Resource Identifier) dell'elemento.
ms.assetid: 323c897b-9b76-44f7-9313-c51595589583
keywords:
- Attributo DLNASourceURI Windows Media Player
topic_type:
- apiref
api_name:
- DLNASourceURI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96ebe21a39a67dec9356c5dd5360efb48f4ef029
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327169"
---
# <a name="dlnasourceuri-attribute"></a><span data-ttu-id="31df1-104">Attributo DLNASourceURI</span><span class="sxs-lookup"><span data-stu-id="31df1-104">DLNASourceURI Attribute</span></span>

<span data-ttu-id="31df1-105">L'attributo **DLNASourceURI** è l'URI (Universal Resource Identifier) dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="31df1-105">The **DLNASourceURI** attribute is the universal resource identifier (URI) of the item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="31df1-106">Si applica a</span><span class="sxs-lookup"><span data-stu-id="31df1-106">Applies To</span></span>

-   [<span data-ttu-id="31df1-107">**Elementi audio**</span><span class="sxs-lookup"><span data-stu-id="31df1-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="31df1-108">**Altri elementi**</span><span class="sxs-lookup"><span data-stu-id="31df1-108">**Other Items**</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="31df1-109">**Elementi foto**</span><span class="sxs-lookup"><span data-stu-id="31df1-109">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="31df1-110">**Elementi della playlist**</span><span class="sxs-lookup"><span data-stu-id="31df1-110">**Playlist Items**</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="31df1-111">**Elementi video**</span><span class="sxs-lookup"><span data-stu-id="31df1-111">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="31df1-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="31df1-112">Remarks</span></span>

<span data-ttu-id="31df1-113">Se l'elemento si trova nella libreria locale dell'utente corrente, questo attributo, l'attributo [**SourceURL**](sourceurl-attribute.md) e il valore restituito da [**IWMPMedia:: Get \_ SourceURL**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_sourceurl) sono tutti uguali.</span><span class="sxs-lookup"><span data-stu-id="31df1-113">If the item is in the current user's local library, this attribute, the [**SourceURL**](sourceurl-attribute.md) attribute, and the value returned by [**IWMPMedia::get\_sourceURL**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_sourceurl) are all the same.</span></span>

<span data-ttu-id="31df1-114">Se l'elemento non è presente nella libreria locale dell'utente corrente, ma appartiene a una libreria remota, questo attributo è un identificatore del formato DLNA-playsingle://*xxx*.</span><span class="sxs-lookup"><span data-stu-id="31df1-114">If the item is not in the current user's local library, but belongs to a remote library, this attribute is an identifier of the form dlna-playsingle://*xxx*.</span></span>

<span data-ttu-id="31df1-115">È possibile passare un URI DLNA-playsingle al metodo [**IWMPCore3:: newMedia**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore3-newmedia) per ottenere un'interfaccia [**IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) che consente di visualizzare i metadati dell'elemento multimediale e di modificare potenzialmente la classificazione a stelle dell'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="31df1-115">You can pass a dlna-playsingle URI to the [**IWMPCore3::newMedia**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore3-newmedia) method to obtain an [**IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) interface that enables you to view the media item's metadata and potentially edit the media item's star rating.</span></span> <span data-ttu-id="31df1-116">Si noti, tuttavia, che l'URI DLNA-playsingle deve essere per un servizio di directory del contenuto (CDS) già individuato da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="31df1-116">Note, however, that the dlna-playsingle URI must be for a content directory service (CDS) that Windows Media Player has already discovered.</span></span> <span data-ttu-id="31df1-117">Il metodo **newMedia** non avvierà l'individuazione UPnP e cercherà i CD.</span><span class="sxs-lookup"><span data-stu-id="31df1-117">The **newMedia** method will not initiate UPnP discovery and search for the CDS.</span></span>

<span data-ttu-id="31df1-118">È possibile modificare la classificazione a stelle di un elemento multimediale in una libreria remota solo se la libreria remota supporta l'operazione di modifica.</span><span class="sxs-lookup"><span data-stu-id="31df1-118">You can edit the star rating of a media item in a remote library only if the remote library supports the edit operation.</span></span> <span data-ttu-id="31df1-119">Le librerie remote ospitate in un computer che esegue Windows 7 supportano l'operazione di modifica.</span><span class="sxs-lookup"><span data-stu-id="31df1-119">Remote libraries hosted on a computer running Windows 7 support the edit operation.</span></span> <span data-ttu-id="31df1-120">Le librerie remote ospitate in un computer che esegue un sistema operativo Windows precedente a Windows 7 non supportano l'operazione di modifica.</span><span class="sxs-lookup"><span data-stu-id="31df1-120">Remote libraries hosted on a computer running a Windows operating system earlier than Windows 7 do not support the edit operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="31df1-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="31df1-121">Requirements</span></span>



| <span data-ttu-id="31df1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="31df1-122">Requirement</span></span> | <span data-ttu-id="31df1-123">Valore</span><span class="sxs-lookup"><span data-stu-id="31df1-123">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="31df1-124">Versione</span><span class="sxs-lookup"><span data-stu-id="31df1-124">Version</span></span><br/> | <span data-ttu-id="31df1-125">Windows Media Player 12</span><span class="sxs-lookup"><span data-stu-id="31df1-125">Windows Media Player 12</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="31df1-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="31df1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31df1-127">**Riferimento agli attributi**</span><span class="sxs-lookup"><span data-stu-id="31df1-127">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





