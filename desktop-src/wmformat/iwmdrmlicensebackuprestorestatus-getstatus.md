---
title: Metodo GetStatus di IWMDRMLicenseBackupRestoreStatus (wmdrmsdk. h)
description: Il metodo GetStatus recupera informazioni dettagliate sullo stato di un'operazione di backup o ripristino delle licenze.
ms.assetid: 1a695baf-0971-4dbf-90fa-1b10178a3348
keywords:
- Metodo GetStatus formato Windows Media
- Metodo GetStatus formato Windows Media, interfaccia IWMDRMLicenseBackupRestoreStatus
- Interfaccia IWMDRMLicenseBackupRestoreStatus-formato Windows Media, metodo GetStatus
topic_type:
- apiref
api_name:
- IWMDRMLicenseBackupRestoreStatus.GetStatus
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3373e71bcae9dc1054e97e8b758ac72389b9a712
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332375"
---
# <a name="iwmdrmlicensebackuprestorestatusgetstatus-method"></a><span data-ttu-id="3248f-106">Metodo IWMDRMLicenseBackupRestoreStatus:: GetStatus</span><span class="sxs-lookup"><span data-stu-id="3248f-106">IWMDRMLicenseBackupRestoreStatus::GetStatus method</span></span>

<span data-ttu-id="3248f-107">Il metodo **GetStatus** recupera informazioni dettagliate sullo stato di un'operazione di backup o ripristino delle licenze.</span><span class="sxs-lookup"><span data-stu-id="3248f-107">The **GetStatus** method retrieves detailed status information about a license backup or restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="3248f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3248f-108">Syntax</span></span>


```C++
HRESULT GetStatus(
  [out] WM_BACKUP_RESTORE_STATUS *pStatus
);
```



## <a name="parameters"></a><span data-ttu-id="3248f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3248f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3248f-110">*pStatus* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3248f-110">*pStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3248f-111">Puntatore a una struttura di [**\_ stato di \_ ripristino \_ del backup WM**](wm-backup-restore-status.md) che riceve le informazioni sullo stato.</span><span class="sxs-lookup"><span data-stu-id="3248f-111">Pointer to a [**WM\_BACKUP\_RESTORE\_STATUS**](wm-backup-restore-status.md) structure that receives the status information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3248f-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3248f-112">Return value</span></span>

<span data-ttu-id="3248f-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3248f-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3248f-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="3248f-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3248f-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3248f-115">Return code</span></span>                                                                          | <span data-ttu-id="3248f-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3248f-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="3248f-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3248f-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="3248f-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="3248f-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3248f-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="3248f-119">Remarks</span></span>

<span data-ttu-id="3248f-120">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="3248f-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="3248f-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3248f-121">Requirements</span></span>



| <span data-ttu-id="3248f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3248f-122">Requirement</span></span> | <span data-ttu-id="3248f-123">Valore</span><span class="sxs-lookup"><span data-stu-id="3248f-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3248f-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3248f-124">Header</span></span><br/>  | <dl> <span data-ttu-id="3248f-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="3248f-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="3248f-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="3248f-126">Library</span></span><br/> | <dl> <span data-ttu-id="3248f-127"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3248f-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3248f-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3248f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3248f-129">**Interfaccia IWMDRMLicenseBackupRestoreStatus**</span><span class="sxs-lookup"><span data-stu-id="3248f-129">**IWMDRMLicenseBackupRestoreStatus Interface**</span></span>](iwmdrmlicensebackuprestorestatus.md)
</dt> </dl>

 

 





