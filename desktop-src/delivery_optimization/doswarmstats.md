---
title: Struttura DOSwarmStats (Deliveryoptimization. h)
description: Contiene i campi per scaricare e caricare le statistiche per un file.
ms.assetid: 66B2498A-38E0-44E4-96C1-F778BD9AA593
keywords:
- Struttura DOSwarmStats
topic_type:
- apiref
api_name:
- DOSwarmStats
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 53d1702c25716ffe90c35727a258134311d5f427
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302658"
---
# <a name="doswarmstats-structure"></a><span data-ttu-id="3d428-104">Struttura DOSwarmStats</span><span class="sxs-lookup"><span data-stu-id="3d428-104">DOSwarmStats structure</span></span>

<span data-ttu-id="3d428-105">Contiene i campi per scaricare e caricare le statistiche per un file.</span><span class="sxs-lookup"><span data-stu-id="3d428-105">Contains fields for download and upload statistics for a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d428-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3d428-106">Syntax</span></span>


```C++
typedef struct _DOSwarmStats {
  LPWSTR       fileId;
  LPWSTR       sourceURL;
  UINT64       fileSize;
  UINT64       totalBytesDownloaded;
  UINT64       bytesFromLanPeers;
  UINT64       bytesFromGroupPeers;
  UINT64       bytesFromInternetPeers;
  UINT64       bytesFromHttp;
  UINT64       bytesFromDoinc;
  UINT64       bytesToLanPeers;
  UINT64       bytesToGroupPeers;
  UINT64       bytesToInternetPeers;
  UINT         httpConnectionCount;
  UINT         doincConnectionCount;
  UINT         lanConnectionCount;
  UINT         groupConnectionCount;
  UINT         internetConnectionCount;
  UINT         downloadDuration;
  DownloadMode downloadMode;
  SwarmStatus  status;
  BOOL         isBackground;
} DOSwarmStats;
```



## <a name="members"></a><span data-ttu-id="3d428-107">Members</span><span class="sxs-lookup"><span data-stu-id="3d428-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="3d428-108">**fileId**</span><span class="sxs-lookup"><span data-stu-id="3d428-108">**fileId**</span></span>
</dt> <dd>

<span data-ttu-id="3d428-109">Stringa con terminazione null specificata con la chiamata **AddFileWithRanges** .</span><span class="sxs-lookup"><span data-stu-id="3d428-109">Null-terminated string that was specified with the **AddFileWithRanges** call.</span></span>

</dd> <dt>

<span data-ttu-id="3d428-110">**sourceURL**</span><span class="sxs-lookup"><span data-stu-id="3d428-110">**sourceURL**</span></span>
</dt> <dd>

<span data-ttu-id="3d428-111">Stringa con terminazione null che contiene il nome del file nel server, ad esempio il percorso del &lt; server https:// &gt; / &lt; &gt; /file.ext.</span><span class="sxs-lookup"><span data-stu-id="3d428-111">Null-terminated string that contains the name of the file on the server (for example, https://&lt;server&gt;/&lt;path&gt;/file.ext).</span></span>

</dd> <dt>

<span data-ttu-id="3d428-112">**fileSize**</span><span class="sxs-lookup"><span data-stu-id="3d428-112">**fileSize**</span></span>
</dt> <dd>

<span data-ttu-id="3d428-113">Dimensioni del file, in byte.</span><span class="sxs-lookup"><span data-stu-id="3d428-113">Size of the file in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="3d428-114">**totalBytesDownloaded**</span><span class="sxs-lookup"><span data-stu-id="3d428-114">**totalBytesDownloaded**</span></span>
</dt> <dd>

<span data-ttu-id="3d428-115">Numero totale di byte trasferiti.</span><span class="sxs-lookup"><span data-stu-id="3d428-115">Total number of bytes transferred.</span></span>

</dd> <dt>

<span data-ttu-id="3d428-116">**bytesFromLanPeers**</span><span class="sxs-lookup"><span data-stu-id="3d428-116">**bytesFromLanPeers**</span></span>
</dt> <dd>

<span data-ttu-id="3d428-117">Numero di byte trasferiti dai peer LAN.</span><span class="sxs-lookup"><span data-stu-id="3d428-117">Number of bytes transferred from LAN peers.</span></span>

</dd> <dt>

<span data-ttu-id="3d428-118">**bytesFromGroupPeers**</span><span class="sxs-lookup"><span data-stu-id="3d428-118">**bytesFromGroupPeers**</span></span>
</dt> <dd>

<span data-ttu-id="3d428-119">Numero di byte trasferiti da peer di gruppo.</span><span class="sxs-lookup"><span data-stu-id="3d428-119">Number of bytes transferred from group peers.</span></span>

</dd> <dt>

<span data-ttu-id="3d428-120">**bytesFromInternetPeers**</span><span class="sxs-lookup"><span data-stu-id="3d428-120">**bytesFromInternetPeers**</span></span>
</dt> <dd>

<span data-ttu-id="3d428-121">Numero di byte trasferiti dai peer internet.</span><span class="sxs-lookup"><span data-stu-id="3d428-121">Number of bytes transferred from Internet peers.</span></span>

</dd> <dt>

<span data-ttu-id="3d428-122">**bytesFromHttp**</span><span class="sxs-lookup"><span data-stu-id="3d428-122">**bytesFromHttp**</span></span>
</dt> <dd>

<span data-ttu-id="3d428-123">Numero di byte trasferiti da http.</span><span class="sxs-lookup"><span data-stu-id="3d428-123">Number of bytes transferred from http.</span></span>

</dd> <dt>

