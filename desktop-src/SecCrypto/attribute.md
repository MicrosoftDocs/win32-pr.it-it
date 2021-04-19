---
description: Rappresenta un singolo attributo autenticato.
ms.assetid: 71c4543b-683f-4ffa-8301-c40c46c490b3
title: Attribute - oggetto
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 34c0800874dc9380b8c9034df2867fc3d1fb578d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332745"
---
# <a name="attribute-object"></a><span data-ttu-id="55b1e-103">Attribute - oggetto</span><span class="sxs-lookup"><span data-stu-id="55b1e-103">Attribute object</span></span>

<span data-ttu-id="55b1e-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="55b1e-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="55b1e-105">Usare invece la [**classe CryptographicAttributeObject**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="55b1e-105">Instead, use the [**CryptographicAttributeObject Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="55b1e-106">L'oggetto **attribute** rappresenta un singolo attributo autenticato.</span><span class="sxs-lookup"><span data-stu-id="55b1e-106">The **Attribute** object represents a single authenticated attribute.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="55b1e-107">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="55b1e-107">When to use</span></span>

<span data-ttu-id="55b1e-108">L'oggetto **attributo** viene utilizzato per eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="55b1e-108">The **Attribute** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="55b1e-109">Imposta o Recupera il nome del CAPICOM dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="55b1e-109">Set or retrieve the CAPICOM name of the attribute.</span></span>
-   <span data-ttu-id="55b1e-110">Impostare o recuperare il valore dell'attributo, ad esempio l'ora di firma, il nome del documento firmato o una descrizione del documento firmato.</span><span class="sxs-lookup"><span data-stu-id="55b1e-110">Set or retrieve the value of the attribute, such as signing time, the name of the document signed, or a description of the document signed.</span></span>

## <a name="members"></a><span data-ttu-id="55b1e-111">Membri</span><span class="sxs-lookup"><span data-stu-id="55b1e-111">Members</span></span>

<span data-ttu-id="55b1e-112">L'oggetto **attributo** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="55b1e-112">The **Attribute** object has these types of members:</span></span>

-   [<span data-ttu-id="55b1e-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="55b1e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="55b1e-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="55b1e-114">Properties</span></span>

<span data-ttu-id="55b1e-115">L'oggetto **attributo** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="55b1e-115">The **Attribute** object has these properties.</span></span>



| <span data-ttu-id="55b1e-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="55b1e-116">Property</span></span>                                    | <span data-ttu-id="55b1e-117">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="55b1e-117">Access type</span></span>           | <span data-ttu-id="55b1e-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="55b1e-118">Description</span></span>                                                                                   |
|:--------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="55b1e-119">**Nome**</span><span class="sxs-lookup"><span data-stu-id="55b1e-119">**Name**</span></span>](attribute-name.md)<br/>   | <span data-ttu-id="55b1e-120">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="55b1e-120">Read/write</span></span><br/> | <span data-ttu-id="55b1e-121">Imposta o Recupera il nome del CAPICOM dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="55b1e-121">Sets or retrieves the CAPICOM name of the attribute.</span></span> <span data-ttu-id="55b1e-122">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="55b1e-122">This is the default property.</span></span><br/> |
| [<span data-ttu-id="55b1e-123">**Valore**</span><span class="sxs-lookup"><span data-stu-id="55b1e-123">**Value**</span></span>](attribute-value.md)<br/> | <span data-ttu-id="55b1e-124">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="55b1e-124">Read/write</span></span><br/> | <span data-ttu-id="55b1e-125">Imposta o Recupera il valore dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="55b1e-125">Sets or retrieves the value of the attribute.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="55b1e-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="55b1e-126">Remarks</span></span>

<span data-ttu-id="55b1e-127">L'oggetto **attributo** può essere creato ed è sicuro per lo scripting.</span><span class="sxs-lookup"><span data-stu-id="55b1e-127">The **Attribute** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="55b1e-128">Il ProgID per l'oggetto **attributo** è capicom. Attributo. 1.</span><span class="sxs-lookup"><span data-stu-id="55b1e-128">The ProgID for the **Attribute** object is CAPICOM.Attribute.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="55b1e-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55b1e-129">Requirements</span></span>



| <span data-ttu-id="55b1e-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="55b1e-130">Requirement</span></span> | <span data-ttu-id="55b1e-131">Valore</span><span class="sxs-lookup"><span data-stu-id="55b1e-131">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="55b1e-132">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="55b1e-132">End of client support</span></span><br/> | <span data-ttu-id="55b1e-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="55b1e-133">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="55b1e-134">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="55b1e-134">End of server support</span></span><br/> | <span data-ttu-id="55b1e-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="55b1e-135">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="55b1e-136">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="55b1e-136">Redistributable</span></span><br/>       | <span data-ttu-id="55b1e-137">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="55b1e-137">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="55b1e-138">DLL</span><span class="sxs-lookup"><span data-stu-id="55b1e-138">DLL</span></span><br/>                   | <dl> <span data-ttu-id="55b1e-139"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55b1e-139"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55b1e-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="55b1e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55b1e-141">**Oggetti Cryptography**</span><span class="sxs-lookup"><span data-stu-id="55b1e-141">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
