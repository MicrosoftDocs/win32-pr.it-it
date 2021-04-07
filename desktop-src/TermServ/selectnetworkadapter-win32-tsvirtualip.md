---
title: Metodo SelectNetworkAdapter della classe Win32_TSVirtualIP
description: Imposta l'indirizzo MAC della scheda di rete da utilizzare per la virtualizzazione IP.
ms.assetid: ad67445c-6a8b-4980-997a-56aceb70965f
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SelectNetworkAdapter
- Metodo SelectNetworkAdapter Servizi Desktop remoto, classe Win32_TSVirtualIP
- Classe Win32_TSVirtualIP Servizi Desktop remoto, metodo SelectNetworkAdapter
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SelectNetworkAdapter
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3a362bea1a5cacbfd727f23504f19164c79ce65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964138"
---
# <a name="selectnetworkadapter-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="57cdb-106">Metodo SelectNetworkAdapter della \_ classe TSVirtualIP Win32</span><span class="sxs-lookup"><span data-stu-id="57cdb-106">SelectNetworkAdapter method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="57cdb-107">Imposta l'indirizzo MAC della scheda di rete da utilizzare per la virtualizzazione IP.</span><span class="sxs-lookup"><span data-stu-id="57cdb-107">Sets the MAC address of the network adapter to use for IP virtualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="57cdb-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="57cdb-108">Syntax</span></span>


```mof
uint32 SelectNetworkAdapter(
  [in] string NetworkAdapterMacAddress
);
```



## <a name="parameters"></a><span data-ttu-id="57cdb-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="57cdb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57cdb-110">*NetworkAdapterMacAddress* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57cdb-110">*NetworkAdapterMacAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57cdb-111">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="57cdb-111">Type: **string**</span></span>

<span data-ttu-id="57cdb-112">Specifica l'indirizzo MAC della scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="57cdb-112">Specifies the MAC address of the network adapter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57cdb-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="57cdb-113">Return value</span></span>

<span data-ttu-id="57cdb-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="57cdb-114">Type: **uint32**</span></span>

<span data-ttu-id="57cdb-115">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="57cdb-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="57cdb-116">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="57cdb-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

<span data-ttu-id="57cdb-117">Se l'indirizzo MAC non è valido o non esiste o se la modalità di virtualizzazione IP è per sessione, viene restituito un errore.</span><span class="sxs-lookup"><span data-stu-id="57cdb-117">If the MAC address is invalid or does not exist, or if the IP virtualization mode is per-session, an error is returned.</span></span>

<span data-ttu-id="57cdb-118">Il metodo restituisce un errore se l'impostazione è sotto il controllo criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="57cdb-118">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="57cdb-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="57cdb-119">Requirements</span></span>



| <span data-ttu-id="57cdb-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="57cdb-120">Requirement</span></span> | <span data-ttu-id="57cdb-121">Valore</span><span class="sxs-lookup"><span data-stu-id="57cdb-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="57cdb-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57cdb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="57cdb-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="57cdb-123">None supported</span></span><br/>                                                               |
| <span data-ttu-id="57cdb-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57cdb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="57cdb-125">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="57cdb-125">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="57cdb-126">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="57cdb-126">Namespace</span></span><br/>                | <span data-ttu-id="57cdb-127">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="57cdb-127">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="57cdb-128">MOF</span><span class="sxs-lookup"><span data-stu-id="57cdb-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="57cdb-129"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="57cdb-129"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="57cdb-130">DLL</span><span class="sxs-lookup"><span data-stu-id="57cdb-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57cdb-131"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57cdb-131"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57cdb-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="57cdb-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57cdb-133">**\_TSVirtualIP Win32**</span><span class="sxs-lookup"><span data-stu-id="57cdb-133">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





