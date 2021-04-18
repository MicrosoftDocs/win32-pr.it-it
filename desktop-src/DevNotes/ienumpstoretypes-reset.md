---
description: Reimposta l'inizio della sequenza di enumerazione.
ms.assetid: 35f14aa5-92cb-4ad8-b80c-2550dedb7a7f
title: 'Metodo IEnumPStoreTypes:: Reset (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes.Reset
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 60aeb1f68bcbf18e903472fa736b5714076dfbfa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324802"
---
# <a name="ienumpstoretypesreset-method"></a><span data-ttu-id="0c62c-103">Metodo IEnumPStoreTypes:: Reset</span><span class="sxs-lookup"><span data-stu-id="0c62c-103">IEnumPStoreTypes::Reset method</span></span>

<span data-ttu-id="0c62c-104">\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0c62c-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="0c62c-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="0c62c-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="0c62c-106">PStore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="0c62c-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="0c62c-107">Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="0c62c-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="0c62c-108">Reimposta l'inizio della sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="0c62c-108">Resets to the beginning of the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c62c-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0c62c-109">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="0c62c-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="0c62c-110">Parameters</span></span>

<span data-ttu-id="0c62c-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="0c62c-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0c62c-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0c62c-112">Return value</span></span>

<span data-ttu-id="0c62c-113">Il valore restituito è un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0c62c-113">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c62c-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0c62c-114">Requirements</span></span>



| <span data-ttu-id="0c62c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c62c-115">Requirement</span></span> | <span data-ttu-id="0c62c-116">Valore</span><span class="sxs-lookup"><span data-stu-id="0c62c-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c62c-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0c62c-117">Header</span></span><br/> | <dl> <span data-ttu-id="0c62c-118"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c62c-118"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="0c62c-119">DLL</span><span class="sxs-lookup"><span data-stu-id="0c62c-119">DLL</span></span><br/>    | <dl> <span data-ttu-id="0c62c-120"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c62c-120"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c62c-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0c62c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c62c-122">**IEnumPStoreTypes**</span><span class="sxs-lookup"><span data-stu-id="0c62c-122">**IEnumPStoreTypes**</span></span>](ienumpstoretypes.md)
</dt> </dl>

 

 
