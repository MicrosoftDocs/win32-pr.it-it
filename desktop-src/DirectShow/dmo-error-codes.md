---
description: La tabella seguente contiene i codici di errore specifici di Microsoft DirectX Media Objects (DMOs). Questi codici di errore sono definiti nel file di intestazione Mediaerr. h.
ms.assetid: 1ded5656-084d-4315-a414-aebf4a1820dc
title: Codici di errore DMO (Mediaerr. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d76c8cd5e7001751cd2cf9eb7da4d88b2dc100bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332865"
---
# <a name="dmo-error-codes"></a><span data-ttu-id="b8e66-104">Codici di errore DMO</span><span class="sxs-lookup"><span data-stu-id="b8e66-104">DMO Error Codes</span></span>

<span data-ttu-id="b8e66-105">La tabella seguente contiene i codici di errore specifici di Microsoft DirectX Media Objects (DMOs).</span><span class="sxs-lookup"><span data-stu-id="b8e66-105">The following table contains error codes that are specific to Microsoft DirectX Media Objects (DMOs).</span></span> <span data-ttu-id="b8e66-106">Questi codici di errore sono definiti nel file di intestazione Mediaerr. h.</span><span class="sxs-lookup"><span data-stu-id="b8e66-106">These error codes are defined in the header file Mediaerr.h.</span></span>



| <span data-ttu-id="b8e66-107">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="b8e66-107">Constant/value</span></span>                                                                                                                                                                                                                                                  | <span data-ttu-id="b8e66-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b8e66-108">Description</span></span>                                                                                                                                                         |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DMO_E_INVALIDSTREAMINDEX"></span><span id="dmo_e_invalidstreamindex"></span><dl> <span data-ttu-id="b8e66-109"><dt>**DMO \_ E \_ INVALIDSTREAMINDEX**</dt> <dt>0x80040201</dt></span><span class="sxs-lookup"><span data-stu-id="b8e66-109"><dt>**DMO\_E\_INVALIDSTREAMINDEX**</dt> <dt>0x80040201</dt></span></span> </dl> | <span data-ttu-id="b8e66-110">Indice del flusso non valido.</span><span class="sxs-lookup"><span data-stu-id="b8e66-110">Invalid stream index.</span></span><br/>                                                                                                                                    |
| <span id="DMO_E_INVALIDTYPE"></span><span id="dmo_e_invalidtype"></span><dl> <span data-ttu-id="b8e66-111"><dt>**DMO \_ E \_ INVALIDTYPE**</dt> <dt>0x80040202</dt></span><span class="sxs-lookup"><span data-stu-id="b8e66-111"><dt>**DMO\_E\_INVALIDTYPE**</dt> <dt>0x80040202</dt></span></span> </dl>                      | <span data-ttu-id="b8e66-112">Tipo di supporto non valido.</span><span class="sxs-lookup"><span data-stu-id="b8e66-112">Invalid media type.</span></span><br/>                                                                                                                                      |
| <span id="DMO_E_TYPE_NOT_SET"></span><span id="dmo_e_type_not_set"></span><dl> <span data-ttu-id="b8e66-113"><dt>**DMO \_ \_Tipo E \_ non \_ impostato**</dt> <dt>0x80040203</dt></span><span class="sxs-lookup"><span data-stu-id="b8e66-113"><dt>**DMO\_E\_TYPE\_NOT\_SET**</dt> <dt>0x80040203</dt></span></span> </dl>                 | <span data-ttu-id="b8e66-114">Il tipo di supporto non è stato impostato.</span><span class="sxs-lookup"><span data-stu-id="b8e66-114">Media type was not set.</span></span> <span data-ttu-id="b8e66-115">Uno o più flussi richiedono un tipo di supporto prima di poter eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="b8e66-115">One or more streams require a media type before this operation can be performed.</span></span><br/>                                                 |
| <span id="DMO_E_NOTACCEPTING"></span><span id="dmo_e_notaccepting"></span><dl> <span data-ttu-id="b8e66-116"><dt>**DMO \_ E \_ NOTACCEPTING**</dt> <dt>0x80040204</dt></span><span class="sxs-lookup"><span data-stu-id="b8e66-116"><dt>**DMO\_E\_NOTACCEPTING**</dt> <dt>0x80040204</dt></span></span> </dl>                   | <span data-ttu-id="b8e66-117">Non è possibile accettare i dati nel flusso.</span><span class="sxs-lookup"><span data-stu-id="b8e66-117">Data cannot be accepted on this stream.</span></span> <span data-ttu-id="b8e66-118">Potrebbe essere necessario elaborare altri dati di output; vedere [**IMediaObject::P rocessinput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processinput).</span><span class="sxs-lookup"><span data-stu-id="b8e66-118">You might need to process more output data; see [**IMediaObject::ProcessInput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processinput).</span></span><br/> |
| <span id="DMO_E_TYPE_NOT_ACCEPTED"></span><span id="dmo_e_type_not_accepted"></span><dl> <span data-ttu-id="b8e66-119"><dt>**DMO \_ \_Tipo E \_ non \_ accettato**</dt> <dt>0x80040205</dt></span><span class="sxs-lookup"><span data-stu-id="b8e66-119"><dt>**DMO\_E\_TYPE\_NOT\_ACCEPTED**</dt> <dt>0x80040205</dt></span></span> </dl>  | <span data-ttu-id="b8e66-120">Il tipo di supporto non è stato accettato.</span><span class="sxs-lookup"><span data-stu-id="b8e66-120">Media type was not accepted.</span></span><br/>                                                                                                                             |
| <span id="DMO_E_NO_MORE_ITEMS"></span><span id="dmo_e_no_more_items"></span><dl> <span data-ttu-id="b8e66-121"><dt>**DMO \_ E \_ nessun \_ altro \_ elemento**</dt> <dt>0x80040206</dt></span><span class="sxs-lookup"><span data-stu-id="b8e66-121"><dt>**DMO\_E\_NO\_MORE\_ITEMS**</dt> <dt>0x80040206</dt></span></span> </dl>              | <span data-ttu-id="b8e66-122">Indice del tipo di supporto non compreso nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="b8e66-122">Media-type index is out of range.</span></span><br/>                                                                                                                        |



## <a name="requirements"></a><span data-ttu-id="b8e66-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b8e66-123">Requirements</span></span>



| <span data-ttu-id="b8e66-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8e66-124">Requirement</span></span> | <span data-ttu-id="b8e66-125">Valore</span><span class="sxs-lookup"><span data-stu-id="b8e66-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b8e66-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b8e66-126">Header</span></span><br/> | <dl> <span data-ttu-id="b8e66-127"><dt>Mediaerr. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8e66-127"><dt>Mediaerr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8e66-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b8e66-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8e66-129">Costanti DMO</span><span class="sxs-lookup"><span data-stu-id="b8e66-129">DMO Constants</span></span>](dmo-constants.md)
</dt> </dl>

 

 




