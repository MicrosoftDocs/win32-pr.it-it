---
title: Classe SystemRestore
description: Fornisce metodi per disabilitare e abilitare il monitoraggio, elencare i punti di ripristino disponibili e avviare un ripristino nel sistema locale.
ms.assetid: 87216a56-6d40-44ea-a1ab-d43590b639a4
keywords:
- Ripristino del sistema della classe SystemRestore
- Ripristino del sistema della classe SystemRestore, descritto
topic_type:
- apiref
api_name:
- SystemRestore
- SystemRestore.Description
- SystemRestore.RestorePointType
- SystemRestore.EventType
- SystemRestore.SequenceNumber
- SystemRestore.CreationTime
api_location:
- Root\Default
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64d2b609a7a49a9b319c15745600aa54193350e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048487"
---
# <a name="systemrestore-class"></a><span data-ttu-id="0403a-105">Classe SystemRestore</span><span class="sxs-lookup"><span data-stu-id="0403a-105">SystemRestore class</span></span>

<span data-ttu-id="0403a-106">Fornisce metodi per disabilitare e abilitare il monitoraggio, elencare i punti di ripristino disponibili e avviare un ripristino nel sistema locale.</span><span class="sxs-lookup"><span data-stu-id="0403a-106">Provides methods for disabling and enabling monitoring, listing available restore points, and initiating a restore on the local system.</span></span>

## <a name="syntax"></a><span data-ttu-id="0403a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0403a-107">Syntax</span></span>

``` syntax
class SystemRestore
{
  String Description;
  uint32 RestorePointType;
  uint32 EventType;
  uint32 SequenceNumber;
  String CreationTime;
};
```

## <a name="members"></a><span data-ttu-id="0403a-108">Members</span><span class="sxs-lookup"><span data-stu-id="0403a-108">Members</span></span>

<span data-ttu-id="0403a-109">La classe **SystemRestore** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0403a-109">The **SystemRestore** class has these types of members:</span></span>

-   [<span data-ttu-id="0403a-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="0403a-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="0403a-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0403a-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0403a-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="0403a-112">Methods</span></span>

<span data-ttu-id="0403a-113">La classe **SystemRestore** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="0403a-113">The **SystemRestore** class has these methods.</span></span>



| <span data-ttu-id="0403a-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="0403a-114">Method</span></span>                                                             | <span data-ttu-id="0403a-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0403a-115">Description</span></span>                                                 |
|:-------------------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="0403a-116">**CreateRestorePoint**</span><span class="sxs-lookup"><span data-stu-id="0403a-116">**CreateRestorePoint**</span></span>](createrestorepoint-systemrestore.md)     | <span data-ttu-id="0403a-117">Crea un punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="0403a-117">Creates a restore point.</span></span><br/>                         |
| [<span data-ttu-id="0403a-118">**Disabilita**</span><span class="sxs-lookup"><span data-stu-id="0403a-118">**Disable**</span></span>](disable-systemrestore.md)                           | <span data-ttu-id="0403a-119">Disabilita il monitoraggio in un'unità specifica.</span><span class="sxs-lookup"><span data-stu-id="0403a-119">Disables monitoring on a particular drive.</span></span><br/>       |
| [<span data-ttu-id="0403a-120">**Abilitare**</span><span class="sxs-lookup"><span data-stu-id="0403a-120">**Enable**</span></span>](enable-systemrestore.md)                             | <span data-ttu-id="0403a-121">Abilita il monitoraggio in un'unità specifica.</span><span class="sxs-lookup"><span data-stu-id="0403a-121">Enables monitoring on a particular drive.</span></span><br/>        |
| [<span data-ttu-id="0403a-122">**GetLastRestoreStatus**</span><span class="sxs-lookup"><span data-stu-id="0403a-122">**GetLastRestoreStatus**</span></span>](getlastrestorestatus-systemrestore.md) | <span data-ttu-id="0403a-123">Recupera lo stato dell'ultimo ripristino di sistema.</span><span class="sxs-lookup"><span data-stu-id="0403a-123">Retrieves the status of the last system restore.</span></span><br/> |
| [<span data-ttu-id="0403a-124">**Restore**</span><span class="sxs-lookup"><span data-stu-id="0403a-124">**Restore**</span></span>](restore-systemrestore.md)                           | <span data-ttu-id="0403a-125">Avvia un ripristino di sistema.</span><span class="sxs-lookup"><span data-stu-id="0403a-125">Initiates a system restore.</span></span><br/>                      |



 