<span data-ttu-id="3d428-124">**bytesFromDoinc**</span><span class="sxs-lookup"><span data-stu-id="3d428-124">**bytesFromDoinc**</span></span>
</dt> <dd>

<span data-ttu-id="3d428-125">Solo per uso interno.</span><span class="sxs-lookup"><span data-stu-id="3d428-125">For internal use only.</span></span>

</dd> <dt>

<span data-ttu-id="3d428-126">**bytesToLanPeers**</span><span class="sxs-lookup"><span data-stu-id="3d428-126">**bytesToLanPeers**</span></span>
</dt> <dd>

<span data-ttu-id="3d428-127">Numero di byte trasferiti ai peer LAN.</span><span class="sxs-lookup"><span data-stu-id="3d428-127">Number of bytes transferred to LAN peers.</span></span>

</dd> <dt>

<span data-ttu-id="3d428-128">**bytesToGroupPeers**</span><span class="sxs-lookup"><span data-stu-id="3d428-128">**bytesToGroupPeers**</span></span>
</dt> <dd>

<span data-ttu-id="3d428-129">Numero di byte trasferiti ai peer di gruppo.</span><span class="sxs-lookup"><span data-stu-id="3d428-129">Number of bytes transferred to group peers.</span></span>

</dd> <dt>

<span data-ttu-id="3d428-130">**bytesToInternetPeers**</span><span class="sxs-lookup"><span data-stu-id="3d428-130">**bytesToInternetPeers**</span></span>
</dt> <dd>

<span data-ttu-id="3d428-131">Numero di byte trasferiti ai peer internet.</span><span class="sxs-lookup"><span data-stu-id="3d428-131">Number of bytes transferred to Internet peers.</span></span>

</dd> <dt>

<span data-ttu-id="3d428-132">**httpConnectionCount**</span><span class="sxs-lookup"><span data-stu-id="3d428-132">**httpConnectionCount**</span></span>
</dt> <dd>

<span data-ttu-id="3d428-133">Numero di connessioni HTTP.</span><span class="sxs-lookup"><span data-stu-id="3d428-133">Count of http connections.</span></span>

</dd> <dt>

<span data-ttu-id="3d428-134">**doincConnectionCount**</span><span class="sxs-lookup"><span data-stu-id="3d428-134">**doincConnectionCount**</span></span>
</dt> <dd>

<span data-ttu-id="3d428-135">Solo per uso interno.</span><span class="sxs-lookup"><span data-stu-id="3d428-135">For internal use only.</span></span>

</dd> <dt>

<span data-ttu-id="3d428-136">**lanConnectionCount**</span><span class="sxs-lookup"><span data-stu-id="3d428-136">**lanConnectionCount**</span></span>
</dt> <dd>

<span data-ttu-id="3d428-137">Conteggio delle connessioni LAN.</span><span class="sxs-lookup"><span data-stu-id="3d428-137">Count of LAN connections.</span></span>

</dd> <dt>

<span data-ttu-id="3d428-138">**groupConnectionCount**</span><span class="sxs-lookup"><span data-stu-id="3d428-138">**groupConnectionCount**</span></span>
</dt> <dd>

<span data-ttu-id="3d428-139">Conteggio delle connessioni al gruppo.</span><span class="sxs-lookup"><span data-stu-id="3d428-139">Count of group connections.</span></span>

</dd> <dt>

<span data-ttu-id="3d428-140">**internetConnectionCount**</span><span class="sxs-lookup"><span data-stu-id="3d428-140">**internetConnectionCount**</span></span>
</dt> <dd>

<span data-ttu-id="3d428-141">Conteggio delle connessioni Internet.</span><span class="sxs-lookup"><span data-stu-id="3d428-141">Count of Internet connections.</span></span>

</dd> <dt>

<span data-ttu-id="3d428-142">**downloadDuration**</span><span class="sxs-lookup"><span data-stu-id="3d428-142">**downloadDuration**</span></span>
</dt> <dd>

<span data-ttu-id="3d428-143">Durata del trasferimento di file in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="3d428-143">Duration of the file transfer in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="3d428-144">**Modalità**</span><span class="sxs-lookup"><span data-stu-id="3d428-144">**downloadMode**</span></span>
</dt> <dd>

<span data-ttu-id="3d428-145">Per la modalità di download usata, vedere [**modalità**](downloadmode.md).</span><span class="sxs-lookup"><span data-stu-id="3d428-145">The download mode used, see [**DownloadMode**](downloadmode.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d428-146">**Stato**</span><span class="sxs-lookup"><span data-stu-id="3d428-146">**status**</span></span>
</dt> <dd>

<span data-ttu-id="3d428-147">Lo stato di un trasferimento di file, vedere [**SwarmStatus**](swarmstatus.md).</span><span class="sxs-lookup"><span data-stu-id="3d428-147">The status of a file transfer, see [**SwarmStatus**](swarmstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d428-148">**isBackground**</span><span class="sxs-lookup"><span data-stu-id="3d428-148">**isBackground**</span></span>
</dt> <dd>

<span data-ttu-id="3d428-149">True se si tratta di un trasferimento in background.</span><span class="sxs-lookup"><span data-stu-id="3d428-149">True, if this is a background transfer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3d428-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d428-150">Requirements</span></span>



| <span data-ttu-id="3d428-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d428-151">Requirement</span></span> | <span data-ttu-id="3d428-152">Valore</span><span class="sxs-lookup"><span data-stu-id="3d428-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d428-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d428-153">Minimum supported client</span></span><br/> | <span data-ttu-id="3d428-154">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="3d428-154">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3d428-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d428-155">Minimum supported server</span></span><br/> | <span data-ttu-id="3d428-156">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3d428-156">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3d428-157">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3d428-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d428-158"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d428-158"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



 

 





