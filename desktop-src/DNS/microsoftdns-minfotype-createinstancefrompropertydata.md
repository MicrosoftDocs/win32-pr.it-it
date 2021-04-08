---
title: Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS_MINFOType
description: Il metodo CreateInstanceFromPropertyData crea un'istanza di un record di risorse MINFO (mail Information).
ms.assetid: 693b4b19-cbdd-48d5-89e0-a700a60477aa
keywords:
- DNS del metodo CreateInstanceFromPropertyData
- DNS del metodo CreateInstanceFromPropertyData, classe MicrosoftDNS_MINFOType
- Classe MicrosoftDNS_MINFOType DNS, metodo CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_MINFOType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a565b1575dc51a59a09faea6fd271d719518f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047892"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_minfotype-class"></a><span data-ttu-id="46b8f-106">Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ MINFOType</span><span class="sxs-lookup"><span data-stu-id="46b8f-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_MINFOType class</span></span>

<span data-ttu-id="46b8f-107">Il metodo **CreateInstanceFromPropertyData** crea un'istanza di un record di risorse MINFO (mail Information).</span><span class="sxs-lookup"><span data-stu-id="46b8f-107">The **CreateInstanceFromPropertyData** method instantiates a Mail Information (MINFO) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="46b8f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46b8f-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                 DnsServerName,
  [in]           string                 ContainerName,
  [in]           string                 OwnerName,
  [in, optional] uint32                 RecordClass = 1,
  [in, optional] uint32                 TTL,
  [in]           string                 ResponsibleMailbox,
  [in]           string                 ErrorMailbox,
  [out, ref]     MicrosoftDNS_MINFOType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="46b8f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="46b8f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46b8f-110">*DnsServerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46b8f-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46b8f-111">FQDN o indirizzo IP del server DNS che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="46b8f-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="46b8f-112">*ContainerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46b8f-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46b8f-113">Nome del contenitore per la zona, la cache o l'istanza di RootHints che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="46b8f-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="46b8f-114">*Proprietarioname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46b8f-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46b8f-115">Nome del proprietario per l'RR.</span><span class="sxs-lookup"><span data-stu-id="46b8f-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="46b8f-116">*RecordClass* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="46b8f-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="46b8f-117">Classe dell'RR.</span><span class="sxs-lookup"><span data-stu-id="46b8f-117">Class of the RR.</span></span> <span data-ttu-id="46b8f-118">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="46b8f-118">Default value is 1.</span></span> <span data-ttu-id="46b8f-119">I valori seguenti sono validi.</span><span class="sxs-lookup"><span data-stu-id="46b8f-119">The following values are valid.</span></span>



| <span data-ttu-id="46b8f-120">Valore</span><span class="sxs-lookup"><span data-stu-id="46b8f-120">Value</span></span>                                                                                                | <span data-ttu-id="46b8f-121">Significato</span><span class="sxs-lookup"><span data-stu-id="46b8f-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="46b8f-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="46b8f-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="46b8f-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="46b8f-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="46b8f-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="46b8f-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="46b8f-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="46b8f-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="46b8f-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="46b8f-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="46b8f-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="46b8f-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="46b8f-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="46b8f-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="46b8f-129">HS (Esiodo)</span><span class="sxs-lookup"><span data-stu-id="46b8f-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="46b8f-130">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="46b8f-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="46b8f-131">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="46b8f-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="46b8f-132">*ResponsibleMailbox* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46b8f-132">*ResponsibleMailbox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46b8f-133">FQDN che specifica una cassetta postale responsabile della lista di distribuzione o della cassetta postale specificata nel nome del proprietario del record.</span><span class="sxs-lookup"><span data-stu-id="46b8f-133">FQDN specifying a mailbox responsible for the mailing list or mailbox specified in the record's Owner Name.</span></span>

</dd> <dt>

<span data-ttu-id="46b8f-134">*ErrorMailbox* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46b8f-134">*ErrorMailbox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46b8f-135">FQDN che specifica una cassetta postale per ricevere i messaggi di errore correlati alla lista di distribuzione o alla cassetta postale specificata dal nome del proprietario del record MINFO.</span><span class="sxs-lookup"><span data-stu-id="46b8f-135">FQDN specifying a mailbox to receive error messages related to either the mailing list, or to the mailbox specified by the owner name of the MINFO record.</span></span>

</dd> <dt>

<span data-ttu-id="46b8f-136">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="46b8f-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="46b8f-137">Riferimento al nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="46b8f-137">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46b8f-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="46b8f-138">Return value</span></span>

<span data-ttu-id="46b8f-139">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="46b8f-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="46b8f-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46b8f-140">Requirements</span></span>



| <span data-ttu-id="46b8f-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="46b8f-141">Requirement</span></span> | <span data-ttu-id="46b8f-142">Valore</span><span class="sxs-lookup"><span data-stu-id="46b8f-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="46b8f-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46b8f-143">Minimum supported client</span></span><br/> | <span data-ttu-id="46b8f-144">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="46b8f-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="46b8f-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46b8f-145">Minimum supported server</span></span><br/> | <span data-ttu-id="46b8f-146">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="46b8f-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="46b8f-147">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="46b8f-147">Namespace</span></span><br/>                | <span data-ttu-id="46b8f-148">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="46b8f-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="46b8f-149">MOF</span><span class="sxs-lookup"><span data-stu-id="46b8f-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46b8f-150"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="46b8f-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46b8f-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46b8f-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46b8f-152">**\_MINFOType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="46b8f-152">**MicrosoftDNS\_MINFOType**</span></span>](microsoftdns-minfotype.md)
</dt> <dt>

[<span data-ttu-id="46b8f-153">**Metodo Modify della \_ classe MINFOType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="46b8f-153">**Modify Method of the MicrosoftDNS\_MINFOType Class**</span></span>](microsoftdns-minfotype-modify.md)
</dt> <dt>

[<span data-ttu-id="46b8f-154">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="46b8f-154">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





