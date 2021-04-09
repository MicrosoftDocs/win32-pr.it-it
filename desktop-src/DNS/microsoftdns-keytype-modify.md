---
title: Metodo Modify della classe MicrosoftDNS_KEYType
description: Il metodo modify aggiorna un record di risorse chiave.
ms.assetid: 0ea1e0e5-ccd1-4800-b0c3-27795c36250c
keywords:
- Modificare il metodo DNS
- Modificare il metodo DNS, MicrosoftDNS_KEYType classe
- Classe MicrosoftDNS_KEYType DNS, metodo modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_KEYType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44ee9182925f3f1d53fb90a4beefeb421f01c24f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121402"
---
# <a name="modify-method-of-the-microsoftdns_keytype-class"></a><span data-ttu-id="8a7dd-106">Metodo Modify della classe di \_ tipo MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="8a7dd-106">Modify method of the MicrosoftDNS\_KEYType class</span></span>

<span data-ttu-id="8a7dd-107">Il metodo **Modify** aggiorna un record di risorse chiave.</span><span class="sxs-lookup"><span data-stu-id="8a7dd-107">The **Modify** method updates a KEY Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a7dd-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8a7dd-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint16               Flags,
  [in, optional] uint16               Protocol,
  [in, optional] uint16               Algorithm,
  [in, optional] string               PublicKey,
  [out, ref]     MicrosoftDNS_KEYType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="8a7dd-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8a7dd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a7dd-110">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="8a7dd-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8a7dd-111">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="8a7dd-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="8a7dd-112">*Flag* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="8a7dd-112">*Flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8a7dd-113">Flag utilizzati per specificare il mapping, come descritto in IETF RFC 2535.</span><span class="sxs-lookup"><span data-stu-id="8a7dd-113">Flags used to specify mapping, as described in IETF RFC 2535.</span></span>

</dd> <dt>

