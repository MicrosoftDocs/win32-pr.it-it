---
description: Rappresenta una proprietà estesa a Microsoft.
ms.assetid: 91375fd5-b3af-4ed4-961d-5cc1db1a14e3
title: ExtendedProperty (oggetto)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperty
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2ec61da301dc1819c899a7da23da9a10efd81ae0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329224"
---
# <a name="extendedproperty-object"></a><span data-ttu-id="66768-103">ExtendedProperty (oggetto)</span><span class="sxs-lookup"><span data-stu-id="66768-103">ExtendedProperty object</span></span>

<span data-ttu-id="66768-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="66768-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="66768-105">Usare invece i servizi PInvoke (Platform Invocation Services) per chiamare la funzione API Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) e ottenere le proprietà.</span><span class="sxs-lookup"><span data-stu-id="66768-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="66768-106">Per informazioni su PInvoke, vedere l' [esercitazione Platform Invoke](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="66768-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="66768-107">Può essere utile anche [.NET e CryptoAPI tramite p/invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.NET e CryptoAPI tramite p/invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sottosezioni di [estensione della crittografia .NET con CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="66768-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="66768-108">L'oggetto **ExtendedProperty** rappresenta una proprietà estesa da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="66768-108">The **ExtendedProperty** object represents a Microsoft-extended property.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="66768-109">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="66768-109">When to use</span></span>

<span data-ttu-id="66768-110">L'oggetto **ExtendedProperty** viene utilizzato per eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="66768-110">The **ExtendedProperty** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="66768-111">Imposta o Recupera il tipo della proprietà estesa.</span><span class="sxs-lookup"><span data-stu-id="66768-111">Set or retrieve the type of the extended property.</span></span>
-   <span data-ttu-id="66768-112">Imposta o Recupera il tipo di codifica utilizzato per codificare la proprietà estesa.</span><span class="sxs-lookup"><span data-stu-id="66768-112">Set or retrieve the type of encoding used to encode the extended property.</span></span>

## <a name="members"></a><span data-ttu-id="66768-113">Membri</span><span class="sxs-lookup"><span data-stu-id="66768-113">Members</span></span>

<span data-ttu-id="66768-114">L'oggetto **ExtendedProperty** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="66768-114">The **ExtendedProperty** object has these types of members:</span></span>

-   [<span data-ttu-id="66768-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="66768-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="66768-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="66768-116">Properties</span></span>

<span data-ttu-id="66768-117">L'oggetto **ExtendedProperty** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="66768-117">The **ExtendedProperty** object has these properties.</span></span>



| <span data-ttu-id="66768-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="66768-118">Property</span></span>                                             | <span data-ttu-id="66768-119">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="66768-119">Access type</span></span>           | <span data-ttu-id="66768-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="66768-120">Description</span></span>                                                                                                                                                                    |
|:-----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="66768-121">**PropID**</span><span class="sxs-lookup"><span data-stu-id="66768-121">**PropID**</span></span>](extendedproperty-propid.md)<br/> | <span data-ttu-id="66768-122">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="66768-122">Read/write</span></span><br/> | <span data-ttu-id="66768-123">Valore dell'enumerazione [**\_ propid di CAPICOM**](capicom-propid.md) che imposta o Recupera il tipo di proprietà estesa.</span><span class="sxs-lookup"><span data-stu-id="66768-123">A value of the [**CAPICOM\_PROPID**](capicom-propid.md) enumeration that sets or retrieves the type of extended property.</span></span><br/> <span data-ttu-id="66768-124">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="66768-124">This is the default property.</span></span><br/> |
| [<span data-ttu-id="66768-125">**Valore**</span><span class="sxs-lookup"><span data-stu-id="66768-125">**Value**</span></span>](extendedproperty-value.md)<br/>   | <span data-ttu-id="66768-126">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="66768-126">Read/write</span></span><br/> | <span data-ttu-id="66768-127">Valore dell'enumerazione del [**\_ \_ tipo di codifica CAPICOM**](capicom-encoding-type.md) che imposta o recupera i dati della proprietà estesa.</span><span class="sxs-lookup"><span data-stu-id="66768-127">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that sets or retrieves the extended property data.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="66768-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="66768-128">Remarks</span></span>

<span data-ttu-id="66768-129">L'oggetto **ExtendedProperty** viene usato dalla raccolta [**ExtendedProperties**](extendedproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="66768-129">The **ExtendedProperty** object is used by the [**ExtendedProperties**](extendedproperties.md) collection.</span></span>

<span data-ttu-id="66768-130">È possibile creare l'oggetto **ExtendedProperty** e non è sicuro per lo scripting.</span><span class="sxs-lookup"><span data-stu-id="66768-130">The **ExtendedProperty** object can be created, and it is not safe for scripting.</span></span> <span data-ttu-id="66768-131">Il ProgID per l'oggetto **ExtendedProperty** è capicom. ExtendedProperty. 1.</span><span class="sxs-lookup"><span data-stu-id="66768-131">The ProgID for the **ExtendedProperty** object is CAPICOM.ExtendedProperty.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="66768-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="66768-132">Requirements</span></span>



| <span data-ttu-id="66768-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="66768-133">Requirement</span></span> | <span data-ttu-id="66768-134">Valore</span><span class="sxs-lookup"><span data-stu-id="66768-134">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="66768-135">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="66768-135">End of client support</span></span><br/> | <span data-ttu-id="66768-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="66768-136">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="66768-137">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="66768-137">End of server support</span></span><br/> | <span data-ttu-id="66768-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="66768-138">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="66768-139">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="66768-139">Redistributable</span></span><br/>       | <span data-ttu-id="66768-140">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="66768-140">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="66768-141">DLL</span><span class="sxs-lookup"><span data-stu-id="66768-141">DLL</span></span><br/>                   | <dl> <span data-ttu-id="66768-142"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66768-142"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
