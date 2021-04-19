---
description: Ottiene il numero specificato successivo di provider nella sequenza di enumerazione.
ms.assetid: 9ef8d330-6f78-4063-825c-9cf5b4f283cf
title: 'Metodo IEnumPStoreProviders:: Next (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders.Next
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: f468d29682c4e3767d4d8fe7d59e60976f103484
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326287"
---
# <a name="ienumpstoreprovidersnext-method"></a><span data-ttu-id="ce196-103">IEnumPStoreProviders:: Next (metodo)</span><span class="sxs-lookup"><span data-stu-id="ce196-103">IEnumPStoreProviders::Next method</span></span>

<span data-ttu-id="ce196-104">\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ce196-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="ce196-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="ce196-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="ce196-106">PStore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="ce196-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="ce196-107">Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="ce196-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="ce196-108">Ottiene il numero specificato successivo di provider nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="ce196-108">Gets the next specified number of providers in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce196-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ce196-109">Syntax</span></span>


```C++
HRESULT Next(
  [in]      DWORD  celt,
  [out]     LPWSTR *rgelt,
  [in, out] DWORD  *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="ce196-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="ce196-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce196-111">*celt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce196-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce196-112">Numero di tipi di provider richiesti.</span><span class="sxs-lookup"><span data-stu-id="ce196-112">The number of provider types requested.</span></span>

</dd> <dt>

<span data-ttu-id="ce196-113">*rgelt* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ce196-113">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce196-114">Puntatore a una stringa in cui restituire il nome del tipo di provider.</span><span class="sxs-lookup"><span data-stu-id="ce196-114">A pointer to a string in which to return the provider type name.</span></span>

</dd> <dt>

<span data-ttu-id="ce196-115">*pceltFetched* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="ce196-115">*pceltFetched* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce196-116">Puntatore al numero di tipi di provider effettivamente forniti.</span><span class="sxs-lookup"><span data-stu-id="ce196-116">A pointer to the number of provider types that was actually supplied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce196-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ce196-117">Return value</span></span>

<span data-ttu-id="ce196-118">Il valore restituito è un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ce196-118">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce196-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce196-119">Requirements</span></span>



| <span data-ttu-id="ce196-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce196-120">Requirement</span></span> | <span data-ttu-id="ce196-121">Valore</span><span class="sxs-lookup"><span data-stu-id="ce196-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce196-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ce196-122">Header</span></span><br/> | <dl> <span data-ttu-id="ce196-123"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce196-123"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="ce196-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ce196-124">DLL</span></span><br/>    | <dl> <span data-ttu-id="ce196-125"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce196-125"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce196-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ce196-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce196-127">**IEnumPStoreProviders**</span><span class="sxs-lookup"><span data-stu-id="ce196-127">**IEnumPStoreProviders**</span></span>](ienumpstoreproviders.md)
</dt> </dl>

 

 
