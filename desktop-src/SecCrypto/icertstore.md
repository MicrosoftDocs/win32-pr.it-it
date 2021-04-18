---
description: Consente di accedere al contesto di un oggetto archivio CAPICOM. Questo contesto consente l'uso dell'archivio certificati CAPICOM in altre derivazioni di CryptoAPI.
ms.assetid: dc108e2d-d6ec-4972-9c8e-e6e738c25756
title: Interfaccia ICertStore
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 119609399709340049bc43693ac51f6259021416
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328596"
---
# <a name="icertstore-interface"></a><span data-ttu-id="cd315-104">Interfaccia ICertStore</span><span class="sxs-lookup"><span data-stu-id="cd315-104">ICertStore interface</span></span>

<span data-ttu-id="cd315-105">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="cd315-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="cd315-106">L'interfaccia **ICertStore** consente di accedere al contesto di un oggetto [**Archivio**](store.md) CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="cd315-106">The **ICertStore** interface provides access to the context of a CAPICOM [**Store**](store.md) object.</span></span> <span data-ttu-id="cd315-107">Questo contesto consente l'uso dell'archivio certificati CAPICOM in altre derivazioni di CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="cd315-107">This context allows the CAPICOM certificate store to be used in other derivations of CryptoAPI.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="cd315-108">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="cd315-108">When to use</span></span>

<span data-ttu-id="cd315-109">Usare questa interfaccia quando è necessario usare un oggetto [**Archivio**](store.md) CAPICOM in un'altra derivazione di CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="cd315-109">Use this interface when you need to use a CAPICOM [**Store**](store.md) object in another derivation of CryptoAPI.</span></span>

## <a name="members"></a><span data-ttu-id="cd315-110">Membri</span><span class="sxs-lookup"><span data-stu-id="cd315-110">Members</span></span>

<span data-ttu-id="cd315-111">L'interfaccia **ICertStore** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="cd315-111">The **ICertStore** interface has these types of members:</span></span>

-   [<span data-ttu-id="cd315-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="cd315-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="cd315-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cd315-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cd315-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="cd315-114">Methods</span></span>

<span data-ttu-id="cd315-115">L'interfaccia **ICertStore** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="cd315-115">The **ICertStore** interface has these methods.</span></span>



| <span data-ttu-id="cd315-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="cd315-116">Method</span></span>                                        | <span data-ttu-id="cd315-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd315-117">Description</span></span>                                                                                                         |
|:----------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd315-118">**CloseHandle**</span><span class="sxs-lookup"><span data-stu-id="cd315-118">**CloseHandle**</span></span>](icertstore-closehandle.md) | <span data-ttu-id="cd315-119">Chiude un handle HCERTSTORE acquisito tramite la proprietà [**storeHandle**](icertstore-storehandle.md) .</span><span class="sxs-lookup"><span data-stu-id="cd315-119">Closes an HCERTSTORE handle acquired through the [**StoreHandle**](icertstore-storehandle.md) property.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="cd315-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cd315-120">Properties</span></span>

<span data-ttu-id="cd315-121">L'interfaccia **ICertStore** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="cd315-121">The **ICertStore** interface has these properties.</span></span>



| <span data-ttu-id="cd315-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cd315-122">Property</span></span>                                                     | <span data-ttu-id="cd315-123">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="cd315-123">Access type</span></span>           | <span data-ttu-id="cd315-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd315-124">Description</span></span>                                                                                                         |
|:-------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd315-125">**StoreHandle**</span><span class="sxs-lookup"><span data-stu-id="cd315-125">**StoreHandle**</span></span>](icertstore-storehandle.md)<br/>     | <span data-ttu-id="cd315-126">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="cd315-126">Read/write</span></span><br/> | <span data-ttu-id="cd315-127">Imposta o recupera l'handle HCERTSTORE di un archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="cd315-127">Sets or retrieves the HCERTSTORE handle of a certificate store.</span></span><br/>                                          |
| [<span data-ttu-id="cd315-128">**StoreLocation**</span><span class="sxs-lookup"><span data-stu-id="cd315-128">**StoreLocation**</span></span>](icertstore-storelocation.md)<br/> | <span data-ttu-id="cd315-129">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="cd315-129">Read/write</span></span><br/> | <span data-ttu-id="cd315-130">Imposta o Recupera il [**\_ \_ percorso dell'archivio CAPICOM**](capicom-store-location.md) di un archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="cd315-130">Sets or retrieves the [**CAPICOM\_STORE\_LOCATION**](capicom-store-location.md) of a certificate store.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cd315-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd315-131">Requirements</span></span>



| <span data-ttu-id="cd315-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd315-132">Requirement</span></span> | <span data-ttu-id="cd315-133">Valore</span><span class="sxs-lookup"><span data-stu-id="cd315-133">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd315-134">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="cd315-134">Redistributable</span></span><br/> | <span data-ttu-id="cd315-135">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="cd315-135">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="cd315-136">DLL</span><span class="sxs-lookup"><span data-stu-id="cd315-136">DLL</span></span><br/>             | <dl> <span data-ttu-id="cd315-137"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd315-137"><dt>Capicom.dll</dt></span></span> </dl> |



 

 




