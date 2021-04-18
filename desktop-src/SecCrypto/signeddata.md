---
description: Fornisce proprietà e metodi per stabilire il contenuto da firmare con una firma digitale, per firmare o cofirmare i dati in modo digitale e per verificare la firma digitale dei dati firmati. Il messaggio firmato è in \# formato PKCS 7.
ms.assetid: 500437e8-a637-4e89-9ac9-aa3ea20d437f
title: Oggetto SignedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6d0424826f7dc5d041b877ced1cd7f50490d7801
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325144"
---
# <a name="signeddata-object"></a><span data-ttu-id="07dd2-104">Oggetto SignedData</span><span class="sxs-lookup"><span data-stu-id="07dd2-104">SignedData object</span></span>

<span data-ttu-id="07dd2-105">\[L'oggetto **SignedData** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="07dd2-105">\[The **SignedData** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="07dd2-106">Usare invece la [**classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="07dd2-106">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="07dd2-107">L'oggetto **SignedData** fornisce proprietà e metodi per stabilire il contenuto da firmare con una [*firma digitale*](../secgloss/d-gly.md), per firmare o cofirmare i dati in modo digitale e per verificare la firma digitale dei dati firmati.</span><span class="sxs-lookup"><span data-stu-id="07dd2-107">The **SignedData** object provides properties and methods to establish the content to be signed with a [*digital signature*](../secgloss/d-gly.md), to sign or cosign data digitally, and to verify the digital signature of signed data.</span></span> <span data-ttu-id="07dd2-108">Il messaggio firmato è in \# formato PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="07dd2-108">The signed message is in PKCS \#7 format.</span></span>

<span data-ttu-id="07dd2-109">Una firma dati, se verificata, dimostra l'associazione tra un firmatario e i dati e indica che i dati non sono stati modificati in alcun modo dopo la creazione della firma.</span><span class="sxs-lookup"><span data-stu-id="07dd2-109">A data signature, if verified, proves the association between a signer and data and shows that the data was not changed in any way after the signature was created.</span></span>

## <a name="members"></a><span data-ttu-id="07dd2-110">Membri</span><span class="sxs-lookup"><span data-stu-id="07dd2-110">Members</span></span>

<span data-ttu-id="07dd2-111">L'oggetto **SignedData** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="07dd2-111">The **SignedData** object has these types of members:</span></span>

-   [<span data-ttu-id="07dd2-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="07dd2-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="07dd2-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="07dd2-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="07dd2-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="07dd2-114">Methods</span></span>

<span data-ttu-id="07dd2-115">L'oggetto **SignedData** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="07dd2-115">The **SignedData** object has these methods.</span></span>



| <span data-ttu-id="07dd2-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="07dd2-116">Method</span></span>                              | <span data-ttu-id="07dd2-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07dd2-117">Description</span></span>                                                         |
|:------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="07dd2-118">**CoSign**</span><span class="sxs-lookup"><span data-stu-id="07dd2-118">**CoSign**</span></span>](signeddata-cosign.md) | <span data-ttu-id="07dd2-119">Firma un messaggio già firmato.</span><span class="sxs-lookup"><span data-stu-id="07dd2-119">Cosigns an already signed message.</span></span><br/>                       |
| [<span data-ttu-id="07dd2-120">**Sign**</span><span class="sxs-lookup"><span data-stu-id="07dd2-120">**Sign**</span></span>](signeddata-sign.md)     | <span data-ttu-id="07dd2-121">Crea una firma digitale sul contenuto da firmare.</span><span class="sxs-lookup"><span data-stu-id="07dd2-121">Creates a digital signature on the content to be signed.</span></span><br/> |
| [<span data-ttu-id="07dd2-122">**Verificare**</span><span class="sxs-lookup"><span data-stu-id="07dd2-122">**Verify**</span></span>](signeddata-verify.md) | <span data-ttu-id="07dd2-123">Determina la validità di una firma o di firme.</span><span class="sxs-lookup"><span data-stu-id="07dd2-123">Determines the validity of a signature or signatures.</span></span><br/>    |



 

### <a name="properties"></a><span data-ttu-id="07dd2-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="07dd2-124">Properties</span></span>

<span data-ttu-id="07dd2-125">L'oggetto **SignedData** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="07dd2-125">The **SignedData** object has these properties.</span></span>



| <span data-ttu-id="07dd2-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="07dd2-126">Property</span></span>                                                   | <span data-ttu-id="07dd2-127">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="07dd2-127">Access type</span></span>           | <span data-ttu-id="07dd2-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07dd2-128">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="07dd2-129">**Certificati**</span><span class="sxs-lookup"><span data-stu-id="07dd2-129">**Certificates**</span></span>](signeddata-certificates.md)<br/> | <span data-ttu-id="07dd2-130">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="07dd2-130">Read-only</span></span><br/>  | <span data-ttu-id="07dd2-131">Recupera la raccolta di [**certificati**](certificates.md) dei dati firmati.</span><span class="sxs-lookup"><span data-stu-id="07dd2-131">Retrieves the [**Certificates**](certificates.md) collection of the signed data.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="07dd2-132">**Contenuto**</span><span class="sxs-lookup"><span data-stu-id="07dd2-132">**Content**</span></span>](signeddata-content.md)<br/>           | <span data-ttu-id="07dd2-133">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="07dd2-133">Read/write</span></span><br/> | <span data-ttu-id="07dd2-134">Dati da firmare.</span><span class="sxs-lookup"><span data-stu-id="07dd2-134">Data to be signed.</span></span> <span data-ttu-id="07dd2-135">Questa proprietà deve essere inizializzata prima che venga chiamato il metodo [**Sign**](signeddata-sign.md) .</span><span class="sxs-lookup"><span data-stu-id="07dd2-135">This property must be initialized before the [**Sign**](signeddata-sign.md) method is called.</span></span><br/> <span data-ttu-id="07dd2-136">Quando il valore di questa proprietà viene reimpostato, direttamente o indirettamente, viene reimpostato l'intero [*stato*](../secgloss/s-gly.md) dell'oggetto e tutte le firme associate all'oggetto prima della modifica della proprietà vengono perse.</span><span class="sxs-lookup"><span data-stu-id="07dd2-136">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset, and any signature that was associated with the object before the property was changed is lost.</span></span><br/> <span data-ttu-id="07dd2-137">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="07dd2-137">This is the default property.</span></span><br/> |
| [<span data-ttu-id="07dd2-138">**Firmatari**</span><span class="sxs-lookup"><span data-stu-id="07dd2-138">**Signers**</span></span>](signeddata-signers.md)<br/>           | <span data-ttu-id="07dd2-139">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="07dd2-139">Read-only</span></span><br/>  | <span data-ttu-id="07dd2-140">Recupera la raccolta di [**firmatari**](signers.md) che rappresenta gli autori della firma dei dati.</span><span class="sxs-lookup"><span data-stu-id="07dd2-140">Retrieves the [**Signers**](signers.md) collection that represents the signature creators of the data.</span></span><br/>                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="07dd2-141">Commenti</span><span class="sxs-lookup"><span data-stu-id="07dd2-141">Remarks</span></span>

<span data-ttu-id="07dd2-142">È possibile creare l'oggetto **SignedData** ed è sicuro per lo scripting.</span><span class="sxs-lookup"><span data-stu-id="07dd2-142">The **SignedData** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="07dd2-143">Il ProgID per l'oggetto **SignedData** è capicom. SignedData. 1.</span><span class="sxs-lookup"><span data-stu-id="07dd2-143">The ProgID for the **SignedData** object is CAPICOM.SignedData.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="07dd2-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07dd2-144">Requirements</span></span>



| <span data-ttu-id="07dd2-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="07dd2-145">Requirement</span></span> | <span data-ttu-id="07dd2-146">Valore</span><span class="sxs-lookup"><span data-stu-id="07dd2-146">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="07dd2-147">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="07dd2-147">Redistributable</span></span><br/> | <span data-ttu-id="07dd2-148">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="07dd2-148">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="07dd2-149">DLL</span><span class="sxs-lookup"><span data-stu-id="07dd2-149">DLL</span></span><br/>             | <dl> <span data-ttu-id="07dd2-150"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07dd2-150"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07dd2-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07dd2-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07dd2-152">**Oggetti Cryptography**</span><span class="sxs-lookup"><span data-stu-id="07dd2-152">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
