---
description: Definisce i codici di errore della chiave multimediale per il motore multimediale.
ms.assetid: F6E13260-74A2-40D0-A704-4E1CDB16B8D8
title: Enumerazione MF_MEDIA_ENGINE_KEYERR
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MEDIA_ENGINE_KEYERR
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 22dd22a7771f5d1e9466709f0b0da9ee936ef2b9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351346"
---
# <a name="mf_media_engine_keyerr-enumeration"></a><span data-ttu-id="e4f03-103">\_ \_ Enumerazione KEYERR del motore multimediale MF \_</span><span class="sxs-lookup"><span data-stu-id="e4f03-103">MF\_MEDIA\_ENGINE\_KEYERR enumeration</span></span>

<span data-ttu-id="e4f03-104">Definisce i codici di errore della chiave multimediale per il motore multimediale.</span><span class="sxs-lookup"><span data-stu-id="e4f03-104">Defines media key error codes for the media engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4f03-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e4f03-105">Syntax</span></span>


```C++
typedef enum _MF_MEDIA_ENGINE_KEYERR { 
  MF_MEDIAENGINE_KEYERR_UNKNOWN          = 1,
  MF_MEDIAENGINE_KEYERR_CLIENT           = 2,
  MF_MEDIAENGINE_KEYERR_SERVICE          = 3,
  MF_MEDIAENGINE_KEYERR_OUTPUT           = 4,
  MF_MEDIAENGINE_KEYERR_HARDWARECHANGE   = 5,
  MF_MEDIAENGINE_KEYERR_DOMAIN           = 6
} MF_MEDIA_ENGINE_KEYERR;
```



## <a name="constants"></a><span data-ttu-id="e4f03-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="e4f03-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e4f03-107"><span id="MF_MEDIAENGINE_KEYERR_UNKNOWN"></span><span id="mf_mediaengine_keyerr_unknown"></span>**MF \_ MEDIAENGINE \_ KEYERR \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="e4f03-107"><span id="MF_MEDIAENGINE_KEYERR_UNKNOWN"></span><span id="mf_mediaengine_keyerr_unknown"></span>**MF\_MEDIAENGINE\_KEYERR\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="e4f03-108">Si è verificato un errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="e4f03-108">Unknown error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="e4f03-109"><span id="MF_MEDIAENGINE_KEYERR_CLIENT"></span><span id="mf_mediaengine_keyerr_client"></span>**\_ \_ client KEYERR MF \_ MEDIAENGINE**</span><span class="sxs-lookup"><span data-stu-id="e4f03-109"><span id="MF_MEDIAENGINE_KEYERR_CLIENT"></span><span id="mf_mediaengine_keyerr_client"></span>**MF\_MEDIAENGINE\_KEYERR\_CLIENT**</span></span>
</dt> <dd>

<span data-ttu-id="e4f03-110">Si è verificato un errore con il client.</span><span class="sxs-lookup"><span data-stu-id="e4f03-110">An error with the client occurred.</span></span>

</dd> <dt>

<span data-ttu-id="e4f03-111"><span id="MF_MEDIAENGINE_KEYERR_SERVICE"></span><span id="mf_mediaengine_keyerr_service"></span>**\_ \_ servizio KEYERR MF \_ MEDIAENGINE**</span><span class="sxs-lookup"><span data-stu-id="e4f03-111"><span id="MF_MEDIAENGINE_KEYERR_SERVICE"></span><span id="mf_mediaengine_keyerr_service"></span>**MF\_MEDIAENGINE\_KEYERR\_SERVICE**</span></span>
</dt> <dd>

<span data-ttu-id="e4f03-112">Si è verificato un errore con il servizio.</span><span class="sxs-lookup"><span data-stu-id="e4f03-112">An error with the service occurred.</span></span>

</dd> <dt>

<span data-ttu-id="e4f03-113"><span id="MF_MEDIAENGINE_KEYERR_OUTPUT"></span><span id="mf_mediaengine_keyerr_output"></span>**\_ \_ output KEYERR MF \_ MEDIAENGINE**</span><span class="sxs-lookup"><span data-stu-id="e4f03-113"><span id="MF_MEDIAENGINE_KEYERR_OUTPUT"></span><span id="mf_mediaengine_keyerr_output"></span>**MF\_MEDIAENGINE\_KEYERR\_OUTPUT**</span></span>
</dt> <dd>

<span data-ttu-id="e4f03-114">Si è verificato un errore con l'output.</span><span class="sxs-lookup"><span data-stu-id="e4f03-114">An error with the output occurred.</span></span>

</dd> <dt>

<span data-ttu-id="e4f03-115"><span id="MF_MEDIAENGINE_KEYERR_HARDWARECHANGE_"></span><span id="mf_mediaengine_keyerr_hardwarechange_"></span>**MF \_ MEDIAENGINE \_ KEYERR \_ HARDWARECHANGE**</span><span class="sxs-lookup"><span data-stu-id="e4f03-115"><span id="MF_MEDIAENGINE_KEYERR_HARDWARECHANGE_"></span><span id="mf_mediaengine_keyerr_hardwarechange_"></span>**MF\_MEDIAENGINE\_KEYERR\_HARDWARECHANGE**</span></span> 
</dt> <dd>

<span data-ttu-id="e4f03-116">Si è verificato un errore relativo a una modifica dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="e4f03-116">An error occurred related to a hardware change.</span></span>

</dd> <dt>

<span data-ttu-id="e4f03-117"><span id="MF_MEDIAENGINE_KEYERR_DOMAIN"></span><span id="mf_mediaengine_keyerr_domain"></span>**\_dominio MF MEDIAENGINE \_ KEYERR \_**</span><span class="sxs-lookup"><span data-stu-id="e4f03-117"><span id="MF_MEDIAENGINE_KEYERR_DOMAIN"></span><span id="mf_mediaengine_keyerr_domain"></span>**MF\_MEDIAENGINE\_KEYERR\_DOMAIN**</span></span>
</dt> <dd>

<span data-ttu-id="e4f03-118">Si è verificato un errore relativo al dominio.</span><span class="sxs-lookup"><span data-stu-id="e4f03-118">An error with the domain occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e4f03-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="e4f03-119">Remarks</span></span>

<span data-ttu-id="e4f03-120">**MF \_ Il \_ motore multimediale \_ KEYERR** viene usato con il parametro *Code* di [**IMFMediaKeySessionNotify:: Error**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediakeysessionnotify-keyerror) e il valore del *codice* restituito da [**IMFMediaKeySession:: GetError**](imfmediakeysession-geterror.md).</span><span class="sxs-lookup"><span data-stu-id="e4f03-120">**MF\_MEDIA\_ENGINE\_KEYERR** is used with the *code* parameter of [**IMFMediaKeySessionNotify::KeyError**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediakeysessionnotify-keyerror) and the *code* value returned from [**IMFMediaKeySession::GetError**](imfmediakeysession-geterror.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4f03-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4f03-121">Requirements</span></span>



| <span data-ttu-id="e4f03-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4f03-122">Requirement</span></span> | <span data-ttu-id="e4f03-123">Valore</span><span class="sxs-lookup"><span data-stu-id="e4f03-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4f03-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4f03-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e4f03-125">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e4f03-125">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e4f03-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4f03-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e4f03-127">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4f03-127">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="e4f03-128">IDL</span><span class="sxs-lookup"><span data-stu-id="e4f03-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e4f03-129"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e4f03-129"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4f03-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e4f03-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4f03-131">Enumerazioni di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e4f03-131">Media Foundation Enumerations</span></span>](media-foundation-enumerations.md)
</dt> </dl>

 

 




