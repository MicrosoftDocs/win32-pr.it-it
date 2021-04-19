---
description: Rappresenta un identificatore di oggetto (OID) utilizzato da diverse proprietà di CAPICOM.
ms.assetid: d9dc2a9a-920b-41e1-91fb-da1628df577d
title: OID (oggetto)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a524bfd8d2eb2edcf3c97919129dd694414d5ace
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333563"
---
# <a name="oid-object"></a><span data-ttu-id="93551-103">OID (oggetto)</span><span class="sxs-lookup"><span data-stu-id="93551-103">OID object</span></span>

<span data-ttu-id="93551-104">\[L'oggetto **OID** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="93551-104">\[The **OID** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="93551-105">Usare invece la [**classe Oid**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="93551-105">Instead, use the [**Oid Class**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="93551-106">L'oggetto **OID** rappresenta un [*identificatore di oggetto*](../secgloss/o-gly.md) (OID) utilizzato da diverse proprietà di CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="93551-106">The **OID** object represents an [*object identifier*](../secgloss/o-gly.md) (OID) that is used by several CAPICOM properties.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="93551-107">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="93551-107">When to use</span></span>

<span data-ttu-id="93551-108">L'oggetto **OID** viene utilizzato per eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="93551-108">The **OID** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="93551-109">Impostare o recuperare un nome di CAPICOM e un nome visualizzato per l'OID.</span><span class="sxs-lookup"><span data-stu-id="93551-109">Set or retrieve a CAPICOM name and display name for the OID.</span></span>
-   <span data-ttu-id="93551-110">Impostare o recuperare il numero tratteggiato per l'OID.</span><span class="sxs-lookup"><span data-stu-id="93551-110">Set or retrieve the dotted number for the OID.</span></span>

## <a name="members"></a><span data-ttu-id="93551-111">Membri</span><span class="sxs-lookup"><span data-stu-id="93551-111">Members</span></span>

<span data-ttu-id="93551-112">L'oggetto **OID** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="93551-112">The **OID** object has these types of members:</span></span>

-   [<span data-ttu-id="93551-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="93551-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="93551-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="93551-114">Properties</span></span>

<span data-ttu-id="93551-115">L'oggetto **OID** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="93551-115">The **OID** object has these properties.</span></span>



| <span data-ttu-id="93551-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="93551-116">Property</span></span>                                            | <span data-ttu-id="93551-117">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="93551-117">Access type</span></span>           | <span data-ttu-id="93551-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93551-118">Description</span></span>                                                                                      |
|:----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="93551-119">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="93551-119">**FriendlyName**</span></span>](oid-friendlyname.md)<br/> | <span data-ttu-id="93551-120">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="93551-120">Read/write</span></span><br/> | <span data-ttu-id="93551-121">Imposta o Recupera il nome visualizzato per l'OID.</span><span class="sxs-lookup"><span data-stu-id="93551-121">Sets or retrieves the display name for the OID.</span></span><br/>                                       |
| [<span data-ttu-id="93551-122">**Nome**</span><span class="sxs-lookup"><span data-stu-id="93551-122">**Name**</span></span>](oid-name.md)<br/>                 | <span data-ttu-id="93551-123">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="93551-123">Read/write</span></span><br/> | <span data-ttu-id="93551-124">Imposta o Recupera il nome definito da CAPICOM per l'OID.</span><span class="sxs-lookup"><span data-stu-id="93551-124">Sets or retrieves the CAPICOM-defined name for the OID.</span></span> <span data-ttu-id="93551-125">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="93551-125">This is the default property.</span></span><br/> |
| [<span data-ttu-id="93551-126">**Valore**</span><span class="sxs-lookup"><span data-stu-id="93551-126">**Value**</span></span>](oid-value.md)<br/>               | <span data-ttu-id="93551-127">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="93551-127">Read/write</span></span><br/> | <span data-ttu-id="93551-128">Imposta o Recupera il valore del numero tratteggiato dell'OID.</span><span class="sxs-lookup"><span data-stu-id="93551-128">Sets or retrieves the value of the OID dotted number of the OID.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="93551-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="93551-129">Remarks</span></span>

<span data-ttu-id="93551-130">È possibile creare l'oggetto **OID** ed è sicuro per lo scripting.</span><span class="sxs-lookup"><span data-stu-id="93551-130">The **OID** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="93551-131">Il ProgID per l'oggetto **OID** è capicom. OID. 1.</span><span class="sxs-lookup"><span data-stu-id="93551-131">The ProgID for the **OID** object is CAPICOM.OID.1.</span></span>

<span data-ttu-id="93551-132">Le proprietà dell'oggetto CAPICOM seguenti restituiscono un oggetto **OID** :</span><span class="sxs-lookup"><span data-stu-id="93551-132">The following CAPICOM object properties return an **OID** object:</span></span>

-   [<span data-ttu-id="93551-133">**PolicyInformation. OID**</span><span class="sxs-lookup"><span data-stu-id="93551-133">**PolicyInformation.OID**</span></span>](policyinformation-oid.md)
-   [<span data-ttu-id="93551-134">**Qualificatore. OID**</span><span class="sxs-lookup"><span data-stu-id="93551-134">**Qualifier.OID**</span></span>](qualifier-oid.md)
-   [<span data-ttu-id="93551-135">**Estensione OID**</span><span class="sxs-lookup"><span data-stu-id="93551-135">**Extension.OID**</span></span>](extension-oid.md)
-   [<span data-ttu-id="93551-136">**Template. OID**</span><span class="sxs-lookup"><span data-stu-id="93551-136">**Template.OID**</span></span>](template-oid.md)

## <a name="requirements"></a><span data-ttu-id="93551-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="93551-137">Requirements</span></span>



| <span data-ttu-id="93551-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="93551-138">Requirement</span></span> | <span data-ttu-id="93551-139">Valore</span><span class="sxs-lookup"><span data-stu-id="93551-139">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="93551-140">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="93551-140">Redistributable</span></span><br/> | <span data-ttu-id="93551-141">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="93551-141">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="93551-142">DLL</span><span class="sxs-lookup"><span data-stu-id="93551-142">DLL</span></span><br/>             | <dl> <span data-ttu-id="93551-143"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93551-143"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
