---
description: "Metodo IEnumPStoreProviders::Reset: reimposta all'inizio della sequenza di enumerazione."
ms.assetid: 9c5044b5-25a3-4d10-829b-ef4d8b5ac095
title: Metodo IEnumPStoreProviders::Reset (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders.Reset
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 3e37e131b6f67f94bb787051123be8eb430eb39e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096759"
---
# <a name="ienumpstoreprovidersreset-method"></a><span data-ttu-id="5fbff-103">Metodo IEnumPStoreProviders::Reset</span><span class="sxs-lookup"><span data-stu-id="5fbff-103">IEnumPStoreProviders::Reset method</span></span>

<span data-ttu-id="5fbff-104">\[L'archiviazione protetta (Pstore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5fbff-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="5fbff-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="5fbff-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="5fbff-106">Pstore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="5fbff-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="5fbff-107">Gli sviluppatori sono fortemente invitati a sfruttare la protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]</span><span class="sxs-lookup"><span data-stu-id="5fbff-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="5fbff-108">Reimposta all'inizio della sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="5fbff-108">Resets to the beginning of the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fbff-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5fbff-109">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="5fbff-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="5fbff-110">Parameters</span></span>

<span data-ttu-id="5fbff-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="5fbff-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5fbff-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5fbff-112">Return value</span></span>

<span data-ttu-id="5fbff-113">Il valore restituito è **un valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="5fbff-113">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fbff-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5fbff-114">Requirements</span></span>



| <span data-ttu-id="5fbff-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fbff-115">Requirement</span></span> | <span data-ttu-id="5fbff-116">Valore</span><span class="sxs-lookup"><span data-stu-id="5fbff-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5fbff-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5fbff-117">Header</span></span><br/> | <dl> <span data-ttu-id="5fbff-118"><dt>Pstore.h</dt></span><span class="sxs-lookup"><span data-stu-id="5fbff-118"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="5fbff-119">DLL</span><span class="sxs-lookup"><span data-stu-id="5fbff-119">DLL</span></span><br/>    | <dl> <span data-ttu-id="5fbff-120"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5fbff-120"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fbff-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5fbff-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fbff-122">**IEnumPStoreProviders**</span><span class="sxs-lookup"><span data-stu-id="5fbff-122">**IEnumPStoreProviders**</span></span>](ienumpstoreproviders.md)
</dt> </dl>

 

 
