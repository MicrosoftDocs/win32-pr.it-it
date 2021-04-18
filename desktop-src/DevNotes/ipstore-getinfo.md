---
description: Restituisce informazioni sul provider di archiviazione.
ms.assetid: bdacb5bb-a37a-4970-add7-57625bec1ce0
title: 'Metodo IPStore:: GetInfo (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.GetInfo
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 7747c3acf15a60f5556a8855ef4825715ef5050b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324280"
---
# <a name="ipstoregetinfo-method"></a><span data-ttu-id="46698-103">Metodo IPStore:: GetInfo</span><span class="sxs-lookup"><span data-stu-id="46698-103">IPStore::GetInfo method</span></span>

<span data-ttu-id="46698-104">\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="46698-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="46698-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="46698-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="46698-106">PStore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="46698-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="46698-107">Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="46698-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="46698-108">Restituisce informazioni sul provider di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="46698-108">Returns information on the storage provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="46698-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46698-109">Syntax</span></span>


```C++
HRESULT GetInfo(
  [out] PPST_PROVIDERINFO *ppProperties
);
```



## <a name="parameters"></a><span data-ttu-id="46698-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="46698-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46698-111">*ppProperties* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="46698-111">*ppProperties* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46698-112">Puntatore a una struttura **PPST \_ ProviderInfo restituito da** che contiene informazioni sul provider di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="46698-112">A pointer to a **PPST\_PROVIDERINFO** structure that contains information about the storage provider.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46698-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="46698-113">Return value</span></span>

<span data-ttu-id="46698-114">Il valore restituito è un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="46698-114">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="46698-115">Il valore **pst \_ E \_ OK** indica che la funzione ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="46698-115">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="46698-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46698-116">Requirements</span></span>



| <span data-ttu-id="46698-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="46698-117">Requirement</span></span> | <span data-ttu-id="46698-118">Valore</span><span class="sxs-lookup"><span data-stu-id="46698-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="46698-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="46698-119">Header</span></span><br/> | <dl> <span data-ttu-id="46698-120"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="46698-120"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="46698-121">DLL</span><span class="sxs-lookup"><span data-stu-id="46698-121">DLL</span></span><br/>    | <dl> <span data-ttu-id="46698-122"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46698-122"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46698-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46698-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46698-124">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="46698-124">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
