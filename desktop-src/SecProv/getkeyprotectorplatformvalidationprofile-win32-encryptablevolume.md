---
description: Recupera il profilo di convalida della piattaforma per una protezione con chiave specificata del tipo appropriato.
ms.assetid: 45fa6ba7-169c-4753-8586-0029a7650acc
title: Metodo GetKeyProtectorPlatformValidationProfile della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorPlatformValidationProfile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: b9b951d3ce9eab52687730831f7052942fcbec93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316104"
---
# <a name="getkeyprotectorplatformvalidationprofile-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="85ce7-103">Metodo GetKeyProtectorPlatformValidationProfile della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="85ce7-103">GetKeyProtectorPlatformValidationProfile method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="85ce7-104">Il metodo **GetKeyProtectorPlatformValidationProfile** Recupera il profilo di convalida della piattaforma per una protezione con chiave specificata del tipo appropriato.</span><span class="sxs-lookup"><span data-stu-id="85ce7-104">The **GetKeyProtectorPlatformValidationProfile** method retrieves the platform validation profile for a given key protector of the appropriate type.</span></span>

<span data-ttu-id="85ce7-105">L'identificatore della protezione con chiave deve fare riferimento a una protezione con chiave di tipo "TPM", "TPM e PIN", "TPM, PIN e chiave di avvio" oppure "TPM e chiave di avvio".</span><span class="sxs-lookup"><span data-stu-id="85ce7-105">The key protector identifier must refer to a key protector of type "TPM", "TPM And PIN", "TPM And PIN And Startup Key", or "TPM And Startup Key".</span></span>

## <a name="syntax"></a><span data-ttu-id="85ce7-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="85ce7-106">Syntax</span></span>


```mof
uint32 GetKeyProtectorPlatformValidationProfile(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  PlatformValidationProfile[]
);
```



## <a name="parameters"></a><span data-ttu-id="85ce7-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="85ce7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85ce7-108">*VolumeKeyProtectorID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85ce7-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85ce7-109">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="85ce7-109">Type: **string**</span></span>

<span data-ttu-id="85ce7-110">Identificatore di stringa univoco utilizzato per gestire una protezione con chiave del volume crittografata.</span><span class="sxs-lookup"><span data-stu-id="85ce7-110">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="85ce7-111">*PlatformValidationProfile* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="85ce7-111">*PlatformValidationProfile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85ce7-112">Tipo: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="85ce7-112">Type: **uint8\[\]**</span></span>

<span data-ttu-id="85ce7-113">Matrice di valori integer che specifica il modo in cui l'hardware di sicurezza del Trusted Platform Module (TPM) del computer protegge la chiave di crittografia del volume del disco.</span><span class="sxs-lookup"><span data-stu-id="85ce7-113">An array of integers that specifies how the Trusted Platform Module (TPM) Security Hardware of the computer secures the encryption key of the disk volume.</span></span>



