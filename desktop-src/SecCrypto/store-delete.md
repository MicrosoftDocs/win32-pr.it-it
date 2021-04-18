---
description: Elimina l'archivio certificati rappresentato dall'oggetto archivio corrente.
ms.assetid: 274914ee-27a0-4bd6-8510-af897aab3a2d
title: Store. Delete (metodo)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Delete
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 41c6417dae5006eb2ecaf64660fd0007cdf37fd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333971"
---
# <a name="storedelete-method"></a><span data-ttu-id="4a16e-103">Store. Delete (metodo)</span><span class="sxs-lookup"><span data-stu-id="4a16e-103">Store.Delete method</span></span>

<span data-ttu-id="4a16e-104">\[Il metodo **Delete** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="4a16e-104">\[The **Delete** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4a16e-105">Usare invece la [**classe X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="4a16e-105">Instead, use the [**X509Store Class**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="4a16e-106">Il metodo **Delete** Elimina l' [*archivio certificati*](../secgloss/c-gly.md) rappresentato dall'oggetto [**Archivio**](certificate.md) corrente.</span><span class="sxs-lookup"><span data-stu-id="4a16e-106">The **Delete** method deletes the [*certificate store*](../secgloss/c-gly.md) that is represented by the current [**Store**](certificate.md) object.</span></span> <span data-ttu-id="4a16e-107">Questo metodo elimina solo gli archivi non di sistema.</span><span class="sxs-lookup"><span data-stu-id="4a16e-107">This method deletes only nonsystem stores.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a16e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4a16e-108">Syntax</span></span>


```VB
Store.Delete()
```



## <a name="parameters"></a><span data-ttu-id="4a16e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="4a16e-109">Parameters</span></span>

<span data-ttu-id="4a16e-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="4a16e-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4a16e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4a16e-111">Return value</span></span>

<span data-ttu-id="4a16e-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="4a16e-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a16e-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="4a16e-113">Remarks</span></span>

<span data-ttu-id="4a16e-114">Gli archivi seguenti sono archivi di sistema e non possono essere eliminati:</span><span class="sxs-lookup"><span data-stu-id="4a16e-114">The following stores are system stores and cannot be deleted:</span></span>

-   <span data-ttu-id="4a16e-115">My</span><span class="sxs-lookup"><span data-stu-id="4a16e-115">My</span></span>
-   <span data-ttu-id="4a16e-116">Radice</span><span class="sxs-lookup"><span data-stu-id="4a16e-116">Root</span></span>
-   <span data-ttu-id="4a16e-117">Trust</span><span class="sxs-lookup"><span data-stu-id="4a16e-117">Trust</span></span>
-   <span data-ttu-id="4a16e-118">CA</span><span class="sxs-lookup"><span data-stu-id="4a16e-118">CA</span></span>
-   <span data-ttu-id="4a16e-119">UserDS</span><span class="sxs-lookup"><span data-stu-id="4a16e-119">UserDS</span></span>
-   <span data-ttu-id="4a16e-120">TrustedPublisher</span><span class="sxs-lookup"><span data-stu-id="4a16e-120">TrustedPublisher</span></span>
-   <span data-ttu-id="4a16e-121">Non consentita</span><span class="sxs-lookup"><span data-stu-id="4a16e-121">Disallowed</span></span>
-   <span data-ttu-id="4a16e-122">AuthRoot</span><span class="sxs-lookup"><span data-stu-id="4a16e-122">AuthRoot</span></span>
-   <span data-ttu-id="4a16e-123">TrustedPeople</span><span class="sxs-lookup"><span data-stu-id="4a16e-123">TrustedPeople</span></span>

<span data-ttu-id="4a16e-124">Il metodo **Delete** restituisce un errore se chiamato da uno script Web.</span><span class="sxs-lookup"><span data-stu-id="4a16e-124">The **Delete** method returns an error if called from a web script.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a16e-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a16e-125">Requirements</span></span>



| <span data-ttu-id="4a16e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a16e-126">Requirement</span></span> | <span data-ttu-id="4a16e-127">Valore</span><span class="sxs-lookup"><span data-stu-id="4a16e-127">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a16e-128">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="4a16e-128">Redistributable</span></span><br/> | <span data-ttu-id="4a16e-129">CAPICOM 2,1 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="4a16e-129">CAPICOM 2.1 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4a16e-130">DLL</span><span class="sxs-lookup"><span data-stu-id="4a16e-130">DLL</span></span><br/>             | <dl> <span data-ttu-id="4a16e-131"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a16e-131"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a16e-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4a16e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a16e-133">**Store**</span><span class="sxs-lookup"><span data-stu-id="4a16e-133">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="4a16e-134">**Oggetti Cryptography**</span><span class="sxs-lookup"><span data-stu-id="4a16e-134">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
