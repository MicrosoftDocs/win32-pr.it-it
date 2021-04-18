---
description: Quando si usa la direttiva RegisterDlls INF per registrare autonomamente le dll, i chiamanti di SetupInstallFromInfSection possono ricevere notifiche su ogni file durante la registrazione o l'annullamento della registrazione.
ms.assetid: 0faf277c-7805-478f-9cec-0dd7b6acdb0e
title: Messaggio SPFILENOTIFY_STARTREGISTRATION (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe795af38c21c17bf4e81692985d4bfe50dc8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316074"
---
# <a name="spfilenotify_startregistration-message"></a><span data-ttu-id="d5e39-103">\_Messaggio SPFILENOTIFY STARTREGISTRATION</span><span class="sxs-lookup"><span data-stu-id="d5e39-103">SPFILENOTIFY\_STARTREGISTRATION message</span></span>

<span data-ttu-id="d5e39-104">Quando si usa la direttiva **RegisterDlls** inf per registrare autonomamente le dll, i chiamanti di [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) possono ricevere notifiche su ogni file durante la registrazione o l'annullamento della registrazione.</span><span class="sxs-lookup"><span data-stu-id="d5e39-104">When using the **RegisterDlls** INF directive to self-register DLLs, callers of [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) may receive notifications on each file as it is registered or unregistered.</span></span> <span data-ttu-id="d5e39-105">Per inviare una notifica **SPFILENOTIFY \_ STARTREGISTRATION** alla routine di callback una volta prima di registrare un file, includere \_ REGISTERCALLBACKAWARE più spin \_ regsvr nel parametro *Flags* di **SetupInstallFromInfSection**.</span><span class="sxs-lookup"><span data-stu-id="d5e39-105">To send a **SPFILENOTIFY\_STARTREGISTRATION** notification to the callback routine once before registering a file, include SPINST\_REGISTERCALLBACKAWARE plus SPINST\_REGSVR in the *Flags* parameter of **SetupInstallFromInfSection**.</span></span> <span data-ttu-id="d5e39-106">Per inviare la notifica di annullamento della registrazione, includere \_ REGISTERCALLBACKAWARE più spin \_ UNREGSVR nel parametro *Flags* .</span><span class="sxs-lookup"><span data-stu-id="d5e39-106">To send notification of unregistration, include SPINST\_REGISTERCALLBACKAWARE plus SPINST\_UNREGSVR in the *Flags* parameter.</span></span>

<span data-ttu-id="d5e39-107">La routine di callback specificata dal parametro *MsgHandler* di [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) deve corrispondere al [ \_ \_ callback dei file](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a)di tipo PSP.</span><span class="sxs-lookup"><span data-stu-id="d5e39-107">The callback routine specified by the *MsgHandler* parameter of [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) must be the type [PSP\_FILE\_CALLBACK](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span></span> <span data-ttu-id="d5e39-108">Impostare il parametro di *contesto* sullo stesso *contesto* specificato in **SetupInstallFromInfSection**.</span><span class="sxs-lookup"><span data-stu-id="d5e39-108">Set the *Context* parameter to the same *Context* specified in **SetupInstallFromInfSection**.</span></span> <span data-ttu-id="d5e39-109">Impostare il parametro *Notification* su **SPFILENOTIFY \_ STARTREGISTRATION**.</span><span class="sxs-lookup"><span data-stu-id="d5e39-109">Set the *Notification* parameter to **SPFILENOTIFY\_STARTREGISTRATION**.</span></span>


```C++
SPFILENOTIFY_STARTREGISTRATION
  Param1 = (UINT_PTR) pointer to file information;
  Param2 = (UINT_PTR) file registration or unregistration;
            
```



## <a name="parameters"></a><span data-ttu-id="d5e39-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="d5e39-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5e39-111">*Param1*</span><span class="sxs-lookup"><span data-stu-id="d5e39-111">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="d5e39-112">Puntatore a una struttura di [**\_ stato del \_ controllo \_ del registro SP**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) contenente le informazioni sul file di cui è in corso la registrazione o l'annullamento della registrazione.</span><span class="sxs-lookup"><span data-stu-id="d5e39-112">Pointer to a [**SP\_REGISTER\_CONTROL\_STATUS**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) structure containing information about the file being registered or unregistered.</span></span> <span data-ttu-id="d5e39-113">Il membro **cbSize** deve essere impostato sulla dimensione della struttura.</span><span class="sxs-lookup"><span data-stu-id="d5e39-113">The member **cbsize** should be set to the size of the structure.</span></span> <span data-ttu-id="d5e39-114">Il membro **filename** deve essere impostato sul percorso completo del file registrato.</span><span class="sxs-lookup"><span data-stu-id="d5e39-114">The **FileName** member should be set to the fully qualified path of the file being registered.</span></span> <span data-ttu-id="d5e39-115">**Win32Error** non viene utilizzato e deve essere impostato su nessun \_ errore.</span><span class="sxs-lookup"><span data-stu-id="d5e39-115">**Win32Error** is not used and should be set to NO\_ERROR.</span></span> <span data-ttu-id="d5e39-116">**FailureCode** non viene usato e deve essere impostato su SPREG \_ Success.</span><span class="sxs-lookup"><span data-stu-id="d5e39-116">**FailureCode** is not used and should be set to SPREG\_SUCCESS.</span></span>

</dd> <dt>

<span data-ttu-id="d5e39-117">*Param2*</span><span class="sxs-lookup"><span data-stu-id="d5e39-117">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="d5e39-118">Se il file viene registrato, *param2* deve essere impostato su un puntatore a un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="d5e39-118">If the file is being registered, *Param2* should be set to a pointer to a nonzero value.</span></span> <span data-ttu-id="d5e39-119">Se è in corso l'annullamento della registrazione del file, *param2* deve essere impostato su un puntatore a zero.</span><span class="sxs-lookup"><span data-stu-id="d5e39-119">If the file is being unregistered, *Param2* should be set to a pointer to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5e39-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d5e39-120">Return value</span></span>

<span data-ttu-id="d5e39-121">Dopo la ricezione della notifica, la funzione di callback può restituire uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="d5e39-121">After receiving notification, the callback function may return one of the following values.</span></span>



| <span data-ttu-id="d5e39-122">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d5e39-122">Return code</span></span>                                                                                  | <span data-ttu-id="d5e39-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d5e39-123">Description</span></span>                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d5e39-124"><dt>**\_interruzione FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="d5e39-124"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="d5e39-125">Non registrare o annullare la registrazione del file e arrestare l'elaborazione della sezione INF.</span><span class="sxs-lookup"><span data-stu-id="d5e39-125">Do not register or unregister the file and stop processing the INF section.</span></span><br/>             |
| <dl> <span data-ttu-id="d5e39-126"><dt>**\_doit FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="d5e39-126"><dt>**FILEOP\_DOIT**</dt></span></span> </dl>  | <span data-ttu-id="d5e39-127">Registrare o annullare la registrazione del file e continuare l'elaborazione della sezione INF.</span><span class="sxs-lookup"><span data-stu-id="d5e39-127">Register or unregister the file and continue processing the INF section.</span></span><br/>                |
| <dl> <span data-ttu-id="d5e39-128"><dt>**\_Ignora file**</dt></span><span class="sxs-lookup"><span data-stu-id="d5e39-128"><dt>**FILE\_SKIP**</dt></span></span> </dl>    | <span data-ttu-id="d5e39-129">Ignora la registrazione o l'annullamento della registrazione del file ma continua l'elaborazione della sezione INF</span><span class="sxs-lookup"><span data-stu-id="d5e39-129">Skip registration or unregistration of the file but continue processing the INF section</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d5e39-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5e39-130">Requirements</span></span>



| <span data-ttu-id="d5e39-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5e39-131">Requirement</span></span> | <span data-ttu-id="d5e39-132">Valore</span><span class="sxs-lookup"><span data-stu-id="d5e39-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d5e39-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5e39-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d5e39-134">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d5e39-134">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d5e39-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5e39-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d5e39-136">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d5e39-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d5e39-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d5e39-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5e39-138"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5e39-138"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5e39-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d5e39-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5e39-140">Overview</span><span class="sxs-lookup"><span data-stu-id="d5e39-140">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="d5e39-141">Notifications</span><span class="sxs-lookup"><span data-stu-id="d5e39-141">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="d5e39-142">**SetupInstallFromInfSection**</span><span class="sxs-lookup"><span data-stu-id="d5e39-142">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> <dt>

[<span data-ttu-id="d5e39-143">**\_ENDREGISTRATION SPFILENOTIFY**</span><span class="sxs-lookup"><span data-stu-id="d5e39-143">**SPFILENOTIFY\_ENDREGISTRATION**</span></span>](spfilenotify-endregistration.md)
</dt> </dl>

 

