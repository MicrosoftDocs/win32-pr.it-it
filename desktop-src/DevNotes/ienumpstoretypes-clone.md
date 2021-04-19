---
description: Crea un enumeratore aggiuntivo che contiene lo stesso stato di enumerazione di quello corrente.
ms.assetid: b4027520-62cc-40d4-b9fd-01fa9c652a54
title: 'Metodo IEnumPStoreTypes:: Clone (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes.Clone
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 4ac088ae708b62f458d7bba52127dadc8ef77c5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332095"
---
# <a name="ienumpstoretypesclone-method"></a><span data-ttu-id="b39bb-103">Metodo IEnumPStoreTypes:: Clone</span><span class="sxs-lookup"><span data-stu-id="b39bb-103">IEnumPStoreTypes::Clone method</span></span>

<span data-ttu-id="b39bb-104">\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b39bb-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="b39bb-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b39bb-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="b39bb-106">PStore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="b39bb-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="b39bb-107">Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="b39bb-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="b39bb-108">Crea un enumeratore aggiuntivo che contiene lo stesso stato di enumerazione di quello corrente.</span><span class="sxs-lookup"><span data-stu-id="b39bb-108">Creates an additional enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="b39bb-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b39bb-109">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumPStoreItems **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="b39bb-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="b39bb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b39bb-111">*ppEnum* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b39bb-111">*ppenum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b39bb-112">Puntatore a un puntatore [**IEnumPStoreItems**](ienumpstoreitems.md) .</span><span class="sxs-lookup"><span data-stu-id="b39bb-112">A pointer to an [**IEnumPStoreItems**](ienumpstoreitems.md) pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b39bb-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b39bb-113">Return value</span></span>

<span data-ttu-id="b39bb-114">Il valore restituito è un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b39bb-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b39bb-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b39bb-115">Requirements</span></span>



| <span data-ttu-id="b39bb-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b39bb-116">Requirement</span></span> | <span data-ttu-id="b39bb-117">Valore</span><span class="sxs-lookup"><span data-stu-id="b39bb-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b39bb-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b39bb-118">Header</span></span><br/> | <dl> <span data-ttu-id="b39bb-119"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="b39bb-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="b39bb-120">DLL</span><span class="sxs-lookup"><span data-stu-id="b39bb-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="b39bb-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b39bb-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b39bb-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b39bb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b39bb-123">**IEnumPStoreItems**</span><span class="sxs-lookup"><span data-stu-id="b39bb-123">**IEnumPStoreItems**</span></span>](ienumpstoreitems.md)
</dt> <dt>

[<span data-ttu-id="b39bb-124">**IEnumPStoreTypes**</span><span class="sxs-lookup"><span data-stu-id="b39bb-124">**IEnumPStoreTypes**</span></span>](ienumpstoretypes.md)
</dt> </dl>

 

 
