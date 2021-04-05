---
title: Metodo Modify della classe MicrosoftDNS_ATMAType
description: Il metodo modify aggiorna un indirizzo ATM al record di risorse Name (ATMA).
ms.assetid: 202fc38d-fb8f-4044-bb7d-9e041cbde8ec
keywords:
- Modificare il metodo DNS
- Modificare il metodo DNS, MicrosoftDNS_ATMAType classe
- Classe MicrosoftDNS_ATMAType DNS, metodo modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_ATMAType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48d784e9421641dc53d64bb39a2e97b0d9ef257b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048376"
---
# <a name="modify-method-of-the-microsoftdns_atmatype-class"></a><span data-ttu-id="8d0d5-106">Metodo Modify della \_ classe ATMAType di MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="8d0d5-106">Modify method of the MicrosoftDNS\_ATMAType class</span></span>

<span data-ttu-id="8d0d5-107">Il metodo **Modify** aggiorna un indirizzo ATM al record di risorse Name (ATMA).</span><span class="sxs-lookup"><span data-stu-id="8d0d5-107">The **Modify** method updates an ATM Address to Name (ATMA) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d0d5-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8d0d5-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] uint16                Format,
  [in, optional] string                ATMAddress,
  [out, ref]     MicrosoftDNS_ATMAType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="8d0d5-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8d0d5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d0d5-110">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="8d0d5-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8d0d5-111">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="8d0d5-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="8d0d5-112">*Formato* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="8d0d5-112">*Format* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8d0d5-113">Formato dell'indirizzo ATM.</span><span class="sxs-lookup"><span data-stu-id="8d0d5-113">ATM address format.</span></span> <span data-ttu-id="8d0d5-114">Due valori possibili per FORMAT sono: 0 che indica il formato AESA (ATM End System Address) e 1 indica il formato E. 164.</span><span class="sxs-lookup"><span data-stu-id="8d0d5-114">Two possible values for FORMAT are: 0 indicating ATM End System Address (AESA) format and 1 indicating E.164 format.</span></span>

</dd> <dt>

<span data-ttu-id="8d0d5-115">*ATMAddress* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="8d0d5-115">*ATMAddress* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8d0d5-116">Stringa di lunghezza variabile di ottetti che contiene l'indirizzo ATM del nodo/proprietario a cui si riferisce questo RR.</span><span class="sxs-lookup"><span data-stu-id="8d0d5-116">Variable length string of octets containing the ATM address of the node/owner to which this RR pertains.</span></span> <span data-ttu-id="8d0d5-117">I primi quattro byte della matrice vengono usati per archiviare le dimensioni della stringa di ottetto.</span><span class="sxs-lookup"><span data-stu-id="8d0d5-117">The first four bytes of the array are used to store the size of the octet string.</span></span> <span data-ttu-id="8d0d5-118">Il byte più significativo viene archiviato nel byte 0.</span><span class="sxs-lookup"><span data-stu-id="8d0d5-118">The most significant byte is stored in byte 0.</span></span>

</dd> <dt>

<span data-ttu-id="8d0d5-119">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="8d0d5-119">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="8d0d5-120">Riferimento al nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="8d0d5-120">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d0d5-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8d0d5-121">Return value</span></span>

<span data-ttu-id="8d0d5-122">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="8d0d5-122">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d0d5-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="8d0d5-123">Remarks</span></span>

<span data-ttu-id="8d0d5-124">Tutti i parametri non specificati rimangono invariati nel record modificato.</span><span class="sxs-lookup"><span data-stu-id="8d0d5-124">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d0d5-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8d0d5-125">Requirements</span></span>



| <span data-ttu-id="8d0d5-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d0d5-126">Requirement</span></span> | <span data-ttu-id="8d0d5-127">Valore</span><span class="sxs-lookup"><span data-stu-id="8d0d5-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d0d5-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d0d5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8d0d5-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8d0d5-129">None supported</span></span><br/>                                                              |
| <span data-ttu-id="8d0d5-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d0d5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8d0d5-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8d0d5-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8d0d5-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8d0d5-132">Namespace</span></span><br/>                | <span data-ttu-id="8d0d5-133">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="8d0d5-133">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="8d0d5-134">MOF</span><span class="sxs-lookup"><span data-stu-id="8d0d5-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8d0d5-135"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8d0d5-135"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d0d5-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8d0d5-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d0d5-137">**\_ATMAType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="8d0d5-137">**MicrosoftDNS\_ATMAType**</span></span>](microsoftdns-atmatype.md)
</dt> <dt>

[<span data-ttu-id="8d0d5-138">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ ATMAType**</span><span class="sxs-lookup"><span data-stu-id="8d0d5-138">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_ATMAType Class**</span></span>](microsoftdns-atmatype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="8d0d5-139">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="8d0d5-139">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





