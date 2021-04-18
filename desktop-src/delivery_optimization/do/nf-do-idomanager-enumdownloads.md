---
title: 'Metodo IDOManager:: EnumDownloads'
description: Recupera un puntatore a interfaccia a un oggetto enumeratore utilizzato per enumerare i download esistenti.
keywords:
- 'Metodo IDOManager:: EnumDownloads'
topic_type:
- apiref
api_name:
- IDOManager.EnumDownloads
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: a1e7fed2955fdc1b5ac0c11cfebc34aa95517603
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "106299303"
---
# <a name="idomanagerenumdownloads-method"></a><span data-ttu-id="d25c6-104">Metodo IDOManager:: EnumDownloads</span><span class="sxs-lookup"><span data-stu-id="d25c6-104">IDOManager::EnumDownloads method</span></span>

<span data-ttu-id="d25c6-105">Recupera un puntatore a interfaccia a un oggetto enumeratore utilizzato per enumerare i download esistenti.</span><span class="sxs-lookup"><span data-stu-id="d25c6-105">Retrieves an interface pointer to an enumerator object that is used to enumerate existing downloads.</span></span>

## <a name="syntax"></a><span data-ttu-id="d25c6-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d25c6-106">Syntax</span></span>

```cpp
HRESULT EnumDownloads(
  DO_DOWNLOAD_ENUM_CATEGORY *category, 
  IEnumUnknown **ppEnum
);
```

## <a name="parameters"></a><span data-ttu-id="d25c6-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="d25c6-107">Parameters</span></span>

`category`

<span data-ttu-id="d25c6-108">Facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d25c6-108">Optional.</span></span> <span data-ttu-id="d25c6-109">Nome della proprietà da utilizzare come categoria da enumerare.</span><span class="sxs-lookup"><span data-stu-id="d25c6-109">The property name to be used as a category to enumerate.</span></span> <span data-ttu-id="d25c6-110">Se `nullptr` si passa, vengono recuperati tutti i download esistenti.</span><span class="sxs-lookup"><span data-stu-id="d25c6-110">Passing `nullptr` will retrieve all existing downloads.</span></span> <span data-ttu-id="d25c6-111">Le proprietà seguenti sono supportate come una categoria.</span><span class="sxs-lookup"><span data-stu-id="d25c6-111">The following properties are supported as a category.</span></span>

- <span data-ttu-id="d25c6-112">**DODownloadProperty_Id**</span><span class="sxs-lookup"><span data-stu-id="d25c6-112">**DODownloadProperty_Id**</span></span>
- <span data-ttu-id="d25c6-113">**DODownloadProperty_Uri**</span><span class="sxs-lookup"><span data-stu-id="d25c6-113">**DODownloadProperty_Uri**</span></span>
- <span data-ttu-id="d25c6-114">**DODownloadProperty_ContentId**</span><span class="sxs-lookup"><span data-stu-id="d25c6-114">**DODownloadProperty_ContentId**</span></span>
- <span data-ttu-id="d25c6-115">**DODownloadProperty_DisplayName**</span><span class="sxs-lookup"><span data-stu-id="d25c6-115">**DODownloadProperty_DisplayName**</span></span>
- <span data-ttu-id="d25c6-116">**DODownloadProperty_LocalPath**</span><span class="sxs-lookup"><span data-stu-id="d25c6-116">**DODownloadProperty_LocalPath**</span></span>

`ppEnum`

<span data-ttu-id="d25c6-117">Indirizzo di un puntatore a interfaccia per **IEnumUnknown**, che viene usato per enumerare i download esistenti.</span><span class="sxs-lookup"><span data-stu-id="d25c6-117">The address of an interface pointer to **IEnumUnknown**, which is used to enumerate existing downloads.</span></span> <span data-ttu-id="d25c6-118">Il contenuto dell'enumeratore dipende dal valore della *categoria*.</span><span class="sxs-lookup"><span data-stu-id="d25c6-118">The contents of the enumerator depend on the value of *category*.</span></span> <span data-ttu-id="d25c6-119">I download inclusi nell'interfaccia di enumerazione sono quelli creati in precedenza dallo stesso chiamante per questa funzione.</span><span class="sxs-lookup"><span data-stu-id="d25c6-119">The downloads included in the enumeration interface are the ones that were previously created by the same caller to this function.</span></span> 

## <a name="return-value"></a><span data-ttu-id="d25c6-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d25c6-120">Return Value</span></span>

<span data-ttu-id="d25c6-121">Se la funzione ha esito positivo, restituisce **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="d25c6-121">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="d25c6-122">In caso contrario, restituisce un [codice di errore](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .</span><span class="sxs-lookup"><span data-stu-id="d25c6-122">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="d25c6-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d25c6-123">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="d25c6-124">**Client minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="d25c6-124">**Minimum supported client**</span></span> | <span data-ttu-id="d25c6-125">Solo applicazioni Win32 Windows 10 versione 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="d25c6-125">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="d25c6-126">**Server minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="d25c6-126">**Minimum supported server**</span></span> | <span data-ttu-id="d25c6-127">Windows Server, \[ solo applicazioni Win32 versione 1809\]</span><span class="sxs-lookup"><span data-stu-id="d25c6-127">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="d25c6-128">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="d25c6-128">**Header**</span></span> | <span data-ttu-id="d25c6-129">Do. h</span><span class="sxs-lookup"><span data-stu-id="d25c6-129">Do.h</span></span> |
