---
description: Crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente.
ms.assetid: c9a53005-4bb2-4a07-8f58-28d51f22c9e8
title: 'Metodo IEnumPStoreProviders:: Clone (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders.Clone
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: fdd7825a44dcea672eff24a15126921f0426a986
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329167"
---
# <a name="ienumpstoreprovidersclone-method"></a><span data-ttu-id="8b2e4-103">Metodo IEnumPStoreProviders:: Clone</span><span class="sxs-lookup"><span data-stu-id="8b2e4-103">IEnumPStoreProviders::Clone method</span></span>

<span data-ttu-id="8b2e4-104">\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8b2e4-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="8b2e4-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="8b2e4-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="8b2e4-106">PStore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="8b2e4-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="8b2e4-107">Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="8b2e4-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="8b2e4-108">Crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente.</span><span class="sxs-lookup"><span data-stu-id="8b2e4-108">Creates another enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b2e4-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8b2e4-109">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumPStoreProviders **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="8b2e4-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="8b2e4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b2e4-111">*ppEnum* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8b2e4-111">*ppenum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b2e4-112">Puntatore a un puntatore [**IEnumPStoreProviders**](ienumpstoreproviders.md) .</span><span class="sxs-lookup"><span data-stu-id="8b2e4-112">A pointer to an [**IEnumPStoreProviders**](ienumpstoreproviders.md) pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b2e4-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8b2e4-113">Return value</span></span>

<span data-ttu-id="8b2e4-114">Il valore restituito è un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8b2e4-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b2e4-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8b2e4-115">Requirements</span></span>



| <span data-ttu-id="8b2e4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b2e4-116">Requirement</span></span> | <span data-ttu-id="8b2e4-117">Valore</span><span class="sxs-lookup"><span data-stu-id="8b2e4-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b2e4-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8b2e4-118">Header</span></span><br/> | <dl> <span data-ttu-id="8b2e4-119"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b2e4-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="8b2e4-120">DLL</span><span class="sxs-lookup"><span data-stu-id="8b2e4-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="8b2e4-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b2e4-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b2e4-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8b2e4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b2e4-123">**IEnumPStoreProviders**</span><span class="sxs-lookup"><span data-stu-id="8b2e4-123">**IEnumPStoreProviders**</span></span>](ienumpstoreproviders.md)
</dt> </dl>

 

 
