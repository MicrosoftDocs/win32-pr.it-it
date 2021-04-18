---
description: Se il Trusted Platform Module (TPM) è disponibile, questo metodo protegge la chiave di crittografia del volume.
ms.assetid: 79bee9ca-c86a-482b-a06f-1cfb887e7fae
title: Metodo ProtectKeyWithTPM della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithTPM
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0369e44d96a4f1dcacf33dbf1b1da6ad6d37eed2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315335"
---
# <a name="protectkeywithtpm-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="c994d-103">Metodo ProtectKeyWithTPM della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="c994d-103">ProtectKeyWithTPM method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="c994d-104">Il metodo **ProtectKeyWithTPM** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) protegge la chiave di crittografia del volume utilizzando l'hardware di sicurezza Trusted Platform Module (TPM) nel computer, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="c994d-104">The **ProtectKeyWithTPM** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key by using the Trusted Platform Module (TPM) Security Hardware on the computer, if available.</span></span>

<span data-ttu-id="c994d-105">Viene creata una protezione con chiave di tipo "TPM" per il volume, se non ne esiste già una.</span><span class="sxs-lookup"><span data-stu-id="c994d-105">A key protector of type "TPM" is created for the volume, if one does not already exist.</span></span>

<span data-ttu-id="c994d-106">Questo metodo è applicabile solo al volume che contiene il sistema operativo attualmente in esecuzione e se una protezione con chiave non esiste già nel volume.</span><span class="sxs-lookup"><span data-stu-id="c994d-106">This method is only applicable for the volume that contains the currently running operating system, and if a key protector does not already exist on the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="c994d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c994d-107">Syntax</span></span>


