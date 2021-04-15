---
title: Metodo Modify della classe MicrosoftDNS_SIGType
description: Il metodo modify aggiorna un RR di firma (SIG).
ms.assetid: 6a7017da-d3f1-4aba-a53a-96f578518304
keywords:
- Modificare il metodo DNS
- Modificare il metodo DNS, MicrosoftDNS_SIGType classe
- Classe MicrosoftDNS_SIGType DNS, metodo modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_SIGType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80fbaa25ec3b6a52aae06f99ed02d50430745dca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475544"
---
# <a name="modify-method-of-the-microsoftdns_sigtype-class"></a><span data-ttu-id="ab82c-106">Metodo Modify della \_ classe SIGType di MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="ab82c-106">Modify method of the MicrosoftDNS\_SIGType class</span></span>

<span data-ttu-id="ab82c-107">Il metodo **Modify** aggiorna un RR di firma (SIG).</span><span class="sxs-lookup"><span data-stu-id="ab82c-107">The **Modify** method updates a Signature (SIG) RR.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab82c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ab82c-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in]           uint16               TypeCovered,
  [in]           uint16               Algorithm,
  [in]           uint16               Labels,
  [in]           uint32               OriginalTTL,
  [in]           uint32               SignatureExpiration,
  [in]           uint32               SignatureInception,
  [in]           uint16               KeyTag,
  [in]           string               SignerName,
  [in]           string               Signature,
  [out, ref]     MicrosoftDNS_SIGType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="ab82c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ab82c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab82c-110">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="ab82c-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ab82c-111">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="ab82c-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="ab82c-112">*TypeCovered* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab82c-112">*TypeCovered* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab82c-113">Tipo di RR coperto da questo SIG.</span><span class="sxs-lookup"><span data-stu-id="ab82c-113">Type of RR covered by this SIG.</span></span>

</dd> <dt>

<span data-ttu-id="ab82c-114">*Algoritmo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ab82c-114">*Algorithm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab82c-115">Algoritmo utilizzato con la chiave specificata nel record di risorse.</span><span class="sxs-lookup"><span data-stu-id="ab82c-115">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="ab82c-116">I valori assegnati sono riportati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="ab82c-116">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="ab82c-117">Valore</span><span class="sxs-lookup"><span data-stu-id="ab82c-117">Value</span></span>                                                                                                | <span data-ttu-id="ab82c-118">Significato</span><span class="sxs-lookup"><span data-stu-id="ab82c-118">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="ab82c-119"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="ab82c-119"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="ab82c-120">RSA/MD5 (RFC 2537)</span><span class="sxs-lookup"><span data-stu-id="ab82c-120">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="ab82c-121"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="ab82c-121"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="ab82c-122">Diffie-Hellman (RFC 2539)</span><span class="sxs-lookup"><span data-stu-id="ab82c-122">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="ab82c-123"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="ab82c-123"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="ab82c-124">DSA (RFC 2536)</span><span class="sxs-lookup"><span data-stu-id="ab82c-124">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="ab82c-125"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="ab82c-125"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="ab82c-126">Crittografia a curva ellittica</span><span class="sxs-lookup"><span data-stu-id="ab82c-126">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ab82c-127">*Etichette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab82c-127">*Labels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab82c-128">Conteggio senza segno delle etichette nel nome originale del proprietario del record di firma.</span><span class="sxs-lookup"><span data-stu-id="ab82c-128">Unsigned count of labels in the original SIG RR owner name.</span></span> <span data-ttu-id="ab82c-129">Il conteggio non include l'etichetta NULL per la radice, né i caratteri jolly iniziali.</span><span class="sxs-lookup"><span data-stu-id="ab82c-129">The count does not include the NULL label for the root, nor any initial wildcards.</span></span>

</dd> <dt>

<span data-ttu-id="ab82c-130">*OriginalTTL* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab82c-130">*OriginalTTL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab82c-131">TTL del set di RR firmato dal SIG.</span><span class="sxs-lookup"><span data-stu-id="ab82c-131">TTL of the RR set signed by the SIG.</span></span>

