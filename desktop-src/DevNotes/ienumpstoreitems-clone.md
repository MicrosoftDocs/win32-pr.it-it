---
description: 'Metodo IEnumPStoreItems::Clone: crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente.'
ms.assetid: ab9eaf63-54e4-4322-9bb5-227982b15c73
title: Metodo IEnumPStoreItems::Clone (Pstore.h)
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
ms.openlocfilehash: 29b618881305296a560dc9102f7571c08236d1bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089329"
---
# <a name="ienumpstoreitemsclone-method"></a><span data-ttu-id="0805a-103">Metodo IEnumPStoreItems::Clone</span><span class="sxs-lookup"><span data-stu-id="0805a-103">IEnumPStoreItems::Clone method</span></span>

<span data-ttu-id="0805a-104">\[L'archiviazione protetta (Pstore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0805a-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="0805a-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="0805a-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="0805a-106">Pstore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="0805a-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="0805a-107">Gli sviluppatori sono fortemente invitati a sfruttare la protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]</span><span class="sxs-lookup"><span data-stu-id="0805a-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="0805a-108">Crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente.</span><span class="sxs-lookup"><span data-stu-id="0805a-108">Creates another enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="0805a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0805a-109">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumPStoreItems **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="0805a-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="0805a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0805a-111">*ppenum* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="0805a-111">*ppenum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0805a-112">Puntatore a un [**puntatore IEnumPStoreItems.**](ienumpstoreitems.md)</span><span class="sxs-lookup"><span data-stu-id="0805a-112">A pointer to an [**IEnumPStoreItems**](ienumpstoreitems.md) pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0805a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0805a-113">Return value</span></span>

<span data-ttu-id="0805a-114">Il valore restituito è **un valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="0805a-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0805a-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0805a-115">Requirements</span></span>



| <span data-ttu-id="0805a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0805a-116">Requirement</span></span> | <span data-ttu-id="0805a-117">Valore</span><span class="sxs-lookup"><span data-stu-id="0805a-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0805a-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0805a-118">Header</span></span><br/> | <dl> <span data-ttu-id="0805a-119"><dt>Pstore.h</dt></span><span class="sxs-lookup"><span data-stu-id="0805a-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="0805a-120">DLL</span><span class="sxs-lookup"><span data-stu-id="0805a-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="0805a-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0805a-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0805a-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0805a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0805a-123">**IEnumPStoreItems**</span><span class="sxs-lookup"><span data-stu-id="0805a-123">**IEnumPStoreItems**</span></span>](ienumpstoreitems.md)
</dt> </dl>

 

 