### <a name="properties"></a><span data-ttu-id="0403a-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0403a-126">Properties</span></span>

<span data-ttu-id="0403a-127">La classe **SystemRestore** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0403a-127">The **SystemRestore** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0403a-128">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="0403a-128">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0403a-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0403a-129">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="0403a-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0403a-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0403a-131">Ora in cui si è verificata la modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="0403a-131">The time at which the state change occurred.</span></span>

</dd> <dt>

<span data-ttu-id="0403a-132">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="0403a-132">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0403a-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0403a-133">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="0403a-134">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0403a-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0403a-135">Descrizione da visualizzare in modo che l'utente possa identificare facilmente un punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="0403a-135">The description to be displayed so the user can easily identify a restore point.</span></span> <span data-ttu-id="0403a-136">La lunghezza massima di una stringa ANSI è MAX \_ desc.</span><span class="sxs-lookup"><span data-stu-id="0403a-136">The maximum length of an ANSI string is MAX\_DESC.</span></span> <span data-ttu-id="0403a-137">La lunghezza massima di una stringa Unicode è MAX \_ desc \_ W.</span><span class="sxs-lookup"><span data-stu-id="0403a-137">The maximum length of a Unicode string is MAX\_DESC\_W.</span></span> <span data-ttu-id="0403a-138">Per ulteriori informazioni, vedere il [testo della descrizione del punto di ripristino](restore-point-description-text.md).</span><span class="sxs-lookup"><span data-stu-id="0403a-138">For more information, see [Restore Point Description Text](restore-point-description-text.md).</span></span>

</dd> <dt>

<span data-ttu-id="0403a-139">**EventType**</span><span class="sxs-lookup"><span data-stu-id="0403a-139">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0403a-140">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0403a-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0403a-141">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0403a-141">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0403a-142">Tipo di evento.</span><span class="sxs-lookup"><span data-stu-id="0403a-142">The type of event.</span></span> <span data-ttu-id="0403a-143">Il membro può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="0403a-143">This member can be one of the following values.</span></span>



