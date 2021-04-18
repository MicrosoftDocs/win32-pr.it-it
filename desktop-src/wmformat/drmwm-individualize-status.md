---
title: Struttura WM_INDIVIDUALIZE_STATUS (wmdrmsdk. h)
description: La \_ \_ struttura dello stato di personalizzazione di WM include informazioni su un processo di individualizzazione in sospeso.
ms.assetid: af7e8758-489b-461f-b241-d7e40c8d61da
keywords:
- Formato di Windows Media per la struttura WM_INDIVIDUALIZE_STATUS
topic_type:
- apiref
api_name:
- WM_INDIVIDUALIZE_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef7617fe6dcddf3397ab1a123132e843f0b1461
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328106"
---
# <a name="wm_individualize_status-structure-wmdrmsdkh"></a><span data-ttu-id="15eca-104">Struttura WM_INDIVIDUALIZE_STATUS (wmdrmsdk. h)</span><span class="sxs-lookup"><span data-stu-id="15eca-104">WM_INDIVIDUALIZE_STATUS structure (Wmdrmsdk.h)</span></span>

<span data-ttu-id="15eca-105">La **struttura \_ \_ dello stato di personalizzazione di WM** include informazioni su un processo di individualizzazione in sospeso.</span><span class="sxs-lookup"><span data-stu-id="15eca-105">The **WM\_INDIVIDUALIZE\_STATUS** structure holds information about a pending individualization process.</span></span>

## <a name="syntax"></a><span data-ttu-id="15eca-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="15eca-106">Syntax</span></span>


```C++
typedef struct _WMIndividualizeStatus {
  HRESULT                      hr;
  DRM_INDIVIDUALIZATION_STATUS enIndiStatus;
  LPSTR                        pszIndiRespUrl;
  DWORD                        dwHTTPRequest;
  DRM_HTTP_STATUS              enHTTPStatus;
  DWORD                        dwHTTPReadProgress;
  DWORD                        dwHTTPReadTotal;
} WM_INDIVIDUALIZE_STATUS;
```



## <a name="members"></a><span data-ttu-id="15eca-107">Members</span><span class="sxs-lookup"><span data-stu-id="15eca-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="15eca-108">**h**</span><span class="sxs-lookup"><span data-stu-id="15eca-108">**hr**</span></span>
</dt> <dd>

<span data-ttu-id="15eca-109">Codice restituito **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="15eca-109">**HRESULT** return code.</span></span>

</dd> <dt>

<span data-ttu-id="15eca-110">**enIndiStatus**</span><span class="sxs-lookup"><span data-stu-id="15eca-110">**enIndiStatus**</span></span>
</dt> <dd>

<span data-ttu-id="15eca-111">Valore del tipo di enumerazione [**\_ \_ dello stato di individualizzazione DRM**](drmdrm-individualization-status.md) che indica lo stato corrente del processo di individualizzazione.</span><span class="sxs-lookup"><span data-stu-id="15eca-111">Value from the [**DRM\_INDIVIDUALIZATION\_STATUS**](drmdrm-individualization-status.md) enumeration type that indicates the current status of the individualization process.</span></span>

</dd> <dt>

<span data-ttu-id="15eca-112">**pszIndiRespUrl**</span><span class="sxs-lookup"><span data-stu-id="15eca-112">**pszIndiRespUrl**</span></span>
</dt> <dd>

<span data-ttu-id="15eca-113">Puntatore a una stringa con terminazione null che contiene l'URL di risposta di individualizzazione.</span><span class="sxs-lookup"><span data-stu-id="15eca-113">Pointer to a null-terminated string containing the individualization response URL.</span></span>

</dd> <dt>

<span data-ttu-id="15eca-114">**dwHTTPRequest**</span><span class="sxs-lookup"><span data-stu-id="15eca-114">**dwHTTPRequest**</span></span>
</dt> <dd>

<span data-ttu-id="15eca-115">Numero di round trip HTTP al servizio di individualizzazione che sono stati completati.</span><span class="sxs-lookup"><span data-stu-id="15eca-115">The number of HTTP round trips to the individualization service that have been completed.</span></span>

</dd> <dt>

<span data-ttu-id="15eca-116">**enHTTPStatus**</span><span class="sxs-lookup"><span data-stu-id="15eca-116">**enHTTPStatus**</span></span>
</dt> <dd>

<span data-ttu-id="15eca-117">Valore del tipo di enumerazione [**\_ \_ dello stato http DRM**](drmdrm-http-status.md) .</span><span class="sxs-lookup"><span data-stu-id="15eca-117">Value from the [**DRM\_HTTP\_STATUS**](drmdrm-http-status.md) enumeration type.</span></span>

</dd> <dt>

<span data-ttu-id="15eca-118">**dwHTTPReadProgress**</span><span class="sxs-lookup"><span data-stu-id="15eca-118">**dwHTTPReadProgress**</span></span>
</dt> <dd>

<span data-ttu-id="15eca-119">Numero di byte scaricati.</span><span class="sxs-lookup"><span data-stu-id="15eca-119">The number of bytes downloaded.</span></span>

</dd> <dt>

<span data-ttu-id="15eca-120">**dwHTTPReadTotal**</span><span class="sxs-lookup"><span data-stu-id="15eca-120">**dwHTTPReadTotal**</span></span>
</dt> <dd>

<span data-ttu-id="15eca-121">Numero totale di byte da scaricare.</span><span class="sxs-lookup"><span data-stu-id="15eca-121">The total number of bytes to be downloaded.</span></span> <span data-ttu-id="15eca-122">È possibile utilizzare questo valore e **dwHTTPReadProgress** per visualizzare un'interfaccia utente che indica la quantità di download completata e la quantità di operazioni da eseguire.</span><span class="sxs-lookup"><span data-stu-id="15eca-122">You can use this value and **dwHTTPReadProgress** to display a user interface indicating how much of the download has completed and how much remains to be done.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="15eca-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="15eca-123">Remarks</span></span>

<span data-ttu-id="15eca-124">Questa struttura viene ricevuta quando si chiama il metodo [**IWMDRMIndividualizationStatus:: GetStatus**](iwmdrmindividualizationstatus-getstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="15eca-124">This structure is received when you call the [**IWMDRMIndividualizationStatus::GetStatus**](iwmdrmindividualizationstatus-getstatus.md) method.</span></span> <span data-ttu-id="15eca-125">Contiene lo stato del processo di individualizzazione in sospeso al momento della chiamata.</span><span class="sxs-lookup"><span data-stu-id="15eca-125">It contains the status of the pending individualization process at the time of the call.</span></span>

## <a name="requirements"></a><span data-ttu-id="15eca-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15eca-126">Requirements</span></span>



| <span data-ttu-id="15eca-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="15eca-127">Requirement</span></span> | <span data-ttu-id="15eca-128">Valore</span><span class="sxs-lookup"><span data-stu-id="15eca-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="15eca-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="15eca-129">Header</span></span><br/> | <dl> <span data-ttu-id="15eca-130"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="15eca-130"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15eca-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15eca-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15eca-132">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="15eca-132">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





