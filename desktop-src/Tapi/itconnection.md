---
description: La funzionalità dell'interfaccia ITConnection è illustrata di seguito.
ms.assetid: 44dc39cf-3222-41ed-b29c-df2d32615500
title: Interfaccia ITConnection (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a00da80631c0ef4e8186aa36425f18e4d2a62bfc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333143"
---
# <a name="itconnection-interface"></a><span data-ttu-id="e13d9-103">Interfaccia ITConnection</span><span class="sxs-lookup"><span data-stu-id="e13d9-103">ITConnection interface</span></span>

<span data-ttu-id="e13d9-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e13d9-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e13d9-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="e13d9-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e13d9-106">L'interfaccia **ITConnection** fornisce le funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="e13d9-106">The **ITConnection** interface provides the following functionality:</span></span>

-   <span data-ttu-id="e13d9-107">Consente di accedere alle informazioni relative all'indirizzo e alla durata (TTL) per la sessione.</span><span class="sxs-lookup"><span data-stu-id="e13d9-107">Provides access to the address and time to live (TTL) information for the session.</span></span>
-   <span data-ttu-id="e13d9-108">Consente di accedere alle informazioni sulla larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="e13d9-108">Provides access to the bandwidth information.</span></span>
-   <span data-ttu-id="e13d9-109">Abilita la manipolazione della chiave di crittografia.</span><span class="sxs-lookup"><span data-stu-id="e13d9-109">Enables manipulation of the encryption key.</span></span>

<span data-ttu-id="e13d9-110">L'interfaccia **ITConnection** viene creata chiamando **QueryInterface** in [**ITConferenceBlob**](itconferenceblob.md).</span><span class="sxs-lookup"><span data-stu-id="e13d9-110">The **ITConnection** interface is created by calling **QueryInterface** on [**ITConferenceBlob**](itconferenceblob.md).</span></span>

## <a name="members"></a><span data-ttu-id="e13d9-111">Membri</span><span class="sxs-lookup"><span data-stu-id="e13d9-111">Members</span></span>

<span data-ttu-id="e13d9-112">L'interfaccia **ITConnection** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="e13d9-112">The **ITConnection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="e13d9-113">**ITConnection** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e13d9-113">**ITConnection** also has these types of members:</span></span>

-   [<span data-ttu-id="e13d9-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="e13d9-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e13d9-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="e13d9-115">Methods</span></span>

<span data-ttu-id="e13d9-116">L'interfaccia **ITConnection** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="e13d9-116">The **ITConnection** interface has these methods.</span></span>



| <span data-ttu-id="e13d9-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="e13d9-117">Method</span></span>                                                               | <span data-ttu-id="e13d9-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e13d9-118">Description</span></span>                                                                                                                                    |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e13d9-119">**ottenere \_ AddressType**</span><span class="sxs-lookup"><span data-stu-id="e13d9-119">**get\_AddressType**</span></span>](itconnection-get-addresstype.md)             | <span data-ttu-id="e13d9-120">Ottiene il tipo di indirizzo.</span><span class="sxs-lookup"><span data-stu-id="e13d9-120">Gets the address type.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="e13d9-121">**ottenere la \_ larghezza di banda**</span><span class="sxs-lookup"><span data-stu-id="e13d9-121">**get\_Bandwidth**</span></span>](itconnection-get-bandwidth.md)                 | <span data-ttu-id="e13d9-122">Ottiene il valore della larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="e13d9-122">Gets bandwidth value.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="e13d9-123">**ottenere \_ BandwidthModifier**</span><span class="sxs-lookup"><span data-stu-id="e13d9-123">**get\_BandwidthModifier**</span></span>](itconnection-get-bandwidthmodifier.md) | <span data-ttu-id="e13d9-124">Ottiene il modificatore della larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="e13d9-124">Gets the bandwidth modifier.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="e13d9-125">**ottenere \_ NetworkType**</span><span class="sxs-lookup"><span data-stu-id="e13d9-125">**get\_NetworkType**</span></span>](itconnection-get-networktype.md)             | <span data-ttu-id="e13d9-126">Ottiene il tipo di rete.</span><span class="sxs-lookup"><span data-stu-id="e13d9-126">Gets the network type.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="e13d9-127">**ottenere \_ NumAddresses**</span><span class="sxs-lookup"><span data-stu-id="e13d9-127">**get\_NumAddresses**</span></span>](itconnection-get-numaddresses.md)           | <span data-ttu-id="e13d9-128">Ottiene il numero di indirizzi da utilizzare per la sessione.</span><span class="sxs-lookup"><span data-stu-id="e13d9-128">Gets the number of addresses to be used for the session.</span></span><br/>                                                                            |
| [<span data-ttu-id="e13d9-129">**ottenere \_ STARTADDRESS**</span><span class="sxs-lookup"><span data-stu-id="e13d9-129">**get\_StartAddress**</span></span>](itconnection-get-startaddress.md)           | <span data-ttu-id="e13d9-130">Ottiene il primo indirizzo da utilizzare per la sessione.</span><span class="sxs-lookup"><span data-stu-id="e13d9-130">Gets the first address to be used for the session.</span></span><br/>                                                                                  |
| [<span data-ttu-id="e13d9-131">**ottenere la durata ( \_ TTL)**</span><span class="sxs-lookup"><span data-stu-id="e13d9-131">**get\_Ttl**</span></span>](itconnection-get-ttl.md)                             | <span data-ttu-id="e13d9-132">Ottiene l'ambito TTL ( [*time to Live*](t-tapgloss.md) ) per le trasmissioni sugli indirizzi.</span><span class="sxs-lookup"><span data-stu-id="e13d9-132">Gets the [*time to live*](t-tapgloss.md) (TTL) scope for transmissions on the addresses.</span></span><br/> |
| [<span data-ttu-id="e13d9-133">**GetEncryptionKey**</span><span class="sxs-lookup"><span data-stu-id="e13d9-133">**GetEncryptionKey**</span></span>](itconnection-getencryptionkey.md)            | <span data-ttu-id="e13d9-134">Ottiene la chiave di crittografia.</span><span class="sxs-lookup"><span data-stu-id="e13d9-134">Gets the encryption key.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="e13d9-135">**Inserisci \_ AddressType**</span><span class="sxs-lookup"><span data-stu-id="e13d9-135">**put\_AddressType**</span></span>](itconnection-put-addresstype.md)             | <span data-ttu-id="e13d9-136">Imposta il tipo di indirizzo.</span><span class="sxs-lookup"><span data-stu-id="e13d9-136">Sets the address type.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="e13d9-137">**Inserisci \_ NetworkType**</span><span class="sxs-lookup"><span data-stu-id="e13d9-137">**put\_NetworkType**</span></span>](itconnection-put-networktype.md)             | <span data-ttu-id="e13d9-138">Imposta il tipo di rete.</span><span class="sxs-lookup"><span data-stu-id="e13d9-138">Sets the network type.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="e13d9-139">**SetAddressInfo**</span><span class="sxs-lookup"><span data-stu-id="e13d9-139">**SetAddressInfo**</span></span>](itconnection-setaddressinfo.md)                | <span data-ttu-id="e13d9-140">Imposta le informazioni sull'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="e13d9-140">Sets address information.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="e13d9-141">**SetBandwidthInfo**</span><span class="sxs-lookup"><span data-stu-id="e13d9-141">**SetBandwidthInfo**</span></span>](itconnection-setbandwidthinfo.md)            | <span data-ttu-id="e13d9-142">Imposta il valore della larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="e13d9-142">Sets the bandwidth value.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="e13d9-143">**SetEncryptionKey**</span><span class="sxs-lookup"><span data-stu-id="e13d9-143">**SetEncryptionKey**</span></span>](itconnection-setencryptionkey.md)            | <span data-ttu-id="e13d9-144">Imposta la chiave di crittografia necessaria per decrittografare la sessione o un'indicazione in un meccanismo per ottenere una chiave utilizzabile per mezzo esterno.</span><span class="sxs-lookup"><span data-stu-id="e13d9-144">Sets the encryption key needed to decrypt the session or an indication to a mechanism to obtain a usable key by external means.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="e13d9-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e13d9-145">Requirements</span></span>



| <span data-ttu-id="e13d9-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="e13d9-146">Requirement</span></span> | <span data-ttu-id="e13d9-147">Valore</span><span class="sxs-lookup"><span data-stu-id="e13d9-147">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e13d9-148">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="e13d9-148">TAPI version</span></span><br/> | <span data-ttu-id="e13d9-149">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="e13d9-149">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="e13d9-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e13d9-150">Header</span></span><br/>       | <dl> <span data-ttu-id="e13d9-151"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="e13d9-151"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="e13d9-152">Libreria</span><span class="sxs-lookup"><span data-stu-id="e13d9-152">Library</span></span><br/>      | <dl> <span data-ttu-id="e13d9-153"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e13d9-153"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="e13d9-154">DLL</span><span class="sxs-lookup"><span data-stu-id="e13d9-154">DLL</span></span><br/>          | <dl> <span data-ttu-id="e13d9-155"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e13d9-155"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

