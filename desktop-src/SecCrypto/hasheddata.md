---
description: Fornisce la funzionalità per l'hashing di una stringa.
ms.assetid: 893639c2-57b9-48f6-bf60-a21c3368ffeb
title: Oggetto HashedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b6e54d7d2ca52ceafe500615af4063dfc7310b0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325597"
---
# <a name="hasheddata-object"></a><span data-ttu-id="42c78-103">Oggetto HashedData</span><span class="sxs-lookup"><span data-stu-id="42c78-103">HashedData object</span></span>

<span data-ttu-id="42c78-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="42c78-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="42c78-105">Usare invece la [**classe HashAlgorithm**](/previous-versions/windows/) nello spazio dei nomi [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="42c78-105">Instead, use the [**HashAlgorithm Class**](/previous-versions/windows/) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="42c78-106">L'oggetto **HashedData** fornisce la funzionalità per l'hashing di una stringa.</span><span class="sxs-lookup"><span data-stu-id="42c78-106">The **HashedData** object provides functionality for hashing a string.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="42c78-107">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="42c78-107">When to use</span></span>

<span data-ttu-id="42c78-108">L'oggetto **HashedData** viene usato per eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="42c78-108">The **HashedData** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="42c78-109">Specificare la stringa di contenuto che contiene i dati di cui eseguire l'hashing.</span><span class="sxs-lookup"><span data-stu-id="42c78-109">Specify the content string that contains the data to be hashed.</span></span>
-   <span data-ttu-id="42c78-110">Applicare un algoritmo hash specificato alla stringa di contenuto.</span><span class="sxs-lookup"><span data-stu-id="42c78-110">Apply a specified hash algorithm to the content string.</span></span>

## <a name="members"></a><span data-ttu-id="42c78-111">Membri</span><span class="sxs-lookup"><span data-stu-id="42c78-111">Members</span></span>

<span data-ttu-id="42c78-112">L'oggetto **HashedData** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="42c78-112">The **HashedData** object has these types of members:</span></span>

-   [<span data-ttu-id="42c78-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="42c78-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="42c78-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="42c78-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="42c78-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="42c78-115">Methods</span></span>

<span data-ttu-id="42c78-116">L'oggetto **HashedData** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="42c78-116">The **HashedData** object has these methods.</span></span>



| <span data-ttu-id="42c78-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="42c78-117">Method</span></span>                          | <span data-ttu-id="42c78-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42c78-118">Description</span></span>                                        |
|:--------------------------------|:---------------------------------------------------|
| [<span data-ttu-id="42c78-119">**Hash**</span><span class="sxs-lookup"><span data-stu-id="42c78-119">**Hash**</span></span>](hasheddata-hash.md) | <span data-ttu-id="42c78-120">Crea un hash della stringa specificata.</span><span class="sxs-lookup"><span data-stu-id="42c78-120">Creates a hash of the specified string.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="42c78-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="42c78-121">Properties</span></span>

<span data-ttu-id="42c78-122">L'oggetto **HashedData** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="42c78-122">The **HashedData** object has these properties.</span></span>



| <span data-ttu-id="42c78-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="42c78-123">Property</span></span>                                             | <span data-ttu-id="42c78-124">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="42c78-124">Access type</span></span>           | <span data-ttu-id="42c78-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42c78-125">Description</span></span>                                                                                                                                                                          |
|:-----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="42c78-126">**Algoritmo**</span><span class="sxs-lookup"><span data-stu-id="42c78-126">**Algorithm**</span></span>](hasheddata-algorithm.md)<br/> | <span data-ttu-id="42c78-127">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="42c78-127">Read/write</span></span><br/> | <span data-ttu-id="42c78-128">Imposta o Recupera il tipo di algoritmo di hash utilizzato.</span><span class="sxs-lookup"><span data-stu-id="42c78-128">Sets or retrieves the type of hashing algorithm used.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="42c78-129">**Valore**</span><span class="sxs-lookup"><span data-stu-id="42c78-129">**Value**</span></span>](hasheddata-value.md)<br/>         | <span data-ttu-id="42c78-130">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="42c78-130">Read-only</span></span><br/>  | <span data-ttu-id="42c78-131">Recupera i dati con hash dopo le chiamate al metodo [**hash**](hasheddata-hash.md) .</span><span class="sxs-lookup"><span data-stu-id="42c78-131">Retrieves the hashed data after successful calls to the [**Hash**](hasheddata-hash.md) method.</span></span> <span data-ttu-id="42c78-132">L'hash viene restituito in formato esadecimale.</span><span class="sxs-lookup"><span data-stu-id="42c78-132">The hash is returned in hexadecimal format.</span></span> <span data-ttu-id="42c78-133">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="42c78-133">This is the default property.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="42c78-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="42c78-134">Remarks</span></span>

<span data-ttu-id="42c78-135">Per creare l'hash di una grande quantità di dati, chiamare il metodo [**hash**](hasheddata-hash.md) per ogni pezzo di dati.</span><span class="sxs-lookup"><span data-stu-id="42c78-135">To create the hash of a large amount of data, call the [**Hash**](hasheddata-hash.md) method for each piece of data.</span></span> <span data-ttu-id="42c78-136">L'hash di ogni porzione di dati viene concatenato alla proprietà [**value**](hasheddata-value.md) fino a quando non viene letta la proprietà.</span><span class="sxs-lookup"><span data-stu-id="42c78-136">The hash of each piece of data is concatenated to the [**Value**](hasheddata-value.md) property until the property is read.</span></span> <span data-ttu-id="42c78-137">Il contenuto della proprietà **value** viene reimpostato quando viene letta la proprietà.</span><span class="sxs-lookup"><span data-stu-id="42c78-137">The contents of the **Value** property are reset when the property is read.</span></span>

<span data-ttu-id="42c78-138">È possibile creare l'oggetto **HashedData** ed è sicuro per lo scripting.</span><span class="sxs-lookup"><span data-stu-id="42c78-138">The **HashedData** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="42c78-139">Il ProgID per l'oggetto **HashedData** è "CAPICOM. HashedData. 1 ".</span><span class="sxs-lookup"><span data-stu-id="42c78-139">The ProgID for the **HashedData** object is "CAPICOM.HashedData.1".</span></span>

## <a name="requirements"></a><span data-ttu-id="42c78-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42c78-140">Requirements</span></span>



| <span data-ttu-id="42c78-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="42c78-141">Requirement</span></span> | <span data-ttu-id="42c78-142">Valore</span><span class="sxs-lookup"><span data-stu-id="42c78-142">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="42c78-143">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="42c78-143">End of client support</span></span><br/> | <span data-ttu-id="42c78-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="42c78-144">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="42c78-145">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="42c78-145">End of server support</span></span><br/> | <span data-ttu-id="42c78-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42c78-146">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="42c78-147">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="42c78-147">Redistributable</span></span><br/>       | <span data-ttu-id="42c78-148">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="42c78-148">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="42c78-149">DLL</span><span class="sxs-lookup"><span data-stu-id="42c78-149">DLL</span></span><br/>                   | <dl> <span data-ttu-id="42c78-150"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42c78-150"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
