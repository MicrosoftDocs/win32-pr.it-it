---
description: Se il Trusted Platform Module (TPM) è disponibile, questo metodo protegge la chiave di crittografia del volume migliorata da una chiave esterna.
ms.assetid: 58bc2de7-645f-4049-949c-975062f8c8ce
title: Metodo ProtectKeyWithTPMAndStartupKey della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithTPMAndStartupKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 06ab2b9474b3564a567374490d9aeb70448338be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306378"
---
# <a name="protectkeywithtpmandstartupkey-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="6427a-103">Metodo ProtectKeyWithTPMAndStartupKey della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="6427a-103">ProtectKeyWithTPMAndStartupKey method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="6427a-104">Il metodo **ProtectKeyWithTPMAndStartupKey** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) protegge la chiave di crittografia del volume utilizzando l'hardware di sicurezza Trusted Platform Module (TPM) nel computer, se disponibile, migliorato da una chiave esterna che deve essere presentata al computer all'avvio.</span><span class="sxs-lookup"><span data-stu-id="6427a-104">The **ProtectKeyWithTPMAndStartupKey** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key by using the Trusted Platform Module (TPM) Security Hardware on the computer, if available, enhanced by an external key that must be presented to the computer at startup.</span></span>

<span data-ttu-id="6427a-105">Sia la convalida del TPM sia l'input di un dispositivo di memoria USB che contiene la chiave esterna sono necessari per accedere alla chiave di crittografia del volume e sbloccare il contenuto del volume.</span><span class="sxs-lookup"><span data-stu-id="6427a-105">Both validation by the TPM and input of a USB memory device that contains the external key are necessary to access the volume's encryption key and unlock the volume contents.</span></span> <span data-ttu-id="6427a-106">Usare il metodo [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) per salvare la chiave esterna in un file in un dispositivo di memoria USB per l'utilizzo come chiave di avvio.</span><span class="sxs-lookup"><span data-stu-id="6427a-106">Use the [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) method to save this external key to a file on a USB memory device for usage as a startup key.</span></span>

<span data-ttu-id="6427a-107">Questo metodo è applicabile solo al volume che contiene il sistema operativo attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="6427a-107">This method is only applicable for the volume that contains the currently running operating system.</span></span>

<span data-ttu-id="6427a-108">Viene creata una protezione con chiave di tipo "TPM e chiave di avvio" per il volume, se non ne esiste già una.</span><span class="sxs-lookup"><span data-stu-id="6427a-108">A key protector of type "TPM And Startup Key" is created for the volume, if one does not already exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="6427a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6427a-109">Syntax</span></span>


