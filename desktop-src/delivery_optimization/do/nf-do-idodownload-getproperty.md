---
title: 'Metodo IDODownload:: GetProperty'
description: Recupera un puntatore a un **Variant** che contiene una specifica proprietà di download.
keywords:
- 'Metodo IDODownload:: GetProperty'
topic_type:
- apiref
api_name:
- IDODownload.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: e734f109e596663ee699c764ca85f1ee45ad7947
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "103857846"
---
# <a name="idodownloadgetproperty-method"></a><span data-ttu-id="4a870-104">Metodo IDODownload:: GetProperty</span><span class="sxs-lookup"><span data-stu-id="4a870-104">IDODownload::GetProperty method</span></span>

<span data-ttu-id="4a870-105">Recupera un puntatore a un **Variant** che contiene una specifica proprietà di download.</span><span class="sxs-lookup"><span data-stu-id="4a870-105">Retrieves a pointer to a **VARIANT** that contains a specific download property.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a870-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4a870-106">Syntax</span></span>

```cpp
HRESULT GetProperty(
  DODownloadProperty propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a><span data-ttu-id="4a870-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="4a870-107">Parameters</span></span>

`propId`

<span data-ttu-id="4a870-108">ID di proprietà obbligatorio da ottenere (di tipo **DODownloadProperty**).</span><span class="sxs-lookup"><span data-stu-id="4a870-108">The required property ID to get (of type **DODownloadProperty**).</span></span>

`propVal`

<span data-ttu-id="4a870-109">Il valore della proprietà risultante, archiviato in una **variante**.</span><span class="sxs-lookup"><span data-stu-id="4a870-109">The resulting property value, stored in a **VARIANT**.</span></span>

## <a name="return-value"></a><span data-ttu-id="4a870-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4a870-110">Return Value</span></span>

<span data-ttu-id="4a870-111">Se la funzione ha esito positivo, restituisce **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="4a870-111">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="4a870-112">In caso contrario, restituisce un [codice di errore](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .</span><span class="sxs-lookup"><span data-stu-id="4a870-112">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

|<span data-ttu-id="4a870-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4a870-113">Return value</span></span>|<span data-ttu-id="4a870-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4a870-114">Description</span></span>|
|-|-|
|<span data-ttu-id="4a870-115">DO_E_UNKNOWN_PROPERTY_ID</span><span class="sxs-lookup"><span data-stu-id="4a870-115">DO_E_UNKNOWN_PROPERTY_ID</span></span>|<span data-ttu-id="4a870-116">*propid* è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="4a870-116">*propId* is unknown.</span></span>|
|<span data-ttu-id="4a870-117">DO_E_WRITE_ONLY_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="4a870-117">DO_E_WRITE_ONLY_PROPERTY</span></span>|<span data-ttu-id="4a870-118">La proprietà è di sola scrittura e non può essere letta.</span><span class="sxs-lookup"><span data-stu-id="4a870-118">The property is write-only, and cannot be read.</span></span>|
|<span data-ttu-id="4a870-119">E_NOT_SET</span><span class="sxs-lookup"><span data-stu-id="4a870-119">E_NOT_SET</span></span>|<span data-ttu-id="4a870-120">Questa proprietà non è stata impostata tramite **SetProperty**.</span><span class="sxs-lookup"><span data-stu-id="4a870-120">No such property was set via **SetProperty**.</span></span>|

## <a name="requirements"></a><span data-ttu-id="4a870-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a870-121">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="4a870-122">**Client minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="4a870-122">**Minimum supported client**</span></span> | <span data-ttu-id="4a870-123">Solo applicazioni Win32 Windows 10 versione 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="4a870-123">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="4a870-124">**Server minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="4a870-124">**Minimum supported server**</span></span> | <span data-ttu-id="4a870-125">Windows Server, \[ solo applicazioni Win32 versione 1809\]</span><span class="sxs-lookup"><span data-stu-id="4a870-125">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="4a870-126">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="4a870-126">**Header**</span></span> | <span data-ttu-id="4a870-127">Do. h</span><span class="sxs-lookup"><span data-stu-id="4a870-127">Do.h</span></span> |
