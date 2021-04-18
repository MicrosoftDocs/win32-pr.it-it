---
description: Progettato per impostare le informazioni sui parametri specificati.
ms.assetid: e1a5766f-a303-47f1-a4bb-33f4253a5464
title: 'Metodo IPStore:: GetProvParam (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.GetProvParam
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: ac45c08f64658d176449d76456e737a1a37dc2b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324801"
---
# <a name="ipstoregetprovparam-method"></a><span data-ttu-id="97659-103">Metodo IPStore:: GetProvParam</span><span class="sxs-lookup"><span data-stu-id="97659-103">IPStore::GetProvParam method</span></span>

<span data-ttu-id="97659-104">\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="97659-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="97659-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="97659-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="97659-106">PStore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="97659-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="97659-107">Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="97659-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="97659-108">\[Questo metodo non è implementato.\]</span><span class="sxs-lookup"><span data-stu-id="97659-108">\[This method is not implemented.\]</span></span>

<span data-ttu-id="97659-109">Progettato per impostare le informazioni sui parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="97659-109">Intended to set the specified parameter information.</span></span> <span data-ttu-id="97659-110">Si noti, tuttavia, che non è implementato e avrà sempre esito negativo.</span><span class="sxs-lookup"><span data-stu-id="97659-110">Note, however, that it is not implemented and will always fail.</span></span>

## <a name="syntax"></a><span data-ttu-id="97659-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="97659-111">Syntax</span></span>


```C++
HRESULT GetProvParam(
  [in]  DWORD dwParam,
  [out] DWORD *pcbData,
  [out] BYTE  **ppbData,
  [in]  DWORD dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="97659-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="97659-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97659-113">*dwParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97659-113">*dwParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97659-114">Riservato.</span><span class="sxs-lookup"><span data-stu-id="97659-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="97659-115">*pcbData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="97659-115">*pcbData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97659-116">Riservato.</span><span class="sxs-lookup"><span data-stu-id="97659-116">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="97659-117">*ppbData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="97659-117">*ppbData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97659-118">Riservato.</span><span class="sxs-lookup"><span data-stu-id="97659-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="97659-119">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97659-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97659-120">Riservato.</span><span class="sxs-lookup"><span data-stu-id="97659-120">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97659-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="97659-121">Return value</span></span>

<span data-ttu-id="97659-122">Le chiamate a questo metodo avranno sempre esito negativo.</span><span class="sxs-lookup"><span data-stu-id="97659-122">Calls to this method will always fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="97659-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="97659-123">Requirements</span></span>



| <span data-ttu-id="97659-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="97659-124">Requirement</span></span> | <span data-ttu-id="97659-125">Valore</span><span class="sxs-lookup"><span data-stu-id="97659-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="97659-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="97659-126">Header</span></span><br/> | <dl> <span data-ttu-id="97659-127"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="97659-127"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="97659-128">DLL</span><span class="sxs-lookup"><span data-stu-id="97659-128">DLL</span></span><br/>    | <dl> <span data-ttu-id="97659-129"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97659-129"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97659-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="97659-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97659-131">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="97659-131">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
