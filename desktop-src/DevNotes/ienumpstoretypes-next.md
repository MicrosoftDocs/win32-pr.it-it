---
description: Ottiene il numero specificato successivo di tipi di provider nella sequenza di enumerazione.
ms.assetid: 9a1d0db0-1e9b-48f8-b373-2a82a48e4f63
title: 'Metodo IEnumPStoreTypes:: Next (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes.Next
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 18981053de897b75d1febdc75e138e6561e65bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332093"
---
# <a name="ienumpstoretypesnext-method"></a><span data-ttu-id="0a51c-103">IEnumPStoreTypes:: Next (metodo)</span><span class="sxs-lookup"><span data-stu-id="0a51c-103">IEnumPStoreTypes::Next method</span></span>

<span data-ttu-id="0a51c-104">\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0a51c-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="0a51c-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="0a51c-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="0a51c-106">PStore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="0a51c-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="0a51c-107">Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="0a51c-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="0a51c-108">Ottiene il numero specificato successivo di tipi di provider nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="0a51c-108">Gets the next specified number of provider types in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a51c-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0a51c-109">Syntax</span></span>


```C++
HRESULT Next(
  [in]      DWORD  celt,
  [out]     LPWSTR *rgelt,
  [in, out] DWORD  *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="0a51c-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="0a51c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a51c-111">*celt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0a51c-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a51c-112">Numero di tipi di provider richiesti.</span><span class="sxs-lookup"><span data-stu-id="0a51c-112">The number of provider types requested.</span></span>

</dd> <dt>

<span data-ttu-id="0a51c-113">*rgelt* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0a51c-113">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a51c-114">Puntatore a una stringa in cui restituire il nome del tipo di provider.</span><span class="sxs-lookup"><span data-stu-id="0a51c-114">A pointer to a string in which to return the provider type name.</span></span>

</dd> <dt>

<span data-ttu-id="0a51c-115">*pceltFetched* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="0a51c-115">*pceltFetched* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a51c-116">Puntatore al numero di tipi di provider effettivamente forniti.</span><span class="sxs-lookup"><span data-stu-id="0a51c-116">A pointer to the number of provider types actually supplied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a51c-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0a51c-117">Return value</span></span>

<span data-ttu-id="0a51c-118">Il valore restituito è un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0a51c-118">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a51c-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0a51c-119">Requirements</span></span>



| <span data-ttu-id="0a51c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a51c-120">Requirement</span></span> | <span data-ttu-id="0a51c-121">Valore</span><span class="sxs-lookup"><span data-stu-id="0a51c-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a51c-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0a51c-122">Header</span></span><br/> | <dl> <span data-ttu-id="0a51c-123"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a51c-123"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="0a51c-124">DLL</span><span class="sxs-lookup"><span data-stu-id="0a51c-124">DLL</span></span><br/>    | <dl> <span data-ttu-id="0a51c-125"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a51c-125"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a51c-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0a51c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a51c-127">**IEnumPStoreTypes**</span><span class="sxs-lookup"><span data-stu-id="0a51c-127">**IEnumPStoreTypes**</span></span>](ienumpstoretypes.md)
</dt> </dl>

 

 
