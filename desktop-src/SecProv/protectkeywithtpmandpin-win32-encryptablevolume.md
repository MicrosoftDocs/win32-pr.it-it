---
description: Se il Trusted Platform Module (TPM) è disponibile, questo metodo protegge la chiave di crittografia del volume migliorata da un numero di identificazione personale specificato dall'utente.
ms.assetid: 8c4c434a-dd60-491a-a983-b3fa78c91c0d
title: Metodo ProtectKeyWithTPMAndPIN della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithTPMAndPIN
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: e5a0a7a253723bec84df7a86fa94ab182bd192dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878922"
---
# <a name="protectkeywithtpmandpin-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="4d0f0-103">Metodo ProtectKeyWithTPMAndPIN della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="4d0f0-103">ProtectKeyWithTPMAndPIN method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="4d0f0-104">Il metodo **ProtectKeyWithTPMAndPIN** della classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) protegge la chiave di crittografia del volume utilizzando l'hardware di sicurezza del Trusted Platform Module (TPM) nel computer, se disponibile, migliorato da un codice PIN (Personal Identification Number) specificato dall'utente che deve essere fornito al computer all'avvio.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-104">The **ProtectKeyWithTPMAndPIN** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key by using the Trusted Platform Module (TPM) Security Hardware on the computer, if available, enhanced by a user-specified personal identification number (PIN) that must be provided to the computer at startup.</span></span>

<span data-ttu-id="4d0f0-105">Sia la convalida del TPM che l'input della stringa di identificazione personale sono necessarie per accedere alla chiave di crittografia del volume e sbloccare il contenuto del volume.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-105">Both validation by the TPM and input of the personal identification string are necessary to access the volume's encryption key and unlock volume contents.</span></span>

<span data-ttu-id="4d0f0-106">Questo metodo è applicabile solo al volume che contiene il sistema operativo attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-106">This method is only applicable for the volume that contains the currently running operating system.</span></span>

<span data-ttu-id="4d0f0-107">Viene creata una protezione con chiave di tipo "TPM e PIN" per il volume, se non ne esiste già una.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-107">A key protector of type "TPM And PIN" is created for the volume, if one does not already exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d0f0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4d0f0-108">Syntax</span></span>


