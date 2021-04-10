---
title: Enumerazione MPSOURCE (MpClient. h)
description: Categoria di origine possibile.
ms.assetid: 1AD12D67-C74B-481A-AC9B-D119AABDB6E9
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione MPSOURCE
- Funzionalità dell'ambiente Windows legacy del puntatore di enumerazione PMPSOURCE
topic_type:
- apiref
api_name:
- MPSOURCE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e9255029512499a0e2948a44701ef4482aff4b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964486"
---
# <a name="mpsource-enumeration"></a><span data-ttu-id="16705-105">Enumerazione MPSOURCE</span><span class="sxs-lookup"><span data-stu-id="16705-105">MPSOURCE enumeration</span></span>

<span data-ttu-id="16705-106">Categoria di origine possibile.</span><span class="sxs-lookup"><span data-stu-id="16705-106">Possible category of source.</span></span>

## <a name="syntax"></a><span data-ttu-id="16705-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="16705-107">Syntax</span></span>


```C++
typedef enum tagMPSOURCE { 
  MPSOURCE_UNKNOWN             = 0,
  MPSOURCE_USER                = 1,
  MPSOURCE_SYSTEM              = 2,
  MPSOURCE_REALTIME            = 3,
  MPSOURCE_IOAV                = 4,
  MPSOURCE_NIS                 = 5,
  MPSOURCE_BHO                 = 6,
  MPSOURCE_IEPROTECT           = 6,
  MPSOURCE_ELAM                = 7,
  MPSOURCE_LOCAL_ATTESTATION   = 8,
  MPSOURCE_REMOTE_ATTESTATION  = 9,
  MPSOURCE_AMSI                = 10,
  MP_SOURCE_MAXVALUE           = 10
} MPSOURCE, *PMPSOURCE;
```



## <a name="constants"></a><span data-ttu-id="16705-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="16705-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="16705-109"><span id="MPSOURCE_UNKNOWN"></span><span id="mpsource_unknown"></span>**MPSOURCE \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="16705-109"><span id="MPSOURCE_UNKNOWN"></span><span id="mpsource_unknown"></span>**MPSOURCE\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="16705-110">Origine sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="16705-110">Source unknown.</span></span>

</dd> <dt>

<span data-ttu-id="16705-111"><span id="MPSOURCE_USER"></span><span id="mpsource_user"></span>**\_utente MPSOURCE**</span><span class="sxs-lookup"><span data-stu-id="16705-111"><span id="MPSOURCE_USER"></span><span id="mpsource_user"></span>**MPSOURCE\_USER**</span></span>
</dt> <dd>

<span data-ttu-id="16705-112">Avviata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="16705-112">User initiated.</span></span>

</dd> <dt>

<span data-ttu-id="16705-113"><span id="MPSOURCE_SYSTEM"></span><span id="mpsource_system"></span>**\_sistema MPSOURCE**</span><span class="sxs-lookup"><span data-stu-id="16705-113"><span id="MPSOURCE_SYSTEM"></span><span id="mpsource_system"></span>**MPSOURCE\_SYSTEM**</span></span>
</dt> <dd>

<span data-ttu-id="16705-114">avviato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="16705-114">system initiated.</span></span>

</dd> <dt>

<span data-ttu-id="16705-115"><span id="MPSOURCE_REALTIME"></span><span id="mpsource_realtime"></span>**MPSOURCE in \_ tempo reale**</span><span class="sxs-lookup"><span data-stu-id="16705-115"><span id="MPSOURCE_REALTIME"></span><span id="mpsource_realtime"></span>**MPSOURCE\_REALTIME**</span></span>
</dt> <dd>

<span data-ttu-id="16705-116">Componente in tempo reale avviato.</span><span class="sxs-lookup"><span data-stu-id="16705-116">Realtime component initiated.</span></span>

</dd> <dt>

<span data-ttu-id="16705-117"><span id="MPSOURCE_IOAV"></span><span id="mpsource_ioav"></span>**\_IOAV MPSOURCE**</span><span class="sxs-lookup"><span data-stu-id="16705-117"><span id="MPSOURCE_IOAV"></span><span id="mpsource_ioav"></span>**MPSOURCE\_IOAV**</span></span>
</dt> <dd>

<span data-ttu-id="16705-118">Vengono avviati i download di IE e gli allegati di Outlook Express.</span><span class="sxs-lookup"><span data-stu-id="16705-118">IE Downloads and Outlook Express Attachments initiated.</span></span>

</dd> <dt>

<span data-ttu-id="16705-119"><span id="MPSOURCE_NIS"></span><span id="mpsource_nis"></span>**\_NIS MPSOURCE**</span><span class="sxs-lookup"><span data-stu-id="16705-119"><span id="MPSOURCE_NIS"></span><span id="mpsource_nis"></span>**MPSOURCE\_NIS**</span></span>
</dt> <dd>

<span data-ttu-id="16705-120">Sistema di ispezione di rete.</span><span class="sxs-lookup"><span data-stu-id="16705-120">Network inspection system.</span></span>

