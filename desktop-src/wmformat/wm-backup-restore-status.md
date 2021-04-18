---
title: Struttura WM_BACKUP_RESTORE_STATUS (wmdrmsdk. h)
description: La \_ \_ struttura dello stato di ripristino del backup WM \_ include informazioni su un'operazione di backup o ripristino delle licenze in sospeso.
ms.assetid: 74e94bc6-376b-4848-a9f9-11c9cb4005f2
keywords:
- Formato di Windows Media per la struttura WM_BACKUP_RESTORE_STATUS
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- WM_BACKUP_RESTORE_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 476cd4ddab42ec9f8f44ff51b492bd3913824cf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331298"
---
# <a name="wm_backup_restore_status-structure"></a><span data-ttu-id="61768-105">\_Struttura di \_ Stato ripristino backup \_ WM</span><span class="sxs-lookup"><span data-stu-id="61768-105">WM\_BACKUP\_RESTORE\_STATUS structure</span></span>

<span data-ttu-id="61768-106">La **struttura \_ \_ \_ dello stato di ripristino del backup WM** include informazioni su un'operazione di backup o ripristino delle licenze in sospeso.</span><span class="sxs-lookup"><span data-stu-id="61768-106">The **WM\_BACKUP\_RESTORE\_STATUS** structure holds information about a pending license backup or restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="61768-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="61768-107">Syntax</span></span>


```C++
typedef struct WM_BACKUP_RESTORE_STATUS {
  MSDRM_STATUS eStatus;
  BSTR         bstrError;
} ;
```



## <a name="members"></a><span data-ttu-id="61768-108">Members</span><span class="sxs-lookup"><span data-stu-id="61768-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="61768-109">**eStatus**</span><span class="sxs-lookup"><span data-stu-id="61768-109">**eStatus**</span></span>
</dt> <dd>

<span data-ttu-id="61768-110">Membro dell'enumerazione [**di \_ stato MSDRM**](msdrm-status.md) che specifica lo stato.</span><span class="sxs-lookup"><span data-stu-id="61768-110">Member of the [**MSDRM\_STATUS**](msdrm-status.md) enumeration specifying the status.</span></span>

</dd> <dt>

<span data-ttu-id="61768-111">**bstrError**</span><span class="sxs-lookup"><span data-stu-id="61768-111">**bstrError**</span></span>
</dt> <dd>

<span data-ttu-id="61768-112">Stringa contenente l'errore.</span><span class="sxs-lookup"><span data-stu-id="61768-112">String containing the error.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="61768-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="61768-113">Remarks</span></span>

<span data-ttu-id="61768-114">Questa struttura viene ricevuta quando si chiama il metodo [**IWMDRMLicenseBackupRestoreStatus:: GetStatus**](iwmdrmlicensebackuprestorestatus-getstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="61768-114">This structure is received when you call the [**IWMDRMLicenseBackupRestoreStatus::GetStatus**](iwmdrmlicensebackuprestorestatus-getstatus.md) method.</span></span> <span data-ttu-id="61768-115">Contiene lo stato dell'operazione di backup o ripristino in sospeso al momento della chiamata.</span><span class="sxs-lookup"><span data-stu-id="61768-115">It contains the status of the pending backup or restore operation at the time of the call.</span></span>

## <a name="requirements"></a><span data-ttu-id="61768-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="61768-116">Requirements</span></span>



| <span data-ttu-id="61768-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="61768-117">Requirement</span></span> | <span data-ttu-id="61768-118">Valore</span><span class="sxs-lookup"><span data-stu-id="61768-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="61768-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="61768-119">Header</span></span><br/> | <dl> <span data-ttu-id="61768-120"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="61768-120"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61768-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="61768-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61768-122">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="61768-122">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





