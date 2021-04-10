---
title: Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS_MXType
description: Il metodo CreateInstanceFromPropertyData crea un'istanza di un record di risorse di Mail Exchanger (Sig.).
ms.assetid: 5724b14a-bb64-460c-ac49-28bac85b8620
keywords:
- DNS del metodo CreateInstanceFromPropertyData
- DNS del metodo CreateInstanceFromPropertyData, classe MicrosoftDNS_MXType
- Classe MicrosoftDNS_MXType DNS, metodo CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_MXType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8154e8ccdc6ac18824e2d56597ac8e0f186f3912
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119886"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_mxtype-class"></a><span data-ttu-id="cdff2-106">Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ MXType</span><span class="sxs-lookup"><span data-stu-id="cdff2-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_MXType class</span></span>

<span data-ttu-id="cdff2-107">Il metodo **CreateInstanceFromPropertyData** crea un'istanza di un record di risorse di Mail Exchanger (Sig.).</span><span class="sxs-lookup"><span data-stu-id="cdff2-107">The **CreateInstanceFromPropertyData** method instantiates a Mail Exchanger (MR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdff2-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cdff2-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           uint16              Preference,
  [in]           string              MailExchange,
  [out, ref]     MicrosoftDNS_MXType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="cdff2-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="cdff2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdff2-110">*DnsServerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdff2-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdff2-111">FQDN o indirizzo IP del server DNS che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="cdff2-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="cdff2-112">*ContainerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdff2-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdff2-113">Nome del contenitore per la zona, la cache o l'istanza di RootHints che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="cdff2-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="cdff2-114">*Proprietarioname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdff2-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdff2-115">Nome del proprietario per l'RR.</span><span class="sxs-lookup"><span data-stu-id="cdff2-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="cdff2-116">*RecordClass* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="cdff2-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cdff2-117">Classe dell'RR.</span><span class="sxs-lookup"><span data-stu-id="cdff2-117">Class of the RR.</span></span> <span data-ttu-id="cdff2-118">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="cdff2-118">Default value is 1.</span></span> <span data-ttu-id="cdff2-119">I valori seguenti sono validi.</span><span class="sxs-lookup"><span data-stu-id="cdff2-119">The following values are valid.</span></span>



| <span data-ttu-id="cdff2-120">Valore</span><span class="sxs-lookup"><span data-stu-id="cdff2-120">Value</span></span>                                                                                                | <span data-ttu-id="cdff2-121">Significato</span><span class="sxs-lookup"><span data-stu-id="cdff2-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="cdff2-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="cdff2-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="cdff2-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="cdff2-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="cdff2-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="cdff2-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="cdff2-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="cdff2-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="cdff2-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="cdff2-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="cdff2-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="cdff2-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="cdff2-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="cdff2-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="cdff2-129">HS (Esiodo)</span><span class="sxs-lookup"><span data-stu-id="cdff2-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="cdff2-130">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="cdff2-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cdff2-131">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="cdff2-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="cdff2-132">*Preferenza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdff2-132">*Preference* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdff2-133">Preferenza assegnata a questo RR tra gli altri nello stesso proprietario.</span><span class="sxs-lookup"><span data-stu-id="cdff2-133">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="cdff2-134">Sono preferibili valori inferiori.</span><span class="sxs-lookup"><span data-stu-id="cdff2-134">Lower values are preferred.</span></span>

</dd> <dt>

<span data-ttu-id="cdff2-135">*MailExchange* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdff2-135">*MailExchange* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdff2-136">FQDN che specifica un host disposto a fungere da scambio di posta elettronica per il nome del proprietario.</span><span class="sxs-lookup"><span data-stu-id="cdff2-136">FQDN specifying a host willing to act as a mail exchange for the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="cdff2-137">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="cdff2-137">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="cdff2-138">Riferimento al nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="cdff2-138">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdff2-139">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cdff2-139">Return value</span></span>

<span data-ttu-id="cdff2-140">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="cdff2-140">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdff2-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cdff2-141">Requirements</span></span>



| <span data-ttu-id="cdff2-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdff2-142">Requirement</span></span> | <span data-ttu-id="cdff2-143">Valore</span><span class="sxs-lookup"><span data-stu-id="cdff2-143">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cdff2-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cdff2-144">Minimum supported client</span></span><br/> | <span data-ttu-id="cdff2-145">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="cdff2-145">None supported</span></span><br/>                                                              |
| <span data-ttu-id="cdff2-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cdff2-146">Minimum supported server</span></span><br/> | <span data-ttu-id="cdff2-147">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cdff2-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="cdff2-148">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cdff2-148">Namespace</span></span><br/>                | <span data-ttu-id="cdff2-149">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="cdff2-149">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="cdff2-150">MOF</span><span class="sxs-lookup"><span data-stu-id="cdff2-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cdff2-151"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cdff2-151"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdff2-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cdff2-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdff2-153">**\_MXType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="cdff2-153">**MicrosoftDNS\_MXType**</span></span>](microsoftdns-mxtype.md)
</dt> <dt>

[<span data-ttu-id="cdff2-154">**Metodo Modify della \_ classe MXType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="cdff2-154">**Modify Method of the MicrosoftDNS\_MXType Class**</span></span>](microsoftdns-mxtype-modify.md)
</dt> <dt>

[<span data-ttu-id="cdff2-155">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="cdff2-155">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