</dd> <dt>

<span data-ttu-id="16705-121"><span id="MPSOURCE_BHO"></span><span id="mpsource_bho"></span>**\_bho MPSOURCE**</span><span class="sxs-lookup"><span data-stu-id="16705-121"><span id="MPSOURCE_BHO"></span><span id="mpsource_bho"></span>**MPSOURCE\_BHO**</span></span>
</dt> <dd>

<span data-ttu-id="16705-122">BHO-script Web (deprecato).</span><span class="sxs-lookup"><span data-stu-id="16705-122">BHO - web script (deprecated).</span></span>

</dd> <dt>

<span data-ttu-id="16705-123"><span id="MPSOURCE_IEPROTECT"></span><span id="mpsource_ieprotect"></span>**\_IEPROTECT MPSOURCE**</span><span class="sxs-lookup"><span data-stu-id="16705-123"><span id="MPSOURCE_IEPROTECT"></span><span id="mpsource_ieprotect"></span>**MPSOURCE\_IEPROTECT**</span></span>
</dt> <dd>

<span data-ttu-id="16705-124">IE-IExtensionValidation.</span><span class="sxs-lookup"><span data-stu-id="16705-124">IE - IExtensionValidation.</span></span>

</dd> <dt>

<span data-ttu-id="16705-125"><span id="MPSOURCE_ELAM"></span><span id="mpsource_elam"></span>**\_Elam MPSOURCE**</span><span class="sxs-lookup"><span data-stu-id="16705-125"><span id="MPSOURCE_ELAM"></span><span id="mpsource_elam"></span>**MPSOURCE\_ELAM**</span></span>
</dt> <dd>

<span data-ttu-id="16705-126">ELAM</span><span class="sxs-lookup"><span data-stu-id="16705-126">ELAM</span></span>

</dd> <dt>

<span data-ttu-id="16705-127"><span id="MPSOURCE_LOCAL_ATTESTATION"></span><span id="mpsource_local_attestation"></span>**\_ \_ attestazione locale MPSOURCE**</span><span class="sxs-lookup"><span data-stu-id="16705-127"><span id="MPSOURCE_LOCAL_ATTESTATION"></span><span id="mpsource_local_attestation"></span>**MPSOURCE\_LOCAL\_ATTESTATION**</span></span>
</dt> <dd>

<span data-ttu-id="16705-128">Attestazione locale.</span><span class="sxs-lookup"><span data-stu-id="16705-128">Local attestation.</span></span>

</dd> <dt>

<span data-ttu-id="16705-129"><span id="MPSOURCE_REMOTE_ATTESTATION"></span><span id="mpsource_remote_attestation"></span>**\_ \_ attestazione remota MPSOURCE**</span><span class="sxs-lookup"><span data-stu-id="16705-129"><span id="MPSOURCE_REMOTE_ATTESTATION"></span><span id="mpsource_remote_attestation"></span>**MPSOURCE\_REMOTE\_ATTESTATION**</span></span>
</dt> <dd>

<span data-ttu-id="16705-130">Attestazione remota.</span><span class="sxs-lookup"><span data-stu-id="16705-130">Remote attestation.</span></span>

</dd> <dt>

<span data-ttu-id="16705-131"><span id="MPSOURCE_AMSI"></span><span id="mpsource_amsi"></span>**\_AMSI MPSOURCE**</span><span class="sxs-lookup"><span data-stu-id="16705-131"><span id="MPSOURCE_AMSI"></span><span id="mpsource_amsi"></span>**MPSOURCE\_AMSI**</span></span>
</dt> <dd>

<span data-ttu-id="16705-132">AMSI</span><span class="sxs-lookup"><span data-stu-id="16705-132">AMSI</span></span>

</dd> <dt>

<span data-ttu-id="16705-133"><span id="MP_SOURCE_MAXVALUE"></span><span id="mp_source_maxvalue"></span>**\_MaxValue origine \_ MP**</span><span class="sxs-lookup"><span data-stu-id="16705-133"><span id="MP_SOURCE_MAXVALUE"></span><span id="mp_source_maxvalue"></span>**MP\_SOURCE\_MAXVALUE**</span></span>
</dt> <dd>

<span data-ttu-id="16705-134">Valore massimo possibile.</span><span class="sxs-lookup"><span data-stu-id="16705-134">Maximum value possible.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="16705-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16705-135">Requirements</span></span>



| <span data-ttu-id="16705-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="16705-136">Requirement</span></span> | <span data-ttu-id="16705-137">Valore</span><span class="sxs-lookup"><span data-stu-id="16705-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="16705-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16705-138">Minimum supported client</span></span><br/> | <span data-ttu-id="16705-139">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="16705-139">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="16705-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16705-140">Minimum supported server</span></span><br/> | <span data-ttu-id="16705-141">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="16705-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="16705-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="16705-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="16705-143"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="16705-143"><dt>MpClient.h</dt></span></span> </dl> |



 

 





