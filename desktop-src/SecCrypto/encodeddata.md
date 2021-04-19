---
description: Rappresenta un blocco di dati con codifica ASN. 1.
ms.assetid: af7acc5f-da0a-4235-8496-05db94664ea5
title: Oggetto EncodedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d05fce31ad4ef08bf9f573c0158a683bdbeba739
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333250"
---
# <a name="encodeddata-object"></a><span data-ttu-id="48bae-103">Oggetto EncodedData</span><span class="sxs-lookup"><span data-stu-id="48bae-103">EncodedData object</span></span>

<span data-ttu-id="48bae-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="48bae-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="48bae-105">Usare invece la [**classe AsnEncodedData**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="48bae-105">Instead, use the [**AsnEncodedData Class**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="48bae-106">L'oggetto **EncodedData** rappresenta un blocco di dati con codifica ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="48bae-106">The **EncodedData** object represents a block of ASN.1 encoded data.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="48bae-107">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="48bae-107">When to use</span></span>

<span data-ttu-id="48bae-108">L'oggetto **EncodedData** viene restituito da diverse proprietà dell'oggetto CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="48bae-108">The **EncodedData** object is returned by several CAPICOM object properties.</span></span> <span data-ttu-id="48bae-109">Quando viene restituito, questo oggetto viene usato per eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="48bae-109">When returned, this object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="48bae-110">Ottenere una rappresentazione di stringa dei dati codificati.</span><span class="sxs-lookup"><span data-stu-id="48bae-110">Obtain a string representation of the encoded data.</span></span>
-   <span data-ttu-id="48bae-111">Ottenere l'oggetto decodificatore, se esistente, associato ai dati codificati.</span><span class="sxs-lookup"><span data-stu-id="48bae-111">Obtain the decoder object, if it exists, that is associated with the encoded data.</span></span>
-   <span data-ttu-id="48bae-112">Determinare il tipo di dati codificati.</span><span class="sxs-lookup"><span data-stu-id="48bae-112">Determine the type of encoded data.</span></span>

## <a name="members"></a><span data-ttu-id="48bae-113">Membri</span><span class="sxs-lookup"><span data-stu-id="48bae-113">Members</span></span>

<span data-ttu-id="48bae-114">L'oggetto **EncodedData** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="48bae-114">The **EncodedData** object has these types of members:</span></span>

-   [<span data-ttu-id="48bae-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="48bae-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="48bae-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="48bae-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="48bae-117">Metodi</span><span class="sxs-lookup"><span data-stu-id="48bae-117">Methods</span></span>

<span data-ttu-id="48bae-118">L'oggetto **EncodedData** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="48bae-118">The **EncodedData** object has these methods.</span></span>



| <span data-ttu-id="48bae-119">Metodo</span><span class="sxs-lookup"><span data-stu-id="48bae-119">Method</span></span>                                 | <span data-ttu-id="48bae-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48bae-120">Description</span></span>                                                     |
|:---------------------------------------|:----------------------------------------------------------------|
| [<span data-ttu-id="48bae-121">**Decodificatore**</span><span class="sxs-lookup"><span data-stu-id="48bae-121">**Decoder**</span></span>](encodeddata-decoder.md) | <span data-ttu-id="48bae-122">Ottiene un oggetto decodificatore, se ne esiste uno.</span><span class="sxs-lookup"><span data-stu-id="48bae-122">Obtains a decoder object, if one exists.</span></span><br/>             |
| [<span data-ttu-id="48bae-123">**Formato**</span><span class="sxs-lookup"><span data-stu-id="48bae-123">**Format**</span></span>](encodeddata-format.md)   | <span data-ttu-id="48bae-124">Restituisce una rappresentazione di stringa dei dati codificati.</span><span class="sxs-lookup"><span data-stu-id="48bae-124">Returns a string representation of the encoded data.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="48bae-125">Proprietà</span><span class="sxs-lookup"><span data-stu-id="48bae-125">Properties</span></span>

<span data-ttu-id="48bae-126">L'oggetto **EncodedData** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="48bae-126">The **EncodedData** object has these properties.</span></span>



| <span data-ttu-id="48bae-127">Proprietà</span><span class="sxs-lookup"><span data-stu-id="48bae-127">Property</span></span>                                      | <span data-ttu-id="48bae-128">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="48bae-128">Access type</span></span>          | <span data-ttu-id="48bae-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48bae-129">Description</span></span>                                                          |
|:----------------------------------------------|:---------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="48bae-130">**Valore**</span><span class="sxs-lookup"><span data-stu-id="48bae-130">**Value**</span></span>](encodeddata-value.md)<br/> | <span data-ttu-id="48bae-131">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="48bae-131">Read-only</span></span><br/> | <span data-ttu-id="48bae-132">Recupera i dati codificati.</span><span class="sxs-lookup"><span data-stu-id="48bae-132">Retrieves the encoded data.</span></span> <span data-ttu-id="48bae-133">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="48bae-133">This is the default property.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="48bae-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="48bae-134">Remarks</span></span>

<span data-ttu-id="48bae-135">L'unico tipo supportato di dati codificati è [**CertificatePolicies**](certificatepolicies.md).</span><span class="sxs-lookup"><span data-stu-id="48bae-135">The only supported type of encoded data is [**CertificatePolicies**](certificatepolicies.md).</span></span>

<span data-ttu-id="48bae-136">Impossibile creare l'oggetto **EncodedData** .</span><span class="sxs-lookup"><span data-stu-id="48bae-136">The **EncodedData** object cannot be created.</span></span>

<span data-ttu-id="48bae-137">Le proprietà dell'oggetto CAPICOM seguenti restituiscono un oggetto **EncodedData** :</span><span class="sxs-lookup"><span data-stu-id="48bae-137">The following CAPICOM object properties return an **EncodedData** object:</span></span>

-   <span data-ttu-id="48bae-138">**PublicKey. EncodedKey**</span><span class="sxs-lookup"><span data-stu-id="48bae-138">**PublicKey.EncodedKey**</span></span>
-   <span data-ttu-id="48bae-139">**PublicKey. EncodedParameters**</span><span class="sxs-lookup"><span data-stu-id="48bae-139">**PublicKey.EncodedParameters**</span></span>
-   <span data-ttu-id="48bae-140">**Estensione. EncodedData**</span><span class="sxs-lookup"><span data-stu-id="48bae-140">**Extension.EncodedData**</span></span>
-   <span data-ttu-id="48bae-141">**Policy. EncodedData**</span><span class="sxs-lookup"><span data-stu-id="48bae-141">**Policy.EncodedData**</span></span>

## <a name="requirements"></a><span data-ttu-id="48bae-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="48bae-142">Requirements</span></span>



| <span data-ttu-id="48bae-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="48bae-143">Requirement</span></span> | <span data-ttu-id="48bae-144">Valore</span><span class="sxs-lookup"><span data-stu-id="48bae-144">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="48bae-145">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="48bae-145">End of client support</span></span><br/> | <span data-ttu-id="48bae-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="48bae-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="48bae-147">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="48bae-147">End of server support</span></span><br/> | <span data-ttu-id="48bae-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="48bae-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="48bae-149">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="48bae-149">Redistributable</span></span><br/>       | <span data-ttu-id="48bae-150">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="48bae-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="48bae-151">DLL</span><span class="sxs-lookup"><span data-stu-id="48bae-151">DLL</span></span><br/>                   | <dl> <span data-ttu-id="48bae-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48bae-152"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
