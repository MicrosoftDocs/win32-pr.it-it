---
title: Attributo DTCPIPPort
description: L'attributo DTCPIPPort è il numero di porta Transmission Control Protocol (TCP) del computer o del dispositivo che deve essere contattato per lo scambio di chiave autenticato di trasmissione digitale protezione del contenuto over Internet Protocol (DTCP-IP) per l'elemento multimediale.
ms.assetid: 63767ec1-dd01-40c2-bf9a-6e9b8a7db7f8
keywords:
- Attributo DTCPIPPort Windows Media Player
topic_type:
- apiref
api_name:
- DTCPIPPort Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16c1c6117425211c0015d218412c8a9ac0971d7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333930"
---
# <a name="dtcpipport-attribute"></a><span data-ttu-id="6c548-104">Attributo DTCPIPPort</span><span class="sxs-lookup"><span data-stu-id="6c548-104">DTCPIPPort Attribute</span></span>

<span data-ttu-id="6c548-105">L'attributo **DTCPIPPort** è il numero di porta Transmission Control Protocol (TCP) del computer o del dispositivo che deve essere contattato per lo scambio di chiave autenticato di trasmissione digitale protezione del contenuto over Internet Protocol (DTCP-IP) per l'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="6c548-105">The **DTCPIPPort** attribute is the Transmission Control Protocol (TCP) port number of the computer or device that must be contacted for the Digital Transmission Content Protection over Internet Protocol (DTCP-IP) Authenticated Key Exchange (AKE) for the media item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="6c548-106">Si applica a</span><span class="sxs-lookup"><span data-stu-id="6c548-106">Applies To</span></span>

-   [<span data-ttu-id="6c548-107">**Elementi audio**</span><span class="sxs-lookup"><span data-stu-id="6c548-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="6c548-108">**Elementi foto**</span><span class="sxs-lookup"><span data-stu-id="6c548-108">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="6c548-109">**Elementi della playlist**</span><span class="sxs-lookup"><span data-stu-id="6c548-109">**Playlist Items**</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="6c548-110">**Elementi video**</span><span class="sxs-lookup"><span data-stu-id="6c548-110">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="6c548-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="6c548-111">Remarks</span></span>

<span data-ttu-id="6c548-112">Se questo attributo è disponibile, l'elemento multimediale viene protetto tramite DTCP-IP.</span><span class="sxs-lookup"><span data-stu-id="6c548-112">If this attribute is available, the media item is protected using DTCP-IP.</span></span>

<span data-ttu-id="6c548-113">Questo attributo non è disponibile per gli elementi multimediali nella libreria locale dell'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="6c548-113">This attribute is not available for media items in the current user's local library.</span></span> <span data-ttu-id="6c548-114">È disponibile solo per gli elementi multimediali che appartengono a una libreria remota; ovvero una libreria che è stata resa disponibile da un altro utente nella rete domestica.</span><span class="sxs-lookup"><span data-stu-id="6c548-114">It is available only for media items that belong to a remote library; that is, a library that has been made available by another user on the home network.</span></span> <span data-ttu-id="6c548-115">Per determinare se un catalogo multimediale è remoto, chiamare [**IWMPLibrary:: Get \_ Type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span><span class="sxs-lookup"><span data-stu-id="6c548-115">To determine whether a media library is remote, call [**IWMPLibrary::get\_type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span></span>

## <a name="requirements"></a><span data-ttu-id="6c548-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6c548-116">Requirements</span></span>



| <span data-ttu-id="6c548-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c548-117">Requirement</span></span> | <span data-ttu-id="6c548-118">Valore</span><span class="sxs-lookup"><span data-stu-id="6c548-118">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="6c548-119">Versione</span><span class="sxs-lookup"><span data-stu-id="6c548-119">Version</span></span><br/> | <span data-ttu-id="6c548-120">Windows Media Player 12</span><span class="sxs-lookup"><span data-stu-id="6c548-120">Windows Media Player 12</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6c548-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6c548-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c548-122">**Riferimento agli attributi**</span><span class="sxs-lookup"><span data-stu-id="6c548-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