| <span data-ttu-id="85ce7-114">Valore</span><span class="sxs-lookup"><span data-stu-id="85ce7-114">Value</span></span>                                                                         | <span data-ttu-id="85ce7-115">Significato</span><span class="sxs-lookup"><span data-stu-id="85ce7-115">Meaning</span></span>                                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="85ce7-116"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="85ce7-116"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="85ce7-117">Radice principale di Trust of Measurement (CRTM), BIOS ed estensioni della piattaforma</span><span class="sxs-lookup"><span data-stu-id="85ce7-117">Core Root of Trust of Measurement (CRTM), BIOS, and Platform Extensions</span></span><br/> |
| <dl> <span data-ttu-id="85ce7-118"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="85ce7-118"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="85ce7-119">Configurazione e dati della piattaforma e della scheda madre</span><span class="sxs-lookup"><span data-stu-id="85ce7-119">Platform and Motherboard Configuration and Data</span></span><br/>                         |
| <dl> <span data-ttu-id="85ce7-120"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="85ce7-120"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="85ce7-121">Codice ROM opzione</span><span class="sxs-lookup"><span data-stu-id="85ce7-121">Option ROM Code</span></span><br/>                                                         |
| <dl> <span data-ttu-id="85ce7-122"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="85ce7-122"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="85ce7-123">Configurazione e dati dell'opzione ROM</span><span class="sxs-lookup"><span data-stu-id="85ce7-123">Option ROM Configuration and Data</span></span><br/>                                       |
| <dl> <span data-ttu-id="85ce7-124"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="85ce7-124"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="85ce7-125">Codice MBR (master boot record)</span><span class="sxs-lookup"><span data-stu-id="85ce7-125">Master Boot Record (MBR) Code</span></span><br/>                                           |
| <dl> <span data-ttu-id="85ce7-126"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="85ce7-126"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="85ce7-127">Tabella di partizione MBR (record di avvio principale)</span><span class="sxs-lookup"><span data-stu-id="85ce7-127">Master Boot Record (MBR) Partition Table</span></span><br/>                                |
| <dl> <span data-ttu-id="85ce7-128"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="85ce7-128"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="85ce7-129">Eventi di riattivazione e transizione di stato</span><span class="sxs-lookup"><span data-stu-id="85ce7-129">State Transition and Wake Events</span></span><br/>                                        |
| <dl> <span data-ttu-id="85ce7-130"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="85ce7-130"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="85ce7-131">Manufacturer-Specific computer</span><span class="sxs-lookup"><span data-stu-id="85ce7-131">Computer Manufacturer-Specific</span></span><br/>                                          |
| <dl> <span data-ttu-id="85ce7-132"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="85ce7-132"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="85ce7-133">Settore di avvio NTFS</span><span class="sxs-lookup"><span data-stu-id="85ce7-133">NTFS Boot Sector</span></span><br/>                                                        |
| <dl> <span data-ttu-id="85ce7-134"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="85ce7-134"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="85ce7-135">Blocco di avvio NTFS</span><span class="sxs-lookup"><span data-stu-id="85ce7-135">NTFS Boot Block</span></span><br/>                                                         |
| <dl> <span data-ttu-id="85ce7-136"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="85ce7-136"><dt>10</dt></span></span> </dl> | <span data-ttu-id="85ce7-137">Gestione avvio</span><span class="sxs-lookup"><span data-stu-id="85ce7-137">Boot Manager</span></span><br/>                                                            |
| <dl> <span data-ttu-id="85ce7-138"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="85ce7-138"><dt>11</dt></span></span> </dl> | <span data-ttu-id="85ce7-139">Controllo di accesso di BitLocker</span><span class="sxs-lookup"><span data-stu-id="85ce7-139">BitLocker Access Control</span></span><br/>                                                |
| <dl> <span data-ttu-id="85ce7-140"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="85ce7-140"><dt>12</dt></span></span> </dl> | <span data-ttu-id="85ce7-141">Definito per l'utilizzo da parte del sistema operativo statico</span><span class="sxs-lookup"><span data-stu-id="85ce7-141">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="85ce7-142"><dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="85ce7-142"><dt>13</dt></span></span> </dl> | <span data-ttu-id="85ce7-143">Definito per l'utilizzo da parte del sistema operativo statico</span><span class="sxs-lookup"><span data-stu-id="85ce7-143">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="85ce7-144"><dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="85ce7-144"><dt>14</dt></span></span> </dl> | <span data-ttu-id="85ce7-145">Definito per l'utilizzo da parte del sistema operativo statico</span><span class="sxs-lookup"><span data-stu-id="85ce7-145">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="85ce7-146"><dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="85ce7-146"><dt>15</dt></span></span> </dl> | <span data-ttu-id="85ce7-147">Definito per l'utilizzo da parte del sistema operativo statico</span><span class="sxs-lookup"><span data-stu-id="85ce7-147">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="85ce7-148"><dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="85ce7-148"><dt>16</dt></span></span> </dl> | <span data-ttu-id="85ce7-149">Usato per il debug</span><span class="sxs-lookup"><span data-stu-id="85ce7-149">Used for debugging</span></span><br/>                                                      |
| <dl> <span data-ttu-id="85ce7-150"><dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="85ce7-150"><dt>17</dt></span></span> </dl> | <span data-ttu-id="85ce7-151">CRTM dinamico</span><span class="sxs-lookup"><span data-stu-id="85ce7-151">Dynamic CRTM</span></span><br/>                                                            |
| <dl> <span data-ttu-id="85ce7-152"><dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="85ce7-152"><dt>18</dt></span></span> </dl> | <span data-ttu-id="85ce7-153">Piattaforma definita</span><span class="sxs-lookup"><span data-stu-id="85ce7-153">Platform defined</span></span><br/>                                                        |
| <dl> <span data-ttu-id="85ce7-154"><dt>19</dt></span><span class="sxs-lookup"><span data-stu-id="85ce7-154"><dt>19</dt></span></span> </dl> | <span data-ttu-id="85ce7-155">Usato da un sistema operativo attendibile</span><span class="sxs-lookup"><span data-stu-id="85ce7-155">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="85ce7-156"><dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="85ce7-156"><dt>20</dt></span></span> </dl> | <span data-ttu-id="85ce7-157">Usato da un sistema operativo attendibile</span><span class="sxs-lookup"><span data-stu-id="85ce7-157">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="85ce7-158"><dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="85ce7-158"><dt>21</dt></span></span> </dl> | <span data-ttu-id="85ce7-159">Usato da un sistema operativo attendibile</span><span class="sxs-lookup"><span data-stu-id="85ce7-159">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="85ce7-160"><dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="85ce7-160"><dt>22</dt></span></span> </dl> | <span data-ttu-id="85ce7-161">Usato da un sistema operativo attendibile</span><span class="sxs-lookup"><span data-stu-id="85ce7-161">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="85ce7-162"><dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="85ce7-162"><dt>23</dt></span></span> </dl> | <span data-ttu-id="85ce7-163">Supporto delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="85ce7-163">Application support</span></span><br/>                                                     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85ce7-164">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="85ce7-164">Return value</span></span>

