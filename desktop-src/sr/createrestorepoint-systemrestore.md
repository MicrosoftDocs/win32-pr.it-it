---
title: Metodo CreateRestorePoint della classe SystemRestore
description: Crea un punto di ripristino.
ms.assetid: 30e1ff03-816c-463f-9f80-6d84149f0e0b
keywords:
- Ripristino del sistema del metodo CreateRestorePoint
- Ripristino del sistema del metodo CreateRestorePoint, classe SystemRestore
- SystemRestore Class System Restore, metodo CreateRestorePoint
topic_type:
- apiref
api_name:
- SystemRestore.CreateRestorePoint
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1cae9e78d1845f628d62dc46362f1bc2bd8a37e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477146"
---
# <a name="createrestorepoint-method-of-the-systemrestore-class"></a><span data-ttu-id="77337-106">Metodo CreateRestorePoint della classe SystemRestore</span><span class="sxs-lookup"><span data-stu-id="77337-106">CreateRestorePoint method of the SystemRestore class</span></span>

<span data-ttu-id="77337-107">Crea un punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="77337-107">Creates a restore point.</span></span>

<span data-ttu-id="77337-108">Questo metodo è l'equivalente tramite script della funzione [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) .</span><span class="sxs-lookup"><span data-stu-id="77337-108">This method is the scriptable equivalent of the [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="77337-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="77337-109">Syntax</span></span>


```mof
uint32 CreateRestorePoint(
  [in] String Description,
  [in] uint32 RestorePointType,
  [in] uint32 EventType
);
```



## <a name="parameters"></a><span data-ttu-id="77337-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="77337-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77337-111">*Descrizione* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="77337-111">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77337-112">Descrizione da visualizzare in modo che l'utente possa identificare facilmente un punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="77337-112">The description to be displayed so the user can easily identify a restore point.</span></span> <span data-ttu-id="77337-113">La lunghezza massima di una stringa ANSI è MAX \_ desc.</span><span class="sxs-lookup"><span data-stu-id="77337-113">The maximum length of an ANSI string is MAX\_DESC.</span></span> <span data-ttu-id="77337-114">La lunghezza massima di una stringa Unicode è MAX \_ desc \_ W.</span><span class="sxs-lookup"><span data-stu-id="77337-114">The maximum length of a Unicode string is MAX\_DESC\_W.</span></span> <span data-ttu-id="77337-115">Per ulteriori informazioni, vedere il [testo della descrizione del punto di ripristino](restore-point-description-text.md).</span><span class="sxs-lookup"><span data-stu-id="77337-115">For more information, see [Restore Point Description Text](restore-point-description-text.md).</span></span>

</dd> <dt>

<span data-ttu-id="77337-116">*RestorePointType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="77337-116">*RestorePointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77337-117">Tipo di punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="77337-117">The type of restore point.</span></span> <span data-ttu-id="77337-118">Il membro può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="77337-118">This member can be one of the following values.</span></span>