| <span data-ttu-id="0403a-144">Valore</span><span class="sxs-lookup"><span data-stu-id="0403a-144">Value</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="0403a-145">Significato</span><span class="sxs-lookup"><span data-stu-id="0403a-145">Meaning</span></span>                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BEGIN_NESTED_SYSTEM_CHANGE"></span><span id="begin_nested_system_change"></span><dl> <span data-ttu-id="0403a-146"><dt>**Inizia \_ \_ \_ Modifica del sistema annidato**</dt> <dt>102</dt></span><span class="sxs-lookup"><span data-stu-id="0403a-146"><dt>**BEGIN\_NESTED\_SYSTEM\_CHANGE**</dt> <dt>102</dt></span></span> </dl> | <span data-ttu-id="0403a-147">Una modifica del sistema è iniziata.</span><span class="sxs-lookup"><span data-stu-id="0403a-147">A system change has begun.</span></span> <span data-ttu-id="0403a-148">Una chiamata nidificata successiva non crea un nuovo punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="0403a-148">A subsequent nested call does not create a new restore point.</span></span> <br/> <span data-ttu-id="0403a-149">Le chiamate successive devono utilizzare la modifica finale del \_ sistema annidato \_ \_ , non la \_ modifica del sistema finale \_ .</span><span class="sxs-lookup"><span data-stu-id="0403a-149">Subsequent calls must use END\_NESTED\_SYSTEM\_CHANGE, not END\_SYSTEM\_CHANGE.</span></span><br/> |
| <span id="BEGIN_SYSTEM_CHANGE"></span><span id="begin_system_change"></span><dl> <span data-ttu-id="0403a-150"><dt>**Inizia \_ \_Modifica del sistema**</dt> <dt>100</dt></span><span class="sxs-lookup"><span data-stu-id="0403a-150"><dt>**BEGIN\_SYSTEM\_CHANGE**</dt> <dt>100</dt></span></span> </dl>                       | <span data-ttu-id="0403a-151">Una modifica del sistema è iniziata.</span><span class="sxs-lookup"><span data-stu-id="0403a-151">A system change has begun.</span></span><br/>                                                                                                                                                           |
| <span id="END_NESTED_SYSTEM_CHANGE"></span><span id="end_nested_system_change"></span><dl> <span data-ttu-id="0403a-152"><dt>**Fine \_ \_ \_ Modifica del sistema annidato**</dt> <dt>103</dt></span><span class="sxs-lookup"><span data-stu-id="0403a-152"><dt>**END\_NESTED\_SYSTEM\_CHANGE**</dt> <dt>103</dt></span></span> </dl>       | <span data-ttu-id="0403a-153">Una modifica del sistema è terminata.</span><span class="sxs-lookup"><span data-stu-id="0403a-153">A system change has ended.</span></span><br/>                                                                                                                                                           |
| <span id="END_SYSTEM_CHANGE"></span><span id="end_system_change"></span><dl> <span data-ttu-id="0403a-154"><dt>**Fine \_ \_Modifica del sistema**</dt> <dt>101</dt></span><span class="sxs-lookup"><span data-stu-id="0403a-154"><dt>**END\_SYSTEM\_CHANGE**</dt> <dt>101</dt></span></span> </dl>                             | <span data-ttu-id="0403a-155">Una modifica del sistema è terminata.</span><span class="sxs-lookup"><span data-stu-id="0403a-155">A system change has ended.</span></span><br/>                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="0403a-156">**RestorePointType**</span><span class="sxs-lookup"><span data-stu-id="0403a-156">**RestorePointType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0403a-157">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0403a-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0403a-158">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0403a-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0403a-159">Tipo di punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="0403a-159">The type of restore point.</span></span> <span data-ttu-id="0403a-160">Il membro può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="0403a-160">This member can be one of the following values.</span></span>



| <span data-ttu-id="0403a-161">Valore</span><span class="sxs-lookup"><span data-stu-id="0403a-161">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="0403a-162">Significato</span><span class="sxs-lookup"><span data-stu-id="0403a-162">Meaning</span></span>                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPLICATION_INSTALL"></span><span id="application_install"></span><dl> <span data-ttu-id="0403a-163"><dt>**Applicazione \_ di INSTALLARE**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0403a-163"><dt>**APPLICATION\_INSTALL**</dt> <dt>0</dt></span></span> </dl>         | <span data-ttu-id="0403a-164">È stata installata un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0403a-164">An application has been installed.</span></span><br/>                                                                                                                 |
| <span id="APPLICATION_UNINSTALL"></span><span id="application_uninstall"></span><dl> <span data-ttu-id="0403a-165"><dt>**Applicazione \_ di Disinstalla**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0403a-165"><dt>**APPLICATION\_UNINSTALL**</dt> <dt>1</dt></span></span> </dl>   | <span data-ttu-id="0403a-166">Un'applicazione è stata disinstallata.</span><span class="sxs-lookup"><span data-stu-id="0403a-166">An application has been uninstalled.</span></span><br/>                                                                                                               |
| <span id="CANCELLED_OPERATION"></span><span id="cancelled_operation"></span><dl> <span data-ttu-id="0403a-167">Operazione <dt>**annullata \_ OPERAZIONE**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="0403a-167"><dt>**CANCELLED\_OPERATION**</dt> <dt>13</dt></span></span> </dl>        | <span data-ttu-id="0403a-168">Un'applicazione deve eliminare il punto di ripristino creato.</span><span class="sxs-lookup"><span data-stu-id="0403a-168">An application needs to delete the restore point it created.</span></span> <span data-ttu-id="0403a-169">Ad esempio, un'applicazione utilizzerebbe questo flag quando un utente annulla un'installazione.</span><span class="sxs-lookup"><span data-stu-id="0403a-169">For example, an application would use this flag when a user cancels an installation.</span></span> <br/> |
| <span id="DEVICE_DRIVER_INSTALL"></span><span id="device_driver_install"></span><dl> <span data-ttu-id="0403a-170"><dt>**Dispositivo \_ \_Installazione driver**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="0403a-170"><dt>**DEVICE\_DRIVER\_INSTALL**</dt> <dt>10</dt></span></span> </dl> | <span data-ttu-id="0403a-171">È stato installato un driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0403a-171">A device driver has been installed.</span></span><br/>                                                                                                                |
| <span id="MODIFY_SETTINGS"></span><span id="modify_settings"></span><dl> <span data-ttu-id="0403a-172"><dt>**Modifica \_ di IMPOSTAZIONI**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="0403a-172"><dt>**MODIFY\_SETTINGS**</dt> <dt>12</dt></span></span> </dl>                    | <span data-ttu-id="0403a-173">Sono state aggiunte o rimosse funzionalità per un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0403a-173">An application has had features added or removed.</span></span><br/>                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="0403a-174">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="0403a-174">**SequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0403a-175">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0403a-175">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0403a-176">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0403a-176">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0403a-177">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="0403a-177">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="0403a-178">Numero di sequenza del punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="0403a-178">The sequence number of the restore point.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0403a-179">Commenti</span><span class="sxs-lookup"><span data-stu-id="0403a-179">Remarks</span></span>

