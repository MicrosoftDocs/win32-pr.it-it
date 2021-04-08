---
description: La struttura NETWORKINFO descrive una scheda di interfaccia di rete.
ms.assetid: 40169409-7de5-44d1-8dff-dfa9f647edc9
title: Struttura NETWORKINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NETWORKINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 8917966d2e090417a95a9ca20158c6c5935bda3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760130"
---
# <a name="networkinfo-structure"></a><span data-ttu-id="3760c-103">Struttura NETWORKINFO</span><span class="sxs-lookup"><span data-stu-id="3760c-103">NETWORKINFO structure</span></span>

<span data-ttu-id="3760c-104">La struttura NETWORKINFO descrive una scheda di interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="3760c-104">The NETWORKINFO structure describes a NIC.</span></span>

## <a name="syntax"></a><span data-ttu-id="3760c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3760c-105">Syntax</span></span>


```C++
typedef struct _NETWORKINFO {
  BYTE    PermanentAddr[6];
  BYTE    CurrentAddr[6];
  ADDRESS OtherAddress;
  DWORD   LinkSpeed;
  DWORD   MacType;
  DWORD   MaxFrameSize;
  DWORD   Flags;
  DWORD   TimestampScaleFactor;
  BYTE    NodeName[32];
  BOOL    PModeSupported;
  BYTE    Comment[ADAPTER_COMMENT_LENGTH];
} NETWORKINFO, *LPNETWORKINFO;
```



## <a name="members"></a><span data-ttu-id="3760c-106">Members</span><span class="sxs-lookup"><span data-stu-id="3760c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3760c-107">**PermanentAddr**</span><span class="sxs-lookup"><span data-stu-id="3760c-107">**PermanentAddr**</span></span>
</dt> <dd>

<span data-ttu-id="3760c-108">Indirizzo MAC permanente.</span><span class="sxs-lookup"><span data-stu-id="3760c-108">Permanent MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="3760c-109">**CurrentAddr**</span><span class="sxs-lookup"><span data-stu-id="3760c-109">**CurrentAddr**</span></span>
</dt> <dd>

<span data-ttu-id="3760c-110">Indirizzo MAC corrente.</span><span class="sxs-lookup"><span data-stu-id="3760c-110">Current MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="3760c-111">**OtherAddress**</span><span class="sxs-lookup"><span data-stu-id="3760c-111">**OtherAddress**</span></span>
</dt> <dd>

<span data-ttu-id="3760c-112">Altro indirizzo che supporta questa operazione (ad esempio, IP, IPX).</span><span class="sxs-lookup"><span data-stu-id="3760c-112">Other address that support this (for example IP, IPX).</span></span>

</dd> <dt>

<span data-ttu-id="3760c-113">**LinkSpeed**</span><span class="sxs-lookup"><span data-stu-id="3760c-113">**LinkSpeed**</span></span>
</dt> <dd>

<span data-ttu-id="3760c-114">Velocità di collegamento, in Mbps.</span><span class="sxs-lookup"><span data-stu-id="3760c-114">Link speed, in Mbps.</span></span>

</dd> <dt>

<span data-ttu-id="3760c-115">**MacType**</span><span class="sxs-lookup"><span data-stu-id="3760c-115">**MacType**</span></span>
</dt> <dd>

<span data-ttu-id="3760c-116">Tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="3760c-116">Media type.</span></span>

</dd> <dt>

<span data-ttu-id="3760c-117">**MaxFrameSize**</span><span class="sxs-lookup"><span data-stu-id="3760c-117">**MaxFrameSize**</span></span>
</dt> <dd>

<span data-ttu-id="3760c-118">Dimensione massima consentita per il frame.</span><span class="sxs-lookup"><span data-stu-id="3760c-118">Maximum frame size allowed.</span></span>

</dd> <dt>

<span data-ttu-id="3760c-119">**Flag**</span><span class="sxs-lookup"><span data-stu-id="3760c-119">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="3760c-120">Questo parametro può essere uno dei seguenti flag informativi:</span><span class="sxs-lookup"><span data-stu-id="3760c-120">This parameter can be one of the following informational flags:</span></span>