| <span data-ttu-id="77337-119">Tipo di punto di ripristino</span><span class="sxs-lookup"><span data-stu-id="77337-119">Restore point type</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="77337-120">Significato</span><span class="sxs-lookup"><span data-stu-id="77337-120">Meaning</span></span>                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPLICATION_INSTALL"></span><span id="application_install"></span><dl> <span data-ttu-id="77337-121"><dt>**Applicazione \_ di INSTALLARE**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="77337-121"><dt>**APPLICATION\_INSTALL**</dt> <dt>0</dt></span></span> </dl>         | <span data-ttu-id="77337-122">È stata installata un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="77337-122">An application has been installed.</span></span><br/>                                                                                                                |
| <span id="APPLICATION_UNINSTALL"></span><span id="application_uninstall"></span><dl> <span data-ttu-id="77337-123"><dt>**Applicazione \_ di Disinstalla**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="77337-123"><dt>**APPLICATION\_UNINSTALL**</dt> <dt>1</dt></span></span> </dl>   | <span data-ttu-id="77337-124">Un'applicazione è stata disinstallata.</span><span class="sxs-lookup"><span data-stu-id="77337-124">An application has been uninstalled.</span></span><br/>                                                                                                              |
| <span id="DEVICE_DRIVER_INSTALL"></span><span id="device_driver_install"></span><dl> <span data-ttu-id="77337-125"><dt>**Dispositivo \_ \_Installazione driver**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="77337-125"><dt>**DEVICE\_DRIVER\_INSTALL**</dt> <dt>10</dt></span></span> </dl> | <span data-ttu-id="77337-126">È stato installato un driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="77337-126">A device driver has been installed.</span></span><br/>                                                                                                               |
| <span id="MODIFY_SETTINGS"></span><span id="modify_settings"></span><dl> <span data-ttu-id="77337-127"><dt>**Modifica \_ di IMPOSTAZIONI**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="77337-127"><dt>**MODIFY\_SETTINGS**</dt> <dt>12</dt></span></span> </dl>                    | <span data-ttu-id="77337-128">Sono state aggiunte o rimosse funzionalità per un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="77337-128">An application has had features added or removed.</span></span><br/>                                                                                                 |
| <span id="CANCELLED_OPERATION"></span><span id="cancelled_operation"></span><dl> <span data-ttu-id="77337-129">Operazione <dt>**annullata \_ OPERAZIONE**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="77337-129"><dt>**CANCELLED\_OPERATION**</dt> <dt>13</dt></span></span> </dl>        | <span data-ttu-id="77337-130">Un'applicazione deve eliminare il punto di ripristino creato.</span><span class="sxs-lookup"><span data-stu-id="77337-130">An application needs to delete the restore point it created.</span></span> <span data-ttu-id="77337-131">Ad esempio, un'applicazione utilizzerebbe questo flag quando un utente annulla un'installazione.</span><span class="sxs-lookup"><span data-stu-id="77337-131">For example, an application would use this flag when a user cancels an installation.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="77337-132">*EventType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="77337-132">*EventType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77337-133">Tipo di evento.</span><span class="sxs-lookup"><span data-stu-id="77337-133">The type of event.</span></span> <span data-ttu-id="77337-134">Il membro può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="77337-134">This member can be one of the following values.</span></span>



