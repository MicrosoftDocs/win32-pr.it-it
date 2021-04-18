---
description: Specifica l'algoritmo utilizzato per la firma, l'inviluppo e la crittografia delle operazioni.
ms.assetid: 9a3071a3-e62d-43d3-acd7-0685592c78b4
title: Oggetto Algorithm (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f564efe9df3122951969a45443d58ace60e9db30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324595"
---
# <a name="algorithm-object"></a><span data-ttu-id="5b28c-103">Oggetto Algorithm</span><span class="sxs-lookup"><span data-stu-id="5b28c-103">Algorithm object</span></span>

<span data-ttu-id="5b28c-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5b28c-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="5b28c-105">Usare invece la [**classe AlgorithmIdentifier**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="5b28c-105">Instead, use the [**AlgorithmIdentifier Class**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="5b28c-106">L'oggetto **Algorithm** specifica l'algoritmo utilizzato per la firma, l'inviluppo e la crittografia delle operazioni.</span><span class="sxs-lookup"><span data-stu-id="5b28c-106">The **Algorithm** object specifies the algorithm used for signing, enveloping, and encrypting operations.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="5b28c-107">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="5b28c-107">When to use</span></span>

<span data-ttu-id="5b28c-108">L'oggetto **Algorithm** viene utilizzato per eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="5b28c-108">The **Algorithm** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="5b28c-109">Impostare o recuperare l'algoritmo da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="5b28c-109">Set or retrieve the algorithm to be used.</span></span>
-   <span data-ttu-id="5b28c-110">Imposta o recupera la lunghezza della chiave.</span><span class="sxs-lookup"><span data-stu-id="5b28c-110">Set or retrieve the key length.</span></span>

> [!Note]  
> <span data-ttu-id="5b28c-111">CAPICOM tenta di utilizzare il provider del servizio di crittografia (CSP) predefinito di sistema.</span><span class="sxs-lookup"><span data-stu-id="5b28c-111">CAPICOM attempts to use the system default cryptographic service provider (CSP).</span></span> <span data-ttu-id="5b28c-112">Se il CSP non è in grado di fornire l'algoritmo o la lunghezza della chiave richiesti, CAPICOM Cerca un provider di servizi CSP fornito da Microsoft in grado di gestire l'algoritmo e la lunghezza della chiave richiesti, in questo ordine di disponibilità: Microsoft Enhanced Cryptographic Provider, Microsoft Strong Cryptographic Provider, Microsoft Base Cryptographic Provider.</span><span class="sxs-lookup"><span data-stu-id="5b28c-112">If that CSP cannot provide the requested algorithm or key length, CAPICOM searches for an available Microsoft-provided CSP that can handle the requested algorithm and key length, in this order of availability: Microsoft Enhanced Cryptographic Provider, Microsoft Strong Cryptographic Provider, Microsoft Base Cryptographic Provider.</span></span>

 

## <a name="members"></a><span data-ttu-id="5b28c-113">Membri</span><span class="sxs-lookup"><span data-stu-id="5b28c-113">Members</span></span>

<span data-ttu-id="5b28c-114">L'oggetto **algoritmo** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5b28c-114">The **Algorithm** object has these types of members:</span></span>

-   [<span data-ttu-id="5b28c-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5b28c-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5b28c-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5b28c-116">Properties</span></span>

<span data-ttu-id="5b28c-117">L'oggetto **Algorithm** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5b28c-117">The **Algorithm** object has these properties.</span></span>



| <span data-ttu-id="5b28c-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5b28c-118">Property</span></span>                                            | <span data-ttu-id="5b28c-119">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="5b28c-119">Access type</span></span>           | <span data-ttu-id="5b28c-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5b28c-120">Description</span></span>                                                                                                                       |
|:----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5b28c-121">**KeyLength**</span><span class="sxs-lookup"><span data-stu-id="5b28c-121">**KeyLength**</span></span>](algorithm-keylength.md)<br/> | <span data-ttu-id="5b28c-122">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="5b28c-122">Read/write</span></span><br/> | <span data-ttu-id="5b28c-123">Imposta o recupera la lunghezza della chiave.</span><span class="sxs-lookup"><span data-stu-id="5b28c-123">Sets or retrieves the length of the key.</span></span><br/>                                                                               |
| [<span data-ttu-id="5b28c-124">**Nome**</span><span class="sxs-lookup"><span data-stu-id="5b28c-124">**Name**</span></span>](algorithm-name.md)<br/>           | <span data-ttu-id="5b28c-125">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="5b28c-125">Read/write</span></span><br/> | <span data-ttu-id="5b28c-126">Imposta o recupera l'algoritmo utilizzato per la firma, l'inviluppo e la crittografia delle operazioni.</span><span class="sxs-lookup"><span data-stu-id="5b28c-126">Sets or retrieves the algorithm used for signing, enveloping, and encrypting operations.</span></span> <span data-ttu-id="5b28c-127">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="5b28c-127">This is the default property.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5b28c-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="5b28c-128">Remarks</span></span>

<span data-ttu-id="5b28c-129">Impossibile creare l'oggetto **algoritmo** .</span><span class="sxs-lookup"><span data-stu-id="5b28c-129">The **Algorithm** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b28c-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5b28c-130">Requirements</span></span>



| <span data-ttu-id="5b28c-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b28c-131">Requirement</span></span> | <span data-ttu-id="5b28c-132">Valore</span><span class="sxs-lookup"><span data-stu-id="5b28c-132">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b28c-133">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="5b28c-133">End of client support</span></span><br/> | <span data-ttu-id="5b28c-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5b28c-134">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="5b28c-135">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="5b28c-135">End of server support</span></span><br/> | <span data-ttu-id="5b28c-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5b28c-136">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="5b28c-137">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="5b28c-137">Redistributable</span></span><br/>       | <span data-ttu-id="5b28c-138">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="5b28c-138">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="5b28c-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5b28c-139">Header</span></span><br/>                | <dl> <span data-ttu-id="5b28c-140"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b28c-140"><dt>Capicom.h</dt></span></span> </dl>   |
| <span data-ttu-id="5b28c-141">DLL</span><span class="sxs-lookup"><span data-stu-id="5b28c-141">DLL</span></span><br/>                   | <dl> <span data-ttu-id="5b28c-142"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b28c-142"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b28c-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5b28c-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b28c-144">**Oggetti Cryptography**</span><span class="sxs-lookup"><span data-stu-id="5b28c-144">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
