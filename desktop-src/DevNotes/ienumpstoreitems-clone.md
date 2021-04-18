---
description: Crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente.
ms.assetid: ab9eaf63-54e4-4322-9bb5-227982b15c73
title: 'Metodo IEnumPStoreItems:: Clone (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems.Clone
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 919c0359f5c7f6d3ab547f53a105246c43e20fb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331968"
---
# <a name="ienumpstoreitemsclone-method"></a><span data-ttu-id="24847-103">Metodo IEnumPStoreItems:: Clone</span><span class="sxs-lookup"><span data-stu-id="24847-103">IEnumPStoreItems::Clone method</span></span>

<span data-ttu-id="24847-104">\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="24847-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="24847-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="24847-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="24847-106">PStore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="24847-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="24847-107">Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="24847-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="24847-108">Crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente.</span><span class="sxs-lookup"><span data-stu-id="24847-108">Creates another enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="24847-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="24847-109">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumPStoreItems **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="24847-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="24847-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24847-111">*ppEnum* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="24847-111">*ppenum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="24847-112">Puntatore a un puntatore [**IEnumPStoreItems**](ienumpstoreitems.md) .</span><span class="sxs-lookup"><span data-stu-id="24847-112">A pointer to an [**IEnumPStoreItems**](ienumpstoreitems.md) pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24847-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="24847-113">Return value</span></span>

<span data-ttu-id="24847-114">Il valore restituito è un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="24847-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="24847-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="24847-115">Requirements</span></span>



| <span data-ttu-id="24847-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="24847-116">Requirement</span></span> | <span data-ttu-id="24847-117">Valore</span><span class="sxs-lookup"><span data-stu-id="24847-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="24847-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="24847-118">Header</span></span><br/> | <dl> <span data-ttu-id="24847-119"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="24847-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="24847-120">DLL</span><span class="sxs-lookup"><span data-stu-id="24847-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="24847-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24847-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24847-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="24847-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24847-123">**IEnumPStoreItems**</span><span class="sxs-lookup"><span data-stu-id="24847-123">**IEnumPStoreItems**</span></span>](ienumpstoreitems.md)
</dt> </dl>

 

 
