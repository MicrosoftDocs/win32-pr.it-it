---
description: Crea un hash della stringa specificata.
ms.assetid: 8d3e16e7-7b93-410c-b771-7684d1bf2160
title: Metodo HashedData. hash
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData.Hash
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d36973340a7dbf67f8a8b0d1aa4cd5738ef97d74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325599"
---
# <a name="hasheddatahash-method"></a><span data-ttu-id="21f51-103">Metodo HashedData. hash</span><span class="sxs-lookup"><span data-stu-id="21f51-103">HashedData.Hash method</span></span>

<span data-ttu-id="21f51-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="21f51-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="21f51-105">Usare invece la [**classe HashAlgorithm**](/previous-versions/windows/) nello spazio dei nomi [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="21f51-105">Instead, use the [**HashAlgorithm Class**](/previous-versions/windows/) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="21f51-106">Il metodo **hash** crea un hash della stringa specificata.</span><span class="sxs-lookup"><span data-stu-id="21f51-106">The **Hash** method creates a hash of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="21f51-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="21f51-107">Syntax</span></span>


```VB
HashedData.Hash( _
  ByVal newVal _
)
```



## <a name="parameters"></a><span data-ttu-id="21f51-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="21f51-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21f51-109">*newVal*</span><span class="sxs-lookup"><span data-stu-id="21f51-109">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="21f51-110">Stringa che contiene il valore di cui eseguire l'hashing.</span><span class="sxs-lookup"><span data-stu-id="21f51-110">String that contains the value to hash.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21f51-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="21f51-111">Return value</span></span>

<span data-ttu-id="21f51-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="21f51-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="21f51-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="21f51-113">Remarks</span></span>

<span data-ttu-id="21f51-114">Per creare l'hash di una grande quantità di dati, chiamare il metodo **hash** per ogni pezzo di dati.</span><span class="sxs-lookup"><span data-stu-id="21f51-114">To create the hash of a large amount of data, call the **Hash** method for each piece of data.</span></span> <span data-ttu-id="21f51-115">L'hash di ogni porzione di dati viene concatenato alla proprietà [**value**](hasheddata-value.md) fino a quando non viene letta la proprietà.</span><span class="sxs-lookup"><span data-stu-id="21f51-115">The hash of each piece of data is concatenated to the [**Value**](hasheddata-value.md) property until the property is read.</span></span> <span data-ttu-id="21f51-116">Il contenuto della proprietà **value** viene reimpostato quando viene letta la proprietà.</span><span class="sxs-lookup"><span data-stu-id="21f51-116">The contents of the **Value** property are reset when the property is read.</span></span>

## <a name="requirements"></a><span data-ttu-id="21f51-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21f51-117">Requirements</span></span>



| <span data-ttu-id="21f51-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="21f51-118">Requirement</span></span> | <span data-ttu-id="21f51-119">Valore</span><span class="sxs-lookup"><span data-stu-id="21f51-119">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="21f51-120">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="21f51-120">End of client support</span></span><br/> | <span data-ttu-id="21f51-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="21f51-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="21f51-122">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="21f51-122">End of server support</span></span><br/> | <span data-ttu-id="21f51-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="21f51-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="21f51-124">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="21f51-124">Redistributable</span></span><br/>       | <span data-ttu-id="21f51-125">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="21f51-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="21f51-126">DLL</span><span class="sxs-lookup"><span data-stu-id="21f51-126">DLL</span></span><br/>                   | <dl> <span data-ttu-id="21f51-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21f51-127"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
