---
title: 'Metodo IDODownloadInternal:: SetPropertyEx'
description: Imposta una proprietà di download estesa. Il metodo accetta un puntatore a una **variante** che contiene un valore della proprietà specifico da applicare al download.
keywords:
- 'Metodo IDODownloadInternal:: SetPropertyEx'
topic_type:
- apiref
api_name:
- IDODownloadInternal.SetPropertyEx
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: e6630cc3e767531dd94da39fe73d88284c9ca0d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963132"
---
# <a name="idodownloadinternalsetpropertyex-method"></a><span data-ttu-id="4d052-105">Metodo IDODownloadInternal:: SetPropertyEx</span><span class="sxs-lookup"><span data-stu-id="4d052-105">IDODownloadInternal::SetPropertyEx method</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4d052-106">L'interfaccia **IDODownloadInternal** è deprecata.</span><span class="sxs-lookup"><span data-stu-id="4d052-106">The **IDODownloadInternal** interface is deprecated.</span></span> <span data-ttu-id="4d052-107">Usare invece l'interfaccia [IDODownload](../do/nn-do-idodownload.md) .</span><span class="sxs-lookup"><span data-stu-id="4d052-107">Instead, use the [IDODownload](../do/nn-do-idodownload.md) interface.</span></span>

<span data-ttu-id="4d052-108">Imposta una proprietà di download estesa.</span><span class="sxs-lookup"><span data-stu-id="4d052-108">Sets an extended download property.</span></span> <span data-ttu-id="4d052-109">Il metodo accetta un puntatore a una **variante** che contiene un valore della proprietà specifico da applicare al download.</span><span class="sxs-lookup"><span data-stu-id="4d052-109">The method accepts a pointer to a **VARIANT** that contains a specific property value to apply to the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d052-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4d052-110">Syntax</span></span>

```cpp
HRESULT SetPropertyEx(
  DODownloadPropertyEx propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a><span data-ttu-id="4d052-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="4d052-111">Parameters</span></span>

`propId`

<span data-ttu-id="4d052-112">ID di proprietà obbligatorio da impostare (di tipo **DODownloadPropertyEx**).</span><span class="sxs-lookup"><span data-stu-id="4d052-112">The required property ID to set (of type **DODownloadPropertyEx**).</span></span>

`propVal`

<span data-ttu-id="4d052-113">Valore della proprietà da impostare, archiviato in una **variante**.</span><span class="sxs-lookup"><span data-stu-id="4d052-113">The property value to set, stored in a **VARIANT**.</span></span>

## <a name="return-value"></a><span data-ttu-id="4d052-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4d052-114">Return Value</span></span>

<span data-ttu-id="4d052-115">Se la funzione ha esito positivo, restituisce **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="4d052-115">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="4d052-116">In caso contrario, restituisce un [codice di errore](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .</span><span class="sxs-lookup"><span data-stu-id="4d052-116">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

|<span data-ttu-id="4d052-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4d052-117">Return value</span></span>|<span data-ttu-id="4d052-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d052-118">Description</span></span>|
|-|-|
|<span data-ttu-id="4d052-119">DO_E_UNKNOWN_PROPERTY_ID</span><span class="sxs-lookup"><span data-stu-id="4d052-119">DO_E_UNKNOWN_PROPERTY_ID</span></span>|<span data-ttu-id="4d052-120">*propid* è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="4d052-120">*propId* is unknown.</span></span>|
|<span data-ttu-id="4d052-121">DO_E_INVALID_STATE</span><span class="sxs-lookup"><span data-stu-id="4d052-121">DO_E_INVALID_STATE</span></span>|<span data-ttu-id="4d052-122">Il download non è attualmente in uno stato che consente di impostare le proprietà.</span><span class="sxs-lookup"><span data-stu-id="4d052-122">The download is not currently in a state that allows setting properties.</span></span>|

## <a name="requirements"></a><span data-ttu-id="4d052-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4d052-123">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="4d052-124">**Client minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="4d052-124">**Minimum supported client**</span></span> | <span data-ttu-id="4d052-125">Solo applicazioni Win32 Windows 10 versione 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="4d052-125">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="4d052-126">**Server minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="4d052-126">**Minimum supported server**</span></span> | <span data-ttu-id="4d052-127">Windows Server, \[ solo applicazioni Win32 versione 1809\]</span><span class="sxs-lookup"><span data-stu-id="4d052-127">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="4d052-128">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="4d052-128">**Header**</span></span> | <span data-ttu-id="4d052-129">DODownloadInternal. h</span><span class="sxs-lookup"><span data-stu-id="4d052-129">DODownloadInternal.h</span></span> |