| <span data-ttu-id="77337-135">Tipo di evento</span><span class="sxs-lookup"><span data-stu-id="77337-135">Event type</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="77337-136">Significato</span><span class="sxs-lookup"><span data-stu-id="77337-136">Meaning</span></span>                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BEGIN_NESTED_SYSTEM_CHANGE"></span><span id="begin_nested_system_change"></span><dl> <span data-ttu-id="77337-137"><dt>**Inizia \_ \_ \_ Modifica del sistema annidato**</dt> <dt>102</dt></span><span class="sxs-lookup"><span data-stu-id="77337-137"><dt>**BEGIN\_NESTED\_SYSTEM\_CHANGE**</dt> <dt>102</dt></span></span> </dl> | <span data-ttu-id="77337-138">Una modifica del sistema è iniziata.</span><span class="sxs-lookup"><span data-stu-id="77337-138">A system change has begun.</span></span> <span data-ttu-id="77337-139">Una chiamata nidificata successiva non crea un nuovo punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="77337-139">A subsequent nested call does not create a new restore point.</span></span> <br/> <span data-ttu-id="77337-140">Le chiamate successive devono utilizzare la modifica finale del \_ sistema annidato \_ \_ , non la \_ modifica del sistema finale \_ .</span><span class="sxs-lookup"><span data-stu-id="77337-140">Subsequent calls must use END\_NESTED\_SYSTEM\_CHANGE, not END\_SYSTEM\_CHANGE.</span></span><br/> |
| <span id="BEGIN_SYSTEM_CHANGE"></span><span id="begin_system_change"></span><dl> <span data-ttu-id="77337-141"><dt>**Inizia \_ \_Modifica del sistema**</dt> <dt>100</dt></span><span class="sxs-lookup"><span data-stu-id="77337-141"><dt>**BEGIN\_SYSTEM\_CHANGE**</dt> <dt>100</dt></span></span> </dl>                       | <span data-ttu-id="77337-142">Una modifica del sistema è iniziata.</span><span class="sxs-lookup"><span data-stu-id="77337-142">A system change has begun.</span></span> <br/> <span data-ttu-id="77337-143">Una chiamata successiva deve utilizzare la \_ modifica del sistema finale \_ , non la modifica finale del \_ sistema annidato \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="77337-143">A subsequent call must use END\_SYSTEM\_CHANGE, not END\_NESTED\_SYSTEM\_CHANGE.</span></span><br/>                                                              |
| <span id="END_NESTED_SYSTEM_CHANGE"></span><span id="end_nested_system_change"></span><dl> <span data-ttu-id="77337-144"><dt>**Fine \_ \_ \_ Modifica del sistema annidato**</dt> <dt>103</dt></span><span class="sxs-lookup"><span data-stu-id="77337-144"><dt>**END\_NESTED\_SYSTEM\_CHANGE**</dt> <dt>103</dt></span></span> </dl>       | <span data-ttu-id="77337-145">Una modifica del sistema è terminata.</span><span class="sxs-lookup"><span data-stu-id="77337-145">A system change has ended.</span></span><br/>                                                                                                                                                           |
| <span id="END_SYSTEM_CHANGE"></span><span id="end_system_change"></span><dl> <span data-ttu-id="77337-146"><dt>**Fine \_ \_Modifica del sistema**</dt> <dt>101</dt></span><span class="sxs-lookup"><span data-stu-id="77337-146"><dt>**END\_SYSTEM\_CHANGE**</dt> <dt>101</dt></span></span> </dl>                             | <span data-ttu-id="77337-147">Una modifica del sistema è terminata.</span><span class="sxs-lookup"><span data-stu-id="77337-147">A system change has ended.</span></span><br/>                                                                                                                                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77337-148">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="77337-148">Return value</span></span>

<span data-ttu-id="77337-149">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="77337-149">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="77337-150">In caso contrario, il metodo restituisce uno dei codici di errore COM definiti in WinError. h.</span><span class="sxs-lookup"><span data-stu-id="77337-150">Otherwise, the method returns one of the COM error codes defined in WinError.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="77337-151">Commenti</span><span class="sxs-lookup"><span data-stu-id="77337-151">Remarks</span></span>

<span data-ttu-id="77337-152">\* \* Windows 8: \* \*</span><span class="sxs-lookup"><span data-stu-id="77337-152">\*\*Windows 8:  \*\*</span></span>

<span data-ttu-id="77337-153">Una nuova chiave del registro di sistema consente agli sviluppatori di applicazioni di modificare la frequenza di creazione di punti di ripristino.</span><span class="sxs-lookup"><span data-stu-id="77337-153">A new registry key enables application developers to change the frequency of restore-point creation.</span></span>

<span data-ttu-id="77337-154">Le applicazioni devono creare questa chiave per utilizzarla perché non sarà preesistente nel sistema.</span><span class="sxs-lookup"><span data-stu-id="77337-154">Applications should create this key to use it because it will not preexist in the system.</span></span> <span data-ttu-id="77337-155">Per impostazione predefinita, verranno applicati gli elementi seguenti se la chiave non esiste.</span><span class="sxs-lookup"><span data-stu-id="77337-155">The following will apply by default if the key does not exist.</span></span> <span data-ttu-id="77337-156">Se un'applicazione chiama il metodo **createrestorepoint** per creare un punto di ripristino, Windows ignora la creazione di questo nuovo punto di ripristino se sono stati creati punti di ripristino nelle ultime 24 ore.</span><span class="sxs-lookup"><span data-stu-id="77337-156">If an application calls the **CreateRestorePoint** method to create a restore point, Windows skips creating this new restore point if any restore points have been created in the last 24 hours.</span></span> <span data-ttu-id="77337-157">Il metodo **createrestorepoint** restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="77337-157">The **CreateRestorePoint** method returns **S\_OK**.</span></span>