<span data-ttu-id="0403a-180">È possibile ottenere un elenco di punti di ripristino usando il metodo [**SWbemServices. InstancesOf**](/windows/desktop/WmiSdk/swbemservices-instancesof) per recuperare una raccolta di oggetti **SystemRestore** .</span><span class="sxs-lookup"><span data-stu-id="0403a-180">You can obtain a list of restore points by using the [**SWbemServices.InstancesOf**](/windows/desktop/WmiSdk/swbemservices-instancesof) method to retrieve a collection of **SystemRestore** objects.</span></span> <span data-ttu-id="0403a-181">È possibile utilizzare le proprietà della classe per identificare il punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="0403a-181">You can use the class properties to identify the restore point.</span></span>

## <a name="examples"></a><span data-ttu-id="0403a-182">Esempio</span><span class="sxs-lookup"><span data-stu-id="0403a-182">Examples</span></span>

<span data-ttu-id="0403a-183">Lo script di esempio seguente enumera i punti di ripristino correnti.</span><span class="sxs-lookup"><span data-stu-id="0403a-183">The following sample script enumerates the current restore points.</span></span>


```VB
'SystemRestore Class
'Provides methods for disabling and enabling monitoring, 
'listing available restore points, and initiating a 
'restore on the local system.

Set RPSet = GetObject("winmgmts:root/default").InstancesOf ("SystemRestore")
for each RP in RPSet
    wscript.Echo "Dir: RP" & RP.SequenceNumber & ", Name: " & RP.Description & ", Type: ", RP.RestorePointType & ", Time: " & RP.CreationTime
next
```



## <a name="requirements"></a><span data-ttu-id="0403a-184">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0403a-184">Requirements</span></span>



| <span data-ttu-id="0403a-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="0403a-185">Requirement</span></span> | <span data-ttu-id="0403a-186">Valore</span><span class="sxs-lookup"><span data-stu-id="0403a-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="0403a-187">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0403a-187">Minimum supported client</span></span><br/> | <span data-ttu-id="0403a-188">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0403a-188">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="0403a-189">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0403a-189">Minimum supported server</span></span><br/> | <span data-ttu-id="0403a-190">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0403a-190">None supported</span></span><br/>                                                         |
| <span data-ttu-id="0403a-191">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0403a-191">Namespace</span></span><br/>                | <span data-ttu-id="0403a-192">\\Impostazioni predefinite radice</span><span class="sxs-lookup"><span data-stu-id="0403a-192">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="0403a-193">MOF</span><span class="sxs-lookup"><span data-stu-id="0403a-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0403a-194"><dt>Sr. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0403a-194"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0403a-195">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0403a-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0403a-196">Strumentazione gestione Windows (WMI)</span><span class="sxs-lookup"><span data-stu-id="0403a-196">Windows Management Instrumentation</span></span>](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