<span data-ttu-id="8a7dd-114">*Protocollo* \[ di in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="8a7dd-114">*Protocol* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8a7dd-115">Protocollo per il quale è possibile utilizzare la chiave specificata nell'RR.</span><span class="sxs-lookup"><span data-stu-id="8a7dd-115">Protocol for which the key specified in the RR can be used.</span></span> <span data-ttu-id="8a7dd-116">I valori assegnati sono riportati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="8a7dd-116">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="8a7dd-117">Valore</span><span class="sxs-lookup"><span data-stu-id="8a7dd-117">Value</span></span>                                                                                                    | <span data-ttu-id="8a7dd-118">Significato</span><span class="sxs-lookup"><span data-stu-id="8a7dd-118">Meaning</span></span>                  |
|----------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="8a7dd-119"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="8a7dd-119"><dt>**1**</dt></span></span> </dl>     | <span data-ttu-id="8a7dd-120">TLS</span><span class="sxs-lookup"><span data-stu-id="8a7dd-120">TLS</span></span><br/>           |
| <span id="2"></span><dl> <span data-ttu-id="8a7dd-121"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="8a7dd-121"><dt>**2**</dt></span></span> </dl>     | <span data-ttu-id="8a7dd-122">Posta elettronica</span><span class="sxs-lookup"><span data-stu-id="8a7dd-122">E-Mail</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="8a7dd-123"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="8a7dd-123"><dt>**3**</dt></span></span> </dl>     | <span data-ttu-id="8a7dd-124">DNSSEC</span><span class="sxs-lookup"><span data-stu-id="8a7dd-124">dnssec</span></span><br/>        |
| <span id="4"></span><dl> <span data-ttu-id="8a7dd-125"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="8a7dd-125"><dt>**4**</dt></span></span> </dl>     | <span data-ttu-id="8a7dd-126">IPsec</span><span class="sxs-lookup"><span data-stu-id="8a7dd-126">IPsec</span></span><br/>         |
| <span id="255"></span><dl> <span data-ttu-id="8a7dd-127"><dt>**255**</dt></span><span class="sxs-lookup"><span data-stu-id="8a7dd-127"><dt>**255**</dt></span></span> </dl> | <span data-ttu-id="8a7dd-128">Tutti i protocolli</span><span class="sxs-lookup"><span data-stu-id="8a7dd-128">All protocols</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8a7dd-129">*Algoritmo* \[ di in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="8a7dd-129">*Algorithm* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8a7dd-130">Algoritmo utilizzato con la chiave specificata nel record di risorse.</span><span class="sxs-lookup"><span data-stu-id="8a7dd-130">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="8a7dd-131">I valori assegnati sono riportati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="8a7dd-131">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="8a7dd-132">Valore</span><span class="sxs-lookup"><span data-stu-id="8a7dd-132">Value</span></span>                                                                                                | <span data-ttu-id="8a7dd-133">Significato</span><span class="sxs-lookup"><span data-stu-id="8a7dd-133">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="8a7dd-134"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="8a7dd-134"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="8a7dd-135">RSA/MD5 (RFC 2537)</span><span class="sxs-lookup"><span data-stu-id="8a7dd-135">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="8a7dd-136"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="8a7dd-136"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="8a7dd-137">Diffie-Hellman (RFC 2539)</span><span class="sxs-lookup"><span data-stu-id="8a7dd-137">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="8a7dd-138"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="8a7dd-138"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="8a7dd-139">DSA (RFC 2536)</span><span class="sxs-lookup"><span data-stu-id="8a7dd-139">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="8a7dd-140"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="8a7dd-140"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="8a7dd-141">Crittografia a curva ellittica</span><span class="sxs-lookup"><span data-stu-id="8a7dd-141">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8a7dd-142">*PublicKey* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="8a7dd-142">*PublicKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8a7dd-143">Chiave pubblica, rappresentata in base 64 come descritto nell'Appendice A di RFC 2535.</span><span class="sxs-lookup"><span data-stu-id="8a7dd-143">Public key, represented in base 64 as described in Appendix A of RFC 2535.</span></span>

</dd> <dt>

<span data-ttu-id="8a7dd-144">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="8a7dd-144">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="8a7dd-145">Riferimento al nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="8a7dd-145">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a7dd-146">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8a7dd-146">Return value</span></span>

<span data-ttu-id="8a7dd-147">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="8a7dd-147">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a7dd-148">Commenti</span><span class="sxs-lookup"><span data-stu-id="8a7dd-148">Remarks</span></span>

<span data-ttu-id="8a7dd-149">Tutti i parametri non specificati rimangono invariati nel record modificato.</span><span class="sxs-lookup"><span data-stu-id="8a7dd-149">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a7dd-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8a7dd-150">Requirements</span></span>



| <span data-ttu-id="8a7dd-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a7dd-151">Requirement</span></span> | <span data-ttu-id="8a7dd-152">Valore</span><span class="sxs-lookup"><span data-stu-id="8a7dd-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a7dd-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8a7dd-153">Minimum supported client</span></span><br/> | <span data-ttu-id="8a7dd-154">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8a7dd-154">None supported</span></span><br/>                                                              |
| <span data-ttu-id="8a7dd-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8a7dd-155">Minimum supported server</span></span><br/> | <span data-ttu-id="8a7dd-156">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8a7dd-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8a7dd-157">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8a7dd-157">Namespace</span></span><br/>                | <span data-ttu-id="8a7dd-158">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="8a7dd-158">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="8a7dd-159">MOF</span><span class="sxs-lookup"><span data-stu-id="8a7dd-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8a7dd-160"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8a7dd-160"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a7dd-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8a7dd-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a7dd-162">**Tipo di MicrosoftDNS \_**</span><span class="sxs-lookup"><span data-stu-id="8a7dd-162">**MicrosoftDNS\_KEYType**</span></span>](microsoftdns-keytype.md)
</dt> <dt>

[<span data-ttu-id="8a7dd-163">**Metodo CreateInstanceFromPropertyData della classe di \_ tipo MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="8a7dd-163">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_KEYType Class**</span></span>](microsoftdns-keytype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="8a7dd-164">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="8a7dd-164">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





