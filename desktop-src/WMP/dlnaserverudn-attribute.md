---
title: Attributo DLNAServerUDN
description: L'attributo DLNAServerUDN è il nome univoco del dispositivo del server che ospita l'elemento multimediale.
ms.assetid: 1965731d-1b6e-4d76-a983-fd57c851fcfb
keywords:
- Attributo DLNAServerUDN Windows Media Player
topic_type:
- apiref
api_name:
- DLNAServerUDN Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caa121df7a4f312e3cb00519d2ac4f519f844d41
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329946"
---
# <a name="dlnaserverudn-attribute"></a><span data-ttu-id="64925-104">Attributo DLNAServerUDN</span><span class="sxs-lookup"><span data-stu-id="64925-104">DLNAServerUDN Attribute</span></span>

<span data-ttu-id="64925-105">L'attributo **DLNAServerUDN** è il nome univoco del dispositivo del server che ospita l'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="64925-105">The **DLNAServerUDN** attribute is the unique device name of the server that hosts the media item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="64925-106">Si applica a</span><span class="sxs-lookup"><span data-stu-id="64925-106">Applies To</span></span>

-   [<span data-ttu-id="64925-107">**Elementi audio**</span><span class="sxs-lookup"><span data-stu-id="64925-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="64925-108">**Elementi foto**</span><span class="sxs-lookup"><span data-stu-id="64925-108">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="64925-109">**Elementi della playlist**</span><span class="sxs-lookup"><span data-stu-id="64925-109">**Playlist Items**</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="64925-110">**Elementi video**</span><span class="sxs-lookup"><span data-stu-id="64925-110">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="64925-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="64925-111">Remarks</span></span>

<span data-ttu-id="64925-112">Questo attributo non è disponibile per gli elementi multimediali nella libreria locale dell'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="64925-112">This attribute is not available for media items in the current user's local library.</span></span> <span data-ttu-id="64925-113">È disponibile solo per gli elementi multimediali che appartengono a una libreria remota; ovvero una libreria che è stata resa disponibile da un altro utente nella rete domestica.</span><span class="sxs-lookup"><span data-stu-id="64925-113">It is available only for media items that belong to a remote library; that is, a library that has been made available by another user on the home network.</span></span> <span data-ttu-id="64925-114">Per determinare se un catalogo multimediale è remoto, chiamare [**IWMPLibrary:: Get \_ Type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span><span class="sxs-lookup"><span data-stu-id="64925-114">To determine whether a media library is remote, call [**IWMPLibrary::get\_type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span></span>

## <a name="requirements"></a><span data-ttu-id="64925-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="64925-115">Requirements</span></span>



| <span data-ttu-id="64925-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="64925-116">Requirement</span></span> | <span data-ttu-id="64925-117">Valore</span><span class="sxs-lookup"><span data-stu-id="64925-117">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="64925-118">Versione</span><span class="sxs-lookup"><span data-stu-id="64925-118">Version</span></span><br/> | <span data-ttu-id="64925-119">Windows Media Player 12</span><span class="sxs-lookup"><span data-stu-id="64925-119">Windows Media Player 12</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="64925-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="64925-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64925-121">**Riferimento agli attributi**</span><span class="sxs-lookup"><span data-stu-id="64925-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





