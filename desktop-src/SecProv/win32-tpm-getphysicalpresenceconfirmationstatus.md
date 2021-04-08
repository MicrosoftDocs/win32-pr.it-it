---
description: Indica se è richiesta la conferma da un utente fisicamente presente per una determinata operazione di presenza fisica.
ms.assetid: 1CE558B7-EB6F-42CB-B52B-2A0101E90BD5
title: 'Metodo Win32_Tpm:: GetPhysicalPresenceConfirmationStatus'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceConfirmationStatus
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 61dc2798973a82cfc75c803f2bf8307c8a43b3c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967874"
---
# <a name="win32_tpmgetphysicalpresenceconfirmationstatus-method"></a><span data-ttu-id="80968-103">\_Metodo Win32 TPM:: GetPhysicalPresenceConfirmationStatus</span><span class="sxs-lookup"><span data-stu-id="80968-103">Win32\_Tpm::GetPhysicalPresenceConfirmationStatus method</span></span>

<span data-ttu-id="80968-104">Indica se è richiesta la conferma da un utente fisicamente presente per una determinata operazione di presenza fisica.</span><span class="sxs-lookup"><span data-stu-id="80968-104">Indicates if confirmation from a physically present user is required for a given physical presence operation.</span></span>

<span data-ttu-id="80968-105">Questo metodo è accessibile solo agli amministratori locali.</span><span class="sxs-lookup"><span data-stu-id="80968-105">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="80968-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="80968-106">Syntax</span></span>


