---
description: Recupera i dati con hash dopo le chiamate al metodo hash.
ms.assetid: 02ba92d2-38eb-4c01-99b9-11676e7d49ff
title: Proprietà HashedData. Value
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 496bdd76400c746ae3209a2e3c99b6cf4e5bc4b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325598"
---
# <a name="hasheddatavalue-property"></a><span data-ttu-id="e0f88-103">Proprietà HashedData. Value</span><span class="sxs-lookup"><span data-stu-id="e0f88-103">HashedData.Value property</span></span>

<span data-ttu-id="e0f88-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e0f88-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="e0f88-105">Usare invece la [**classe HashAlgorithm**](/previous-versions/windows/) nello spazio dei nomi [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="e0f88-105">Instead, use the [**HashAlgorithm Class**](/previous-versions/windows/) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="e0f88-106">La proprietà **value** recupera i dati con hash dopo le chiamate al metodo [**hash**](hasheddata-hash.md) .</span><span class="sxs-lookup"><span data-stu-id="e0f88-106">The **Value** property retrieves the hashed data after successful calls to the [**Hash**](hasheddata-hash.md) method.</span></span> <span data-ttu-id="e0f88-107">Il valore hash viene restituito in formato esadecimale.</span><span class="sxs-lookup"><span data-stu-id="e0f88-107">The hash value is returned in hexadecimal format.</span></span> <span data-ttu-id="e0f88-108">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="e0f88-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0f88-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e0f88-109">Syntax</span></span>


```VB
HashedData.Value As String
```



## <a name="property-value"></a><span data-ttu-id="e0f88-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="e0f88-110">Property value</span></span>

<span data-ttu-id="e0f88-111">Stringa che contiene i dati con hash in formato esadecimale.</span><span class="sxs-lookup"><span data-stu-id="e0f88-111">A string that contains the hashed data in hexadecimal format.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0f88-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="e0f88-112">Remarks</span></span>

<span data-ttu-id="e0f88-113">Per creare l'hash di una grande quantità di dati, chiamare il metodo [**hash**](hasheddata-hash.md) per ogni pezzo di dati.</span><span class="sxs-lookup"><span data-stu-id="e0f88-113">To create the hash of a large amount of data, call the [**Hash**](hasheddata-hash.md) method for each piece of data.</span></span> <span data-ttu-id="e0f88-114">L'hash di ogni porzione di dati viene concatenato alla proprietà **value** fino a quando non viene letta la proprietà.</span><span class="sxs-lookup"><span data-stu-id="e0f88-114">The hash of each piece of data is concatenated to the **Value** property until the property is read.</span></span> <span data-ttu-id="e0f88-115">Il contenuto della proprietà **value** viene reimpostato quando viene letta la proprietà.</span><span class="sxs-lookup"><span data-stu-id="e0f88-115">The contents of the **Value** property are reset when the property is read.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0f88-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0f88-116">Requirements</span></span>



| <span data-ttu-id="e0f88-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0f88-117">Requirement</span></span> | <span data-ttu-id="e0f88-118">Valore</span><span class="sxs-lookup"><span data-stu-id="e0f88-118">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0f88-119">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="e0f88-119">End of client support</span></span><br/> | <span data-ttu-id="e0f88-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e0f88-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e0f88-121">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="e0f88-121">End of server support</span></span><br/> | <span data-ttu-id="e0f88-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e0f88-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e0f88-123">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="e0f88-123">Redistributable</span></span><br/>       | <span data-ttu-id="e0f88-124">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="e0f88-124">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e0f88-125">DLL</span><span class="sxs-lookup"><span data-stu-id="e0f88-125">DLL</span></span><br/>                   | <dl> <span data-ttu-id="e0f88-126"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0f88-126"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0f88-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e0f88-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0f88-128">**HashedData**</span><span class="sxs-lookup"><span data-stu-id="e0f88-128">**HashedData**</span></span>](hasheddata.md)
</dt> </dl>

 

 
