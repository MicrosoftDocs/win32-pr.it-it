---
description: Ignora il numero specificato successivo di elementi nella sequenza di enumerazione.
ms.assetid: 4c02aac8-0496-4ad9-9863-2074b2c71902
title: 'Metodo IEnumPStoreTypes:: Skip (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes.Skip
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 511595dd55f66e91ae0f5606f9e047918e7ff0fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332094"
---
# <a name="ienumpstoretypesskip-method"></a><span data-ttu-id="1460a-103">Metodo IEnumPStoreTypes:: Skip</span><span class="sxs-lookup"><span data-stu-id="1460a-103">IEnumPStoreTypes::Skip method</span></span>

<span data-ttu-id="1460a-104">\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1460a-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="1460a-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="1460a-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="1460a-106">PStore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="1460a-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="1460a-107">Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="1460a-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="1460a-108">Ignora il numero specificato successivo di elementi nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="1460a-108">Skips over the next specified number of items in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="1460a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1460a-109">Syntax</span></span>


```C++
HRESULT Skip(
  [in] DWORD celt
);
```



## <a name="parameters"></a><span data-ttu-id="1460a-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="1460a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1460a-111">*celt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1460a-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1460a-112">Numero di tipi di provider da ignorare.</span><span class="sxs-lookup"><span data-stu-id="1460a-112">The number of provider types to be skipped.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1460a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1460a-113">Return value</span></span>

<span data-ttu-id="1460a-114">Il valore restituito è un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1460a-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1460a-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1460a-115">Requirements</span></span>



| <span data-ttu-id="1460a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1460a-116">Requirement</span></span> | <span data-ttu-id="1460a-117">Valore</span><span class="sxs-lookup"><span data-stu-id="1460a-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1460a-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1460a-118">Header</span></span><br/> | <dl> <span data-ttu-id="1460a-119"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="1460a-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="1460a-120">DLL</span><span class="sxs-lookup"><span data-stu-id="1460a-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="1460a-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1460a-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1460a-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1460a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1460a-123">**IEnumPStoreTypes**</span><span class="sxs-lookup"><span data-stu-id="1460a-123">**IEnumPStoreTypes**</span></span>](ienumpstoretypes.md)
</dt> </dl>

 

 
