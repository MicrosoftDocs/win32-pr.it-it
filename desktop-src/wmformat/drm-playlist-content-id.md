---
title: Struttura DRM_PLAYLIST_CONTENT_ID (Drmexternals. h)
description: La \_ struttura di \_ ID contenuto della playlist DRM \_ contiene informazioni sul contenuto che deve essere copiato su CD come parte di un Burn della playlist.
ms.assetid: 124e86ac-b0d4-40b2-868b-fe2fed1898e1
keywords:
- Formato di Windows Media per la struttura DRM_PLAYLIST_CONTENT_ID
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- DRM_PLAYLIST_CONTENT_ID
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f475a8c3620ff1af64cb70914ca1ac591aa55106
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302061"
---
# <a name="drm_playlist_content_id-structure"></a><span data-ttu-id="ed02a-105">\_Struttura dell' \_ ID contenuto della playlist DRM \_</span><span class="sxs-lookup"><span data-stu-id="ed02a-105">DRM\_PLAYLIST\_CONTENT\_ID structure</span></span>

<span data-ttu-id="ed02a-106">La struttura di **\_ \_ \_ ID contenuto della playlist DRM** contiene informazioni sul contenuto che deve essere copiato su CD come parte di un Burn della playlist.</span><span class="sxs-lookup"><span data-stu-id="ed02a-106">The **DRM\_PLAYLIST\_CONTENT\_ID** structure contains information about content that is to be copied to CD as part of a playlist burn.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed02a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ed02a-107">Syntax</span></span>


```C++
typedef struct DRM_PLAYLIST_CONTENT_ID {
  LPCWSTR lpcwszV2Header;
  LPCSTR  lpcszV1KID;
  BYTE    *pbOtherData;
  DWORD   cbOtherData;
  DWORD   dwUniqueIDForSession;
  DWORD   dwValidFields;
} ;
```



## <a name="members"></a><span data-ttu-id="ed02a-108">Members</span><span class="sxs-lookup"><span data-stu-id="ed02a-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="ed02a-109">**lpcwszV2Header**</span><span class="sxs-lookup"><span data-stu-id="ed02a-109">**lpcwszV2Header**</span></span>
</dt> <dd>

<span data-ttu-id="ed02a-110">Intestazione DRM.</span><span class="sxs-lookup"><span data-stu-id="ed02a-110">DRM header.</span></span> <span data-ttu-id="ed02a-111">Utilizzare questo membro se il contenuto è protetto da Windows Media DRM versione 2 o successiva.</span><span class="sxs-lookup"><span data-stu-id="ed02a-111">Use this member if the content is protected by Windows Media DRM version 2 or later.</span></span>

</dd> <dt>

<span data-ttu-id="ed02a-112">**lpcszV1KID**</span><span class="sxs-lookup"><span data-stu-id="ed02a-112">**lpcszV1KID**</span></span>
</dt> <dd>

<span data-ttu-id="ed02a-113">ID chiave</span><span class="sxs-lookup"><span data-stu-id="ed02a-113">Key ID.</span></span> <span data-ttu-id="ed02a-114">Utilizzare questo membro se il contenuto è protetto da Windows Media DRM versione 1.</span><span class="sxs-lookup"><span data-stu-id="ed02a-114">Use this member if the content is protected by Windows Media DRM version 1.</span></span>

</dd> <dt>

<span data-ttu-id="ed02a-115">**pbOtherData**</span><span class="sxs-lookup"><span data-stu-id="ed02a-115">**pbOtherData**</span></span>
</dt> <dd>

<span data-ttu-id="ed02a-116">Buffer contenente dati supplementari.</span><span class="sxs-lookup"><span data-stu-id="ed02a-116">Buffer containing supplementary data.</span></span>

</dd> <dt>

<span data-ttu-id="ed02a-117">**cbOtherData**</span><span class="sxs-lookup"><span data-stu-id="ed02a-117">**cbOtherData**</span></span>
</dt> <dd>

<span data-ttu-id="ed02a-118">Dimensioni del buffer **pbOtherData** in byte.</span><span class="sxs-lookup"><span data-stu-id="ed02a-118">Size of the **pbOtherData** buffer in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ed02a-119">**dwUniqueIDForSession**</span><span class="sxs-lookup"><span data-stu-id="ed02a-119">**dwUniqueIDForSession**</span></span>
</dt> <dd>

<span data-ttu-id="ed02a-120">Identificatore univoco del contenuto da utilizzare nella sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="ed02a-120">Unique identifier for the content to be used in the current session.</span></span>

</dd> <dt>

<span data-ttu-id="ed02a-121">**dwValidFields**</span><span class="sxs-lookup"><span data-stu-id="ed02a-121">**dwValidFields**</span></span>
</dt> <dd>

<span data-ttu-id="ed02a-122">**DWORD** che indica i campi validi di questa struttura.</span><span class="sxs-lookup"><span data-stu-id="ed02a-122">**DWORD** indicating the valid fields of this structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ed02a-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed02a-123">Requirements</span></span>



| <span data-ttu-id="ed02a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed02a-124">Requirement</span></span> | <span data-ttu-id="ed02a-125">Valore</span><span class="sxs-lookup"><span data-stu-id="ed02a-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed02a-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed02a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ed02a-127">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ed02a-127">Windows XP \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ed02a-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed02a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ed02a-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ed02a-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="ed02a-130">Versione</span><span class="sxs-lookup"><span data-stu-id="ed02a-130">Version</span></span><br/>                  | <span data-ttu-id="ed02a-131">SDK di Windows Media Format 11</span><span class="sxs-lookup"><span data-stu-id="ed02a-131">Windows Media Format 11 SDK</span></span><br/>                                                    |
| <span data-ttu-id="ed02a-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ed02a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed02a-133"><dt>Drmexternals. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed02a-133"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed02a-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed02a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed02a-135">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="ed02a-135">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