| <span data-ttu-id="3760c-121">Valore</span><span class="sxs-lookup"><span data-stu-id="3760c-121">Value</span></span>                                                                                                                                                                                                                                       | <span data-ttu-id="3760c-122">Significato</span><span class="sxs-lookup"><span data-stu-id="3760c-122">Meaning</span></span>                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NETWORKINFO_FLAGS_PMODE_NOT_SUPPORTED"></span><span id="networkinfo_flags_pmode_not_supported"></span><dl> <span data-ttu-id="3760c-123"><dt>**\_flag NETWORKINFO \_ pmode \_ non \_ supportati**</dt></span><span class="sxs-lookup"><span data-stu-id="3760c-123"><dt>**NETWORKINFO\_FLAGS\_PMODE\_NOT\_SUPPORTED**</dt></span></span> </dl>    | <span data-ttu-id="3760c-124">La scheda di rete non supporta la modalità promiscua, ovvero acquisisce solo il traffico trasmesso in natura o solo il computer locale.</span><span class="sxs-lookup"><span data-stu-id="3760c-124">The network card does not support promiscuous mode, meaning that it will only capture traffic which is broadcast in nature or only involves the local machine.</span></span><br/> |
| <span id="NETWORKINFO_FLAGS_RAS"></span><span id="networkinfo_flags_ras"></span><dl> <span data-ttu-id="3760c-125"><dt>**\_RAS flag \_ NETWORKINFO**</dt></span><span class="sxs-lookup"><span data-stu-id="3760c-125"><dt>**NETWORKINFO\_FLAGS\_RAS**</dt></span></span> </dl>                                                      | <span data-ttu-id="3760c-126">Si tratta di una scheda di rete virtuale che è una connessione RAS (server di accesso remoto) tramite un modem o un'altra scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="3760c-126">This is a virtual network card that is a RAS (Remote Access Server) connection through a modem or another network card.</span></span><br/>                                        |
| <span id="NETWORKINFO_FLAGS_REMOTE_CARD"></span><span id="networkinfo_flags_remote_card"></span><dl> <span data-ttu-id="3760c-127"><dt>**\_ \_ scheda remota flag \_ NETWORKINFO**</dt></span><span class="sxs-lookup"><span data-stu-id="3760c-127"><dt>**NETWORKINFO\_FLAGS\_REMOTE\_CARD**</dt></span></span> </dl>                             | <span data-ttu-id="3760c-128">La scheda di rete non si trova nel computer locale, ma viene acquisita in un computer remoto con il lascio del computer locale.</span><span class="sxs-lookup"><span data-stu-id="3760c-128">The network card is not on the local computer, but is capturing on a remote machine at the bequest of the local computer.</span></span><br/>                                      |
| <span id="NETWORKINFO_FLAGS_REMOTE_NAL"></span><span id="networkinfo_flags_remote_nal"></span><dl> <span data-ttu-id="3760c-129"><dt>**NETWORKINFO \_ flag \_ \_ NAL remoto**</dt></span><span class="sxs-lookup"><span data-stu-id="3760c-129"><dt>**NETWORKINFO\_FLAGS\_REMOTE\_NAL**</dt></span></span> </dl>                                | <span data-ttu-id="3760c-130">Obsoleto Non usare.</span><span class="sxs-lookup"><span data-stu-id="3760c-130">Obsolete; do not use.</span></span><br/>                                                                                                                                          |
| <span id="NETWORKINFO_FLAGS_REMOTE_NAL_CONNECTED"></span><span id="networkinfo_flags_remote_nal_connected"></span><dl> <span data-ttu-id="3760c-131"><dt>**NETWORKINFO \_ flags \_ Remote \_ NAL \_ Connected**</dt></span><span class="sxs-lookup"><span data-stu-id="3760c-131"><dt>**NETWORKINFO\_FLAGS\_REMOTE\_NAL\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="3760c-132">Obsoleto Non usare.</span><span class="sxs-lookup"><span data-stu-id="3760c-132">Obsolete; do not use.</span></span><br/>                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="3760c-133">**TimestampScaleFactor**</span><span class="sxs-lookup"><span data-stu-id="3760c-133">**TimestampScaleFactor**</span></span>
</dt> <dd>

<span data-ttu-id="3760c-134">Ad esempio, il valore 1 indica 1/1 MS, 10 indica 1/10 ms, 100 indica 1/100 ms e così via.</span><span class="sxs-lookup"><span data-stu-id="3760c-134">For example, a value of 1 indicates 1/1 ms, 10 indicates 1/10 ms, 100 indicates 1/100 ms, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="3760c-135">**NodeName**</span><span class="sxs-lookup"><span data-stu-id="3760c-135">**NodeName**</span></span>
</dt> <dd>

<span data-ttu-id="3760c-136">Nome della workstation remota.</span><span class="sxs-lookup"><span data-stu-id="3760c-136">Name of remote workstation.</span></span>

</dd> <dt>

<span data-ttu-id="3760c-137">**PModeSupported**</span><span class="sxs-lookup"><span data-stu-id="3760c-137">**PModeSupported**</span></span>
</dt> <dd>

<span data-ttu-id="3760c-138">Indicatore di supporto della modalità P NIC.</span><span class="sxs-lookup"><span data-stu-id="3760c-138">NIC P-mode support indicator.</span></span>

</dd> <dt>

<span data-ttu-id="3760c-139">**Commento**</span><span class="sxs-lookup"><span data-stu-id="3760c-139">**Comment**</span></span>
</dt> <dd>

<span data-ttu-id="3760c-140">Campo di commento dell'adapter.</span><span class="sxs-lookup"><span data-stu-id="3760c-140">Adapter comment field.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3760c-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3760c-141">Requirements</span></span>



| <span data-ttu-id="3760c-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="3760c-142">Requirement</span></span> | <span data-ttu-id="3760c-143">Valore</span><span class="sxs-lookup"><span data-stu-id="3760c-143">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3760c-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3760c-144">Minimum supported client</span></span><br/> | <span data-ttu-id="3760c-145">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3760c-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3760c-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3760c-146">Minimum supported server</span></span><br/> | <span data-ttu-id="3760c-147">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3760c-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3760c-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3760c-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="3760c-149"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3760c-149"><dt>Netmon.h</dt></span></span> </dl> |



 

 