```mof
uint32 ProtectKeyWithTPMAndStartupKey(
  [in, optional] string FriendlyName,
  [in, optional] uint8  PlatformValidationProfile[],
  [in, optional] uint8  ExternalKey[],
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="6427a-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="6427a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6427a-111">*FriendlyName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="6427a-111">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6427a-112">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="6427a-112">Type: **string**</span></span>

<span data-ttu-id="6427a-113">Identificatore di stringa assegnato dall'utente per la protezione con chiave.</span><span class="sxs-lookup"><span data-stu-id="6427a-113">A user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="6427a-114">Se questo parametro non è specificato, viene utilizzato un valore blank.</span><span class="sxs-lookup"><span data-stu-id="6427a-114">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="6427a-115">*PlatformValidationProfile* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="6427a-115">*PlatformValidationProfile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6427a-116">Tipo: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="6427a-116">Type: **uint8\[\]**</span></span>

<span data-ttu-id="6427a-117">Matrice di valori integer che specifica il modo in cui l'hardware di sicurezza del Trusted Platform Module (TPM) del computer protegge la chiave di crittografia del volume del disco.</span><span class="sxs-lookup"><span data-stu-id="6427a-117">An array of integers that specifies how the computer's Trusted Platform Module (TPM) Security Hardware secures the encryption key of the disk volume.</span></span>

<span data-ttu-id="6427a-118">Un profilo di convalida della piattaforma è costituito da un set di indici di registro di configurazione della piattaforma (PCR) compresi tra 0 e 23, inclusi.</span><span class="sxs-lookup"><span data-stu-id="6427a-118">A platform validation profile consists of a set of Platform Configuration Register (PCR) indices ranging from 0 to 23, inclusive.</span></span> <span data-ttu-id="6427a-119">I valori repeat nel parametro vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="6427a-119">Repeat values in the parameter are ignored.</span></span> <span data-ttu-id="6427a-120">Ogni indice di PCR è associato ai servizi che vengono eseguiti all'avvio del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="6427a-120">Each PCR index is associated with services that run when the operating system starts.</span></span> <span data-ttu-id="6427a-121">Ogni volta che il computer viene avviato, il TPM verificherà che i servizi specificati nel profilo di convalida della piattaforma non siano stati modificati.</span><span class="sxs-lookup"><span data-stu-id="6427a-121">Each time the computer starts, the TPM will check that the services you specified in the platform validation profile have not changed.</span></span> <span data-ttu-id="6427a-122">Se uno di questi servizi viene modificato mentre la protezione Crittografia unità BitLocker (BDE) rimane attiva, il TPM non rilascia la chiave di crittografia per sbloccare il volume del disco e il computer entrerà in modalità di ripristino.</span><span class="sxs-lookup"><span data-stu-id="6427a-122">If any of these services change while BitLocker Drive Encryption (BDE) protection remains on, the TPM will not release the encryption key to unlock the disk volume, and the computer will enter into recovery mode.</span></span>

<span data-ttu-id="6427a-123">Se questo parametro viene specificato mentre l'impostazione Criteri di gruppo corrispondente è stata abilitata, deve corrispondere all'impostazione Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="6427a-123">If this parameter is specified while the corresponding Group Policy setting has been enabled, it must match the Group Policy setting.</span></span>

<span data-ttu-id="6427a-124">Se questo parametro non è specificato, viene usato il valore predefinito 0, 2, 4, 5, 8, 9, 10 e 11.</span><span class="sxs-lookup"><span data-stu-id="6427a-124">If this parameter is not specified, the default of 0, 2, 4, 5, 8, 9, 10, and 11 is used.</span></span> <span data-ttu-id="6427a-125">Il profilo di convalida della piattaforma predefinito protegge la chiave di crittografia in base alle modifiche apportate agli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="6427a-125">The default platform validation profile secures the encryption key against changes to the following elements:</span></span>

-   <span data-ttu-id="6427a-126">Radice principale di Trust of Measurement (CRTM)</span><span class="sxs-lookup"><span data-stu-id="6427a-126">Core Root of Trust of Measurement (CRTM)</span></span>
-   <span data-ttu-id="6427a-127">BIOS</span><span class="sxs-lookup"><span data-stu-id="6427a-127">BIOS</span></span>
-   <span data-ttu-id="6427a-128">Estensioni della piattaforma (PCR 0)</span><span class="sxs-lookup"><span data-stu-id="6427a-128">Platform Extensions (PCR 0)</span></span>
-   <span data-ttu-id="6427a-129">Codice dell'opzione ROM (PCR 2)</span><span class="sxs-lookup"><span data-stu-id="6427a-129">Option ROM Code (PCR 2)</span></span>
-   <span data-ttu-id="6427a-130">Codice MBR (master boot record) (PCR 4)</span><span class="sxs-lookup"><span data-stu-id="6427a-130">Master Boot Record (MBR) Code (PCR 4)</span></span>
-   <span data-ttu-id="6427a-131">Tabella di partizione MBR (record di avvio principale) (PCR 5)</span><span class="sxs-lookup"><span data-stu-id="6427a-131">Master Boot Record (MBR) Partition Table (PCR 5)</span></span>
-   <span data-ttu-id="6427a-132">Settore di avvio NTFS (PCR 8)</span><span class="sxs-lookup"><span data-stu-id="6427a-132">NTFS Boot Sector (PCR 8)</span></span>
-   <span data-ttu-id="6427a-133">Blocco di avvio NTFS (PCR 9)</span><span class="sxs-lookup"><span data-stu-id="6427a-133">NTFS Boot Block (PCR 9)</span></span>
-   <span data-ttu-id="6427a-134">Boot Manager (PCR 10)</span><span class="sxs-lookup"><span data-stu-id="6427a-134">Boot Manager (PCR 10)</span></span>
-   <span data-ttu-id="6427a-135">Controllo di accesso di BitLocker (PCR 11)</span><span class="sxs-lookup"><span data-stu-id="6427a-135">BitLocker Access Control (PCR 11)</span></span>

<span data-ttu-id="6427a-136">Per la sicurezza del computer, è consigliabile usare il profilo predefinito.</span><span class="sxs-lookup"><span data-stu-id="6427a-136">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="6427a-137">Per una protezione aggiuntiva dalle modifiche di configurazione all'avvio iniziale, usare un profilo di PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span><span class="sxs-lookup"><span data-stu-id="6427a-137">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span> <span data-ttu-id="6427a-138">Per impostazione predefinita, i computer basati su Unified Extensible Firmware Interface (UEFI) non utilizzano PCR 5.</span><span class="sxs-lookup"><span data-stu-id="6427a-138">Unified Extensible Firmware Interface (UEFI)–based computers do not use PCR 5 by default.</span></span>

<span data-ttu-id="6427a-139">La modifica dal profilo predefinito influiscono sulla sicurezza e la gestibilità del computer.</span><span class="sxs-lookup"><span data-stu-id="6427a-139">Changing from the default profile affects the security and manageability of your computer.</span></span> <span data-ttu-id="6427a-140">La riservatezza delle modifiche da BitLocker a piattaforma (dannose o autorizzate) viene aumentata o ridotta a seconda dell'inclusione o dell'esclusione, rispettivamente, del PCRs.</span><span class="sxs-lookup"><span data-stu-id="6427a-140">The sensitivity of BitLocker to platform modifications (malicious or authorized) is increased or decreased depending upon the inclusion or exclusion, respectively, of the PCRs.</span></span> <span data-ttu-id="6427a-141">Per abilitare la protezione BitLocker, è necessario che il profilo di convalida della piattaforma includa PCR 11.</span><span class="sxs-lookup"><span data-stu-id="6427a-141">For BitLocker protection to be enabled, the platform validation profile must include PCR 11.</span></span>



| <span data-ttu-id="6427a-142">Valore</span><span class="sxs-lookup"><span data-stu-id="6427a-142">Value</span></span>                                                                         | <span data-ttu-id="6427a-143">Significato</span><span class="sxs-lookup"><span data-stu-id="6427a-143">Meaning</span></span>                                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6427a-144"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6427a-144"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="6427a-145">Radice principale di Trust of Measurement (CRTM), BIOS ed estensioni della piattaforma</span><span class="sxs-lookup"><span data-stu-id="6427a-145">Core Root of Trust of Measurement (CRTM), BIOS, and Platform Extensions</span></span><br/> |
| <dl> <span data-ttu-id="6427a-146"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6427a-146"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="6427a-147">Configurazione e dati della piattaforma e della scheda madre</span><span class="sxs-lookup"><span data-stu-id="6427a-147">Platform and Motherboard Configuration and Data</span></span><br/>                         |
| <dl> <span data-ttu-id="6427a-148"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6427a-148"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="6427a-149">Codice ROM opzione</span><span class="sxs-lookup"><span data-stu-id="6427a-149">Option ROM Code</span></span><br/>                                                         |
| <dl> <span data-ttu-id="6427a-150"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="6427a-150"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="6427a-151">Configurazione e dati dell'opzione ROM</span><span class="sxs-lookup"><span data-stu-id="6427a-151">Option ROM Configuration and Data</span></span><br/>                                       |
| <dl> <span data-ttu-id="6427a-152"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="6427a-152"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="6427a-153">Codice MBR (master boot record)</span><span class="sxs-lookup"><span data-stu-id="6427a-153">Master Boot Record (MBR) Code</span></span><br/>                                           |
| <dl> <span data-ttu-id="6427a-154"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="6427a-154"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="6427a-155">Tabella di partizione MBR (record di avvio principale)</span><span class="sxs-lookup"><span data-stu-id="6427a-155">Master Boot Record (MBR) Partition Table</span></span><br/>                                |
| <dl> <span data-ttu-id="6427a-156"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="6427a-156"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="6427a-157">Eventi di riattivazione e transizione di stato</span><span class="sxs-lookup"><span data-stu-id="6427a-157">State Transition and Wake Events</span></span><br/>                                        |
| <dl> <span data-ttu-id="6427a-158"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="6427a-158"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="6427a-159">Manufacturer-Specific computer</span><span class="sxs-lookup"><span data-stu-id="6427a-159">Computer Manufacturer-Specific</span></span><br/>                                          |
| <dl> <span data-ttu-id="6427a-160"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="6427a-160"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="6427a-161">Settore di avvio NTFS</span><span class="sxs-lookup"><span data-stu-id="6427a-161">NTFS Boot Sector</span></span><br/>                                                        |
| <dl> <span data-ttu-id="6427a-162"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="6427a-162"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="6427a-163">Blocco di avvio NTFS</span><span class="sxs-lookup"><span data-stu-id="6427a-163">NTFS Boot Block</span></span><br/>                                                         |
| <dl> <span data-ttu-id="6427a-164"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="6427a-164"><dt>10</dt></span></span> </dl> | <span data-ttu-id="6427a-165">Gestione avvio</span><span class="sxs-lookup"><span data-stu-id="6427a-165">Boot Manager</span></span><br/>                                                            |
| <dl> <span data-ttu-id="6427a-166"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="6427a-166"><dt>11</dt></span></span> </dl> | <span data-ttu-id="6427a-167">Controllo di accesso di BitLocker</span><span class="sxs-lookup"><span data-stu-id="6427a-167">BitLocker Access Control</span></span><br/>                                                |
| <dl> <span data-ttu-id="6427a-168"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="6427a-168"><dt>12</dt></span></span> </dl> | <span data-ttu-id="6427a-169">Definito per l'utilizzo da parte del sistema operativo statico</span><span class="sxs-lookup"><span data-stu-id="6427a-169">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="6427a-170"><dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="6427a-170"><dt>13</dt></span></span> </dl> | <span data-ttu-id="6427a-171">Definito per l'utilizzo da parte del sistema operativo statico</span><span class="sxs-lookup"><span data-stu-id="6427a-171">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="6427a-172"><dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="6427a-172"><dt>14</dt></span></span> </dl> | <span data-ttu-id="6427a-173">Definito per l'utilizzo da parte del sistema operativo statico</span><span class="sxs-lookup"><span data-stu-id="6427a-173">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="6427a-174"><dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="6427a-174"><dt>15</dt></span></span> </dl> | <span data-ttu-id="6427a-175">Definito per l'utilizzo da parte del sistema operativo statico</span><span class="sxs-lookup"><span data-stu-id="6427a-175">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="6427a-176"><dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="6427a-176"><dt>16</dt></span></span> </dl> | <span data-ttu-id="6427a-177">Usato per il debug</span><span class="sxs-lookup"><span data-stu-id="6427a-177">Used for debugging</span></span><br/>                                                      |
| <dl> <span data-ttu-id="6427a-178"><dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="6427a-178"><dt>17</dt></span></span> </dl> | <span data-ttu-id="6427a-179">CRTM dinamico</span><span class="sxs-lookup"><span data-stu-id="6427a-179">Dynamic CRTM</span></span><br/>                                                            |
| <dl> <span data-ttu-id="6427a-180"><dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="6427a-180"><dt>18</dt></span></span> </dl> | <span data-ttu-id="6427a-181">Piattaforma definita</span><span class="sxs-lookup"><span data-stu-id="6427a-181">Platform defined</span></span><br/>                                                        |
| <dl> <span data-ttu-id="6427a-182"><dt>19</dt></span><span class="sxs-lookup"><span data-stu-id="6427a-182"><dt>19</dt></span></span> </dl> | <span data-ttu-id="6427a-183">Usato da un sistema operativo attendibile</span><span class="sxs-lookup"><span data-stu-id="6427a-183">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="6427a-184"><dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="6427a-184"><dt>20</dt></span></span> </dl> | <span data-ttu-id="6427a-185">Usato da un sistema operativo attendibile</span><span class="sxs-lookup"><span data-stu-id="6427a-185">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="6427a-186"><dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="6427a-186"><dt>21</dt></span></span> </dl> | <span data-ttu-id="6427a-187">Usato da un sistema operativo attendibile</span><span class="sxs-lookup"><span data-stu-id="6427a-187">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="6427a-188"><dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="6427a-188"><dt>22</dt></span></span> </dl> | <span data-ttu-id="6427a-189">Usato da un sistema operativo attendibile</span><span class="sxs-lookup"><span data-stu-id="6427a-189">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="6427a-190"><dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="6427a-190"><dt>23</dt></span></span> </dl> | <span data-ttu-id="6427a-191">Supporto delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="6427a-191">Application support</span></span><br/>                                                     |



 

</dd> <dt>

<span data-ttu-id="6427a-192">*ExternalKey* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="6427a-192">*ExternalKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6427a-193">Tipo: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="6427a-193">Type: **uint8\[\]**</span></span>

<span data-ttu-id="6427a-194">Matrice di byte che specifica la chiave esterna a 256 bit utilizzata per sbloccare il volume all'avvio del computer.</span><span class="sxs-lookup"><span data-stu-id="6427a-194">An array of bytes that specifies the 256-bit external key used to unlock the volume when the computer starts.</span></span>

<span data-ttu-id="6427a-195">Se non viene specificata alcuna chiave esterna, ne viene generata una in modo casuale.</span><span class="sxs-lookup"><span data-stu-id="6427a-195">If no external key is specified, one is randomly generated.</span></span> <span data-ttu-id="6427a-196">Usare il metodo [**GetKeyProtectorExternalKey**](getkeyprotectorexternalkey-win32-encryptablevolume.md) per ottenere la chiave generata in modo casuale.</span><span class="sxs-lookup"><span data-stu-id="6427a-196">Use the [**GetKeyProtectorExternalKey**](getkeyprotectorexternalkey-win32-encryptablevolume.md) method to obtain the randomly generated key.</span></span>

</dd> <dt>

<span data-ttu-id="6427a-197">*VolumeKeyProtectorID* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6427a-197">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6427a-198">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="6427a-198">Type: **string**</span></span>

<span data-ttu-id="6427a-199">Stringa che rappresenta l'identificatore univoco associato alla protezione con chiave creata che può essere utilizzata per gestire la protezione con chiave.</span><span class="sxs-lookup"><span data-stu-id="6427a-199">A string that is the unique identifier associated with the created key protector that can be used to manage the key protector.</span></span>

<span data-ttu-id="6427a-200">Se l'unità supporta la crittografia hardware e BitLocker non ha assunto la proprietà della banda, la stringa ID è impostata su "BitLocker" e la protezione con chiave viene scritta in base ai metadati della banda.</span><span class="sxs-lookup"><span data-stu-id="6427a-200">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6427a-201">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6427a-201">Return value</span></span>

<span data-ttu-id="6427a-202">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6427a-202">Type: **uint32**</span></span>

<span data-ttu-id="6427a-203">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="6427a-203">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="6427a-204">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="6427a-204">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="6427a-205">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6427a-205">Description</span></span>                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6427a-206"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="6427a-206"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="6427a-207">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="6427a-207">The method was successful.</span></span><br/>                                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="6427a-208"><dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="6427a-208"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>        | <span data-ttu-id="6427a-209">Il volume è bloccato.</span><span class="sxs-lookup"><span data-stu-id="6427a-209">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="6427a-210"><dt>**TBS \_ \_Servizio E \_ non \_ in esecuzione**</dt> <dt>2150121480 (0x80284008)</dt></span><span class="sxs-lookup"><span data-stu-id="6427a-210"><dt>**TBS\_E\_SERVICE\_NOT\_RUNNING**</dt> <dt>2150121480 (0x80284008)</dt></span></span> </dl> | <span data-ttu-id="6427a-211">Nel computer non è stato trovato alcun TPM compatibile.</span><span class="sxs-lookup"><span data-stu-id="6427a-211">No compatible TPM is found on this computer.</span></span><br/>                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="6427a-212"><dt>**FVE \_ E \_ \_ VOLUME esterno**</dt> <dt>2150694947 (0x80310023)</dt></span><span class="sxs-lookup"><span data-stu-id="6427a-212"><dt>**FVE\_E\_FOREIGN\_VOLUME**</dt> <dt>2150694947 (0x80310023)</dt></span></span> </dl>       | <span data-ttu-id="6427a-213">Il TPM non è in grado di proteggere la chiave di crittografia del volume perché il volume non contiene il sistema operativo attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="6427a-213">The TPM cannot secure the volume's encryption key because the volume does not contain the currently running operating system.</span></span><br/>                                                                                                                               |
| <dl> <span data-ttu-id="6427a-214"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="6427a-214"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                 | <span data-ttu-id="6427a-215">Viene specificato il parametro *PlatformValidationProfile* , ma i relativi valori non rientrano nell'intervallo noto oppure non corrisponde all'impostazione criteri di gruppo attualmente attiva.</span><span class="sxs-lookup"><span data-stu-id="6427a-215">The *PlatformValidationProfile* parameter is provided, but its values are not within the known range, or it does not match the Group Policy setting currently in effect.</span></span><br/> <span data-ttu-id="6427a-216">Il parametro *ExternalKey* è specificato ma non è una matrice di dimensione 32.</span><span class="sxs-lookup"><span data-stu-id="6427a-216">The *ExternalKey* parameter is provided but is not an array of size 32.</span></span><br/> |
| <dl> <span data-ttu-id="6427a-217"><dt>**FVE \_ E \_ \_ CDDVD di avvio**</dt> <dt>2150694960 (0x80310030)</dt></span><span class="sxs-lookup"><span data-stu-id="6427a-217"><dt>**FVE\_E\_BOOTABLE\_CDDVD**</dt> <dt>2150694960 (0x80310030)</dt></span></span> </dl>       | <span data-ttu-id="6427a-218">Nel computer è presente un CD/DVD di avvio.</span><span class="sxs-lookup"><span data-stu-id="6427a-218">A bootable CD/DVD is found in this computer.</span></span> <span data-ttu-id="6427a-219">Rimuovere il CD/DVD e riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="6427a-219">Remove the CD/DVD and restart the computer.</span></span><br/>                                                                                                                                                                    |
| <dl> <span data-ttu-id="6427a-220"><dt>**FVE \_ La \_ protezione E \_ esiste**</dt> <dt>2150694961 (0x80310031)</dt></span><span class="sxs-lookup"><span data-stu-id="6427a-220"><dt>**FVE\_E\_PROTECTOR\_EXISTS**</dt> <dt>2150694961 (0x80310031)</dt></span></span> </dl>     | <span data-ttu-id="6427a-221">Esiste già una protezione con chiave di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="6427a-221">A key protector of this type already exists.</span></span><br/>                                                                                                                                                                                                                |



 

## <a name="security-considerations"></a><span data-ttu-id="6427a-222">Considerazioni relative alla sicurezza</span><span class="sxs-lookup"><span data-stu-id="6427a-222">Security Considerations</span></span>

<span data-ttu-id="6427a-223">Per la sicurezza del computer, è consigliabile usare il profilo predefinito.</span><span class="sxs-lookup"><span data-stu-id="6427a-223">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="6427a-224">Per una protezione aggiuntiva dalle prime modifiche del codice di avvio, usare un profilo di PCRs 0, 2, 4, 5, 8, 9, 10 e 11.</span><span class="sxs-lookup"><span data-stu-id="6427a-224">For additional protection against early startup code changes, use a profile of PCRs 0, 2, 4, 5, 8, 9, 10, and 11.</span></span> <span data-ttu-id="6427a-225">Per una protezione aggiuntiva dalle modifiche di configurazione all'avvio iniziale, usare un profilo di PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span><span class="sxs-lookup"><span data-stu-id="6427a-225">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span>

<span data-ttu-id="6427a-226">La modifica dal profilo predefinito influiscono sulla sicurezza o sull'usabilità del computer.</span><span class="sxs-lookup"><span data-stu-id="6427a-226">Changing from the default profile affects the security or usability of your computer.</span></span>

## <a name="remarks"></a><span data-ttu-id="6427a-227">Commenti</span><span class="sxs-lookup"><span data-stu-id="6427a-227">Remarks</span></span>

<span data-ttu-id="6427a-228">Può esistere al massimo una protezione con chiave di tipo "TPM e chiave di avvio" per un volume in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="6427a-228">At most one key protector of type "TPM And Startup Key" can exist for a volume at any time.</span></span> <span data-ttu-id="6427a-229">Se si desidera modificare il nome visualizzato o il profilo di convalida della piattaforma utilizzato da una protezione con chiave "TPM più chiave di avvio" esistente, è necessario innanzitutto rimuovere la protezione con chiave esistente e quindi chiamare **ProtectKeyWithTPMAndStartupKey** per crearne una nuova.</span><span class="sxs-lookup"><span data-stu-id="6427a-229">If you want to change the display name or the platform validation profile used by an existing "TPM plus Startup Key" key protector, you must first remove the existing key protector and then call **ProtectKeyWithTPMAndStartupKey** to create a new one.</span></span> <span data-ttu-id="6427a-230">È necessario specificare protezioni con chiave aggiuntive per sbloccare il volume negli scenari di ripristino in cui non è possibile ottenere l'accesso alla chiave di crittografia del volume. ad esempio, quando il TPM non è in grado di convalidare correttamente il profilo di convalida della piattaforma o quando la memoria USB che contiene la chiave esterna viene persa.</span><span class="sxs-lookup"><span data-stu-id="6427a-230">Additional key protectors should be specified to unlock the volume in recovery scenarios where access to the volume's encryption key cannot be obtained; for example, when the TPM cannot successfully validate against the platform validation profile or when USB memory that contains the external key is lost.</span></span>

<span data-ttu-id="6427a-231">Usare [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) o [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) per creare una o più protezioni con chiave per il ripristino di un volume altrimenti bloccato.</span><span class="sxs-lookup"><span data-stu-id="6427a-231">Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) or [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) to create one or more key protectors for recovering an otherwise locked volume.</span></span>

<span data-ttu-id="6427a-232">Sebbene sia possibile disporre di una protezione con chiave di tipo "TPM" e di un altro tipo "TPM e chiave di avvio", la presenza del tipo di protezione con chiave "TPM" nega gli effetti di altre protezioni con chiave basate su TPM.</span><span class="sxs-lookup"><span data-stu-id="6427a-232">While it is possible to have both a key protector of the type "TPM" and another of the type "TPM And Startup Key", the presence of the "TPM" key protector type negates the effects of other TPM-based key protectors.</span></span>

<span data-ttu-id="6427a-233">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="6427a-233">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6427a-234">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="6427a-234">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="6427a-235">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="6427a-235">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6427a-236">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="6427a-236">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6427a-237">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6427a-237">Requirements</span></span>



| <span data-ttu-id="6427a-238">Requisito</span><span class="sxs-lookup"><span data-stu-id="6427a-238">Requirement</span></span> | <span data-ttu-id="6427a-239">Valore</span><span class="sxs-lookup"><span data-stu-id="6427a-239">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6427a-240">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6427a-240">Minimum supported client</span></span><br/> | <span data-ttu-id="6427a-241">Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="6427a-241">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6427a-242">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6427a-242">Minimum supported server</span></span><br/> | <span data-ttu-id="6427a-243">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6427a-243">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6427a-244">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6427a-244">Namespace</span></span><br/>                | <span data-ttu-id="6427a-245">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="6427a-245">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="6427a-246">MOF</span><span class="sxs-lookup"><span data-stu-id="6427a-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6427a-247"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6427a-247"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6427a-248">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6427a-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6427a-249">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="6427a-249">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="6427a-250">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="6427a-250">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
