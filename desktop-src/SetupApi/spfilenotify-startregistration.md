---
description: "SPFILENOTIFY_STARTREGISTRATION messaggio: quando si usa la direttiva REGISTERDlls INF per registrare automaticamente le DLL, i chiamanti di SetupInstallFromInfSection possono ricevere notifiche su ogni file durante la registrazione o l'annullamento della registrazione."
ms.assetid: 0faf277c-7805-478f-9cec-0dd7b6acdb0e
title: SPFILENOTIFY_STARTREGISTRATION messaggio (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47e71a884d079515436f296faf515a83a985311e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094499"
---
# <a name="spfilenotify_startregistration-message"></a><span data-ttu-id="12cc5-103">Messaggio SPFILENOTIFY \_ STARTREGISTRATION</span><span class="sxs-lookup"><span data-stu-id="12cc5-103">SPFILENOTIFY\_STARTREGISTRATION message</span></span>

<span data-ttu-id="12cc5-104">Quando si usa la direttiva **REGISTERDlls** INF per registrare automaticamente le DLL, i chiamanti di [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) possono ricevere notifiche in ogni file durante la registrazione o l'annullamento della registrazione.</span><span class="sxs-lookup"><span data-stu-id="12cc5-104">When using the **RegisterDlls** INF directive to self-register DLLs, callers of [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) may receive notifications on each file as it is registered or unregistered.</span></span> <span data-ttu-id="12cc5-105">Per inviare una notifica **SPFILENOTIFY \_ STARTREGISTRATION** alla routine di callback una volta prima di registrare un file, includere SPINST \_ REGISTERCALLBACKAWARE e SPINST REGSVR nel parametro Flags di \_  **SetupInstallFromInfSection**.</span><span class="sxs-lookup"><span data-stu-id="12cc5-105">To send a **SPFILENOTIFY\_STARTREGISTRATION** notification to the callback routine once before registering a file, include SPINST\_REGISTERCALLBACKAWARE plus SPINST\_REGSVR in the *Flags* parameter of **SetupInstallFromInfSection**.</span></span> <span data-ttu-id="12cc5-106">Per inviare una notifica di annullamento della registrazione, includere SPINST \_ REGISTERCALLBACKAWARE e SPINST \_ UNREGSVR nel *parametro Flags.*</span><span class="sxs-lookup"><span data-stu-id="12cc5-106">To send notification of unregistration, include SPINST\_REGISTERCALLBACKAWARE plus SPINST\_UNREGSVR in the *Flags* parameter.</span></span>

<span data-ttu-id="12cc5-107">La routine di callback specificata dal *parametro MsgHandler* [**di SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) deve essere di tipo [PSP FILE \_ \_ CALLBACK](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span><span class="sxs-lookup"><span data-stu-id="12cc5-107">The callback routine specified by the *MsgHandler* parameter of [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) must be the type [PSP\_FILE\_CALLBACK](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span></span> <span data-ttu-id="12cc5-108">Impostare il *parametro Context* sullo stesso *contesto* specificato in **SetupInstallFromInfSection**.</span><span class="sxs-lookup"><span data-stu-id="12cc5-108">Set the *Context* parameter to the same *Context* specified in **SetupInstallFromInfSection**.</span></span> <span data-ttu-id="12cc5-109">Impostare il *parametro Notification* su **SPFILENOTIFY \_ STARTREGISTRATION**.</span><span class="sxs-lookup"><span data-stu-id="12cc5-109">Set the *Notification* parameter to **SPFILENOTIFY\_STARTREGISTRATION**.</span></span>


```C++
SPFILENOTIFY_STARTREGISTRATION
  Param1 = (UINT_PTR) pointer to file information;
  Param2 = (UINT_PTR) file registration or unregistration;
            
```



## <a name="parameters"></a><span data-ttu-id="12cc5-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="12cc5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12cc5-111">*Param1*</span><span class="sxs-lookup"><span data-stu-id="12cc5-111">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="12cc5-112">Puntatore a una [**struttura SP REGISTER CONTROL \_ \_ \_ STATUS**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) contenente informazioni sul file da registrare o annullare la registrazione.</span><span class="sxs-lookup"><span data-stu-id="12cc5-112">Pointer to a [**SP\_REGISTER\_CONTROL\_STATUS**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) structure containing information about the file being registered or unregistered.</span></span> <span data-ttu-id="12cc5-113">Il membro **cbsize** deve essere impostato sulla dimensione della struttura .</span><span class="sxs-lookup"><span data-stu-id="12cc5-113">The member **cbsize** should be set to the size of the structure.</span></span> <span data-ttu-id="12cc5-114">Il **membro FileName** deve essere impostato sul percorso completo del file registrato.</span><span class="sxs-lookup"><span data-stu-id="12cc5-114">The **FileName** member should be set to the fully qualified path of the file being registered.</span></span> <span data-ttu-id="12cc5-115">**Win32Error** non viene usato e deve essere impostato su NO \_ ERROR.</span><span class="sxs-lookup"><span data-stu-id="12cc5-115">**Win32Error** is not used and should be set to NO\_ERROR.</span></span> <span data-ttu-id="12cc5-116">**FailureCode** non viene usato e deve essere impostato su SPREG \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="12cc5-116">**FailureCode** is not used and should be set to SPREG\_SUCCESS.</span></span>

</dd> <dt>

<span data-ttu-id="12cc5-117">*Param2*</span><span class="sxs-lookup"><span data-stu-id="12cc5-117">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="12cc5-118">Se il file viene registrato, *Param2* deve essere impostato su un puntatore a un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="12cc5-118">If the file is being registered, *Param2* should be set to a pointer to a nonzero value.</span></span> <span data-ttu-id="12cc5-119">Se viene annullata la registrazione del file, *Param2* deve essere impostato su un puntatore a zero.</span><span class="sxs-lookup"><span data-stu-id="12cc5-119">If the file is being unregistered, *Param2* should be set to a pointer to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12cc5-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="12cc5-120">Return value</span></span>

<span data-ttu-id="12cc5-121">Dopo aver ricevuto la notifica, la funzione di callback può restituire uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="12cc5-121">After receiving notification, the callback function may return one of the following values.</span></span>



| <span data-ttu-id="12cc5-122">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="12cc5-122">Return code</span></span>                                                                                  | <span data-ttu-id="12cc5-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12cc5-123">Description</span></span>                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="12cc5-124"><dt>**INTERRUZIONE \_ FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="12cc5-124"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="12cc5-125">Non registrare o annullare la registrazione del file e arrestare l'elaborazione della sezione INF.</span><span class="sxs-lookup"><span data-stu-id="12cc5-125">Do not register or unregister the file and stop processing the INF section.</span></span><br/>             |
| <dl> <span data-ttu-id="12cc5-126"><dt>**FILEOP \_ DOIT**</dt></span><span class="sxs-lookup"><span data-stu-id="12cc5-126"><dt>**FILEOP\_DOIT**</dt></span></span> </dl>  | <span data-ttu-id="12cc5-127">Registrare o annullare la registrazione del file e continuare l'elaborazione della sezione INF.</span><span class="sxs-lookup"><span data-stu-id="12cc5-127">Register or unregister the file and continue processing the INF section.</span></span><br/>                |
| <dl> <span data-ttu-id="12cc5-128"><dt>**FILE \_ SKIP**</dt></span><span class="sxs-lookup"><span data-stu-id="12cc5-128"><dt>**FILE\_SKIP**</dt></span></span> </dl>    | <span data-ttu-id="12cc5-129">Ignorare la registrazione o annullare la registrazione del file, ma continuare l'elaborazione della sezione INF</span><span class="sxs-lookup"><span data-stu-id="12cc5-129">Skip registration or unregistration of the file but continue processing the INF section</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="12cc5-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12cc5-130">Requirements</span></span>



| <span data-ttu-id="12cc5-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="12cc5-131">Requirement</span></span> | <span data-ttu-id="12cc5-132">Valore</span><span class="sxs-lookup"><span data-stu-id="12cc5-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="12cc5-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12cc5-133">Minimum supported client</span></span><br/> | <span data-ttu-id="12cc5-134">Solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="12cc5-134">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="12cc5-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12cc5-135">Minimum supported server</span></span><br/> | <span data-ttu-id="12cc5-136">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="12cc5-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="12cc5-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="12cc5-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="12cc5-138"><dt>Setupapi.h</dt></span><span class="sxs-lookup"><span data-stu-id="12cc5-138"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12cc5-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="12cc5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12cc5-140">Panoramica</span><span class="sxs-lookup"><span data-stu-id="12cc5-140">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="12cc5-141">Notifications</span><span class="sxs-lookup"><span data-stu-id="12cc5-141">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="12cc5-142">**SetupInstallFromInfSection**</span><span class="sxs-lookup"><span data-stu-id="12cc5-142">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> <dt>

[<span data-ttu-id="12cc5-143">**SPFILENOTIFY \_ ENDREGISTRATION**</span><span class="sxs-lookup"><span data-stu-id="12cc5-143">**SPFILENOTIFY\_ENDREGISTRATION**</span></span>](spfilenotify-endregistration.md)
</dt> </dl>

 