<span data-ttu-id="85ce7-165">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="85ce7-165">Type: **uint32**</span></span>

<span data-ttu-id="85ce7-166">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="85ce7-166">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="85ce7-167">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="85ce7-167">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="85ce7-168">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85ce7-168">Description</span></span>                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="85ce7-169"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="85ce7-169"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="85ce7-170">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="85ce7-170">The method was successful.</span></span><br/>                                                                                                                                        |
| <dl> <span data-ttu-id="85ce7-171"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="85ce7-171"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="85ce7-172">Il parametro *VolumeKeyProtectorID* non fa riferimento a una protezione con chiave di tipo "TPM", "TPM e pin", "TPM, pin e chiave di avvio" oppure "TPM e chiave di avvio".</span><span class="sxs-lookup"><span data-stu-id="85ce7-172">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "TPM", "TPM And PIN", "TPM And PIN And Startup Key", or "TPM And Startup Key".</span></span><br/> |
| <dl> <span data-ttu-id="85ce7-173"><dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="85ce7-173"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="85ce7-174">Nel volume non è abilitato BitLocker.</span><span class="sxs-lookup"><span data-stu-id="85ce7-174">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="85ce7-175">Aggiungere una protezione con chiave per abilitare BitLocker.</span><span class="sxs-lookup"><span data-stu-id="85ce7-175">Add a key protector to enable BitLocker.</span></span><br/>                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="85ce7-176">Commenti</span><span class="sxs-lookup"><span data-stu-id="85ce7-176">Remarks</span></span>

<span data-ttu-id="85ce7-177">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="85ce7-177">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="85ce7-178">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="85ce7-178">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="85ce7-179">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="85ce7-179">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="85ce7-180">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="85ce7-180">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="85ce7-181">Requisiti</span><span class="sxs-lookup"><span data-stu-id="85ce7-181">Requirements</span></span>



| <span data-ttu-id="85ce7-182">Requisito</span><span class="sxs-lookup"><span data-stu-id="85ce7-182">Requirement</span></span> | <span data-ttu-id="85ce7-183">Valore</span><span class="sxs-lookup"><span data-stu-id="85ce7-183">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85ce7-184">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85ce7-184">Minimum supported client</span></span><br/> | <span data-ttu-id="85ce7-185">Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="85ce7-185">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="85ce7-186">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85ce7-186">Minimum supported server</span></span><br/> | <span data-ttu-id="85ce7-187">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="85ce7-187">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="85ce7-188">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="85ce7-188">Namespace</span></span><br/>                | <span data-ttu-id="85ce7-189">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="85ce7-189">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="85ce7-190">MOF</span><span class="sxs-lookup"><span data-stu-id="85ce7-190">MOF</span></span><br/>                      | <dl> <span data-ttu-id="85ce7-191"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="85ce7-191"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85ce7-192">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="85ce7-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85ce7-193">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="85ce7-193">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
