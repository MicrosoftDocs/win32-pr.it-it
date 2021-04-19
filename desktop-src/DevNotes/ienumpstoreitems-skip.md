---
description: Ignora il numero specificato successivo di elementi nella sequenza di enumerazione specificata.
ms.assetid: 1459c18a-ccff-451f-8904-32858cc72b78
title: 'Metodo IEnumPStoreItems:: Skip (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems.Skip
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 912dea836ec5ac04ddaf54de9f7f7b609e4e23ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332371"
---
# <a name="ienumpstoreitemsskip-method"></a><span data-ttu-id="dcfdd-103">Metodo IEnumPStoreItems:: Skip</span><span class="sxs-lookup"><span data-stu-id="dcfdd-103">IEnumPStoreItems::Skip method</span></span>

<span data-ttu-id="dcfdd-104">\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="dcfdd-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="dcfdd-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="dcfdd-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="dcfdd-106">PStore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="dcfdd-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="dcfdd-107">Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="dcfdd-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="dcfdd-108">Ignora il numero specificato successivo di elementi nella sequenza di enumerazione specificata.</span><span class="sxs-lookup"><span data-stu-id="dcfdd-108">Skips over the next specified number of items in the given enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcfdd-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dcfdd-109">Syntax</span></span>


```C++
HRESULT Skip(
  [in] DWORD celt
);
```



## <a name="parameters"></a><span data-ttu-id="dcfdd-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="dcfdd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcfdd-111">*celt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dcfdd-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcfdd-112">Numero di elementi di dati da ignorare.</span><span class="sxs-lookup"><span data-stu-id="dcfdd-112">The number of data items to be skipped.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcfdd-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dcfdd-113">Return value</span></span>

<span data-ttu-id="dcfdd-114">Il valore restituito è un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dcfdd-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcfdd-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dcfdd-115">Requirements</span></span>



| <span data-ttu-id="dcfdd-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcfdd-116">Requirement</span></span> | <span data-ttu-id="dcfdd-117">Valore</span><span class="sxs-lookup"><span data-stu-id="dcfdd-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dcfdd-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dcfdd-118">Header</span></span><br/> | <dl> <span data-ttu-id="dcfdd-119"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcfdd-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="dcfdd-120">DLL</span><span class="sxs-lookup"><span data-stu-id="dcfdd-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="dcfdd-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dcfdd-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcfdd-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dcfdd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcfdd-123">**IEnumPStoreItems**</span><span class="sxs-lookup"><span data-stu-id="dcfdd-123">**IEnumPStoreItems**</span></span>](ienumpstoreitems.md)
</dt> </dl>

 

 
