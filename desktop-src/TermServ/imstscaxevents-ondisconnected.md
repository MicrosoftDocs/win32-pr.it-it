---
title: Metodo disconnected IMsTscAxEvents
description: Chiamato quando il controllo client è stato disconnesso dal server host sessione Desktop remoto (host sessione Desktop remoto).
ms.assetid: f01086e7-61d1-41df-ba0a-4eecfa57d492
ms.tgt_platform: multiple
keywords:
- Metodo disconnected Servizi Desktop remoto
- Metodo disconnected Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo disconnected
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnDisconnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 372ad98c73b1b0e90753891e01e46c61a78c23dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301880"
---
# <a name="imstscaxeventsondisconnected-method"></a><span data-ttu-id="d50c5-106">Metodo IMsTscAxEvents:: disconnected</span><span class="sxs-lookup"><span data-stu-id="d50c5-106">IMsTscAxEvents::OnDisconnected method</span></span>

<span data-ttu-id="d50c5-107">Chiamato quando il controllo client è stato disconnesso dal server host sessione Desktop remoto (host sessione Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="d50c5-107">Called when the client control has been disconnected from the Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="d50c5-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d50c5-108">Syntax</span></span>


```C++
void OnDisconnected(
  [in] long discReason
);
```



## <a name="parameters"></a><span data-ttu-id="d50c5-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d50c5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d50c5-110">*discReason* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d50c5-110">*discReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d50c5-111">Specifica il motivo della disconnessione.</span><span class="sxs-lookup"><span data-stu-id="d50c5-111">Specifies the reason for the disconnection.</span></span> <span data-ttu-id="d50c5-112">Di seguito è riportato un elenco di codici di errore.</span><span class="sxs-lookup"><span data-stu-id="d50c5-112">The following is a list of error codes.</span></span> <span data-ttu-id="d50c5-113">Alcuni di questi codici di errore sono definiti in winCred. h.</span><span class="sxs-lookup"><span data-stu-id="d50c5-113">Some of these error codes are defined in Wincred.h.</span></span>

<dt>

<span id="disconnectReasonAtClientWinsockFDCLOSE"></span><span id="disconnectreasonatclientwinsockfdclose"></span><span id="DISCONNECTREASONATCLIENTWINSOCKFDCLOSE"></span>

<span data-ttu-id="d50c5-114"><span id="disconnectReasonAtClientWinsockFDCLOSE"></span><span id="disconnectreasonatclientwinsockfdclose"></span><span id="DISCONNECTREASONATCLIENTWINSOCKFDCLOSE"></span>**disconnectReasonAtClientWinsockFDCLOSE** (2308 (0x904))</span><span class="sxs-lookup"><span data-stu-id="d50c5-114"><span id="disconnectReasonAtClientWinsockFDCLOSE"></span><span id="disconnectreasonatclientwinsockfdclose"></span><span id="DISCONNECTREASONATCLIENTWINSOCKFDCLOSE"></span>**disconnectReasonAtClientWinsockFDCLOSE** (2308 (0x904))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-115">Socket chiuso.</span><span class="sxs-lookup"><span data-stu-id="d50c5-115">Socket closed.</span></span>

</dd> <dt>

<span id="disconnectReasonByServer"></span><span id="disconnectreasonbyserver"></span><span id="DISCONNECTREASONBYSERVER"></span>

<span data-ttu-id="d50c5-116"><span id="disconnectReasonByServer"></span><span id="disconnectreasonbyserver"></span><span id="DISCONNECTREASONBYSERVER"></span>**disconnectReasonByServer** (3 (0x3))</span><span class="sxs-lookup"><span data-stu-id="d50c5-116"><span id="disconnectReasonByServer"></span><span id="disconnectreasonbyserver"></span><span id="DISCONNECTREASONBYSERVER"></span>**disconnectReasonByServer** (3 (0x3))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-117">Disconnessione remota dal server.</span><span class="sxs-lookup"><span data-stu-id="d50c5-117">Remote disconnection by server.</span></span> <span data-ttu-id="d50c5-118">Questo non è un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="d50c5-118">This is not an error code.</span></span>

</dd> <dt>

<span id="disconnectReasonClientDecompressionError"></span><span id="disconnectreasonclientdecompressionerror"></span><span id="DISCONNECTREASONCLIENTDECOMPRESSIONERROR"></span>

<span data-ttu-id="d50c5-119"><span id="disconnectReasonClientDecompressionError"></span><span id="disconnectreasonclientdecompressionerror"></span><span id="DISCONNECTREASONCLIENTDECOMPRESSIONERROR"></span>**disconnectReasonClientDecompressionError** (3080 (0xC08))</span><span class="sxs-lookup"><span data-stu-id="d50c5-119"><span id="disconnectReasonClientDecompressionError"></span><span id="disconnectreasonclientdecompressionerror"></span><span id="DISCONNECTREASONCLIENTDECOMPRESSIONERROR"></span>**disconnectReasonClientDecompressionError** (3080 (0xC08))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-120">Errore di decompressione.</span><span class="sxs-lookup"><span data-stu-id="d50c5-120">Decompression error.</span></span>

</dd> <dt>

<span id="disconnectReasonConnectionTimedOut"></span><span id="disconnectreasonconnectiontimedout"></span><span id="DISCONNECTREASONCONNECTIONTIMEDOUT"></span>

<span data-ttu-id="d50c5-121"><span id="disconnectReasonConnectionTimedOut"></span><span id="disconnectreasonconnectiontimedout"></span><span id="DISCONNECTREASONCONNECTIONTIMEDOUT"></span>**disconnectReasonConnectionTimedOut** (264 (0x108))</span><span class="sxs-lookup"><span data-stu-id="d50c5-121"><span id="disconnectReasonConnectionTimedOut"></span><span id="disconnectreasonconnectiontimedout"></span><span id="DISCONNECTREASONCONNECTIONTIMEDOUT"></span>**disconnectReasonConnectionTimedOut** (264 (0x108))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-122">Timeout della connessione.</span><span class="sxs-lookup"><span data-stu-id="d50c5-122">Connection timed out.</span></span>

</dd> <dt>

<span id="disconnectReasonDecryptionError"></span><span id="disconnectreasondecryptionerror"></span><span id="DISCONNECTREASONDECRYPTIONERROR"></span>

<span data-ttu-id="d50c5-123"><span id="disconnectReasonDecryptionError"></span><span id="disconnectreasondecryptionerror"></span><span id="DISCONNECTREASONDECRYPTIONERROR"></span>**disconnectReasonDecryptionError** (3078 (0xC06))</span><span class="sxs-lookup"><span data-stu-id="d50c5-123"><span id="disconnectReasonDecryptionError"></span><span id="disconnectreasondecryptionerror"></span><span id="DISCONNECTREASONDECRYPTIONERROR"></span>**disconnectReasonDecryptionError** (3078 (0xC06))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-124">Errore di decrittografia.</span><span class="sxs-lookup"><span data-stu-id="d50c5-124">Decryption error.</span></span>

</dd> <dt>

<span id="disconnectReasonDNSLookupFailed"></span><span id="disconnectreasondnslookupfailed"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED"></span>

<span data-ttu-id="d50c5-125"><span id="disconnectReasonDNSLookupFailed"></span><span id="disconnectreasondnslookupfailed"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED"></span>**disconnectReasonDNSLookupFailed** (260 (0x104))</span><span class="sxs-lookup"><span data-stu-id="d50c5-125"><span id="disconnectReasonDNSLookupFailed"></span><span id="disconnectreasondnslookupfailed"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED"></span>**disconnectReasonDNSLookupFailed** (260 (0x104))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-126">Errore di ricerca del nome DNS.</span><span class="sxs-lookup"><span data-stu-id="d50c5-126">DNS name lookup failure.</span></span>

</dd> <dt>

<span id="disconnectReasonDNSLookupFailed2"></span><span id="disconnectreasondnslookupfailed2"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED2"></span>

<span data-ttu-id="d50c5-127"><span id="disconnectReasonDNSLookupFailed2"></span><span id="disconnectreasondnslookupfailed2"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED2"></span>**disconnectReasonDNSLookupFailed2** (1288 (0x508))</span><span class="sxs-lookup"><span data-stu-id="d50c5-127"><span id="disconnectReasonDNSLookupFailed2"></span><span id="disconnectreasondnslookupfailed2"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED2"></span>**disconnectReasonDNSLookupFailed2** (1288 (0x508))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-128">Ricerca DNS non riuscita.</span><span class="sxs-lookup"><span data-stu-id="d50c5-128">DNS lookup failed.</span></span>

</dd> <dt>

<span id="disconnectReasonEncryptionError"></span><span id="disconnectreasonencryptionerror"></span><span id="DISCONNECTREASONENCRYPTIONERROR"></span>

<span data-ttu-id="d50c5-129"><span id="disconnectReasonEncryptionError"></span><span id="disconnectreasonencryptionerror"></span><span id="DISCONNECTREASONENCRYPTIONERROR"></span>**disconnectReasonEncryptionError** (2822 (0xB06))</span><span class="sxs-lookup"><span data-stu-id="d50c5-129"><span id="disconnectReasonEncryptionError"></span><span id="disconnectreasonencryptionerror"></span><span id="DISCONNECTREASONENCRYPTIONERROR"></span>**disconnectReasonEncryptionError** (2822 (0xB06))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-130">Errore di crittografia.</span><span class="sxs-lookup"><span data-stu-id="d50c5-130">Encryption error.</span></span>

</dd> <dt>

<span id="disconnectReasonGetHostByNameFailed"></span><span id="disconnectreasongethostbynamefailed"></span><span id="DISCONNECTREASONGETHOSTBYNAMEFAILED"></span>

<span data-ttu-id="d50c5-131"><span id="disconnectReasonGetHostByNameFailed"></span><span id="disconnectreasongethostbynamefailed"></span><span id="DISCONNECTREASONGETHOSTBYNAMEFAILED"></span>**disconnectReasonGetHostByNameFailed** (1540 (0x604))</span><span class="sxs-lookup"><span data-stu-id="d50c5-131"><span id="disconnectReasonGetHostByNameFailed"></span><span id="disconnectreasongethostbynamefailed"></span><span id="DISCONNECTREASONGETHOSTBYNAMEFAILED"></span>**disconnectReasonGetHostByNameFailed** (1540 (0x604))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-132">Chiamata [**gethostbyname**](/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname) di Windows Sockets non riuscita.</span><span class="sxs-lookup"><span data-stu-id="d50c5-132">Windows Sockets [**gethostbyname**](/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname) call failed.</span></span>

</dd> <dt>

<span id="disconnectReasonHostNotFound"></span><span id="disconnectreasonhostnotfound"></span><span id="DISCONNECTREASONHOSTNOTFOUND"></span>

<span data-ttu-id="d50c5-133"><span id="disconnectReasonHostNotFound"></span><span id="disconnectreasonhostnotfound"></span><span id="DISCONNECTREASONHOSTNOTFOUND"></span>**disconnectReasonHostNotFound** (520 (0x208))</span><span class="sxs-lookup"><span data-stu-id="d50c5-133"><span id="disconnectReasonHostNotFound"></span><span id="disconnectreasonhostnotfound"></span><span id="DISCONNECTREASONHOSTNOTFOUND"></span>**disconnectReasonHostNotFound** (520 (0x208))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-134">Errore host non trovato.</span><span class="sxs-lookup"><span data-stu-id="d50c5-134">Host not found error.</span></span>

</dd> <dt>

<span id="disconnectReasonInternalError"></span><span id="disconnectreasoninternalerror"></span><span id="DISCONNECTREASONINTERNALERROR"></span>

<span data-ttu-id="d50c5-135"><span id="disconnectReasonInternalError"></span><span id="disconnectreasoninternalerror"></span><span id="DISCONNECTREASONINTERNALERROR"></span>**disconnectReasonInternalError** (1032 (0x408))</span><span class="sxs-lookup"><span data-stu-id="d50c5-135"><span id="disconnectReasonInternalError"></span><span id="disconnectreasoninternalerror"></span><span id="DISCONNECTREASONINTERNALERROR"></span>**disconnectReasonInternalError** (1032 (0x408))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-136">Errore interno.</span><span class="sxs-lookup"><span data-stu-id="d50c5-136">Internal error.</span></span>

</dd> <dt>

<span id="disconnectReasonInternalSecurityError"></span><span id="disconnectreasoninternalsecurityerror"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR"></span>

<span data-ttu-id="d50c5-137"><span id="disconnectReasonInternalSecurityError"></span><span id="disconnectreasoninternalsecurityerror"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR"></span>**disconnectReasonInternalSecurityError** (2310 (0x906))</span><span class="sxs-lookup"><span data-stu-id="d50c5-137"><span id="disconnectReasonInternalSecurityError"></span><span id="disconnectreasoninternalsecurityerror"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR"></span>**disconnectReasonInternalSecurityError** (2310 (0x906))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-138">Errore interno di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="d50c5-138">Internal security error.</span></span>

</dd> <dt>

<span id="disconnectReasonInternalSecurityError2"></span><span id="disconnectreasoninternalsecurityerror2"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR2"></span>

<span data-ttu-id="d50c5-139"><span id="disconnectReasonInternalSecurityError2"></span><span id="disconnectreasoninternalsecurityerror2"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR2"></span>**disconnectReasonInternalSecurityError2** (2566 (0xA06))</span><span class="sxs-lookup"><span data-stu-id="d50c5-139"><span id="disconnectReasonInternalSecurityError2"></span><span id="disconnectreasoninternalsecurityerror2"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR2"></span>**disconnectReasonInternalSecurityError2** (2566 (0xA06))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-140">Errore interno di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="d50c5-140">Internal security error.</span></span>

</dd> <dt>

<span id="disconnectReasonInvalidEncryption"></span><span id="disconnectreasoninvalidencryption"></span><span id="DISCONNECTREASONINVALIDENCRYPTION"></span>

<span data-ttu-id="d50c5-141"><span id="disconnectReasonInvalidEncryption"></span><span id="disconnectreasoninvalidencryption"></span><span id="DISCONNECTREASONINVALIDENCRYPTION"></span>**disconnectReasonInvalidEncryption** (1286 (0x506))</span><span class="sxs-lookup"><span data-stu-id="d50c5-141"><span id="disconnectReasonInvalidEncryption"></span><span id="disconnectreasoninvalidencryption"></span><span id="DISCONNECTREASONINVALIDENCRYPTION"></span>**disconnectReasonInvalidEncryption** (1286 (0x506))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-142">Il metodo di crittografia specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="d50c5-142">The encryption method specified is not valid.</span></span>

</dd> <dt>

<span id="disconnectReasonInvalidIP"></span><span id="disconnectreasoninvalidip"></span><span id="DISCONNECTREASONINVALIDIP"></span>

<span data-ttu-id="d50c5-143"><span id="disconnectReasonInvalidIP"></span><span id="disconnectreasoninvalidip"></span><span id="DISCONNECTREASONINVALIDIP"></span>**disconnectReasonInvalidIP** (2052 (0x804))</span><span class="sxs-lookup"><span data-stu-id="d50c5-143"><span id="disconnectReasonInvalidIP"></span><span id="disconnectreasoninvalidip"></span><span id="DISCONNECTREASONINVALIDIP"></span>**disconnectReasonInvalidIP** (2052 (0x804))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-144">È stato specificato un indirizzo IP non valido.</span><span class="sxs-lookup"><span data-stu-id="d50c5-144">Bad IP address specified.</span></span>

</dd> <dt>

<span id="disconnectReasonInvalidServerSecurityInfo"></span><span id="disconnectreasoninvalidserversecurityinfo"></span><span id="DISCONNECTREASONINVALIDSERVERSECURITYINFO"></span>

<span data-ttu-id="d50c5-145"><span id="disconnectReasonInvalidServerSecurityInfo"></span><span id="disconnectreasoninvalidserversecurityinfo"></span><span id="DISCONNECTREASONINVALIDSERVERSECURITYINFO"></span>**disconnectReasonInvalidServerSecurityInfo** (1542 (0x606))</span><span class="sxs-lookup"><span data-stu-id="d50c5-145"><span id="disconnectReasonInvalidServerSecurityInfo"></span><span id="disconnectreasoninvalidserversecurityinfo"></span><span id="DISCONNECTREASONINVALIDSERVERSECURITYINFO"></span>**disconnectReasonInvalidServerSecurityInfo** (1542 (0x606))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-146">I dati di sicurezza del server non sono validi.</span><span class="sxs-lookup"><span data-stu-id="d50c5-146">Server security data is not valid.</span></span>

</dd> <dt>

<span id="disconnectReasonInvalidSecurityData"></span><span id="disconnectreasoninvalidsecuritydata"></span><span id="DISCONNECTREASONINVALIDSECURITYDATA"></span>

<span data-ttu-id="d50c5-147"><span id="disconnectReasonInvalidSecurityData"></span><span id="disconnectreasoninvalidsecuritydata"></span><span id="DISCONNECTREASONINVALIDSECURITYDATA"></span>**disconnectReasonInvalidSecurityData** (1030 (0x406))</span><span class="sxs-lookup"><span data-stu-id="d50c5-147"><span id="disconnectReasonInvalidSecurityData"></span><span id="disconnectreasoninvalidsecuritydata"></span><span id="DISCONNECTREASONINVALIDSECURITYDATA"></span>**disconnectReasonInvalidSecurityData** (1030 (0x406))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-148">I dati di sicurezza non sono validi.</span><span class="sxs-lookup"><span data-stu-id="d50c5-148">Security data is not valid.</span></span>

</dd> <dt>

<span id="disconnectReasonInvalidIPAddr"></span><span id="disconnectreasoninvalidipaddr"></span><span id="DISCONNECTREASONINVALIDIPADDR"></span>

<span data-ttu-id="d50c5-149"><span id="disconnectReasonInvalidIPAddr"></span><span id="disconnectreasoninvalidipaddr"></span><span id="DISCONNECTREASONINVALIDIPADDR"></span>**disconnectReasonInvalidIPAddr** (776 (0x308))</span><span class="sxs-lookup"><span data-stu-id="d50c5-149"><span id="disconnectReasonInvalidIPAddr"></span><span id="disconnectreasoninvalidipaddr"></span><span id="DISCONNECTREASONINVALIDIPADDR"></span>**disconnectReasonInvalidIPAddr** (776 (0x308))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-150">L'indirizzo IP specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="d50c5-150">The IP address specified is not valid.</span></span>

</dd> <dt>

<span id="disconnectReasonLicensingFailed"></span><span id="disconnectreasonlicensingfailed"></span><span id="DISCONNECTREASONLICENSINGFAILED"></span>

<span data-ttu-id="d50c5-151"><span id="disconnectReasonLicensingFailed"></span><span id="disconnectreasonlicensingfailed"></span><span id="DISCONNECTREASONLICENSINGFAILED"></span>**disconnectReasonLicensingFailed** (2056 (0x808))</span><span class="sxs-lookup"><span data-stu-id="d50c5-151"><span id="disconnectReasonLicensingFailed"></span><span id="disconnectreasonlicensingfailed"></span><span id="DISCONNECTREASONLICENSINGFAILED"></span>**disconnectReasonLicensingFailed** (2056 (0x808))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-152">Negoziazione della licenza non riuscita.</span><span class="sxs-lookup"><span data-stu-id="d50c5-152">License negotiation failed.</span></span>

</dd> <dt>

<span id="disconnectReasonLicensingTimeout"></span><span id="disconnectreasonlicensingtimeout"></span><span id="DISCONNECTREASONLICENSINGTIMEOUT"></span>

<span data-ttu-id="d50c5-153"><span id="disconnectReasonLicensingTimeout"></span><span id="disconnectreasonlicensingtimeout"></span><span id="DISCONNECTREASONLICENSINGTIMEOUT"></span>**disconnectReasonLicensingTimeout** (2312 (0x908))</span><span class="sxs-lookup"><span data-stu-id="d50c5-153"><span id="disconnectReasonLicensingTimeout"></span><span id="disconnectreasonlicensingtimeout"></span><span id="DISCONNECTREASONLICENSINGTIMEOUT"></span>**disconnectReasonLicensingTimeout** (2312 (0x908))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-154">Timeout della gestione delle licenze.</span><span class="sxs-lookup"><span data-stu-id="d50c5-154">Licensing time-out.</span></span>

</dd> <dt>

<span id="disconnectReasonLocalNotError"></span><span id="disconnectreasonlocalnoterror"></span><span id="DISCONNECTREASONLOCALNOTERROR"></span>

<span data-ttu-id="d50c5-155"><span id="disconnectReasonLocalNotError"></span><span id="disconnectreasonlocalnoterror"></span><span id="DISCONNECTREASONLOCALNOTERROR"></span>**disconnectReasonLocalNotError** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="d50c5-155"><span id="disconnectReasonLocalNotError"></span><span id="disconnectreasonlocalnoterror"></span><span id="DISCONNECTREASONLOCALNOTERROR"></span>**disconnectReasonLocalNotError** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-156">Disconnessione locale.</span><span class="sxs-lookup"><span data-stu-id="d50c5-156">Local disconnection.</span></span> <span data-ttu-id="d50c5-157">Questo non è un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="d50c5-157">This is not an error code.</span></span>

</dd> <dt>

<span id="disconnectReasonNoInfo"></span><span id="disconnectreasonnoinfo"></span><span id="DISCONNECTREASONNOINFO"></span>

<span data-ttu-id="d50c5-158"><span id="disconnectReasonNoInfo"></span><span id="disconnectreasonnoinfo"></span><span id="DISCONNECTREASONNOINFO"></span>**disconnectReasonNoInfo** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="d50c5-158"><span id="disconnectReasonNoInfo"></span><span id="disconnectreasonnoinfo"></span><span id="DISCONNECTREASONNOINFO"></span>**disconnectReasonNoInfo** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-159">Nessuna informazione disponibile.</span><span class="sxs-lookup"><span data-stu-id="d50c5-159">No information is available.</span></span>

</dd> <dt>

<span id="disconnectReasonOutOfMemory"></span><span id="disconnectreasonoutofmemory"></span><span id="DISCONNECTREASONOUTOFMEMORY"></span>

<span data-ttu-id="d50c5-160"><span id="disconnectReasonOutOfMemory"></span><span id="disconnectreasonoutofmemory"></span><span id="DISCONNECTREASONOUTOFMEMORY"></span>**disconnectReasonOutOfMemory** (262 (0x106))</span><span class="sxs-lookup"><span data-stu-id="d50c5-160"><span id="disconnectReasonOutOfMemory"></span><span id="disconnectreasonoutofmemory"></span><span id="DISCONNECTREASONOUTOFMEMORY"></span>**disconnectReasonOutOfMemory** (262 (0x106))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-161">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="d50c5-161">Out of memory.</span></span>

</dd> <dt>

<span id="disconnectReasonOutOfMemory2"></span><span id="disconnectreasonoutofmemory2"></span><span id="DISCONNECTREASONOUTOFMEMORY2"></span>

<span data-ttu-id="d50c5-162"><span id="disconnectReasonOutOfMemory2"></span><span id="disconnectreasonoutofmemory2"></span><span id="DISCONNECTREASONOUTOFMEMORY2"></span>**disconnectReasonOutOfMemory2** (518 (0x206))</span><span class="sxs-lookup"><span data-stu-id="d50c5-162"><span id="disconnectReasonOutOfMemory2"></span><span id="disconnectreasonoutofmemory2"></span><span id="DISCONNECTREASONOUTOFMEMORY2"></span>**disconnectReasonOutOfMemory2** (518 (0x206))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-163">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="d50c5-163">Out of memory.</span></span>

</dd> <dt>

<span id="disconnectReasonOutOfMemory3"></span><span id="disconnectreasonoutofmemory3"></span><span id="DISCONNECTREASONOUTOFMEMORY3"></span>

<span data-ttu-id="d50c5-164"><span id="disconnectReasonOutOfMemory3"></span><span id="disconnectreasonoutofmemory3"></span><span id="DISCONNECTREASONOUTOFMEMORY3"></span>**disconnectReasonOutOfMemory3** (774 (0x306))</span><span class="sxs-lookup"><span data-stu-id="d50c5-164"><span id="disconnectReasonOutOfMemory3"></span><span id="disconnectreasonoutofmemory3"></span><span id="DISCONNECTREASONOUTOFMEMORY3"></span>**disconnectReasonOutOfMemory3** (774 (0x306))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-165">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="d50c5-165">Out of memory.</span></span>

</dd> <dt>

<span id="disconnectReasonRemoteByUser"></span><span id="disconnectreasonremotebyuser"></span><span id="DISCONNECTREASONREMOTEBYUSER"></span>

<span data-ttu-id="d50c5-166"><span id="disconnectReasonRemoteByUser"></span><span id="disconnectreasonremotebyuser"></span><span id="DISCONNECTREASONREMOTEBYUSER"></span>**disconnectReasonRemoteByUser** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="d50c5-166"><span id="disconnectReasonRemoteByUser"></span><span id="disconnectreasonremotebyuser"></span><span id="DISCONNECTREASONREMOTEBYUSER"></span>**disconnectReasonRemoteByUser** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-167">Disconnessione remota da un utente.</span><span class="sxs-lookup"><span data-stu-id="d50c5-167">Remote disconnection by user.</span></span> <span data-ttu-id="d50c5-168">Questo non è un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="d50c5-168">This is not an error code.</span></span>

</dd> <dt>

<span id="disconnectReasonServerCertificateUnpackErr"></span><span id="disconnectreasonservercertificateunpackerr"></span><span id="DISCONNECTREASONSERVERCERTIFICATEUNPACKERR"></span>

<span data-ttu-id="d50c5-169"><span id="disconnectReasonServerCertificateUnpackErr"></span><span id="disconnectreasonservercertificateunpackerr"></span><span id="DISCONNECTREASONSERVERCERTIFICATEUNPACKERR"></span>**disconnectReasonServerCertificateUnpackErr** (1798 (0x706))</span><span class="sxs-lookup"><span data-stu-id="d50c5-169"><span id="disconnectReasonServerCertificateUnpackErr"></span><span id="disconnectreasonservercertificateunpackerr"></span><span id="DISCONNECTREASONSERVERCERTIFICATEUNPACKERR"></span>**disconnectReasonServerCertificateUnpackErr** (1798 (0x706))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-170">Non è stato possibile decomprimere il certificato server.</span><span class="sxs-lookup"><span data-stu-id="d50c5-170">Failed to unpack server certificate.</span></span>

</dd> <dt>

<span id="disconnectReasonSocketConnectFailed"></span><span id="disconnectreasonsocketconnectfailed"></span><span id="DISCONNECTREASONSOCKETCONNECTFAILED"></span>

<span data-ttu-id="d50c5-171"><span id="disconnectReasonSocketConnectFailed"></span><span id="disconnectreasonsocketconnectfailed"></span><span id="DISCONNECTREASONSOCKETCONNECTFAILED"></span>**disconnectReasonSocketConnectFailed** (516 (0x204))</span><span class="sxs-lookup"><span data-stu-id="d50c5-171"><span id="disconnectReasonSocketConnectFailed"></span><span id="disconnectreasonsocketconnectfailed"></span><span id="DISCONNECTREASONSOCKETCONNECTFAILED"></span>**disconnectReasonSocketConnectFailed** (516 (0x204))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-172">[**Connessione**](/windows/desktop/api/winsock2/nf-winsock2-connect) Windows Sockets non riuscita.</span><span class="sxs-lookup"><span data-stu-id="d50c5-172">Windows Sockets [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) failed.</span></span>

</dd> <dt>

<span id="disconnectReasonSocketRecvFailed"></span><span id="disconnectreasonsocketrecvfailed"></span><span id="DISCONNECTREASONSOCKETRECVFAILED"></span>

<span data-ttu-id="d50c5-173"><span id="disconnectReasonSocketRecvFailed"></span><span id="disconnectreasonsocketrecvfailed"></span><span id="DISCONNECTREASONSOCKETRECVFAILED"></span>**disconnectReasonSocketRecvFailed** (1028 (0x404))</span><span class="sxs-lookup"><span data-stu-id="d50c5-173"><span id="disconnectReasonSocketRecvFailed"></span><span id="disconnectreasonsocketrecvfailed"></span><span id="DISCONNECTREASONSOCKETRECVFAILED"></span>**disconnectReasonSocketRecvFailed** (1028 (0x404))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-174">Chiamata [**ricezione**](/windows/desktop/api/winsock/nf-winsock-recv) di Windows Sockets non riuscita.</span><span class="sxs-lookup"><span data-stu-id="d50c5-174">Windows Sockets [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) call failed.</span></span>

</dd> <dt>

<span id="disconnectReasonTimeoutOccurred"></span><span id="disconnectreasontimeoutoccurred"></span><span id="DISCONNECTREASONTIMEOUTOCCURRED"></span>

<span data-ttu-id="d50c5-175"><span id="disconnectReasonTimeoutOccurred"></span><span id="disconnectreasontimeoutoccurred"></span><span id="DISCONNECTREASONTIMEOUTOCCURRED"></span>**disconnectReasonTimeoutOccurred** (1796 (0x704))</span><span class="sxs-lookup"><span data-stu-id="d50c5-175"><span id="disconnectReasonTimeoutOccurred"></span><span id="disconnectreasontimeoutoccurred"></span><span id="DISCONNECTREASONTIMEOUTOCCURRED"></span>**disconnectReasonTimeoutOccurred** (1796 (0x704))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-176">Si è verificato il timeout.</span><span class="sxs-lookup"><span data-stu-id="d50c5-176">Time-out occurred.</span></span>

</dd> <dt>

<span id="disconnectReasonTimerError"></span><span id="disconnectreasontimererror"></span><span id="DISCONNECTREASONTIMERERROR"></span>

<span data-ttu-id="d50c5-177"><span id="disconnectReasonTimerError"></span><span id="disconnectreasontimererror"></span><span id="DISCONNECTREASONTIMERERROR"></span>**disconnectReasonTimerError** (1544 (0x608))</span><span class="sxs-lookup"><span data-stu-id="d50c5-177"><span id="disconnectReasonTimerError"></span><span id="disconnectreasontimererror"></span><span id="DISCONNECTREASONTIMERERROR"></span>**disconnectReasonTimerError** (1544 (0x608))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-178">Errore interno del timer.</span><span class="sxs-lookup"><span data-stu-id="d50c5-178">Internal timer error.</span></span>

</dd> <dt>

<span id="disconnectReasonWinsockSendFailed"></span><span id="disconnectreasonwinsocksendfailed"></span><span id="DISCONNECTREASONWINSOCKSENDFAILED"></span>

<span data-ttu-id="d50c5-179"><span id="disconnectReasonWinsockSendFailed"></span><span id="disconnectreasonwinsocksendfailed"></span><span id="DISCONNECTREASONWINSOCKSENDFAILED"></span>**disconnectReasonWinsockSendFailed** (772 (0x304))</span><span class="sxs-lookup"><span data-stu-id="d50c5-179"><span id="disconnectReasonWinsockSendFailed"></span><span id="disconnectreasonwinsocksendfailed"></span><span id="DISCONNECTREASONWINSOCKSENDFAILED"></span>**disconnectReasonWinsockSendFailed** (772 (0x304))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-180">Chiamata di [**invio**](/windows/desktop/api/winsock2/nf-winsock2-send) Windows Sockets non riuscita.</span><span class="sxs-lookup"><span data-stu-id="d50c5-180">Windows Sockets [**send**](/windows/desktop/api/winsock2/nf-winsock2-send) call failed.</span></span>

</dd> <dt>

<span id="SSL_ERR_ACCOUNT_DISABLED"></span><span id="ssl_err_account_disabled"></span>

<span data-ttu-id="d50c5-181"><span id="SSL_ERR_ACCOUNT_DISABLED"></span><span id="ssl_err_account_disabled"></span>**SSL \_ \_Account ERR \_ disabilitato** (2823 (0xB07))</span><span class="sxs-lookup"><span data-stu-id="d50c5-181"><span id="SSL_ERR_ACCOUNT_DISABLED"></span><span id="ssl_err_account_disabled"></span>**SSL\_ERR\_ACCOUNT\_DISABLED** (2823 (0xB07))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-182">L'account è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="d50c5-182">The account is disabled.</span></span>

</dd> <dt>

<span id="SSL_ERR_ACCOUNT_EXPIRED"></span><span id="ssl_err_account_expired"></span>

<span data-ttu-id="d50c5-183"><span id="SSL_ERR_ACCOUNT_EXPIRED"></span><span id="ssl_err_account_expired"></span>**SSL \_ \_Account ERR \_ scaduto** (3591 (0xE07))</span><span class="sxs-lookup"><span data-stu-id="d50c5-183"><span id="SSL_ERR_ACCOUNT_EXPIRED"></span><span id="ssl_err_account_expired"></span>**SSL\_ERR\_ACCOUNT\_EXPIRED** (3591 (0xE07))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-184">L'account è scaduto.</span><span class="sxs-lookup"><span data-stu-id="d50c5-184">The account is expired.</span></span>

</dd> <dt>

<span id="SSL_ERR_ACCOUNT_LOCKED_OUT"></span><span id="ssl_err_account_locked_out"></span>

<span data-ttu-id="d50c5-185"><span id="SSL_ERR_ACCOUNT_LOCKED_OUT"></span><span id="ssl_err_account_locked_out"></span>**SSL \_ \_Account ERR \_ bloccato \_** (3335 (0xD07))</span><span class="sxs-lookup"><span data-stu-id="d50c5-185"><span id="SSL_ERR_ACCOUNT_LOCKED_OUT"></span><span id="ssl_err_account_locked_out"></span>**SSL\_ERR\_ACCOUNT\_LOCKED\_OUT** (3335 (0xD07))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-186">L'account è bloccato.</span><span class="sxs-lookup"><span data-stu-id="d50c5-186">The account is locked out.</span></span>

</dd> <dt>

<span id="SSL_ERR_ACCOUNT_RESTRICTION"></span><span id="ssl_err_account_restriction"></span>

<span data-ttu-id="d50c5-187"><span id="SSL_ERR_ACCOUNT_RESTRICTION"></span><span id="ssl_err_account_restriction"></span>**SSL \_ \_ \_ Restrizione dell'account ERR** (3079 (0xC07))</span><span class="sxs-lookup"><span data-stu-id="d50c5-187"><span id="SSL_ERR_ACCOUNT_RESTRICTION"></span><span id="ssl_err_account_restriction"></span>**SSL\_ERR\_ACCOUNT\_RESTRICTION** (3079 (0xC07))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-188">L'account è limitato.</span><span class="sxs-lookup"><span data-stu-id="d50c5-188">The account is restricted.</span></span>

</dd> <dt>

<span id="SSL_ERR_CERT_EXPIRED"></span><span id="ssl_err_cert_expired"></span>

<span data-ttu-id="d50c5-189"><span id="SSL_ERR_CERT_EXPIRED"></span><span id="ssl_err_cert_expired"></span>**SSL \_ Il \_ certificato \_ Err è scaduto** (6919 (0x1B07))</span><span class="sxs-lookup"><span data-stu-id="d50c5-189"><span id="SSL_ERR_CERT_EXPIRED"></span><span id="ssl_err_cert_expired"></span>**SSL\_ERR\_CERT\_EXPIRED** (6919 (0x1B07))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-190">Il certificato ricevuto è scaduto.</span><span class="sxs-lookup"><span data-stu-id="d50c5-190">The received certificate is expired.</span></span>

</dd> <dt>

<span id="SSL_ERR_DELEGATION_POLICY"></span><span id="ssl_err_delegation_policy"></span>

<span data-ttu-id="d50c5-191"><span id="SSL_ERR_DELEGATION_POLICY"></span><span id="ssl_err_delegation_policy"></span>**SSL \_ \_ \_ Criteri di delega ERR** (5639 (0x1607))</span><span class="sxs-lookup"><span data-stu-id="d50c5-191"><span id="SSL_ERR_DELEGATION_POLICY"></span><span id="ssl_err_delegation_policy"></span>**SSL\_ERR\_DELEGATION\_POLICY** (5639 (0x1607))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-192">Il criterio non supporta la delega delle credenziali al server di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d50c5-192">The policy does not support delegation of credentials to the target server.</span></span>

</dd> <dt>

<span id="SSL_ERR_FRESH_CRED_REQUIRED_BY_SERVER"></span><span id="ssl_err_fresh_cred_required_by_server"></span>

<span data-ttu-id="d50c5-193"><span id="SSL_ERR_FRESH_CRED_REQUIRED_BY_SERVER"></span><span id="ssl_err_fresh_cred_required_by_server"></span>**SSL \_ ERR \_ Fresh \_ cred \_ richiesta \_ dal \_ Server** (8455 (0x2107))</span><span class="sxs-lookup"><span data-stu-id="d50c5-193"><span id="SSL_ERR_FRESH_CRED_REQUIRED_BY_SERVER"></span><span id="ssl_err_fresh_cred_required_by_server"></span>**SSL\_ERR\_FRESH\_CRED\_REQUIRED\_BY\_SERVER** (8455 (0x2107))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-194">Il criterio di autenticazione server non consente le richieste di connessione tramite le credenziali salvate.</span><span class="sxs-lookup"><span data-stu-id="d50c5-194">The server authentication policy does not allow connection requests using saved credentials.</span></span> <span data-ttu-id="d50c5-195">L'utente deve immettere le nuove credenziali.</span><span class="sxs-lookup"><span data-stu-id="d50c5-195">The user must enter new credentials.</span></span>

</dd> <dt>

<span id="SSL_ERR_LOGON_FAILURE"></span><span id="ssl_err_logon_failure"></span>

<span data-ttu-id="d50c5-196"><span id="SSL_ERR_LOGON_FAILURE"></span><span id="ssl_err_logon_failure"></span>**SSL \_ \_ \_ Errore di accesso ERR** (2055 (0x807))</span><span class="sxs-lookup"><span data-stu-id="d50c5-196"><span id="SSL_ERR_LOGON_FAILURE"></span><span id="ssl_err_logon_failure"></span>**SSL\_ERR\_LOGON\_FAILURE** (2055 (0x807))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-197">Accesso non riuscito.</span><span class="sxs-lookup"><span data-stu-id="d50c5-197">Login failed.</span></span>

</dd> <dt>

<span id="SSL_ERR_NO_AUTHENTICATING_AUTHORITY"></span><span id="ssl_err_no_authenticating_authority"></span>

<span data-ttu-id="d50c5-198"><span id="SSL_ERR_NO_AUTHENTICATING_AUTHORITY"></span><span id="ssl_err_no_authenticating_authority"></span>**SSL \_ \_Nessuna \_ \_ autorità di autenticazione** (6151 (0x1807))</span><span class="sxs-lookup"><span data-stu-id="d50c5-198"><span id="SSL_ERR_NO_AUTHENTICATING_AUTHORITY"></span><span id="ssl_err_no_authenticating_authority"></span>**SSL\_ERR\_NO\_AUTHENTICATING\_AUTHORITY** (6151 (0x1807))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-199">Non è stato possibile contattare un'autorità per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="d50c5-199">No authority could be contacted for authentication.</span></span> <span data-ttu-id="d50c5-200">Il nome di dominio dell'entità di autenticazione potrebbe essere errato, il dominio potrebbe non essere raggiungibile o potrebbe essersi verificato un errore di relazione di trust.</span><span class="sxs-lookup"><span data-stu-id="d50c5-200">The domain name of the authenticating party could be wrong, the domain could be unreachable, or there might have been a trust relationship failure.</span></span>

</dd> <dt>

<span id="SSL_ERR_NO_SUCH_USER"></span><span id="ssl_err_no_such_user"></span>

<span data-ttu-id="d50c5-201"><span id="SSL_ERR_NO_SUCH_USER"></span><span id="ssl_err_no_such_user"></span>**SSL \_ ERR \_ No \_ \_ User** (2567 (0xA07))</span><span class="sxs-lookup"><span data-stu-id="d50c5-201"><span id="SSL_ERR_NO_SUCH_USER"></span><span id="ssl_err_no_such_user"></span>**SSL\_ERR\_NO\_SUCH\_USER** (2567 (0xA07))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-202">L'utente specificato non dispone di alcun account.</span><span class="sxs-lookup"><span data-stu-id="d50c5-202">The specified user has no account.</span></span>

</dd> <dt>

<span id="SSL_ERR_PASSWORD_EXPIRED"></span><span id="ssl_err_password_expired"></span>

<span data-ttu-id="d50c5-203"><span id="SSL_ERR_PASSWORD_EXPIRED"></span><span id="ssl_err_password_expired"></span>**SSL \_ \_Password ERR \_ scaduta** (3847 (0xF07))</span><span class="sxs-lookup"><span data-stu-id="d50c5-203"><span id="SSL_ERR_PASSWORD_EXPIRED"></span><span id="ssl_err_password_expired"></span>**SSL\_ERR\_PASSWORD\_EXPIRED** (3847 (0xF07))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-204">La password è scaduta.</span><span class="sxs-lookup"><span data-stu-id="d50c5-204">The password is expired.</span></span>

</dd> <dt>

<span id="SSL_ERR_PASSWORD_MUST_CHANGE"></span><span id="ssl_err_password_must_change"></span>

<span data-ttu-id="d50c5-205"><span id="SSL_ERR_PASSWORD_MUST_CHANGE"></span><span id="ssl_err_password_must_change"></span>**SSL \_ \_ \_ \_ Modificare la PASSWORD Err** (4615 (0x1207))</span><span class="sxs-lookup"><span data-stu-id="d50c5-205"><span id="SSL_ERR_PASSWORD_MUST_CHANGE"></span><span id="ssl_err_password_must_change"></span>**SSL\_ERR\_PASSWORD\_MUST\_CHANGE** (4615 (0x1207))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-206">È necessario modificare la password utente prima di accedere per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="d50c5-206">The user password must be changed before logging on for the first time.</span></span>

</dd> <dt>

<span id="SSL_ERR_POLICY_NTLM_ONLY"></span><span id="ssl_err_policy_ntlm_only"></span>

<span data-ttu-id="d50c5-207"><span id="SSL_ERR_POLICY_NTLM_ONLY"></span><span id="ssl_err_policy_ntlm_only"></span>**SSL \_ \_Criterio ERR \_ \_ solo NTLM** (5895 (0x1707))</span><span class="sxs-lookup"><span data-stu-id="d50c5-207"><span id="SSL_ERR_POLICY_NTLM_ONLY"></span><span id="ssl_err_policy_ntlm_only"></span>**SSL\_ERR\_POLICY\_NTLM\_ONLY** (5895 (0x1707))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-208">La delega delle credenziali al server di destinazione non è consentita, a meno che non sia stata eseguita l'autenticazione reciproca.</span><span class="sxs-lookup"><span data-stu-id="d50c5-208">Delegation of credentials to the target server is not allowed unless mutual authentication has been achieved.</span></span>

</dd> <dt>

<span id="SSL_ERR_SMARTCARD_CARD_BLOCKED"></span><span id="ssl_err_smartcard_card_blocked"></span>

<span data-ttu-id="d50c5-209"><span id="SSL_ERR_SMARTCARD_CARD_BLOCKED"></span><span id="ssl_err_smartcard_card_blocked"></span>**SSL \_ \_Scheda SmartCard \_ Err \_ bloccata** (8711 (0x2207))</span><span class="sxs-lookup"><span data-stu-id="d50c5-209"><span id="SSL_ERR_SMARTCARD_CARD_BLOCKED"></span><span id="ssl_err_smartcard_card_blocked"></span>**SSL\_ERR\_SMARTCARD\_CARD\_BLOCKED** (8711 (0x2207))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-210">La smart card è bloccata.</span><span class="sxs-lookup"><span data-stu-id="d50c5-210">The smart card is blocked.</span></span>

</dd> <dt>

<span id="SSL_ERR_SMARTCARD_WRONG_PIN"></span><span id="ssl_err_smartcard_wrong_pin"></span>

<span data-ttu-id="d50c5-211"><span id="SSL_ERR_SMARTCARD_WRONG_PIN"></span><span id="ssl_err_smartcard_wrong_pin"></span>**SSL \_ ERRORE \_ \_ \_ pin SMARTCARD errato** (7175 (0x1C07))</span><span class="sxs-lookup"><span data-stu-id="d50c5-211"><span id="SSL_ERR_SMARTCARD_WRONG_PIN"></span><span id="ssl_err_smartcard_wrong_pin"></span>**SSL\_ERR\_SMARTCARD\_WRONG\_PIN** (7175 (0x1C07))</span></span>


</dt> <dd>

<span data-ttu-id="d50c5-212">Un PIN errato è stato presentato alla smart card.</span><span class="sxs-lookup"><span data-stu-id="d50c5-212">An incorrect PIN was presented to the smart card.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d50c5-213">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d50c5-213">Return value</span></span>

<span data-ttu-id="d50c5-214">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="d50c5-214">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d50c5-215">Commenti</span><span class="sxs-lookup"><span data-stu-id="d50c5-215">Remarks</span></span>

<span data-ttu-id="d50c5-216">Per recuperare una descrizione dell'errore di disconnessione, chiamare il metodo [**GetErrorDescription**](imsrdpclient5-geterrordescription.md) e passargli il parametro *discReason* e la proprietà [**ExtendedDisconnectReason**](imsrdpclient-extendeddisconnectreason.md) dell'interfaccia [**IMsRdpClient**](imsrdpclient-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="d50c5-216">To retrieve a description of the disconnect error, call the [**GetErrorDescription**](imsrdpclient5-geterrordescription.md) method and pass it the *discReason* parameter and the [**ExtendedDisconnectReason**](imsrdpclient-extendeddisconnectreason.md) property of the [**IMsRdpClient**](imsrdpclient-interface.md) interface.</span></span>

<span data-ttu-id="d50c5-217">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="d50c5-217">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d50c5-218">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d50c5-218">Requirements</span></span>



| <span data-ttu-id="d50c5-219">Requisito</span><span class="sxs-lookup"><span data-stu-id="d50c5-219">Requirement</span></span> | <span data-ttu-id="d50c5-220">Valore</span><span class="sxs-lookup"><span data-stu-id="d50c5-220">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d50c5-221">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d50c5-221">Minimum supported client</span></span><br/> | <span data-ttu-id="d50c5-222">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d50c5-222">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d50c5-223">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d50c5-223">Minimum supported server</span></span><br/> | <span data-ttu-id="d50c5-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d50c5-224">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d50c5-225">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="d50c5-225">Type library</span></span><br/>             | <dl> <span data-ttu-id="d50c5-226"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d50c5-226"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d50c5-227">DLL</span><span class="sxs-lookup"><span data-stu-id="d50c5-227">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d50c5-228"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d50c5-228"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d50c5-229">IID</span><span class="sxs-lookup"><span data-stu-id="d50c5-229">IID</span></span><br/>                      | <span data-ttu-id="d50c5-230">IMsTscAxEvents è definito come 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="d50c5-230">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="d50c5-231">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d50c5-231">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d50c5-232">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="d50c5-232">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