```mof
uint32 ProtectKeyWithTPM(
  [in, optional] string FriendlyName,
  [in, optional] uint8  PlatformValidationProfile[],
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="c994d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c994d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c994d-109">*FriendlyName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="c994d-109">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c994d-110">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="c994d-110">Type: **string**</span></span>

<span data-ttu-id="c994d-111">Stringa che specifica un identificatore di stringa assegnato dall'utente per la protezione con chiave.</span><span class="sxs-lookup"><span data-stu-id="c994d-111">A string that specifies a user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="c994d-112">Se questo parametro non è specificato, viene utilizzato un valore blank.</span><span class="sxs-lookup"><span data-stu-id="c994d-112">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="c994d-113">*PlatformValidationProfile* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="c994d-113">*PlatformValidationProfile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c994d-114">Tipo: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="c994d-114">Type: **uint8\[\]**</span></span>

<span data-ttu-id="c994d-115">Matrice di valori integer che specifica il modo in cui l'hardware di sicurezza del Trusted Platform Module (TPM) del computer protegge la chiave di crittografia del volume del disco.</span><span class="sxs-lookup"><span data-stu-id="c994d-115">An array of integers that specifies how the computer's Trusted Platform Module (TPM) Security Hardware secures the disk volume's encryption key.</span></span>

<span data-ttu-id="c994d-116">Un profilo di convalida della piattaforma è costituito da un set di indici di registro di configurazione della piattaforma (PCR) compresi tra 0 e 23, inclusi.</span><span class="sxs-lookup"><span data-stu-id="c994d-116">A platform validation profile consists of a set of Platform Configuration Register (PCR) indices ranging from 0 to 23, inclusive.</span></span> <span data-ttu-id="c994d-117">I valori repeat nel parametro vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="c994d-117">Repeat values in the parameter are ignored.</span></span> <span data-ttu-id="c994d-118">Ogni indice di PCR è associato ai servizi che vengono eseguiti all'avvio del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c994d-118">Each PCR index is associated with services that run when the operating system starts.</span></span> <span data-ttu-id="c994d-119">Ogni volta che il computer viene avviato, il TPM verificherà che i servizi specificati nel profilo di convalida della piattaforma non siano stati modificati.</span><span class="sxs-lookup"><span data-stu-id="c994d-119">Each time the computer starts, the TPM will check that the services you specified in the platform validation profile have not changed.</span></span> <span data-ttu-id="c994d-120">Se uno di questi servizi viene modificato mentre la protezione Crittografia unità BitLocker (BDE) rimane attiva, il TPM non rilascia la chiave di crittografia per sbloccare il volume del disco e il computer entrerà in modalità di ripristino.</span><span class="sxs-lookup"><span data-stu-id="c994d-120">If any of these services change while BitLocker Drive Encryption (BDE) protection remains on, the TPM will not release the encryption key to unlock the disk volume and the computer will enter into recovery mode.</span></span>

<span data-ttu-id="c994d-121">Se questo parametro viene specificato mentre l'impostazione Criteri di gruppo corrispondente è stata abilitata, deve corrispondere all'impostazione Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="c994d-121">If this parameter is specified while the corresponding Group Policy setting has been enabled, it must match the Group Policy setting.</span></span>

<span data-ttu-id="c994d-122">Se questo parametro non è specificato, viene usato il valore predefinito 0, 2, 4, 5, 8, 9, 10 e 11.</span><span class="sxs-lookup"><span data-stu-id="c994d-122">If this parameter is not specified, the default of 0, 2, 4, 5, 8, 9, 10, and 11 is used.</span></span> <span data-ttu-id="c994d-123">Il profilo di convalida della piattaforma predefinito protegge la chiave di crittografia in base alle modifiche apportate alla radice principale di Trust of Measurement (CRTM). BIOS, and Platform Extensions (PCR 0), Option ROM code (PCR 2), il codice MBR (master boot record) (PCR 4), la tabella di partizione MBR (master boot record) (PCR 5), il settore di avvio NTFS (PCR 8), il codice di avvio NTFS (PCR 9), Boot Manager (PCR 10) e il controllo di accesso Crittografia unità BitLocker (PCR 11).</span><span class="sxs-lookup"><span data-stu-id="c994d-123">The default platform validation profile secures the encryption key against changes to the Core Root of Trust of Measurement (CRTM), BIOS, and Platform Extensions (PCR 0), Option ROM Code (PCR 2), the Master Boot Record (MBR) Code (PCR 4), the Master Boot Record (MBR) Partition Table (PCR 5), the NTFS Boot Sector (PCR 8), the NTFS Boot Code (PCR 9), the Boot Manager (PCR 10), and the BitLocker Drive Encryption Access Control (PCR 11).</span></span> <span data-ttu-id="c994d-124">Per la sicurezza del computer, è consigliabile usare il profilo predefinito.</span><span class="sxs-lookup"><span data-stu-id="c994d-124">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="c994d-125">Per impostazione predefinita, i computer basati su Unified Extensible Firmware Interface (UEFI) non utilizzano PCR 5.</span><span class="sxs-lookup"><span data-stu-id="c994d-125">Unified Extensible Firmware Interface (UEFI)–based computers do not use PCR 5 by default.</span></span> <span data-ttu-id="c994d-126">Per una protezione aggiuntiva dalle modifiche di configurazione all'avvio iniziale, usare un profilo di PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span><span class="sxs-lookup"><span data-stu-id="c994d-126">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span>

<span data-ttu-id="c994d-127">La modifica dal profilo predefinito influiscono sulla sicurezza e la gestibilità del computer.</span><span class="sxs-lookup"><span data-stu-id="c994d-127">Changing from the default profile affects the security and manageability of your computer.</span></span> <span data-ttu-id="c994d-128">La riservatezza delle modifiche da BitLocker a piattaforma (dannose o autorizzate) viene aumentata o ridotta a seconda dell'inclusione o dell'esclusione, rispettivamente, del PCRs.</span><span class="sxs-lookup"><span data-stu-id="c994d-128">The sensitivity of BitLocker to platform modifications (malicious or authorized) is increased or decreased depending upon the inclusion or exclusion, respectively, of the PCRs.</span></span> <span data-ttu-id="c994d-129">Per abilitare la protezione BitLocker, è necessario che il profilo di convalida della piattaforma includa PCR 11.</span><span class="sxs-lookup"><span data-stu-id="c994d-129">For BitLocker protection to be enabled, the platform validation profile must include PCR 11.</span></span>



| <span data-ttu-id="c994d-130">Valore</span><span class="sxs-lookup"><span data-stu-id="c994d-130">Value</span></span>                                                                         | <span data-ttu-id="c994d-131">Significato</span><span class="sxs-lookup"><span data-stu-id="c994d-131">Meaning</span></span>                                                                             |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c994d-132"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c994d-132"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="c994d-133">Radice principale di Trust of Measurement (CRTM), BIOS ed estensioni della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="c994d-133">Core Root of Trust of Measurement (CRTM), BIOS, and Platform Extensions.</span></span><br/> |
| <dl> <span data-ttu-id="c994d-134"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c994d-134"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="c994d-135">Configurazione e dati della piattaforma e della scheda madre</span><span class="sxs-lookup"><span data-stu-id="c994d-135">Platform and Motherboard Configuration and Data</span></span><br/>                          |
| <dl> <span data-ttu-id="c994d-136"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c994d-136"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="c994d-137">Codice ROM opzione</span><span class="sxs-lookup"><span data-stu-id="c994d-137">Option ROM Code</span></span><br/>                                                          |
| <dl> <span data-ttu-id="c994d-138"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c994d-138"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="c994d-139">Configurazione e dati dell'opzione ROM</span><span class="sxs-lookup"><span data-stu-id="c994d-139">Option ROM Configuration and Data</span></span><br/>                                        |
| <dl> <span data-ttu-id="c994d-140"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="c994d-140"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="c994d-141">Codice MBR (master boot record)</span><span class="sxs-lookup"><span data-stu-id="c994d-141">Master Boot Record (MBR) Code</span></span><br/>                                            |
| <dl> <span data-ttu-id="c994d-142"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="c994d-142"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="c994d-143">Tabella di partizione MBR (record di avvio principale)</span><span class="sxs-lookup"><span data-stu-id="c994d-143">Master Boot Record (MBR) Partition Table</span></span><br/>                                 |
| <dl> <span data-ttu-id="c994d-144"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="c994d-144"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="c994d-145">Eventi di riattivazione e transizione di stato</span><span class="sxs-lookup"><span data-stu-id="c994d-145">State Transition and Wake Events</span></span><br/>                                         |
| <dl> <span data-ttu-id="c994d-146"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="c994d-146"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="c994d-147">Manufacturer-Specific computer</span><span class="sxs-lookup"><span data-stu-id="c994d-147">Computer Manufacturer-Specific</span></span><br/>                                           |
| <dl> <span data-ttu-id="c994d-148"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="c994d-148"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="c994d-149">Settore di avvio NTFS</span><span class="sxs-lookup"><span data-stu-id="c994d-149">NTFS Boot Sector</span></span><br/>                                                         |
| <dl> <span data-ttu-id="c994d-150"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="c994d-150"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="c994d-151">Codice di avvio NTFS</span><span class="sxs-lookup"><span data-stu-id="c994d-151">NTFS Boot Code</span></span><br/>                                                           |
| <dl> <span data-ttu-id="c994d-152"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="c994d-152"><dt>10</dt></span></span> </dl> | <span data-ttu-id="c994d-153">Gestione avvio</span><span class="sxs-lookup"><span data-stu-id="c994d-153">Boot Manager</span></span><br/>                                                             |
| <dl> <span data-ttu-id="c994d-154"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="c994d-154"><dt>11</dt></span></span> </dl> | <span data-ttu-id="c994d-155">Controllo di accesso Crittografia unità BitLocker</span><span class="sxs-lookup"><span data-stu-id="c994d-155">BitLocker Drive Encryption Access Control</span></span><br/>                                |
| <dl> <span data-ttu-id="c994d-156"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="c994d-156"><dt>12</dt></span></span> </dl> | <span data-ttu-id="c994d-157">Definito per l'utilizzo da parte del sistema operativo statico</span><span class="sxs-lookup"><span data-stu-id="c994d-157">Defined for use by the static operating system</span></span><br/>                           |
| <dl> <span data-ttu-id="c994d-158"><dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="c994d-158"><dt>13</dt></span></span> </dl> | <span data-ttu-id="c994d-159">Definito per l'utilizzo da parte del sistema operativo statico</span><span class="sxs-lookup"><span data-stu-id="c994d-159">Defined for use by the static operating system</span></span><br/>                           |
| <dl> <span data-ttu-id="c994d-160"><dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="c994d-160"><dt>14</dt></span></span> </dl> | <span data-ttu-id="c994d-161">Definito per l'utilizzo da parte del sistema operativo statico</span><span class="sxs-lookup"><span data-stu-id="c994d-161">Defined for use by the static operating system</span></span><br/>                           |
| <dl> <span data-ttu-id="c994d-162"><dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="c994d-162"><dt>15</dt></span></span> </dl> | <span data-ttu-id="c994d-163">Definito per l'utilizzo da parte del sistema operativo statico</span><span class="sxs-lookup"><span data-stu-id="c994d-163">Defined for use by the static operating system</span></span><br/>                           |
| <dl> <span data-ttu-id="c994d-164"><dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="c994d-164"><dt>16</dt></span></span> </dl> | <span data-ttu-id="c994d-165">Usato per il debug</span><span class="sxs-lookup"><span data-stu-id="c994d-165">Used for debugging</span></span><br/>                                                       |
| <dl> <span data-ttu-id="c994d-166"><dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="c994d-166"><dt>17</dt></span></span> </dl> | <span data-ttu-id="c994d-167">CRTM dinamico</span><span class="sxs-lookup"><span data-stu-id="c994d-167">Dynamic CRTM</span></span><br/>                                                             |
| <dl> <span data-ttu-id="c994d-168"><dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="c994d-168"><dt>18</dt></span></span> </dl> | <span data-ttu-id="c994d-169">Piattaforma definita</span><span class="sxs-lookup"><span data-stu-id="c994d-169">Platform defined</span></span><br/>                                                         |
| <dl> <span data-ttu-id="c994d-170"><dt>19</dt></span><span class="sxs-lookup"><span data-stu-id="c994d-170"><dt>19</dt></span></span> </dl> | <span data-ttu-id="c994d-171">Utilizzato dal sistema operativo attendibile</span><span class="sxs-lookup"><span data-stu-id="c994d-171">Used by trusted operating system</span></span><br/>                                         |
| <dl> <span data-ttu-id="c994d-172"><dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="c994d-172"><dt>20</dt></span></span> </dl> | <span data-ttu-id="c994d-173">Utilizzato dal sistema operativo attendibile</span><span class="sxs-lookup"><span data-stu-id="c994d-173">Used by trusted operating system</span></span><br/>                                         |
| <dl> <span data-ttu-id="c994d-174"><dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="c994d-174"><dt>21</dt></span></span> </dl> | <span data-ttu-id="c994d-175">Utilizzato dal sistema operativo attendibile</span><span class="sxs-lookup"><span data-stu-id="c994d-175">Used by trusted operating system</span></span><br/>                                         |
| <dl> <span data-ttu-id="c994d-176"><dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="c994d-176"><dt>22</dt></span></span> </dl> | <span data-ttu-id="c994d-177">Utilizzato dal sistema operativo attendibile</span><span class="sxs-lookup"><span data-stu-id="c994d-177">Used by trusted operating system</span></span><br/>                                         |
| <dl> <span data-ttu-id="c994d-178"><dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="c994d-178"><dt>23</dt></span></span> </dl> | <span data-ttu-id="c994d-179">Supporto delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="c994d-179">Application support</span></span><br/>                                                      |



 

</dd> <dt>

<span data-ttu-id="c994d-180">*VolumeKeyProtectorID* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c994d-180">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c994d-181">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="c994d-181">Type: **string**</span></span>

<span data-ttu-id="c994d-182">Stringa che identifica in modo univoco la protezione creata e che può essere utilizzata per gestire la protezione con chiave.</span><span class="sxs-lookup"><span data-stu-id="c994d-182">A string that uniquely identifies the created protector and which can be used to manage the key protector.</span></span>

<span data-ttu-id="c994d-183">Se l'unità supporta la crittografia hardware e BitLocker non ha assunto la proprietà della banda, la stringa ID è impostata su "BitLocker" e la protezione con chiave viene scritta in base ai metadati della banda.</span><span class="sxs-lookup"><span data-stu-id="c994d-183">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c994d-184">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c994d-184">Return value</span></span>

<span data-ttu-id="c994d-185">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c994d-185">Type: **uint32**</span></span>

<span data-ttu-id="c994d-186">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="c994d-186">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="c994d-187">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="c994d-187">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="c994d-188">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c994d-188">Description</span></span>                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c994d-189"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="c994d-189"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="c994d-190">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="c994d-190">The method was successful.</span></span><br/>                                                                                                                                              |
| <dl> <span data-ttu-id="c994d-191"><dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="c994d-191"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>        | <span data-ttu-id="c994d-192">Il volume è bloccato.</span><span class="sxs-lookup"><span data-stu-id="c994d-192">The volume is locked.</span></span><br/>                                                                                                                                                   |
| <dl> <span data-ttu-id="c994d-193"><dt>**TBS \_ \_Servizio E \_ non \_ in esecuzione**</dt> <dt>2150121480 (0x80284008)</dt></span><span class="sxs-lookup"><span data-stu-id="c994d-193"><dt>**TBS\_E\_SERVICE\_NOT\_RUNNING**</dt> <dt>2150121480 (0x80284008)</dt></span></span> </dl> | <span data-ttu-id="c994d-194">Nel computer non è stato trovato alcun TPM compatibile.</span><span class="sxs-lookup"><span data-stu-id="c994d-194">No compatible TPM is found on this computer.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="c994d-195"><dt>**FVE \_ E \_ \_ VOLUME esterno**</dt> <dt>2150694947 (0x80310023)</dt></span><span class="sxs-lookup"><span data-stu-id="c994d-195"><dt>**FVE\_E\_FOREIGN\_VOLUME**</dt> <dt>2150694947 (0x80310023)</dt></span></span> </dl>       | <span data-ttu-id="c994d-196">Il TPM non è in grado di proteggere la chiave di crittografia del volume perché il volume non contiene il sistema operativo attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="c994d-196">The TPM cannot secure the volume's encryption key because the volume does not contain the currently running operating system.</span></span><br/>                                           |
| <dl> <span data-ttu-id="c994d-197"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="c994d-197"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                 | <span data-ttu-id="c994d-198">Il parametro *PlatformValidationProfile* viene specificato, ma i relativi valori non sono compresi nell'intervallo noto o non corrisponde all'impostazione criteri di gruppo attualmente attiva.</span><span class="sxs-lookup"><span data-stu-id="c994d-198">The *PlatformValidationProfile* parameter is provided but its values are not within the known range, or it does not match the Group Policy setting currently in effect.</span></span><br/> |
| <dl> <span data-ttu-id="c994d-199"><dt>**FVE \_ La \_ protezione E \_ esiste**</dt> <dt>2150694961 (0x80310031)</dt></span><span class="sxs-lookup"><span data-stu-id="c994d-199"><dt>**FVE\_E\_PROTECTOR\_EXISTS**</dt> <dt>2150694961 (0x80310031)</dt></span></span> </dl>            | <span data-ttu-id="c994d-200">Esiste già una protezione con chiave di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="c994d-200">A key protector of this type already exists.</span></span><br/>                                                                                                                             |



 

## <a name="security-considerations"></a><span data-ttu-id="c994d-201">Considerazioni relative alla sicurezza</span><span class="sxs-lookup"><span data-stu-id="c994d-201">Security Considerations</span></span>

<span data-ttu-id="c994d-202">Per la sicurezza del computer, è consigliabile usare il profilo predefinito.</span><span class="sxs-lookup"><span data-stu-id="c994d-202">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="c994d-203">Per una protezione aggiuntiva dalle modifiche di configurazione all'avvio iniziale, usare un profilo di PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span><span class="sxs-lookup"><span data-stu-id="c994d-203">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span>

<span data-ttu-id="c994d-204">La modifica dal profilo predefinito influiscono sulla sicurezza o sull'usabilità del computer.</span><span class="sxs-lookup"><span data-stu-id="c994d-204">Changing from the default profile affects the security or usability of your computer.</span></span>

## <a name="remarks"></a><span data-ttu-id="c994d-205">Commenti</span><span class="sxs-lookup"><span data-stu-id="c994d-205">Remarks</span></span>

<span data-ttu-id="c994d-206">Può esistere al massimo una protezione con chiave di tipo "TPM" per un volume in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="c994d-206">At most one key protector of type "TPM" can exist for a volume at any time.</span></span> <span data-ttu-id="c994d-207">Se si desidera modificare il nome visualizzato o il profilo di convalida della piattaforma utilizzato da una protezione con chiave "TPM" esistente, è necessario prima rimuovere la protezione con chiave esistente e quindi chiamare **ProtectKeyWithTPM** per crearne una nuova.</span><span class="sxs-lookup"><span data-stu-id="c994d-207">If you want to change the display name or the platform validation profile used by an existing "TPM" key protector, you must first remove the existing key protector and then call **ProtectKeyWithTPM** to create a new one.</span></span>

<span data-ttu-id="c994d-208">Per gli indici di PCR da 0 a 5, le misurazioni correnti nei registri vengono usate per proteggere la chiave di crittografia.</span><span class="sxs-lookup"><span data-stu-id="c994d-208">For PCR indices 0 through 5, the current measurements in the registers are used to protect the encryption key.</span></span> <span data-ttu-id="c994d-209">Per i valori di PCR da 8 a 11, le misurazioni usate sono quelle che dovrebbero esistere al successivo ciclo di avvio.</span><span class="sxs-lookup"><span data-stu-id="c994d-209">For PCR values 8 through 11, the measurements used are the ones expected to exist on the next start cycle.</span></span>

<span data-ttu-id="c994d-210">È necessario specificare protezioni con chiave aggiuntive per sbloccare il volume negli scenari di ripristino in cui non è possibile ottenere l'accesso alla chiave di crittografia del volume. ad esempio, quando il TPM non è in grado di convalidare correttamente il profilo di convalida della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="c994d-210">Additional key protectors should be specified to unlock the volume in recovery scenarios where access to the volume's encryption key cannot be obtained; for example, when the TPM cannot successfully validate against the platform validation profile.</span></span> <span data-ttu-id="c994d-211">Usare [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) o [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) per creare una o più protezioni con chiave per il ripristino di un volume altrimenti bloccato.</span><span class="sxs-lookup"><span data-stu-id="c994d-211">Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) or [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) to create one or more key protectors for recovering an otherwise locked volume.</span></span>

<span data-ttu-id="c994d-212">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="c994d-212">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c994d-213">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="c994d-213">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="c994d-214">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="c994d-214">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c994d-215">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="c994d-215">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c994d-216">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c994d-216">Requirements</span></span>



| <span data-ttu-id="c994d-217">Requisito</span><span class="sxs-lookup"><span data-stu-id="c994d-217">Requirement</span></span> | <span data-ttu-id="c994d-218">Valore</span><span class="sxs-lookup"><span data-stu-id="c994d-218">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c994d-219">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c994d-219">Minimum supported client</span></span><br/> | <span data-ttu-id="c994d-220">Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="c994d-220">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c994d-221">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c994d-221">Minimum supported server</span></span><br/> | <span data-ttu-id="c994d-222">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c994d-222">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c994d-223">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c994d-223">Namespace</span></span><br/>                | <span data-ttu-id="c994d-224">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="c994d-224">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="c994d-225">MOF</span><span class="sxs-lookup"><span data-stu-id="c994d-225">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c994d-226"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c994d-226"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c994d-227">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c994d-227">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c994d-228">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="c994d-228">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="c994d-229">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="c994d-229">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
