---
title: 'Metodo IDODownload:: SetProperty'
description: Imposta una proprietà di download.
keywords:
- 'Metodo IDODownload:: SetProperty'
topic_type:
- apiref
api_name:
- IDODownload.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0d496f49851aab665e49f3aaeb51e4b941d6c183
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "103719564"
---
# <a name="idodownloadsetproperty-method"></a><span data-ttu-id="de2f5-104">Metodo IDODownload:: SetProperty</span><span class="sxs-lookup"><span data-stu-id="de2f5-104">IDODownload::SetProperty method</span></span>

<span data-ttu-id="de2f5-105">Imposta una proprietà di download.</span><span class="sxs-lookup"><span data-stu-id="de2f5-105">Sets a download property.</span></span> <span data-ttu-id="de2f5-106">Il metodo accetta un puntatore a una **variante** che contiene una proprietà specifica da applicare al download.</span><span class="sxs-lookup"><span data-stu-id="de2f5-106">The method accepts a pointer to a **VARIANT** that contains a specific property to apply to the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="de2f5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="de2f5-107">Syntax</span></span>

```cpp
HRESULT SetProperty(
  DODownloadProperty propId,
  VARIANT* propVal
);
```

## <a name="parameters"></a><span data-ttu-id="de2f5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="de2f5-108">Parameters</span></span>

`propId`

<span data-ttu-id="de2f5-109">ID di proprietà obbligatorio da impostare (di tipo **DODownloadProperty**).</span><span class="sxs-lookup"><span data-stu-id="de2f5-109">The required property ID to set (of type **DODownloadProperty**).</span></span>

`propVal`

<span data-ttu-id="de2f5-110">Valore della proprietà da impostare, archiviato in una **variante**.</span><span class="sxs-lookup"><span data-stu-id="de2f5-110">The property value to set, stored in a **VARIANT**.</span></span>

## <a name="return-value"></a><span data-ttu-id="de2f5-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="de2f5-111">Return Value</span></span>

<span data-ttu-id="de2f5-112">Se la funzione ha esito positivo, restituisce **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="de2f5-112">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="de2f5-113">In caso contrario, restituisce un [codice di errore](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .</span><span class="sxs-lookup"><span data-stu-id="de2f5-113">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

|<span data-ttu-id="de2f5-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="de2f5-114">Return value</span></span>|<span data-ttu-id="de2f5-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de2f5-115">Description</span></span>|
|-|-|
|<span data-ttu-id="de2f5-116">DO_E_UNKNOWN_PROPERTY_ID</span><span class="sxs-lookup"><span data-stu-id="de2f5-116">DO_E_UNKNOWN_PROPERTY_ID</span></span>|<span data-ttu-id="de2f5-117">*propid* è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="de2f5-117">*propId* is unknown.</span></span>|
|<span data-ttu-id="de2f5-118">DO_E_INVALID_STATE</span><span class="sxs-lookup"><span data-stu-id="de2f5-118">DO_E_INVALID_STATE</span></span>|<span data-ttu-id="de2f5-119">Il download non è attualmente in uno stato che consente di impostare le proprietà.</span><span class="sxs-lookup"><span data-stu-id="de2f5-119">The download is not currently in a state that allows setting properties.</span></span>|

## <a name="requirements"></a><span data-ttu-id="de2f5-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="de2f5-120">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="de2f5-121">**Client minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="de2f5-121">**Minimum supported client**</span></span> | <span data-ttu-id="de2f5-122">Solo applicazioni Win32 Windows 10 versione 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="de2f5-122">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="de2f5-123">**Server minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="de2f5-123">**Minimum supported server**</span></span> | <span data-ttu-id="de2f5-124">Windows Server, \[ solo applicazioni Win32 versione 1809\]</span><span class="sxs-lookup"><span data-stu-id="de2f5-124">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="de2f5-125">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="de2f5-125">**Header**</span></span> | <span data-ttu-id="de2f5-126">Do. h</span><span class="sxs-lookup"><span data-stu-id="de2f5-126">Do.h</span></span> |
