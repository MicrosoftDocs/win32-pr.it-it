---
description: 'Metodo IEnumPStoreProviders::Skip: ignora il successivo numero specificato di elementi nella sequenza di enumerazione.'
ms.assetid: bf9ea700-3f44-48a7-8ea0-ee66dea61836
title: Metodo IEnumPStoreProviders::Skip (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders.Skip
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 2f74c44de172d9235d9768b8f484405b5e8fb7fe
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096749"
---
# <a name="ienumpstoreprovidersskip-method"></a><span data-ttu-id="c436e-103">Metodo IEnumPStoreProviders::Skip</span><span class="sxs-lookup"><span data-stu-id="c436e-103">IEnumPStoreProviders::Skip method</span></span>

<span data-ttu-id="c436e-104">\[L'archiviazione protetta (Pstore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c436e-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="c436e-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c436e-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="c436e-106">Pstore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="c436e-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="c436e-107">Gli sviluppatori sono fortemente invitati a sfruttare la protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]</span><span class="sxs-lookup"><span data-stu-id="c436e-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="c436e-108">Ignora il successivo numero specificato di elementi nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="c436e-108">Skips over the next specified number of items in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="c436e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c436e-109">Syntax</span></span>


```C++
HRESULT Skip(
  [in] DWORD celt
);
```



## <a name="parameters"></a><span data-ttu-id="c436e-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="c436e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c436e-111">*celt* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c436e-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c436e-112">Numero di tipi di provider da ignorare.</span><span class="sxs-lookup"><span data-stu-id="c436e-112">The number of provider types to be skipped.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c436e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c436e-113">Return value</span></span>

<span data-ttu-id="c436e-114">Il valore restituito è un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="c436e-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c436e-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c436e-115">Requirements</span></span>



| <span data-ttu-id="c436e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c436e-116">Requirement</span></span> | <span data-ttu-id="c436e-117">Valore</span><span class="sxs-lookup"><span data-stu-id="c436e-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c436e-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c436e-118">Header</span></span><br/> | <dl> <span data-ttu-id="c436e-119"><dt>Pstore.h</dt></span><span class="sxs-lookup"><span data-stu-id="c436e-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="c436e-120">DLL</span><span class="sxs-lookup"><span data-stu-id="c436e-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="c436e-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c436e-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c436e-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c436e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c436e-123">**IEnumPStoreProviders**</span><span class="sxs-lookup"><span data-stu-id="c436e-123">**IEnumPStoreProviders**</span></span>](ienumpstoreproviders.md)
</dt> </dl>

 

 
