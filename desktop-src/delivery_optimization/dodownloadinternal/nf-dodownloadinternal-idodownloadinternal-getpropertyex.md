---
title: 'Metodo IDODownloadInternal:: GetPropertyEx'
description: Recupera un puntatore a un **Variant** che contiene un valore di proprietà di download esteso specifico.
keywords:
- 'Metodo IDODownloadInternal:: GetPropertyEx'
topic_type:
- apiref
api_name:
- IDODownloadInternal.GetPropertyEx
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: 908f9b15df5c0c4a2769149419ff12d545201e5c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399285"
---
# <a name="idodownloadinternalgetpropertyex-method"></a><span data-ttu-id="934a5-104">Metodo IDODownloadInternal:: GetPropertyEx</span><span class="sxs-lookup"><span data-stu-id="934a5-104">IDODownloadInternal::GetPropertyEx method</span></span>

> [!IMPORTANT]
> <span data-ttu-id="934a5-105">L'interfaccia **IDODownloadInternal** è deprecata.</span><span class="sxs-lookup"><span data-stu-id="934a5-105">The **IDODownloadInternal** interface is deprecated.</span></span> <span data-ttu-id="934a5-106">Usare invece l'interfaccia [IDODownload](../do/nn-do-idodownload.md) .</span><span class="sxs-lookup"><span data-stu-id="934a5-106">Instead, use the [IDODownload](../do/nn-do-idodownload.md) interface.</span></span>

<span data-ttu-id="934a5-107">Recupera un puntatore a un **Variant** che contiene un valore di proprietà di download esteso specifico.</span><span class="sxs-lookup"><span data-stu-id="934a5-107">Retrieves a pointer to a **VARIANT** that contains a specific extended download property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="934a5-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="934a5-108">Syntax</span></span>

```cpp
HRESULT GetPropertyEx(
  DODownloadPropertyEx propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a><span data-ttu-id="934a5-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="934a5-109">Parameters</span></span>

`propId`

<span data-ttu-id="934a5-110">ID di proprietà obbligatorio da ottenere (di tipo **DODownloadPropertyEx**).</span><span class="sxs-lookup"><span data-stu-id="934a5-110">The required property ID to get (of type **DODownloadPropertyEx**).</span></span>

`propVal`

<span data-ttu-id="934a5-111">Il valore della proprietà risultante, archiviato in una **variante**.</span><span class="sxs-lookup"><span data-stu-id="934a5-111">The resulting property value, stored in a **VARIANT**.</span></span>

## <a name="return-value"></a><span data-ttu-id="934a5-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="934a5-112">Return Value</span></span>

<span data-ttu-id="934a5-113">Se la funzione ha esito positivo, restituisce **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="934a5-113">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="934a5-114">In caso contrario, restituisce un [codice di errore](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .</span><span class="sxs-lookup"><span data-stu-id="934a5-114">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

|<span data-ttu-id="934a5-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="934a5-115">Return value</span></span>|<span data-ttu-id="934a5-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="934a5-116">Description</span></span>|
|-|-|
|<span data-ttu-id="934a5-117">DO_E_UNKNOWN_PROPERTY_ID</span><span class="sxs-lookup"><span data-stu-id="934a5-117">DO_E_UNKNOWN_PROPERTY_ID</span></span>|<span data-ttu-id="934a5-118">*propid* è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="934a5-118">*propId* is unknown.</span></span>|
|<span data-ttu-id="934a5-119">DO_E_WRITE_ONLY_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="934a5-119">DO_E_WRITE_ONLY_PROPERTY</span></span>|<span data-ttu-id="934a5-120">La proprietà è di sola scrittura e non può essere letta.</span><span class="sxs-lookup"><span data-stu-id="934a5-120">The property is write-only, and cannot be read.</span></span>|
|<span data-ttu-id="934a5-121">E_NOT_SET</span><span class="sxs-lookup"><span data-stu-id="934a5-121">E_NOT_SET</span></span>|<span data-ttu-id="934a5-122">Questa proprietà non è stata impostata tramite **SetPropertyEx**.</span><span class="sxs-lookup"><span data-stu-id="934a5-122">No such property was set via **SetPropertyEx**.</span></span>|

## <a name="requirements"></a><span data-ttu-id="934a5-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="934a5-123">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="934a5-124">**Client minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="934a5-124">**Minimum supported client**</span></span> | <span data-ttu-id="934a5-125">Solo applicazioni Win32 Windows 10 versione 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="934a5-125">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="934a5-126">**Server minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="934a5-126">**Minimum supported server**</span></span> | <span data-ttu-id="934a5-127">Windows Server, \[ solo applicazioni Win32 versione 1809\]</span><span class="sxs-lookup"><span data-stu-id="934a5-127">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="934a5-128">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="934a5-128">**Header**</span></span> | <span data-ttu-id="934a5-129">DODownloadInternal. h</span><span class="sxs-lookup"><span data-stu-id="934a5-129">DODownloadInternal.h</span></span> |