```mof
uint32 ProtectKeyWithTPMAndPIN(
  [in, optional] string FriendlyName,
  [in, optional] uint8  PlatformValidationProfile[],
  [in]           string PIN,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="4d0f0-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="4d0f0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d0f0-110">*FriendlyName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="4d0f0-110">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4d0f0-111">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="4d0f0-111">Type: **string**</span></span>

<span data-ttu-id="4d0f0-112">Identificatore di stringa assegnato dall'utente per la protezione con chiave.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-112">A user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="4d0f0-113">Se questo parametro non è specificato, viene utilizzato un valore blank.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-113">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="4d0f0-114">*PlatformValidationProfile* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="4d0f0-114">*PlatformValidationProfile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4d0f0-115">Tipo: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="4d0f0-115">Type: **uint8\[\]**</span></span>

<span data-ttu-id="4d0f0-116">Matrice di valori integer che specifica il modo in cui l'hardware di sicurezza del Trusted Platform Module (TPM) del computer protegge la chiave di crittografia del volume del disco.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-116">An array of integers that specifies how the computer's Trusted Platform Module (TPM) Security Hardware secures the disk volume's encryption key.</span></span>

<span data-ttu-id="4d0f0-117">Un profilo di convalida della piattaforma è costituito da un set di indici di registro di configurazione della piattaforma (PCR) compresi tra 0 e 23, inclusi.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-117">A platform validation profile consists of a set of Platform Configuration Register (PCR) indices ranging from 0 to 23, inclusive.</span></span> <span data-ttu-id="4d0f0-118">I valori repeat nel parametro vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-118">Repeat values in the parameter are ignored.</span></span> <span data-ttu-id="4d0f0-119">Ogni indice di PCR è associato ai servizi che vengono eseguiti all'avvio del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-119">Each PCR index is associated with services that run when the operating system starts.</span></span> <span data-ttu-id="4d0f0-120">Ogni volta che il computer viene avviato, il TPM verificherà che i servizi specificati nel profilo di convalida della piattaforma non siano stati modificati.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-120">Each time the computer starts, the TPM will check that the services you specified in the platform validation profile have not changed.</span></span> <span data-ttu-id="4d0f0-121">Se uno di questi servizi viene modificato mentre la protezione Crittografia unità BitLocker (BDE) rimane attiva, il TPM non rilascia la chiave di crittografia per sbloccare il volume del disco e il computer entrerà in modalità di ripristino.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-121">If any of these services change while BitLocker Drive Encryption (BDE) protection remains on, the TPM will not release the encryption key to unlock the disk volume, and the computer will enter into recovery mode.</span></span>

<span data-ttu-id="4d0f0-122">Se questo parametro viene specificato mentre l'impostazione Criteri di gruppo corrispondente è stata abilitata, deve corrispondere all'impostazione Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-122">If this parameter is specified while the corresponding Group Policy setting has been enabled, it must match the Group Policy setting.</span></span>

<span data-ttu-id="4d0f0-123">Se questo parametro non è specificato, viene usato il valore predefinito 0, 2, 4, 5, 8, 9, 10 e 11.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-123">If this parameter is not specified, the default of 0, 2, 4, 5, 8, 9, 10, and 11 is used.</span></span> <span data-ttu-id="4d0f0-124">Il profilo di convalida della piattaforma predefinito protegge la chiave di crittografia in base alle modifiche apportate agli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="4d0f0-124">The default platform validation profile secures the encryption key against changes to the following elements:</span></span>

-   <span data-ttu-id="4d0f0-125">Radice principale di Trust of Measurement (CRTM)</span><span class="sxs-lookup"><span data-stu-id="4d0f0-125">Core Root of Trust of Measurement (CRTM)</span></span>
-   <span data-ttu-id="4d0f0-126">BIOS</span><span class="sxs-lookup"><span data-stu-id="4d0f0-126">BIOS</span></span>
-   <span data-ttu-id="4d0f0-127">Estensioni della piattaforma (PCR 0)</span><span class="sxs-lookup"><span data-stu-id="4d0f0-127">Platform Extensions (PCR 0)</span></span>
-   <span data-ttu-id="4d0f0-128">Codice dell'opzione ROM (PCR 2)</span><span class="sxs-lookup"><span data-stu-id="4d0f0-128">Option ROM Code (PCR 2)</span></span>
-   <span data-ttu-id="4d0f0-129">Codice MBR (master boot record) (PCR 4)</span><span class="sxs-lookup"><span data-stu-id="4d0f0-129">Master Boot Record (MBR) Code (PCR 4)</span></span>
-   <span data-ttu-id="4d0f0-130">Tabella di partizione MBR (record di avvio principale) (PCR 5)</span><span class="sxs-lookup"><span data-stu-id="4d0f0-130">Master Boot Record (MBR) Partition Table (PCR 5)</span></span>
-   <span data-ttu-id="4d0f0-131">Settore di avvio NTFS (PCR 8)</span><span class="sxs-lookup"><span data-stu-id="4d0f0-131">NTFS Boot Sector (PCR 8)</span></span>
-   <span data-ttu-id="4d0f0-132">Blocco di avvio NTFS (PCR 9)</span><span class="sxs-lookup"><span data-stu-id="4d0f0-132">NTFS Boot Block (PCR 9)</span></span>
-   <span data-ttu-id="4d0f0-133">Boot Manager (PCR 10)</span><span class="sxs-lookup"><span data-stu-id="4d0f0-133">Boot Manager (PCR 10)</span></span>
-   <span data-ttu-id="4d0f0-134">Controllo di accesso di BitLocker (PCR 11)</span><span class="sxs-lookup"><span data-stu-id="4d0f0-134">BitLocker Access Control (PCR 11)</span></span>

<span data-ttu-id="4d0f0-135">Per la sicurezza del computer, è consigliabile usare il profilo predefinito.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-135">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="4d0f0-136">Per una protezione aggiuntiva dalle modifiche di configurazione all'avvio iniziale, usare un profilo di PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-136">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span> <span data-ttu-id="4d0f0-137">Per impostazione predefinita, i computer basati su Unified Extensible Firmware Interface (UEFI) non utilizzano PCR 5.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-137">Unified Extensible Firmware Interface (UEFI)–based computers do not use PCR 5 by default.</span></span>

<span data-ttu-id="4d0f0-138">La modifica dal profilo predefinito influiscono sulla sicurezza e la gestibilità del computer.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-138">Changing from the default profile affects the security and manageability of your computer.</span></span> <span data-ttu-id="4d0f0-139">La riservatezza delle modifiche da BitLocker a piattaforma (dannose o autorizzate) viene aumentata o ridotta a seconda dell'inclusione o dell'esclusione, rispettivamente, del PCRs.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-139">The sensitivity of BitLocker to platform modifications (malicious or authorized) is increased or decreased depending upon the inclusion or exclusion, respectively, of the PCRs.</span></span> <span data-ttu-id="4d0f0-140">Per abilitare la protezione BitLocker, è necessario che il profilo di convalida della piattaforma includa PCR 11.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-140">For BitLocker protection to be enabled, the platform validation profile must include PCR 11.</span></span>



| <span data-ttu-id="4d0f0-141">Valore</span><span class="sxs-lookup"><span data-stu-id="4d0f0-141">Value</span></span>                                                                         | <span data-ttu-id="4d0f0-142">Significato</span><span class="sxs-lookup"><span data-stu-id="4d0f0-142">Meaning</span></span>                                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4d0f0-143"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4d0f0-143"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="4d0f0-144">Radice principale di Trust of Measurement (CRTM), BIOS ed estensioni della piattaforma</span><span class="sxs-lookup"><span data-stu-id="4d0f0-144">Core Root of Trust of Measurement (CRTM), BIOS, and Platform Extensions</span></span><br/> |
| <dl> <span data-ttu-id="4d0f0-145"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4d0f0-145"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="4d0f0-146">Configurazione e dati della piattaforma e della scheda madre</span><span class="sxs-lookup"><span data-stu-id="4d0f0-146">Platform and Motherboard Configuration and Data</span></span><br/>                         |
| <dl> <span data-ttu-id="4d0f0-147"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4d0f0-147"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="4d0f0-148">Codice ROM opzione</span><span class="sxs-lookup"><span data-stu-id="4d0f0-148">Option ROM Code</span></span><br/>                                                         |
| <dl> <span data-ttu-id="4d0f0-149"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="4d0f0-149"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="4d0f0-150">Configurazione e dati dell'opzione ROM</span><span class="sxs-lookup"><span data-stu-id="4d0f0-150">Option ROM Configuration and Data</span></span><br/>                                       |
| <dl> <span data-ttu-id="4d0f0-151"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="4d0f0-151"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="4d0f0-152">Codice MBR (master boot record)</span><span class="sxs-lookup"><span data-stu-id="4d0f0-152">Master Boot Record (MBR) Code</span></span><br/>                                           |
| <dl> <span data-ttu-id="4d0f0-153"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="4d0f0-153"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="4d0f0-154">Tabella di partizione MBR (record di avvio principale)</span><span class="sxs-lookup"><span data-stu-id="4d0f0-154">Master Boot Record (MBR) Partition Table</span></span><br/>                                |
| <dl> <span data-ttu-id="4d0f0-155"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="4d0f0-155"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="4d0f0-156">Eventi di riattivazione e transizione di stato</span><span class="sxs-lookup"><span data-stu-id="4d0f0-156">State Transition and Wake Events</span></span><br/>                                        |
| <dl> <span data-ttu-id="4d0f0-157"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="4d0f0-157"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="4d0f0-158">Manufacturer-Specific computer</span><span class="sxs-lookup"><span data-stu-id="4d0f0-158">Computer Manufacturer-Specific</span></span><br/>                                          |
| <dl> <span data-ttu-id="4d0f0-159"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="4d0f0-159"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="4d0f0-160">Settore di avvio NTFS</span><span class="sxs-lookup"><span data-stu-id="4d0f0-160">NTFS Boot Sector</span></span><br/>                                                        |
| <dl> <span data-ttu-id="4d0f0-161"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="4d0f0-161"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="4d0f0-162">Blocco di avvio NTFS</span><span class="sxs-lookup"><span data-stu-id="4d0f0-162">NTFS Boot Block</span></span><br/>                                                         |
| <dl> <span data-ttu-id="4d0f0-163"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="4d0f0-163"><dt>10</dt></span></span> </dl> | <span data-ttu-id="4d0f0-164">Gestione avvio</span><span class="sxs-lookup"><span data-stu-id="4d0f0-164">Boot Manager</span></span><br/>                                                            |
| <dl> <span data-ttu-id="4d0f0-165"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="4d0f0-165"><dt>11</dt></span></span> </dl> | <span data-ttu-id="4d0f0-166">Controllo di accesso di BitLocker</span><span class="sxs-lookup"><span data-stu-id="4d0f0-166">BitLocker Access Control</span></span><br/>                                                |
| <dl> <span data-ttu-id="4d0f0-167"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="4d0f0-167"><dt>12</dt></span></span> </dl> | <span data-ttu-id="4d0f0-168">Definito per l'utilizzo da parte del sistema operativo statico</span><span class="sxs-lookup"><span data-stu-id="4d0f0-168">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="4d0f0-169"><dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="4d0f0-169"><dt>13</dt></span></span> </dl> | <span data-ttu-id="4d0f0-170">Definito per l'utilizzo da parte del sistema operativo statico</span><span class="sxs-lookup"><span data-stu-id="4d0f0-170">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="4d0f0-171"><dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="4d0f0-171"><dt>14</dt></span></span> </dl> | <span data-ttu-id="4d0f0-172">Definito per l'utilizzo da parte del sistema operativo statico</span><span class="sxs-lookup"><span data-stu-id="4d0f0-172">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="4d0f0-173"><dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="4d0f0-173"><dt>15</dt></span></span> </dl> | <span data-ttu-id="4d0f0-174">Definito per l'utilizzo da parte del sistema operativo statico</span><span class="sxs-lookup"><span data-stu-id="4d0f0-174">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="4d0f0-175"><dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="4d0f0-175"><dt>16</dt></span></span> </dl> | <span data-ttu-id="4d0f0-176">Usato per il debug</span><span class="sxs-lookup"><span data-stu-id="4d0f0-176">Used for debugging</span></span><br/>                                                      |
| <dl> <span data-ttu-id="4d0f0-177"><dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="4d0f0-177"><dt>17</dt></span></span> </dl> | <span data-ttu-id="4d0f0-178">CRTM dinamico</span><span class="sxs-lookup"><span data-stu-id="4d0f0-178">Dynamic CRTM</span></span><br/>                                                            |
| <dl> <span data-ttu-id="4d0f0-179"><dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="4d0f0-179"><dt>18</dt></span></span> </dl> | <span data-ttu-id="4d0f0-180">Piattaforma definita</span><span class="sxs-lookup"><span data-stu-id="4d0f0-180">Platform defined</span></span><br/>                                                        |
| <dl> <span data-ttu-id="4d0f0-181"><dt>19</dt></span><span class="sxs-lookup"><span data-stu-id="4d0f0-181"><dt>19</dt></span></span> </dl> | <span data-ttu-id="4d0f0-182">Usato da un sistema operativo attendibile</span><span class="sxs-lookup"><span data-stu-id="4d0f0-182">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="4d0f0-183"><dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="4d0f0-183"><dt>20</dt></span></span> </dl> | <span data-ttu-id="4d0f0-184">Usato da un sistema operativo attendibile</span><span class="sxs-lookup"><span data-stu-id="4d0f0-184">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="4d0f0-185"><dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="4d0f0-185"><dt>21</dt></span></span> </dl> | <span data-ttu-id="4d0f0-186">Usato da un sistema operativo attendibile</span><span class="sxs-lookup"><span data-stu-id="4d0f0-186">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="4d0f0-187"><dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="4d0f0-187"><dt>22</dt></span></span> </dl> | <span data-ttu-id="4d0f0-188">Usato da un sistema operativo attendibile</span><span class="sxs-lookup"><span data-stu-id="4d0f0-188">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="4d0f0-189"><dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="4d0f0-189"><dt>23</dt></span></span> </dl> | <span data-ttu-id="4d0f0-190">Supporto delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="4d0f0-190">Application support</span></span><br/>                                                     |



 

</dd> <dt>

<span data-ttu-id="4d0f0-191">*Aggiungi* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4d0f0-191">*PIN* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d0f0-192">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="4d0f0-192">Type: **string**</span></span>

<span data-ttu-id="4d0f0-193">Stringa di identificazione personale specificata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-193">A user-specified personal identification string.</span></span> <span data-ttu-id="4d0f0-194">Questa stringa deve essere composta da una sequenza di 6 a 20 cifre oppure, se i criteri di gruppo "Consenti PIN avanzati per l'avvio" sono abilitati, da 6 a 20 lettere, simboli, spazi o numeri.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-194">This string must consist of a sequence of 6 to 20 digits or, if the "Allow enhanced PINs for startup" group policy is enabled, 6 to 20 letters, symbols, spaces, or numbers.</span></span>

</dd> <dt>

<span data-ttu-id="4d0f0-195">*VolumeKeyProtectorID* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4d0f0-195">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d0f0-196">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="4d0f0-196">Type: **string**</span></span>

<span data-ttu-id="4d0f0-197">Identificatore di stringa univoco aggiornato usato per gestire una protezione con chiave del volume crittografata.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-197">The updated unique string identifier used to manage an encrypted volume key protector.</span></span>

<span data-ttu-id="4d0f0-198">Se l'unità supporta la crittografia hardware e BitLocker non ha assunto la proprietà della banda, la stringa ID è impostata su "BitLocker" e la protezione con chiave viene scritta in base ai metadati della banda.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-198">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d0f0-199">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4d0f0-199">Return value</span></span>

<span data-ttu-id="4d0f0-200">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d0f0-200">Type: **uint32**</span></span>

<span data-ttu-id="4d0f0-201">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-201">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="4d0f0-202">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="4d0f0-202">Return code/value</span></span>                                                                                                                                                                                | <span data-ttu-id="4d0f0-203">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d0f0-203">Description</span></span>                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4d0f0-204"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="4d0f0-204"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                | <span data-ttu-id="4d0f0-205">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-205">The method was successful.</span></span><br/>                                                                                                                                               |
| <dl> <span data-ttu-id="4d0f0-206"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="4d0f0-206"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                        | <span data-ttu-id="4d0f0-207">Viene specificato il parametro *PlatformValidationProfile* , ma i relativi valori non rientrano nell'intervallo noto oppure non corrisponde all'impostazione criteri di gruppo attualmente attiva.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-207">The *PlatformValidationProfile* parameter is provided, but its values are not within the known range, or it does not match the Group Policy setting currently in effect.</span></span><br/> |
| <dl> <span data-ttu-id="4d0f0-208"><dt>**FVE \_ E \_ \_ CDDVD di avvio**</dt> <dt>2150694960 (0x80310030)</dt></span><span class="sxs-lookup"><span data-stu-id="4d0f0-208"><dt>**FVE\_E\_BOOTABLE\_CDDVD**</dt> <dt>2150694960 (0x80310030)</dt></span></span> </dl>              | <span data-ttu-id="4d0f0-209">Nel computer è presente un CD/DVD di avvio.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-209">A bootable CD/DVD is found in this computer.</span></span> <span data-ttu-id="4d0f0-210">Rimuovere il CD/DVD e riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-210">Remove the CD/DVD and restart the computer.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="4d0f0-211"><dt>**FVE \_ E \_ \_ VOLUME esterno**</dt> <dt>2150694947 (0x80310023)</dt></span><span class="sxs-lookup"><span data-stu-id="4d0f0-211"><dt>**FVE\_E\_FOREIGN\_VOLUME**</dt> <dt>2150694947 (0x80310023)</dt></span></span> </dl>              | <span data-ttu-id="4d0f0-212">Il TPM non è in grado di proteggere la chiave di crittografia del volume perché il volume non contiene il sistema operativo attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-212">The TPM cannot secure the volume's encryption key because the volume does not contain the currently running operating system.</span></span><br/>                                            |
| <dl> <span data-ttu-id="4d0f0-213"><dt>**FVE \_ E \_ \_ \_ caratteri PIN non validi**</dt> <dt>2150695066 (0x8031009A)</dt></span><span class="sxs-lookup"><span data-stu-id="4d0f0-213"><dt>**FVE\_E\_INVALID\_PIN\_CHARS**</dt> <dt>2150695066 (0x8031009A)</dt></span></span> </dl>          | <span data-ttu-id="4d0f0-214">Il parametro *NewPIN* contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-214">The *NewPIN* parameter contains characters that are not valid.</span></span> <span data-ttu-id="4d0f0-215">Quando il Criteri di gruppo "Consenti PIN avanzati per l'avvio" è disabilitato, sono supportati solo i numeri.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-215">When the "Allow enhanced PINs for startup" Group Policy is disabled, only numbers are supported.</span></span><br/>          |
| <dl> <span data-ttu-id="4d0f0-216"><dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="4d0f0-216"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>               | <span data-ttu-id="4d0f0-217">Il volume è bloccato.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-217">The volume is locked.</span></span><br/>                                                                                                                                                    |
| <dl> <span data-ttu-id="4d0f0-218"><dt>**FVE \_ \_Criterio E \_ \_ \_ lunghezza PIN non valida**</dt> <dt>2150695016 (0x80310068)</dt></span><span class="sxs-lookup"><span data-stu-id="4d0f0-218"><dt>**FVE\_E\_POLICY\_INVALID\_PIN\_LENGTH**</dt> <dt>2150695016 (0x80310068)</dt></span></span> </dl> | <span data-ttu-id="4d0f0-219">Il parametro *NewPIN* specificato è più lungo di 20 caratteri, più breve di 6 caratteri o più breve della lunghezza minima specificata dal criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-219">The *NewPIN* parameter supplied is either longer than 20 characters, shorter than 6 characters, or shorter than the minimum length specified by Group Policy.</span></span><br/>            |
| <dl> <span data-ttu-id="4d0f0-220"><dt>**FVE \_ La \_ protezione E \_ esiste**</dt> <dt>2150694961 (0x80310031)</dt></span><span class="sxs-lookup"><span data-stu-id="4d0f0-220"><dt>**FVE\_E\_PROTECTOR\_EXISTS**</dt> <dt>2150694961 (0x80310031)</dt></span></span> </dl>            | <span data-ttu-id="4d0f0-221">Esiste già una protezione con chiave di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-221">A key protector of this type already exists.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="4d0f0-222"><dt>**TBS \_ \_Servizio E \_ non \_ in esecuzione**</dt> <dt>2150121480 (0x80284008)</dt></span><span class="sxs-lookup"><span data-stu-id="4d0f0-222"><dt>**TBS\_E\_SERVICE\_NOT\_RUNNING**</dt> <dt>2150121480 (0x80284008)</dt></span></span> </dl>        | <span data-ttu-id="4d0f0-223">Nel computer non è stato trovato alcun TPM compatibile.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-223">No compatible TPM is found on this computer.</span></span><br/>                                                                                                                             |



 

## <a name="security-considerations"></a><span data-ttu-id="4d0f0-224">Considerazioni relative alla sicurezza</span><span class="sxs-lookup"><span data-stu-id="4d0f0-224">Security Considerations</span></span>

<span data-ttu-id="4d0f0-225">Per la sicurezza del computer, è consigliabile usare il profilo predefinito.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-225">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="4d0f0-226">Per una protezione aggiuntiva dalle prime modifiche del codice di avvio, usare un profilo di PCRs 0, 2, 4, 5, 8, 9, 10 e 11.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-226">For additional protection against early startup code changes, use a profile of PCRs 0, 2, 4, 5, 8, 9, 10, and 11.</span></span> <span data-ttu-id="4d0f0-227">Per una protezione aggiuntiva dalle modifiche di configurazione all'avvio iniziale, usare un profilo di PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-227">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span>

<span data-ttu-id="4d0f0-228">La modifica dal profilo predefinito influiscono sulla sicurezza o sull'usabilità del computer.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-228">Changing from the default profile affects the security or usability of your computer.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d0f0-229">Commenti</span><span class="sxs-lookup"><span data-stu-id="4d0f0-229">Remarks</span></span>

<span data-ttu-id="4d0f0-230">Per un volume possono esistere al massimo una protezione con chiave di tipo "TPM e PIN" per un volume in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-230">At most one key protector of type "TPM And PIN" can exist for a volume at any time.</span></span> <span data-ttu-id="4d0f0-231">Se si desidera modificare il nome visualizzato o il profilo di convalida della piattaforma utilizzato da una protezione con chiave "TPM e PIN" esistente, è necessario prima rimuovere la protezione con chiave esistente e quindi chiamare **ProtectKeyWithTPMAndPIN** per crearne una nuova.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-231">If you want to change the display name or the platform validation profile used by an existing "TPM And PIN" key protector, you must first remove the existing key protector and then call **ProtectKeyWithTPMAndPIN** to create a new one.</span></span>

<span data-ttu-id="4d0f0-232">È necessario specificare protezioni con chiave aggiuntive per sbloccare il volume negli scenari di ripristino in cui non è possibile ottenere l'accesso alla chiave di crittografia del volume. ad esempio, quando il TPM non può essere convalidato correttamente rispetto al profilo di convalida della piattaforma o quando il PIN viene perso.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-232">Additional key protectors should be specified to unlock the volume in recovery scenarios where access to the volume's encryption key cannot be obtained; for example, when the TPM cannot successfully validate against the platform validation profile or when the PIN is lost.</span></span>

<span data-ttu-id="4d0f0-233">Usare [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) o [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) per creare una o più protezioni con chiave per il ripristino di un volume altrimenti bloccato.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-233">Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) or [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) to create one or more key protectors for recovering an otherwise locked volume.</span></span>

<span data-ttu-id="4d0f0-234">Sebbene sia possibile disporre di una protezione con chiave di tipo "TPM" e di un altro tipo "TPM e PIN", la presenza del tipo di protezione con chiave "TPM" nega gli effetti di altre protezioni con chiave basata su TPM.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-234">While it is possible to have both a key protector of the type "TPM" and another of the type "TPM And PIN", the presence of the "TPM" key protector type negates the effects of other TPM-based key protectors.</span></span>

<span data-ttu-id="4d0f0-235">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="4d0f0-235">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4d0f0-236">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-236">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="4d0f0-237">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-237">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4d0f0-238">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="4d0f0-238">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4d0f0-239">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4d0f0-239">Requirements</span></span>



| <span data-ttu-id="4d0f0-240">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d0f0-240">Requirement</span></span> | <span data-ttu-id="4d0f0-241">Valore</span><span class="sxs-lookup"><span data-stu-id="4d0f0-241">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d0f0-242">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d0f0-242">Minimum supported client</span></span><br/> | <span data-ttu-id="4d0f0-243">Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="4d0f0-243">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="4d0f0-244">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d0f0-244">Minimum supported server</span></span><br/> | <span data-ttu-id="4d0f0-245">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4d0f0-245">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4d0f0-246">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4d0f0-246">Namespace</span></span><br/>                | <span data-ttu-id="4d0f0-247">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="4d0f0-247">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="4d0f0-248">MOF</span><span class="sxs-lookup"><span data-stu-id="4d0f0-248">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4d0f0-249"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4d0f0-249"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d0f0-250">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4d0f0-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d0f0-251">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="4d0f0-251">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="4d0f0-252">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="4d0f0-252">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