<span data-ttu-id="77337-158">Gli sviluppatori possono scrivere applicazioni che creano il valore **DWORD** **SystemRestorePointCreationFrequency** nella chiave del registro di sistema **HKLM \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ SystemRestore**.</span><span class="sxs-lookup"><span data-stu-id="77337-158">Developers can write applications that create the **DWORD** value **SystemRestorePointCreationFrequency** under the registry key **HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\SystemRestore**.</span></span> <span data-ttu-id="77337-159">Il valore di questa chiave del registro di sistema può modificare la frequenza di creazione del punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="77337-159">The value of this registry key can change the frequency of restore point creation.</span></span> <span data-ttu-id="77337-160">Il valore di questa chiave del registro di sistema può modificare la frequenza di creazione del punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="77337-160">The value of this registry key can change the frequency of restore point creation.</span></span>

<span data-ttu-id="77337-161">Se l'applicazione chiama **createrestorepoint** per creare un punto di ripristino e il valore della chiave del registro di sistema è 0, ripristino configurazione di sistema non ignora la creazione del nuovo punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="77337-161">If the application calls **CreateRestorePoint** to create a restore point, and the registry key value is 0, system restore does not skip creating the new restore point.</span></span>

<span data-ttu-id="77337-162">Se l'applicazione chiama **createrestorepoint** per creare un punto di ripristino e il valore della chiave del registro di sistema è Integer N, ripristino configurazione di sistema ignora la creazione di un nuovo punto di ripristino se sono stati creati punti di ripristino nei precedenti N minuti.</span><span class="sxs-lookup"><span data-stu-id="77337-162">If the application calls **CreateRestorePoint** to create a restore point, and the registry key value is the integer N, system restore skips creating a new restore point if any restore points were created in the previous N minutes.</span></span>

## <a name="examples"></a><span data-ttu-id="77337-163">Esempio</span><span class="sxs-lookup"><span data-stu-id="77337-163">Examples</span></span>


```VB
'CreateRestorePoint Method of the SystemRestore Class
'Creates a restore point. Specifies the beginning and 
'the ending of a set of changes so that System Restore 
'can create a restore point.This method is the 
'scriptable equivalent of the SRSetRestorePoint function.

Set Args = wscript.Arguments
If Args.Count() > 0 Then
    RpName = Args.item(0)
Else 
    RpName = "Vbscript"
End If

Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")

If (obj.CreateRestorePoint(RpName, 0, 100)) = 0 Then
    wscript.Echo "Success"
Else 
    wscript.Echo "Failed"
End If
```



## <a name="requirements"></a><span data-ttu-id="77337-164">Requisiti</span><span class="sxs-lookup"><span data-stu-id="77337-164">Requirements</span></span>



| <span data-ttu-id="77337-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="77337-165">Requirement</span></span> | <span data-ttu-id="77337-166">Valore</span><span class="sxs-lookup"><span data-stu-id="77337-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="77337-167">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="77337-167">Minimum supported client</span></span><br/> | <span data-ttu-id="77337-168">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="77337-168">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="77337-169">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="77337-169">Minimum supported server</span></span><br/> | <span data-ttu-id="77337-170">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="77337-170">None supported</span></span><br/>                                                         |
| <span data-ttu-id="77337-171">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="77337-171">Namespace</span></span><br/>                | <span data-ttu-id="77337-172">\\Impostazioni predefinite radice</span><span class="sxs-lookup"><span data-stu-id="77337-172">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="77337-173">MOF</span><span class="sxs-lookup"><span data-stu-id="77337-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="77337-174"><dt>Sr. mof</dt></span><span class="sxs-lookup"><span data-stu-id="77337-174"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77337-175">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="77337-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77337-176">**SystemRestore**</span><span class="sxs-lookup"><span data-stu-id="77337-176">**SystemRestore**</span></span>](systemrestore.md)
</dt> </dl>

 

 





