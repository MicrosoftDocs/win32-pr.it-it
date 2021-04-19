---
description: Consente di accedere al contesto di un oggetto certificato CAPICOM X. 509v3. Questo contesto consente l'uso del certificato di CAPICOM in altre derivazioni di CryptoAPI.
ms.assetid: 084a3a7b-7523-419f-a504-6fd397030d78
title: Interfaccia ICertContext
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f282b97e2257292849a76bc42017e48a95204d01
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332691"
---
# <a name="icertcontext-interface"></a><span data-ttu-id="f494a-104">Interfaccia ICertContext</span><span class="sxs-lookup"><span data-stu-id="f494a-104">ICertContext interface</span></span>

<span data-ttu-id="f494a-105">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="f494a-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="f494a-106">L'interfaccia **ICertContext** consente di accedere al contesto di un oggetto [**certificato**](certificate.md) capicol X. 509v3.</span><span class="sxs-lookup"><span data-stu-id="f494a-106">The **ICertContext** interface provides access to the context of a CAPICOM X.509v3 [**Certificate**](certificate.md) object.</span></span> <span data-ttu-id="f494a-107">Questo contesto consente l'uso del certificato di CAPICOM in altre derivazioni di CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="f494a-107">This context allows the CAPICOM certificate to be used in other derivations of CryptoAPI.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="f494a-108">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="f494a-108">When to use</span></span>

<span data-ttu-id="f494a-109">Usare questa interfaccia quando è necessario usare un oggetto [**certificato**](certificate.md) CAPICOM in un'altra derivazione di CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="f494a-109">Use this interface when you need to use a CAPICOM [**Certificate**](certificate.md) object in another derivation of CryptoAPI.</span></span>

## <a name="members"></a><span data-ttu-id="f494a-110">Membri</span><span class="sxs-lookup"><span data-stu-id="f494a-110">Members</span></span>

<span data-ttu-id="f494a-111">L'interfaccia **ICertContext** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f494a-111">The **ICertContext** interface has these types of members:</span></span>

-   [<span data-ttu-id="f494a-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="f494a-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="f494a-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f494a-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f494a-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="f494a-114">Methods</span></span>

<span data-ttu-id="f494a-115">L'interfaccia **ICertContext** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="f494a-115">The **ICertContext** interface has these methods.</span></span>



| <span data-ttu-id="f494a-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="f494a-116">Method</span></span>                                          | <span data-ttu-id="f494a-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f494a-117">Description</span></span>                                                                                                          |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f494a-118">**FreeContext**</span><span class="sxs-lookup"><span data-stu-id="f494a-118">**FreeContext**</span></span>](icertcontext-freecontext.md) | <span data-ttu-id="f494a-119">Rilascia un \_ contesto PCCERT acquisito tramite la proprietà [**CertContext**](icertcontext-certcontext.md) .</span><span class="sxs-lookup"><span data-stu-id="f494a-119">Releases a PCCERT\_CONTEXT acquired through the [**CertContext**](icertcontext-certcontext.md) property.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f494a-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f494a-120">Properties</span></span>

<span data-ttu-id="f494a-121">L'interfaccia **ICertContext** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f494a-121">The **ICertContext** interface has these properties.</span></span>



| <span data-ttu-id="f494a-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f494a-122">Property</span></span>                                                   | <span data-ttu-id="f494a-123">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="f494a-123">Access type</span></span>           | <span data-ttu-id="f494a-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f494a-124">Description</span></span>                                                        |
|:-----------------------------------------------------------|:----------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="f494a-125">**CertContext**</span><span class="sxs-lookup"><span data-stu-id="f494a-125">**CertContext**</span></span>](icertcontext-certcontext.md)<br/> | <span data-ttu-id="f494a-126">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="f494a-126">Read/write</span></span><br/> | <span data-ttu-id="f494a-127">Imposta o Recupera il \_ contesto PCCERT di un certificato.</span><span class="sxs-lookup"><span data-stu-id="f494a-127">Sets or retrieves the PCCERT\_CONTEXT of a certificate.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f494a-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f494a-128">Requirements</span></span>



| <span data-ttu-id="f494a-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="f494a-129">Requirement</span></span> | <span data-ttu-id="f494a-130">Valore</span><span class="sxs-lookup"><span data-stu-id="f494a-130">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f494a-131">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="f494a-131">Redistributable</span></span><br/> | <span data-ttu-id="f494a-132">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="f494a-132">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f494a-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f494a-133">DLL</span></span><br/>             | <dl> <span data-ttu-id="f494a-134"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f494a-134"><dt>Capicom.dll</dt></span></span> </dl> |



 

 