```C++
uint32 GetPhysicalPresenceConfirmationStatus(
  [in]  uint32 Operation,
  [out] uint32 ConfirmationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="80968-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="80968-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80968-108">*Operazione* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="80968-108">*Operation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80968-109">Valore intero che specifica l'operazione TPM richiesta che richiede la presenza fisica.</span><span class="sxs-lookup"><span data-stu-id="80968-109">An integer value that specifies the requested TPM operation that requires physical presence.</span></span> <span data-ttu-id="80968-110">Sono supportati anche i comandi specifici del fornitore.</span><span class="sxs-lookup"><span data-stu-id="80968-110">Vendor specific commands are supported as well.</span></span>

<span data-ttu-id="80968-111">Il parametro *Operation* può essere costituito dai valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="80968-111">The *Operation* parameter may consist of the following values.</span></span>



| <span data-ttu-id="80968-112">Valore</span><span class="sxs-lookup"><span data-stu-id="80968-112">Value</span></span>                                                                                                                               | <span data-ttu-id="80968-113">Significato</span><span class="sxs-lookup"><span data-stu-id="80968-113">Meaning</span></span>                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="80968-114"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="80968-114"><dt>1</dt></span></span> </dl>                                                        | <span data-ttu-id="80968-115">Abilitare</span><span class="sxs-lookup"><span data-stu-id="80968-115">Enable</span></span><br/>                                        |
| <dl> <span data-ttu-id="80968-116"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="80968-116"><dt>2</dt></span></span> </dl>                                                        | <span data-ttu-id="80968-117">Disabilita</span><span class="sxs-lookup"><span data-stu-id="80968-117">Disable</span></span><br/>                                       |
| <dl> <span data-ttu-id="80968-118"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="80968-118"><dt>3</dt></span></span> </dl>                                                        | <span data-ttu-id="80968-119">Activate</span><span class="sxs-lookup"><span data-stu-id="80968-119">Activate</span></span><br/>                                      |
| <dl> <span data-ttu-id="80968-120"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="80968-120"><dt>4</dt></span></span> </dl>                                                        | <span data-ttu-id="80968-121">Disattivare</span><span class="sxs-lookup"><span data-stu-id="80968-121">Deactivate</span></span><br/>                                    |
| <dl> <span data-ttu-id="80968-122"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="80968-122"><dt>5</dt></span></span> </dl>                                                        | <span data-ttu-id="80968-123">Cancella</span><span class="sxs-lookup"><span data-stu-id="80968-123">Clear</span></span><br/>                                         |
| <dl> <span data-ttu-id="80968-124"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="80968-124"><dt>6</dt></span></span> </dl>                                                        | <span data-ttu-id="80968-125">Abilita + attiva</span><span class="sxs-lookup"><span data-stu-id="80968-125">Enable + Activate</span></span><br/>                             |
| <dl> <span data-ttu-id="80968-126"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="80968-126"><dt>7</dt></span></span> </dl>                                                        | <span data-ttu-id="80968-127">Disattiva + Disabilita</span><span class="sxs-lookup"><span data-stu-id="80968-127">Deactivate + Disable</span></span><br/>                          |
| <dl> <span data-ttu-id="80968-128"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="80968-128"><dt>8</dt></span></span> </dl>                                                        | <span data-ttu-id="80968-129">SetOwnerInstall \_ true</span><span class="sxs-lookup"><span data-stu-id="80968-129">SetOwnerInstall\_True</span></span><br/>                         |
| <dl> <span data-ttu-id="80968-130"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="80968-130"><dt>9</dt></span></span> </dl>                                                        | <span data-ttu-id="80968-131">SetOwnerInstall \_ false</span><span class="sxs-lookup"><span data-stu-id="80968-131">SetOwnerInstall\_False</span></span><br/>                        |
| <dl> <span data-ttu-id="80968-132"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="80968-132"><dt>10</dt></span></span> </dl>                                                       | <span data-ttu-id="80968-133">Enable + Activate + SetOwnerInstall \_ true</span><span class="sxs-lookup"><span data-stu-id="80968-133">Enable + Activate + SetOwnerInstall\_True</span></span><br/>     |
| <dl> <span data-ttu-id="80968-134"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="80968-134"><dt>11</dt></span></span> </dl>                                                       | <span data-ttu-id="80968-135">SetOwnerInstall \_ false + disattiva + Disabilita</span><span class="sxs-lookup"><span data-stu-id="80968-135">SetOwnerInstall\_False + Deactivate + Disable</span></span><br/> |
| <dl> <span data-ttu-id="80968-136"><dt></dt><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="80968-136"><dt></dt> <dt>12</dt></span></span> </dl> | <span data-ttu-id="80968-137">PresenceunownedFieldUpgrade fisico posticipato</span><span class="sxs-lookup"><span data-stu-id="80968-137">Deferred Physical PresenceunownedFieldUpgrade</span></span><br/> |
| <dl> <span data-ttu-id="80968-138"><dt></dt><dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="80968-138"><dt></dt> <dt>14</dt></span></span> </dl> | <span data-ttu-id="80968-139">Deselezionare + Abilita + attiva</span><span class="sxs-lookup"><span data-stu-id="80968-139">Clear + Enable + Activate</span></span><br/>                     |
| <dl> <span data-ttu-id="80968-140"><dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="80968-140"><dt>15</dt></span></span> </dl>                                                       | <span data-ttu-id="80968-141">SetNoPPIProvision \_ false</span><span class="sxs-lookup"><span data-stu-id="80968-141">SetNoPPIProvision\_False</span></span><br/>                      |
| <dl> <span data-ttu-id="80968-142"><dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="80968-142"><dt>16</dt></span></span> </dl>                                                       | <span data-ttu-id="80968-143">SetNoPPIProvision \_ true</span><span class="sxs-lookup"><span data-stu-id="80968-143">SetNoPPIProvision\_True</span></span><br/>                       |
| <dl> <span data-ttu-id="80968-144"><dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="80968-144"><dt>17</dt></span></span> </dl>                                                       | <span data-ttu-id="80968-145">SetNoPPIClear \_ false</span><span class="sxs-lookup"><span data-stu-id="80968-145">SetNoPPIClear\_False</span></span><br/>                          |
| <dl> <span data-ttu-id="80968-146"><dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="80968-146"><dt>18</dt></span></span> </dl>                                                       | <span data-ttu-id="80968-147">SetNoPPIClear \_ true</span><span class="sxs-lookup"><span data-stu-id="80968-147">SetNoPPIClear\_True</span></span><br/>                           |
| <dl> <span data-ttu-id="80968-148"><dt>19</dt></span><span class="sxs-lookup"><span data-stu-id="80968-148"><dt>19</dt></span></span> </dl>                                                       | <span data-ttu-id="80968-149">SetNoPPIMaintenance \_ false</span><span class="sxs-lookup"><span data-stu-id="80968-149">SetNoPPIMaintenance\_False</span></span><br/>                    |
| <dl> <span data-ttu-id="80968-150"><dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="80968-150"><dt>20</dt></span></span> </dl>                                                       | <span data-ttu-id="80968-151">SetNoPPIMaintenance \_ true</span><span class="sxs-lookup"><span data-stu-id="80968-151">SetNoPPIMaintenance\_True</span></span><br/>                     |
| <dl> <span data-ttu-id="80968-152"><dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="80968-152"><dt>21</dt></span></span> </dl>                                                       | <span data-ttu-id="80968-153">Abilita + attiva + Cancella</span><span class="sxs-lookup"><span data-stu-id="80968-153">Enable + Activate + Clear</span></span><br/>                     |
| <dl> <span data-ttu-id="80968-154"><dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="80968-154"><dt>22</dt></span></span> </dl>                                                       | <span data-ttu-id="80968-155">Abilita + attiva + Cancella + Abilita + attiva</span><span class="sxs-lookup"><span data-stu-id="80968-155">Enable + Activate + Clear + Enable + Activate</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="80968-156">*ConfirmationStatus* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="80968-156">*ConfirmationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80968-157">Restituisce lo stato di conferma per il comando presenza fisica.</span><span class="sxs-lookup"><span data-stu-id="80968-157">Returns the confirmation status for physical presence command.</span></span>

<span data-ttu-id="80968-158">Il parametro *ConfirmationStatus* può essere costituito dai valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="80968-158">The *ConfirmationStatus* parameter may consist of the following values.</span></span>



| <span data-ttu-id="80968-159">Valore</span><span class="sxs-lookup"><span data-stu-id="80968-159">Value</span></span>                                                                        | <span data-ttu-id="80968-160">Significato</span><span class="sxs-lookup"><span data-stu-id="80968-160">Meaning</span></span>                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="80968-161"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="80968-161"><dt>0</dt></span></span> </dl> | <span data-ttu-id="80968-162">Non implementato</span><span class="sxs-lookup"><span data-stu-id="80968-162">Not implemented</span></span><br/>                                             |
| <dl> <span data-ttu-id="80968-163"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="80968-163"><dt>1</dt></span></span> </dl> | <span data-ttu-id="80968-164">Solo BIOS.</span><span class="sxs-lookup"><span data-stu-id="80968-164">BIOS only.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="80968-165"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="80968-165"><dt>2</dt></span></span> </dl> | <span data-ttu-id="80968-166">Bloccato per il sistema operativo dalla configurazione del BIOS.</span><span class="sxs-lookup"><span data-stu-id="80968-166">Blocked for the operating system by the BIOS configuration.</span></span><br/> |
| <dl> <span data-ttu-id="80968-167"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="80968-167"><dt>3</dt></span></span> </dl> | <span data-ttu-id="80968-168">È necessario che l'utente sia consentito e fisicamente presente.</span><span class="sxs-lookup"><span data-stu-id="80968-168">Allowed and physically present user required.</span></span><br/>               |
| <dl> <span data-ttu-id="80968-169"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="80968-169"><dt>4</dt></span></span> </dl> | <span data-ttu-id="80968-170">Utenti consentiti e fisicamente presenti non necessari</span><span class="sxs-lookup"><span data-stu-id="80968-170">Allowed and physically present user not required</span></span><br/>            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80968-171">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="80968-171">Return value</span></span>

<span data-ttu-id="80968-172">È possibile restituire tutti gli errori del TPM, nonché gli errori specifici [dei servizi di base TPM](../tbs/tbs-return-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="80968-172">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="80968-173">I codici restituiti comuni sono elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="80968-173">Common return codes are listed below.</span></span>



| <span data-ttu-id="80968-174">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="80968-174">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="80968-175">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80968-175">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="80968-176"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="80968-176"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="80968-177">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="80968-177">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="80968-178">Commenti</span><span class="sxs-lookup"><span data-stu-id="80968-178">Remarks</span></span>

<span data-ttu-id="80968-179">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="80968-179">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="80968-180">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="80968-180">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="80968-181">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="80968-181">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="80968-182">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="80968-182">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="80968-183">Requisiti</span><span class="sxs-lookup"><span data-stu-id="80968-183">Requirements</span></span>



| <span data-ttu-id="80968-184">Requisito</span><span class="sxs-lookup"><span data-stu-id="80968-184">Requirement</span></span> | <span data-ttu-id="80968-185">Valore</span><span class="sxs-lookup"><span data-stu-id="80968-185">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="80968-186">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="80968-186">Minimum supported client</span></span><br/> | <span data-ttu-id="80968-187">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="80968-187">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="80968-188">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="80968-188">Minimum supported server</span></span><br/> | <span data-ttu-id="80968-189">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="80968-189">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="80968-190">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="80968-190">Namespace</span></span><br/>                | <span data-ttu-id="80968-191">\\\\.\\ radice \\ CIMV2 \\ sicurezza \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="80968-191">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="80968-192">MOF</span><span class="sxs-lookup"><span data-stu-id="80968-192">MOF</span></span><br/>                      | <dl> <span data-ttu-id="80968-193"><dt>\_TPM Win32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="80968-193"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="80968-194">DLL</span><span class="sxs-lookup"><span data-stu-id="80968-194">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80968-195"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="80968-195"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80968-196">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="80968-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80968-197">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="80968-197">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
