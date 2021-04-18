---
description: Quando si usa la direttiva RegisterDlls INF per registrare autonomamente le dll, i chiamanti di SetupInstallFromInfSection possono ricevere notifiche su ogni file durante la registrazione o l'annullamento della registrazione.
ms.assetid: 6304f406-c9f8-41cc-a7b7-5ef606f62efb
title: Messaggio SPFILENOTIFY_ENDREGISTRATION (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c8992d318d605110d74521efdb8a9c911aeeb9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318618"
---
# <a name="spfilenotify_endregistration-message"></a><span data-ttu-id="efc20-103">\_Messaggio SPFILENOTIFY ENDREGISTRATION</span><span class="sxs-lookup"><span data-stu-id="efc20-103">SPFILENOTIFY\_ENDREGISTRATION message</span></span>

<span data-ttu-id="efc20-104">Quando si usa la direttiva **RegisterDlls** inf per registrare autonomamente le dll, i chiamanti di [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) possono ricevere notifiche su ogni file durante la registrazione o l'annullamento della registrazione.</span><span class="sxs-lookup"><span data-stu-id="efc20-104">When using the **RegisterDlls** INF directive to self-register DLLs, callers of [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) may receive notifications on each file as it is registered or unregistered.</span></span> <span data-ttu-id="efc20-105">Per inviare una **notifica \_ ENDREGISTRATION di SPFILENOTIFY** a una routine di callback una volta dopo la registrazione o l'annullamento della registrazione di un file, includere \_ il REGISTERCALLBACKAWARE più spinoso \_ regsvr nel parametro *Flags* di **SetupInstallFromInfSection**.</span><span class="sxs-lookup"><span data-stu-id="efc20-105">To send a **SPFILENOTIFY\_ENDREGISTRATION** notification to a callback routine once after registering or unregistering a file, include SPINST\_REGISTERCALLBACKAWARE plus SPINST\_REGSVR in the *Flags* parameter of **SetupInstallFromInfSection**.</span></span> <span data-ttu-id="efc20-106">Per inviare la notifica di annullamento della registrazione, includere \_ REGISTERCALLBACKAWARE più spin \_ UNREGSVR nel parametro *Flags* .</span><span class="sxs-lookup"><span data-stu-id="efc20-106">To send notification of unregistration, include SPINST\_REGISTERCALLBACKAWARE plus SPINST\_UNREGSVR in the *Flags* parameter.</span></span>

<span data-ttu-id="efc20-107">La routine di callback specificata dal parametro *MsgHandler* di [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) deve corrispondere al [ \_ \_ callback dei file](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a)di tipo PSP.</span><span class="sxs-lookup"><span data-stu-id="efc20-107">The callback routine specified by the *MsgHandler* parameter of [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) must be the type [PSP\_FILE\_CALLBACK](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span></span> <span data-ttu-id="efc20-108">Impostare il parametro di *contesto* sullo stesso *contesto* specificato in **SetupInstallFromInfSection**.</span><span class="sxs-lookup"><span data-stu-id="efc20-108">Set the *Context* parameter to the same *Context* specified in **SetupInstallFromInfSection**.</span></span> <span data-ttu-id="efc20-109">Impostare il parametro *Notification* su **SPFILENOTIFY \_ ENDREGISTRATION**.</span><span class="sxs-lookup"><span data-stu-id="efc20-109">Set the *Notification* parameter to **SPFILENOTIFY\_ENDREGISTRATION**.</span></span>


```C++
SPFILENOTIFY_ENDREGISTRATION
  Param1 = (UINT_PTR) pointer to file information;
  Param2 = (UINT_PTR) file registration or unregistration;
            
```



## <a name="parameters"></a><span data-ttu-id="efc20-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="efc20-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efc20-111">*Param1*</span><span class="sxs-lookup"><span data-stu-id="efc20-111">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="efc20-112">Puntatore a una struttura di [**\_ stato del \_ controllo \_ del registro SP**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) contenente le informazioni sul file di cui è in corso la registrazione o l'annullamento della registrazione.</span><span class="sxs-lookup"><span data-stu-id="efc20-112">Pointer to a [**SP\_REGISTER\_CONTROL\_STATUS**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) structure containing information about the file being registered or unregistered.</span></span> <span data-ttu-id="efc20-113">Il membro **cbSize** deve essere impostato sulla dimensione della struttura.</span><span class="sxs-lookup"><span data-stu-id="efc20-113">The member **cbsize** should be set to the size of the structure.</span></span> <span data-ttu-id="efc20-114">**Filename** deve essere impostato sul percorso completo del file registrato.</span><span class="sxs-lookup"><span data-stu-id="efc20-114">**FileName** should be set to the fully qualified path of the file being registered.</span></span> <span data-ttu-id="efc20-115">**Win32Error** deve essere impostato su un [codice di errore di sistema](/windows/desktop/Debug/system-error-codes) che indica un codice di errore esteso.</span><span class="sxs-lookup"><span data-stu-id="efc20-115">**Win32Error** should be set to a [system error code](/windows/desktop/Debug/system-error-codes) indicating an extended error code.</span></span> <span data-ttu-id="efc20-116">**FailureCode** deve essere impostato su uno dei codici di errore validi che indicano il risultato della registrazione.</span><span class="sxs-lookup"><span data-stu-id="efc20-116">**FailureCode** should be set to one of the valid failure codes indicating the outcome of the registration.</span></span> <span data-ttu-id="efc20-117">Per i codici di errore validi, vedere [**SP \_ Register \_ Control \_ status**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa).</span><span class="sxs-lookup"><span data-stu-id="efc20-117">For valid failure codes see [**SP\_REGISTER\_CONTROL\_STATUS**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa).</span></span>

</dd> <dt>

<span data-ttu-id="efc20-118">*Param2*</span><span class="sxs-lookup"><span data-stu-id="efc20-118">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="efc20-119">Se il file viene registrato, *param2* deve essere impostato su un puntatore a un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="efc20-119">If the file is being registered, *Param2* should be set to a pointer to a nonzero value.</span></span> <span data-ttu-id="efc20-120">Se è in corso l'annullamento della registrazione del file, *param2* deve essere impostato su un puntatore a zero.</span><span class="sxs-lookup"><span data-stu-id="efc20-120">If the file is being unregistered, *Param2* should be set to a pointer to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efc20-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="efc20-121">Return value</span></span>

<span data-ttu-id="efc20-122">Dopo la ricezione della notifica, la funzione di callback può restituire uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="efc20-122">After receiving notification, the callback function may return one of the following values.</span></span>



| <span data-ttu-id="efc20-123">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="efc20-123">Return code</span></span>                                                                                  | <span data-ttu-id="efc20-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="efc20-124">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="efc20-125"><dt>**\_interruzione FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="efc20-125"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="efc20-126">Interrompere l'elaborazione della sezione INF.</span><span class="sxs-lookup"><span data-stu-id="efc20-126">Stop processing the INF section.</span></span><br/>     |
| <dl> <span data-ttu-id="efc20-127"><dt>**\_doit FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="efc20-127"><dt>**FILEOP\_DOIT**</dt></span></span> </dl>  | <span data-ttu-id="efc20-128">Continuare l'elaborazione della sezione INF.</span><span class="sxs-lookup"><span data-stu-id="efc20-128">Continue processing the INF section.</span></span><br/> |
| <dl> <span data-ttu-id="efc20-129"><dt>**\_Ignora file**</dt></span><span class="sxs-lookup"><span data-stu-id="efc20-129"><dt>**FILE\_SKIP**</dt></span></span> </dl>    | <span data-ttu-id="efc20-130">Continua l'elaborazione della sezione INF</span><span class="sxs-lookup"><span data-stu-id="efc20-130">Continue processing the INF section</span></span><br/>  |



 

## <a name="requirements"></a><span data-ttu-id="efc20-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="efc20-131">Requirements</span></span>



| <span data-ttu-id="efc20-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="efc20-132">Requirement</span></span> | <span data-ttu-id="efc20-133">Valore</span><span class="sxs-lookup"><span data-stu-id="efc20-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="efc20-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="efc20-134">Minimum supported client</span></span><br/> | <span data-ttu-id="efc20-135">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="efc20-135">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="efc20-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="efc20-136">Minimum supported server</span></span><br/> | <span data-ttu-id="efc20-137">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="efc20-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="efc20-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="efc20-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="efc20-139"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="efc20-139"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efc20-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="efc20-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efc20-141">Overview</span><span class="sxs-lookup"><span data-stu-id="efc20-141">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="efc20-142">Notifications</span><span class="sxs-lookup"><span data-stu-id="efc20-142">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="efc20-143">**SetupInstallFromInfSection**</span><span class="sxs-lookup"><span data-stu-id="efc20-143">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> <dt>

[<span data-ttu-id="efc20-144">**\_STARTREGISTRATION SPFILENOTIFY**</span><span class="sxs-lookup"><span data-stu-id="efc20-144">**SPFILENOTIFY\_STARTREGISTRATION**</span></span>](spfilenotify-startregistration.md)
</dt> </dl>

 

