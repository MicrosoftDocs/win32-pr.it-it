---
description: Recupera l'algoritmo di crittografia e la lunghezza della chiave.
ms.assetid: 13b2a3db-f04b-4436-b64f-f194fc9ddac2
title: Proprietà EnvelopedData. Algorithm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9d6550be7ac32c08568baa8ef811478de50b27c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327899"
---
# <a name="envelopeddataalgorithm-property"></a><span data-ttu-id="d391c-103">Proprietà EnvelopedData. Algorithm</span><span class="sxs-lookup"><span data-stu-id="d391c-103">EnvelopedData.Algorithm property</span></span>

<span data-ttu-id="d391c-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d391c-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="d391c-105">Usare invece la [**classe EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="d391c-105">Instead, use the [**EnvelopedCms Class**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="d391c-106">La proprietà **Algorithm** recupera l'algoritmo di crittografia e la [*lunghezza della chiave*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d391c-106">The **Algorithm** property retrieves the encryption algorithm and [*key length*](../secgloss/k-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d391c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d391c-107">Syntax</span></span>


```VB
EnvelopedData.Algorithm As Algorithm
```



## <a name="property-value"></a><span data-ttu-id="d391c-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d391c-108">Property value</span></span>

<span data-ttu-id="d391c-109">Oggetto [**algoritmo**](algorithm.md) che contiene l'algoritmo di crittografia e la lunghezza della chiave.</span><span class="sxs-lookup"><span data-stu-id="d391c-109">An [**Algorithm**](algorithm.md) object that contains the encryption algorithm and key length.</span></span>

## <a name="requirements"></a><span data-ttu-id="d391c-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d391c-110">Requirements</span></span>



| <span data-ttu-id="d391c-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="d391c-111">Requirement</span></span> | <span data-ttu-id="d391c-112">Valore</span><span class="sxs-lookup"><span data-stu-id="d391c-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d391c-113">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="d391c-113">End of client support</span></span><br/> | <span data-ttu-id="d391c-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d391c-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d391c-115">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="d391c-115">End of server support</span></span><br/> | <span data-ttu-id="d391c-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d391c-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d391c-117">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="d391c-117">Redistributable</span></span><br/>       | <span data-ttu-id="d391c-118">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="d391c-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d391c-119">DLL</span><span class="sxs-lookup"><span data-stu-id="d391c-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="d391c-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d391c-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d391c-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d391c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d391c-122">**EnvelopedData**</span><span class="sxs-lookup"><span data-stu-id="d391c-122">**EnvelopedData**</span></span>](envelopeddata.md)
</dt> </dl>

 

 
