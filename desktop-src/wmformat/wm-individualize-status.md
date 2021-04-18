---
title: Struttura WM_INDIVIDUALIZE_STATUS (Drmexternals. h)
description: La \_ \_ struttura dello stato di personalizzazione di WM registra lo stato del processo di individualizzazione.
ms.assetid: 3779ed6f-c133-4a9d-b60c-ef8c41fcc4af
keywords:
- Formato di Windows Media per la struttura WM_INDIVIDUALIZE_STATUS
topic_type:
- apiref
api_name:
- WM_INDIVIDUALIZE_STATUS
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddec51fbdfecd407a68b3e168a82af449decce6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302060"
---
# <a name="wm_individualize_status-structure-drmexternalsh"></a><span data-ttu-id="5d211-104">Struttura WM_INDIVIDUALIZE_STATUS (Drmexternals. h)</span><span class="sxs-lookup"><span data-stu-id="5d211-104">WM_INDIVIDUALIZE_STATUS structure (Drmexternals.h)</span></span>

<span data-ttu-id="5d211-105">La **struttura \_ \_ dello stato di personalizzazione di WM** registra lo stato del processo di [*individualizzazione*](wmformat-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="5d211-105">The **WM\_INDIVIDUALIZE\_STATUS** structure records the status of the [*individualization*](wmformat-glossary.md) process.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d211-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5d211-106">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="5d211-107">Members</span><span class="sxs-lookup"><span data-stu-id="5d211-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="5d211-108">**h**</span><span class="sxs-lookup"><span data-stu-id="5d211-108">**hr**</span></span>
</dt> <dd>

<span data-ttu-id="5d211-109">Codice restituito **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5d211-109">**HRESULT** return code.</span></span>

</dd> <dt>

<span data-ttu-id="5d211-110">**enIndiStatus**</span><span class="sxs-lookup"><span data-stu-id="5d211-110">**enIndiStatus**</span></span>
</dt> <dd>

<span data-ttu-id="5d211-111">Valore del tipo di enumerazione [**\_ \_ dello stato di individualizzazione DRM**](drm-individualization-status.md) .</span><span class="sxs-lookup"><span data-stu-id="5d211-111">Value from the [**DRM\_INDIVIDUALIZATION\_STATUS**](drm-individualization-status.md) enumeration type.</span></span>

</dd> <dt>

<span data-ttu-id="5d211-112">**pszIndiRespUrl**</span><span class="sxs-lookup"><span data-stu-id="5d211-112">**pszIndiRespUrl**</span></span>
</dt> <dd>

<span data-ttu-id="5d211-113">Puntatore a una stringa con terminazione null che contiene l'URL di risposta di individualizzazione.</span><span class="sxs-lookup"><span data-stu-id="5d211-113">Pointer to a null-terminated string containing the individualization response URL.</span></span>

</dd> <dt>

<span data-ttu-id="5d211-114">**dwHTTPRequest**</span><span class="sxs-lookup"><span data-stu-id="5d211-114">**dwHTTPRequest**</span></span>
</dt> <dd>

<span data-ttu-id="5d211-115">**DWORD** che indica il numero di round trip HTTP al servizio di individualizzazione che sono stati completati.</span><span class="sxs-lookup"><span data-stu-id="5d211-115">**DWORD** that indicates the number of HTTP round trips to the individualization service that have been completed..</span></span>

</dd> <dt>

<span data-ttu-id="5d211-116">**enHTTPStatus**</span><span class="sxs-lookup"><span data-stu-id="5d211-116">**enHTTPStatus**</span></span>
</dt> <dd>

<span data-ttu-id="5d211-117">Valore del tipo di enumerazione [**\_ \_ dello stato http DRM**](drm-http-status.md) .</span><span class="sxs-lookup"><span data-stu-id="5d211-117">Value from the [**DRM\_HTTP\_STATUS**](drm-http-status.md) enumeration type.</span></span>

</dd> <dt>

<span data-ttu-id="5d211-118">**dwHTTPReadProgress**</span><span class="sxs-lookup"><span data-stu-id="5d211-118">**dwHTTPReadProgress**</span></span>
</dt> <dd>

<span data-ttu-id="5d211-119">**DWORD** contenente il numero di byte scaricati finora...</span><span class="sxs-lookup"><span data-stu-id="5d211-119">**DWORD** containing the number of bytes downloaded until now..</span></span>

</dd> <dt>

<span data-ttu-id="5d211-120">**dwHTTPReadTotal**</span><span class="sxs-lookup"><span data-stu-id="5d211-120">**dwHTTPReadTotal**</span></span>
</dt> <dd>

<span data-ttu-id="5d211-121">**DWORD** contenente il numero totale di byte da scaricare.</span><span class="sxs-lookup"><span data-stu-id="5d211-121">**DWORD** containing the total number of bytes to be downloaded.</span></span> <span data-ttu-id="5d211-122">Usare questo valore e **dwHTTPReadProgress** per visualizzare un'interfaccia utente che indica la quantità di download completata e la quantità di operazioni da eseguire.</span><span class="sxs-lookup"><span data-stu-id="5d211-122">Use this value and **dwHTTPReadProgress** to display a user interface indicating how much of the download has completed and how much remains to be done.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5d211-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="5d211-123">Remarks</span></span>

<span data-ttu-id="5d211-124">Questa struttura viene compilata dai componenti della fase di esecuzione di DRM e viene inviata alle applicazioni nel parametro *pValue* del metodo [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) di applicazioni quando l'evento è uguale a WMT \_ .</span><span class="sxs-lookup"><span data-stu-id="5d211-124">This structure is filled in by the DRM run-time components and is sent to applications in the *pValue* parameter of the applications [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method when the event equals WMT\_INDIVIDUALIZE.</span></span> <span data-ttu-id="5d211-125">L'applicazione riceve questo evento più volte durante il processo di download.</span><span class="sxs-lookup"><span data-stu-id="5d211-125">The application receives this event multiple times during the download process.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d211-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5d211-126">Requirements</span></span>



| <span data-ttu-id="5d211-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d211-127">Requirement</span></span> | <span data-ttu-id="5d211-128">Valore</span><span class="sxs-lookup"><span data-stu-id="5d211-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d211-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5d211-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5d211-130">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5d211-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5d211-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5d211-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5d211-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5d211-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="5d211-133">Versione</span><span class="sxs-lookup"><span data-stu-id="5d211-133">Version</span></span><br/>                  | <span data-ttu-id="5d211-134">Windows Media Format 7 SDK o versioni successive dell'SDK</span><span class="sxs-lookup"><span data-stu-id="5d211-134">Windows Media Format 7 SDK, or later versions of the SDK</span></span><br/>                       |
| <span data-ttu-id="5d211-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5d211-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d211-136"><dt>Drmexternals. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d211-136"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d211-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5d211-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d211-138">**\_stato http \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="5d211-138">**DRM\_HTTP\_STATUS**</span></span>](drm-http-status.md)
</dt> <dt>

[<span data-ttu-id="5d211-139">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="5d211-139">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





