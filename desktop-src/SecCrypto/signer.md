---
description: Stabilisce il firmatario di un oggetto SignedData o SignedCode.
ms.assetid: fca6489c-56cf-472f-ac0f-73ba531fa212
title: Oggetto firmatario
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 974341eb996f2b5d3701757a5352ef56e2837390
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332008"
---
# <a name="signer-object"></a><span data-ttu-id="6c8c9-103">Oggetto firmatario</span><span class="sxs-lookup"><span data-stu-id="6c8c9-103">Signer object</span></span>

<span data-ttu-id="6c8c9-104">\[L'oggetto **firmatario** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="6c8c9-104">\[The **Signer** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6c8c9-105">Usare invece la [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="6c8c9-105">Instead, use the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="6c8c9-106">L'oggetto **firmatario** stabilisce il firmatario di un oggetto [**SignedData**](signeddata.md) o [**SignedCode**](signedcode.md) .</span><span class="sxs-lookup"><span data-stu-id="6c8c9-106">The **Signer** object establishes the signer of a [**SignedData**](signeddata.md) or [**SignedCode**](signedcode.md) object.</span></span> <span data-ttu-id="6c8c9-107">Il [**certificato**](certificate.md) dell'oggetto **firmatario** deve avere una chiave privata disponibile che può essere usata per firmare i dati.</span><span class="sxs-lookup"><span data-stu-id="6c8c9-107">The [**Certificate**](certificate.md) of the **Signer** object must have an available private key that can be used to sign data.</span></span>

## <a name="members"></a><span data-ttu-id="6c8c9-108">Membri</span><span class="sxs-lookup"><span data-stu-id="6c8c9-108">Members</span></span>

<span data-ttu-id="6c8c9-109">L'oggetto **firmatario** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6c8c9-109">The **Signer** object has these types of members:</span></span>

-   [<span data-ttu-id="6c8c9-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="6c8c9-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="6c8c9-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6c8c9-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6c8c9-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="6c8c9-112">Methods</span></span>

<span data-ttu-id="6c8c9-113">L'oggetto **firmatario** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="6c8c9-113">The **Signer** object has these methods.</span></span>



| <span data-ttu-id="6c8c9-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="6c8c9-114">Method</span></span>                      | <span data-ttu-id="6c8c9-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6c8c9-115">Description</span></span>                                                       |
|:----------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="6c8c9-116">**Caricamento**</span><span class="sxs-lookup"><span data-stu-id="6c8c9-116">**Load**</span></span>](signer-load.md) | <span data-ttu-id="6c8c9-117">Carica un certificato di firma da un file PFX specificato.</span><span class="sxs-lookup"><span data-stu-id="6c8c9-117">Loads a signing certificate from a specified PFX file.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6c8c9-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6c8c9-118">Properties</span></span>

<span data-ttu-id="6c8c9-119">L'oggetto **firmatario** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6c8c9-119">The **Signer** object has these properties.</span></span>



| <span data-ttu-id="6c8c9-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6c8c9-120">Property</span></span>                                                                     | <span data-ttu-id="6c8c9-121">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="6c8c9-121">Access type</span></span>           | <span data-ttu-id="6c8c9-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6c8c9-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6c8c9-123">**AuthenticatedAttributes**</span><span class="sxs-lookup"><span data-stu-id="6c8c9-123">**AuthenticatedAttributes**</span></span>](signer-authenticatedattributes.md)<br/> | <span data-ttu-id="6c8c9-124">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="6c8c9-124">Read-only</span></span><br/>  | <span data-ttu-id="6c8c9-125">Raccolta di attributi autenticati.</span><span class="sxs-lookup"><span data-stu-id="6c8c9-125">The collection of authenticated attributes.</span></span><br/>                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="6c8c9-126">**Certificato**</span><span class="sxs-lookup"><span data-stu-id="6c8c9-126">**Certificate**</span></span>](signer-certificate.md)<br/>                         | <span data-ttu-id="6c8c9-127">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="6c8c9-127">Read/write</span></span><br/> | <span data-ttu-id="6c8c9-128">Oggetto [**certificato**](certificate.md) che rappresenta il certificato di un firmatario dei dati.</span><span class="sxs-lookup"><span data-stu-id="6c8c9-128">The [**Certificate**](certificate.md) object that represents the certificate of a signer of the data.</span></span><br/> <span data-ttu-id="6c8c9-129">Quando il valore di questa proprietà viene reimpostato, direttamente o indirettamente, viene reimpostato l'intero [*stato*](../secgloss/s-gly.md) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6c8c9-129">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset.</span></span><br/> <span data-ttu-id="6c8c9-130">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="6c8c9-130">This is the default property.</span></span><br/> |
| [<span data-ttu-id="6c8c9-131">**Catena**</span><span class="sxs-lookup"><span data-stu-id="6c8c9-131">**Chain**</span></span>](signer-chain.md)<br/>                                     | <span data-ttu-id="6c8c9-132">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="6c8c9-132">Read-only</span></span><br/>  | <span data-ttu-id="6c8c9-133">Catena del firmatario.</span><span class="sxs-lookup"><span data-stu-id="6c8c9-133">The chain of the signer.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="6c8c9-134">**Opzioni**</span><span class="sxs-lookup"><span data-stu-id="6c8c9-134">**Options**</span></span>](signer-options.md)<br/>                                 | <span data-ttu-id="6c8c9-135">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="6c8c9-135">Read/write</span></span><br/> | <span data-ttu-id="6c8c9-136">Imposta o recupera l'opzione del certificato del firmatario.</span><span class="sxs-lookup"><span data-stu-id="6c8c9-136">Sets or retrieves the signer's certificate option.</span></span><br/>                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="6c8c9-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="6c8c9-137">Remarks</span></span>

<span data-ttu-id="6c8c9-138">È possibile creare l'oggetto **firmatario** ed è sicuro per lo scripting.</span><span class="sxs-lookup"><span data-stu-id="6c8c9-138">The **Signer** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="6c8c9-139">Il ProgID per l'oggetto **firmatario** è capicom. Firmatario. 2.</span><span class="sxs-lookup"><span data-stu-id="6c8c9-139">The ProgID for the **Signer** object is CAPICOM.Signer.2.</span></span>

<span data-ttu-id="6c8c9-140">**CAPICOM 1. *x*:** il ProgID per l'oggetto **firmatario** è capicom. Firmatario. 1.</span><span class="sxs-lookup"><span data-stu-id="6c8c9-140">**CAPICOM 1.*x*:** The ProgID for the **Signer** object is CAPICOM.Signer.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c8c9-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6c8c9-141">Requirements</span></span>



| <span data-ttu-id="6c8c9-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c8c9-142">Requirement</span></span> | <span data-ttu-id="6c8c9-143">Valore</span><span class="sxs-lookup"><span data-stu-id="6c8c9-143">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c8c9-144">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="6c8c9-144">Redistributable</span></span><br/> | <span data-ttu-id="6c8c9-145">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="6c8c9-145">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6c8c9-146">DLL</span><span class="sxs-lookup"><span data-stu-id="6c8c9-146">DLL</span></span><br/>             | <dl> <span data-ttu-id="6c8c9-147"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c8c9-147"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c8c9-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6c8c9-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c8c9-149">**Oggetti Cryptography**</span><span class="sxs-lookup"><span data-stu-id="6c8c9-149">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