</dd> <dt>

<span data-ttu-id="ab82c-132">*SignatureExpiration* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab82c-132">*SignatureExpiration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab82c-133">Data di scadenza della firma, espressa in secondi dall'inizio del 1 gennaio 1970, ora di Greenwich (GMT), esclusi i secondi intercalari.</span><span class="sxs-lookup"><span data-stu-id="ab82c-133">Signature expiration date, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="ab82c-134">*SignatureInception* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab82c-134">*SignatureInception* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab82c-135">Data e ora in cui la firma diventa valida, espressa in secondi a partire dall'inizio del 1 ° gennaio 1970, ora di Greenwich (GMT), esclusi i secondi intercalari.</span><span class="sxs-lookup"><span data-stu-id="ab82c-135">Date and time at which the Signature becomes valid, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="ab82c-136">*KeyTag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab82c-136">*KeyTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab82c-137">Metodo usato per scegliere una chiave che verifica un SIG.</span><span class="sxs-lookup"><span data-stu-id="ab82c-137">Method used to choose a key that verifies a SIG.</span></span> <span data-ttu-id="ab82c-138">Vedere RFC 2535, Appendice C per il metodo usato per calcolare un KeyTag.</span><span class="sxs-lookup"><span data-stu-id="ab82c-138">See RFC 2535, Appendix C for the method used to calculate a KeyTag.</span></span>

</dd> <dt>

<span data-ttu-id="ab82c-139">*SignerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab82c-139">*SignerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab82c-140">Nome di dominio del firmatario che ha generato il record SIG.</span><span class="sxs-lookup"><span data-stu-id="ab82c-140">Domain name of the signer that generated the SIG RR.</span></span>

</dd> <dt>

<span data-ttu-id="ab82c-141">*Firma* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ab82c-141">*Signature* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab82c-142">Firma, rappresentata in base 64, formattata come definito nella RFC 2535, Appendice A.</span><span class="sxs-lookup"><span data-stu-id="ab82c-142">Signature, represented in base 64, formatted as defined in RFC 2535, Appendix A.</span></span>

</dd> <dt>

<span data-ttu-id="ab82c-143">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="ab82c-143">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="ab82c-144">Riferimento al nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="ab82c-144">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab82c-145">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ab82c-145">Return value</span></span>

<span data-ttu-id="ab82c-146">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="ab82c-146">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab82c-147">Commenti</span><span class="sxs-lookup"><span data-stu-id="ab82c-147">Remarks</span></span>

<span data-ttu-id="ab82c-148">Tutti i parametri non specificati rimangono invariati nel record modificato.</span><span class="sxs-lookup"><span data-stu-id="ab82c-148">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab82c-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab82c-149">Requirements</span></span>



| <span data-ttu-id="ab82c-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab82c-150">Requirement</span></span> | <span data-ttu-id="ab82c-151">Valore</span><span class="sxs-lookup"><span data-stu-id="ab82c-151">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab82c-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab82c-152">Minimum supported client</span></span><br/> | <span data-ttu-id="ab82c-153">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ab82c-153">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ab82c-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab82c-154">Minimum supported server</span></span><br/> | <span data-ttu-id="ab82c-155">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ab82c-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ab82c-156">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ab82c-156">Namespace</span></span><br/>                | <span data-ttu-id="ab82c-157">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="ab82c-157">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="ab82c-158">MOF</span><span class="sxs-lookup"><span data-stu-id="ab82c-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ab82c-159"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ab82c-159"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab82c-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab82c-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab82c-161">**\_SIGType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="ab82c-161">**MicrosoftDNS\_SIGType**</span></span>](microsoftdns-sigtype.md)
</dt> <dt>

[<span data-ttu-id="ab82c-162">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ SIGType**</span><span class="sxs-lookup"><span data-stu-id="ab82c-162">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_SIGType Class**</span></span>](microsoftdns-sigtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="ab82c-163">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="ab82c-163">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





