---
description: Fornisce l'accesso al contesto di un oggetto chain di capico. Questo contesto consente l'uso della catena di certificati del certificato CAPICOM in altre derivazioni di CryptoAPI.
ms.assetid: ee258586-028e-486e-8129-07f43b6cc468
title: Interfaccia IChainContext
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 34ba471c50ceb9475121139c3ecb997cf1d26f2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323966"
---
# <a name="ichaincontext-interface"></a><span data-ttu-id="43f44-104">Interfaccia IChainContext</span><span class="sxs-lookup"><span data-stu-id="43f44-104">IChainContext interface</span></span>

<span data-ttu-id="43f44-105">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="43f44-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="43f44-106">L'interfaccia **IChainContext** fornisce l'accesso al contesto di un oggetto [**Chain**](chain.md) di capico.</span><span class="sxs-lookup"><span data-stu-id="43f44-106">The **IChainContext** interface provides access to the context of a CAPICOM [**Chain**](chain.md) object.</span></span> <span data-ttu-id="43f44-107">Questo contesto consente l'uso della catena di certificati del certificato CAPICOM in altre derivazioni di CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="43f44-107">This context allows the CAPICOM certificate trust chain to be used in other derivations of CryptoAPI.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="43f44-108">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="43f44-108">When to use</span></span>

<span data-ttu-id="43f44-109">Usare questa interfaccia quando è necessario usare un oggetto [**catena**](chain.md) di CAPICOM in un'altra derivazione di CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="43f44-109">Use this interface when you need to use a CAPICOM [**Chain**](chain.md) object in another derivation of CryptoAPI.</span></span>

## <a name="members"></a><span data-ttu-id="43f44-110">Membri</span><span class="sxs-lookup"><span data-stu-id="43f44-110">Members</span></span>

<span data-ttu-id="43f44-111">L'interfaccia **IChainContext** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="43f44-111">The **IChainContext** interface has these types of members:</span></span>

-   [<span data-ttu-id="43f44-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="43f44-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="43f44-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="43f44-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="43f44-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="43f44-114">Methods</span></span>

<span data-ttu-id="43f44-115">L'interfaccia **IChainContext** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="43f44-115">The **IChainContext** interface has these methods.</span></span>



| <span data-ttu-id="43f44-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="43f44-116">Method</span></span>                                           | <span data-ttu-id="43f44-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43f44-117">Description</span></span>                                                                                                                    |
|:-------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="43f44-118">**FreeContext**</span><span class="sxs-lookup"><span data-stu-id="43f44-118">**FreeContext**</span></span>](ichaincontext-freecontext.md) | <span data-ttu-id="43f44-119">Rilascia un \_ \_ contesto della catena PCCERT acquisito tramite la proprietà [**chainContext**](ichaincontext-chaincontext.md) .</span><span class="sxs-lookup"><span data-stu-id="43f44-119">Releases a PCCERT\_CHAIN\_CONTEXT acquired through the [**ChainContext**](ichaincontext-chaincontext.md) property.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="43f44-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="43f44-120">Properties</span></span>

<span data-ttu-id="43f44-121">L'interfaccia **IChainContext** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="43f44-121">The **IChainContext** interface has these properties.</span></span>



| <span data-ttu-id="43f44-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="43f44-122">Property</span></span>                                                      | <span data-ttu-id="43f44-123">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="43f44-123">Access type</span></span>           | <span data-ttu-id="43f44-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43f44-124">Description</span></span>                                                               |
|:--------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="43f44-125">**ChainContext**</span><span class="sxs-lookup"><span data-stu-id="43f44-125">**ChainContext**</span></span>](ichaincontext-chaincontext.md)<br/> | <span data-ttu-id="43f44-126">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="43f44-126">Read/write</span></span><br/> | <span data-ttu-id="43f44-127">Imposta o Recupera il \_ \_ contesto della catena PCCERT di un certificato.</span><span class="sxs-lookup"><span data-stu-id="43f44-127">Sets or retrieves the PCCERT\_CHAIN\_CONTEXT of a certificate.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="43f44-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43f44-128">Requirements</span></span>



| <span data-ttu-id="43f44-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="43f44-129">Requirement</span></span> | <span data-ttu-id="43f44-130">Valore</span><span class="sxs-lookup"><span data-stu-id="43f44-130">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="43f44-131">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="43f44-131">Redistributable</span></span><br/> | <span data-ttu-id="43f44-132">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="43f44-132">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="43f44-133">DLL</span><span class="sxs-lookup"><span data-stu-id="43f44-133">DLL</span></span><br/>             | <dl> <span data-ttu-id="43f44-134"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43f44-134"><dt>Capicom.dll</dt></span></span> </dl> |



 

 




