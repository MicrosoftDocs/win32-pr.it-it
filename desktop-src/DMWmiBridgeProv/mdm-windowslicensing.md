---
title: Classe MDM_WindowsLicensing
description: La \_ classe MDM WindowsLicensing è progettata per scenari di gestione delle licenze correlati.
ms.assetid: 9b26d8dc-aab6-4c67-9dbc-4b53525b9354
keywords:
- Classe MDM_WindowsLicensing
- Classe MDM_WindowsLicensing, descritta
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing
- MDM_WindowsLicensing.InstanceID
- MDM_WindowsLicensing.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd77bbdb1a7e5c708ebcd955a0c8854c7c7404b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301470"
---
# <a name="mdm_windowslicensing-class"></a><span data-ttu-id="3531b-105">MDM \_ WindowsLicensing (classe)</span><span class="sxs-lookup"><span data-stu-id="3531b-105">MDM\_WindowsLicensing class</span></span>

<span data-ttu-id="3531b-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="3531b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3531b-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="3531b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3531b-108">La classe **MDM \_ WindowsLicensing** è progettata per scenari di gestione delle licenze correlati.</span><span class="sxs-lookup"><span data-stu-id="3531b-108">The **MDM\_WindowsLicensing** class is designed for licensing related management scenarios.</span></span> <span data-ttu-id="3531b-109">Attualmente, l'ambito è limitato agli aggiornamenti dell'edizione dei dispositivi Windows 10 desktop e mobile, ad esempio Windows 10 Pro a Windows 10 Enterprise.</span><span class="sxs-lookup"><span data-stu-id="3531b-109">Currently the scope is limited to edition upgrades of Windows 10 desktop and mobile devices, such as Windows 10 Pro to Windows 10 Enterprise.</span></span> <span data-ttu-id="3531b-110">Questo CSP offre inoltre la possibilità di attivare o modificare il codice Product Key dei dispositivi Windows 10 desktop.</span><span class="sxs-lookup"><span data-stu-id="3531b-110">In addition, this CSP provides the capability to activate or change the product key of Windows 10 desktop devices.</span></span>

<span data-ttu-id="3531b-111">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="3531b-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3531b-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3531b-112">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_WindowsLicensing
{
  string InstanceID;
  string ParentID;
  sint32 Edition;
  sint32 Status;
  string LicenseKeyType;
};
```

## <a name="members"></a><span data-ttu-id="3531b-113">Members</span><span class="sxs-lookup"><span data-stu-id="3531b-113">Members</span></span>

<span data-ttu-id="3531b-114">La classe **MDM \_ WindowsLicensing** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3531b-114">The **MDM\_WindowsLicensing** class has these types of members:</span></span>

-   [<span data-ttu-id="3531b-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="3531b-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="3531b-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3531b-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3531b-117">Metodi</span><span class="sxs-lookup"><span data-stu-id="3531b-117">Methods</span></span>

<span data-ttu-id="3531b-118">La classe **MDM \_ WindowsLicensing** ha questi metodi.</span><span class="sxs-lookup"><span data-stu-id="3531b-118">The **MDM\_WindowsLicensing** class has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="3531b-119">Metodo</span><span class="sxs-lookup"><span data-stu-id="3531b-119">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="3531b-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3531b-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="3531b-121"><a href="mdm-windowslicensing-changeproductkeymethod.md"><strong>ChangeProductKeyMethod</strong></a></span><span class="sxs-lookup"><span data-stu-id="3531b-121"><a href="mdm-windowslicensing-changeproductkeymethod.md"><strong>ChangeProductKeyMethod</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3531b-122">Installa un codice Product Key per i dispositivi Windows 10 desktop.</span><span class="sxs-lookup"><span data-stu-id="3531b-122">Installs a product key for Windows 10 desktop devices.</span></span> <span data-ttu-id="3531b-123">Non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="3531b-123">Does not reboot.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="3531b-124"><a href="mdm-windowslicensing-checkapplicabilitymethod.md"><strong>CheckApplicabilityMethod</strong></a></span><span class="sxs-lookup"><span data-stu-id="3531b-124"><a href="mdm-windowslicensing-checkapplicabilitymethod.md"><strong>CheckApplicabilityMethod</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3531b-125">Metodo per verificare se il codice Product Key immesso può essere usato per l'aggiornamento di un'edizione, l'attivazione o la modifica di un codice Product Key di Windows 10 per i dispositivi desktop.</span><span class="sxs-lookup"><span data-stu-id="3531b-125">Method to check if the entered product key can be used for an edition upgrade, activation or changing a product key of Windows 10 for desktop devices.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="3531b-126"><a href="mdm-windowslicensing-upgradeeditionwithlicensemethod.md"><strong>UpgradeEditionWithLicenseMethod</strong></a></span><span class="sxs-lookup"><span data-stu-id="3531b-126"><a href="mdm-windowslicensing-upgradeeditionwithlicensemethod.md"><strong>UpgradeEditionWithLicenseMethod</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3531b-127">Fornire una licenza per l'aggiornamento di un'edizione di dispositivi Windows 10 Mobile.</span><span class="sxs-lookup"><span data-stu-id="3531b-127">Provide a license for an edition upgrade of Windows 10 mobile devices.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3531b-128">Questo processo di aggiornamento non richiede un riavvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="3531b-128">This upgrade process does not require a system restart.</span></span>
</blockquote>
<br/> <br/> <span data-ttu-id="3531b-129">Il tipo di data è XML.</span><span class="sxs-lookup"><span data-stu-id="3531b-129">The date type is XML.</span></span><br/> <span data-ttu-id="3531b-130">L'operazione supportata è Execute.</span><span class="sxs-lookup"><span data-stu-id="3531b-130">The supported operation is Execute.</span></span><br/>
<blockquote>
[!Important]<br />
<span data-ttu-id="3531b-131">Il contenuto del file di licenza XML deve essere preceduto da un carattere di escape, ovvero non dovrebbe essere semplicemente un XML copiato. in caso contrario, l'aggiornamento dell'edizione nei dispositivi Windows 10 Mobile avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="3531b-131">The XML license file contents must be properly escaped (that is, it should not simply be a copied XML), otherwise the edition upgrade on Windows 10 mobile devices will fail.</span></span> <span data-ttu-id="3531b-132">Per ulteriori informazioni sull'escape corretto del file di licenza XML, vedere la sezione 2,4 della <a href="https://www.w3.org/TR/xml/">specifica W3C XML</a>. Il file di licenza XML viene acquisito da Microsoft Volume Licensing Service Center.</span><span class="sxs-lookup"><span data-stu-id="3531b-132">For more information on proper escaping of the XML license file, see Section 2.4 of the <a href="https://www.w3.org/TR/xml/">W3C XML spec</a>. The XML license file is acquired from the Microsoft Volume Licensing Service Center.</span></span> <span data-ttu-id="3531b-133">L'organizzazione deve disporre di un contratto multilicenza con Microsoft per accedere al portale.</span><span class="sxs-lookup"><span data-stu-id="3531b-133">Your organization must have a Volume Licensing contract with Microsoft to access the portal.</span></span>
</blockquote>
<br/> <span data-ttu-id="3531b-134">Di seguito sono riportati i percorsi di aggiornamento validi per l'edizione quando si usa questo nodo tramite un pacchetto MDM o di provisioning:</span><span class="sxs-lookup"><span data-stu-id="3531b-134">The following are valid edition upgrade paths when using this node through an MDM or provisioning package:</span></span>
<ul>
<li><span data-ttu-id="3531b-135">Windows 10 Mobileto Windows 10 Mobile Enterprise</span><span class="sxs-lookup"><span data-stu-id="3531b-135">Windows 10 Mobileto Windows 10 Mobile Enterprise</span></span><br/></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="3531b-136"><a href="mdm-windowslicensing-upgradeeditionwithproductkeymethod.md"><strong>UpgradeEditionWithProductKeyMethod</strong></a></span><span class="sxs-lookup"><span data-stu-id="3531b-136"><a href="mdm-windowslicensing-upgradeeditionwithproductkeymethod.md"><strong>UpgradeEditionWithProductKeyMethod</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3531b-137">Attiva il dispositivo per l'esecuzione del codice Product Key e l'aggiornamento dell'edizione del client.</span><span class="sxs-lookup"><span data-stu-id="3531b-137">Triggers the device to take the product key and upgrade the edition of the client.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="3531b-138">Questo processo di aggiornamento richiede un riavvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="3531b-138">This upgrade process requires a system restart.</span></span>
</blockquote>
<br/> <br/> <span data-ttu-id="3531b-139">L'operazione supportata è Execute.</span><span class="sxs-lookup"><span data-stu-id="3531b-139">The supported operation is Execute.</span></span><br/> <span data-ttu-id="3531b-140">Quando viene effettuato il push di un codice Product Key da un server MDM a un dispositivo dell'utente, <strong>changepk.exe</strong> viene eseguito con il codice Product Key.</span><span class="sxs-lookup"><span data-stu-id="3531b-140">When a product key is pushed from an MDM server to a user's device, <strong>changepk.exe</strong> runs using the product key.</span></span> <span data-ttu-id="3531b-141">Al termine, viene visualizzata una notifica all'utente che è disponibile una nuova edizione di Windows 10.</span><span class="sxs-lookup"><span data-stu-id="3531b-141">After it completes, a notification is shown to the user that a new edition of Windows 10 is available.</span></span> <span data-ttu-id="3531b-142">L'utente può quindi riavviare il sistema manualmente o, dopo due ore, il dispositivo verrà riavviato automaticamente per completare l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="3531b-142">The user can then restart their system manually or, after two hours, the device will restart automatically to complete the upgrade.</span></span> <span data-ttu-id="3531b-143">L'utente riceverà una notifica di promemoria 10 minuti prima del riavvio automatico.</span><span class="sxs-lookup"><span data-stu-id="3531b-143">The user will receive a reminder notification 10 minutes before the automatic restart.</span></span><br/> <span data-ttu-id="3531b-144">Al termine del riavvio del dispositivo, il processo di aggiornamento dell'edizione viene completato.</span><span class="sxs-lookup"><span data-stu-id="3531b-144">After the device restarts, the edition upgrade process completes.</span></span> <span data-ttu-id="3531b-145">L'utente riceverà una notifica dell'esito positivo dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="3531b-145">The user will receive a notification of the successful upgrade.</span></span>
<blockquote>
[!Important]<br />
<span data-ttu-id="3531b-146">Se un altro criterio richiede un riavvio del sistema che si verifica quando <strong>changepk.exe</strong> è in esecuzione, l'aggiornamento dell'edizione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="3531b-146">If another policy requires a system reboot that occurs when <strong>changepk.exe</strong> is running, the edition upgrade will fail.</span></span>
</blockquote>
<br/> <br/> <span data-ttu-id="3531b-147">Se un codice Product Key viene immesso in un pacchetto di provisioning e l'utente inizia l'installazione del pacchetto, viene visualizzata una notifica per l'utente che il sistema verrà riavviato per completare l'installazione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="3531b-147">If a product key is entered in a provisioning package and the user begins installation of the package, a notification is shown to the user that their system will restart to complete the package installation.</span></span> <span data-ttu-id="3531b-148">Al momento del consenso esplicito da parte dell'utente, il pacchetto continua l'installazione e <strong>changepk.exe</strong> viene eseguito con il codice Product Key.</span><span class="sxs-lookup"><span data-stu-id="3531b-148">Upon explicit consent from the user to proceed, the package continues installation and <strong>changepk.exe</strong> runs using the product key.</span></span> <span data-ttu-id="3531b-149">L'utente riceverà una notifica di promemoria 30 secondi prima del riavvio automatico.</span><span class="sxs-lookup"><span data-stu-id="3531b-149">The user will receive a reminder notification 30 seconds before the automatic restart.</span></span> <br/> <span data-ttu-id="3531b-150">Al termine del riavvio del dispositivo, il processo di aggiornamento dell'edizione viene completato.</span><span class="sxs-lookup"><span data-stu-id="3531b-150">After the device restarts, the edition upgrade process completes.</span></span> <span data-ttu-id="3531b-151">L'utente riceverà una notifica dell'esito positivo dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="3531b-151">The user will receive a notification of the successful upgrade.</span></span> <br/> <span data-ttu-id="3531b-152">Questo nodo può essere usato anche per attivare o modificare un codice Product Key in un'edizione specifica del dispositivo desktop Windows 10 immettendo un codice Product Key.</span><span class="sxs-lookup"><span data-stu-id="3531b-152">This node can also be used to activate or change a product key on a particular edition of Windows 10 desktop device by entering a product key.</span></span> <span data-ttu-id="3531b-153">L'attivazione o la modifica di un codice Product Key non richiede un riavvio ed è un processo invisibile per l'utente.</span><span class="sxs-lookup"><span data-stu-id="3531b-153">Activation or changing a product key does not require a reboot and is a silent process for the user.</span></span><br/>
<blockquote>
[!Important]<br />
<span data-ttu-id="3531b-154">Il codice Product Key immesso deve essere costituito da 29 caratteri, ovvero deve includere trattini. in caso contrario, l'attivazione, l'aggiornamento dell'edizione o la modifica del codice Product Key nei dispositivi desktop Windows 10 avranno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="3531b-154">The product key entered must be 29 characters (that is, it should include dashes), otherwise the activation, edition upgrade, or product key change on Windows 10 desktop devices will fail.</span></span> <span data-ttu-id="3531b-155">Il codice Product Key viene acquisito da Microsoft Volume Licensing Service Center.</span><span class="sxs-lookup"><span data-stu-id="3531b-155">The product key is acquired from Microsoft Volume Licensing Service Center.</span></span> <span data-ttu-id="3531b-156">L'organizzazione deve disporre di un contratto multilicenza con Microsoft per accedere al portale.</span><span class="sxs-lookup"><span data-stu-id="3531b-156">Your organization must have a Volume Licensing contract with Microsoft to access the portal.</span></span>
</blockquote>
<br/> <span data-ttu-id="3531b-157">Di seguito sono riportati i percorsi di aggiornamento validi per l'edizione quando si usa questo nodo tramite MDM:</span><span class="sxs-lookup"><span data-stu-id="3531b-157">The following are valid edition upgrade paths when using this node through an MDM:</span></span>
<ul>
<li><span data-ttu-id="3531b-158">Windows 10 Enterprise per Windows 10 Education</span><span class="sxs-lookup"><span data-stu-id="3531b-158">Windows 10 Enterprise to Windows 10 Education</span></span></li>
<li><span data-ttu-id="3531b-159">Windows 10 Home a Windows 10 Education</span><span class="sxs-lookup"><span data-stu-id="3531b-159">Windows 10 Home to Windows 10 Education</span></span></li>
<li><span data-ttu-id="3531b-160">Windows 10 Pro a Windows 10 Education</span><span class="sxs-lookup"><span data-stu-id="3531b-160">Windows 10 Pro to Windows 10 Education</span></span></li>
<li><span data-ttu-id="3531b-161">Da Windows 10 Pro a Windows 10 Enterprise</span><span class="sxs-lookup"><span data-stu-id="3531b-161">Windows 10 Pro to Windows 10 Enterprise</span></span></li>
</ul>
<br/> <span data-ttu-id="3531b-162">L'attivazione o la modifica di un codice Product Key può essere eseguita nelle edizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="3531b-162">Activation or changing a product key can be carried out on the following editions:</span></span>
<ul>
<li><span data-ttu-id="3531b-163">Windows 10 Education</span><span class="sxs-lookup"><span data-stu-id="3531b-163">Windows 10 Education</span></span></li>
<li><span data-ttu-id="3531b-164">Windows 10 Enterprise</span><span class="sxs-lookup"><span data-stu-id="3531b-164">Windows 10 Enterprise</span></span></li>
<li><span data-ttu-id="3531b-165">Windows 10 Home</span><span class="sxs-lookup"><span data-stu-id="3531b-165">Windows 10 Home</span></span></li>
<li><span data-ttu-id="3531b-166">Windows 10 Pro</span><span class="sxs-lookup"><span data-stu-id="3531b-166">Windows 10 Pro</span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="3531b-167">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3531b-167">Properties</span></span>

<span data-ttu-id="3531b-168">La classe **MDM \_ WindowsLicensing** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3531b-168">The **MDM\_WindowsLicensing** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="3531b-169">Edizione</span><span class="sxs-lookup"><span data-stu-id="3531b-169">Edition</span></span>](/windows/client-management/mdm/windowslicensing-csp#edition)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3531b-170">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3531b-170">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3531b-171">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3531b-171">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3531b-172">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3531b-172">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3531b-173">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3531b-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3531b-174">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3531b-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3531b-175">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3531b-175">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3531b-176">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="3531b-176">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="3531b-177">LicenseKeyType</span><span class="sxs-lookup"><span data-stu-id="3531b-177">LicenseKeyType</span></span>](/windows/client-management/mdm/windowslicensing-csp#licensekeytype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3531b-178">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3531b-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3531b-179">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3531b-179">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3531b-180">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="3531b-180">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3531b-181">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3531b-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3531b-182">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3531b-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3531b-183">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3531b-183">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3531b-184">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="3531b-184">Describes the full path to the parent node.</span></span> <span data-ttu-id="3531b-185">Per questa classe la stringa è "./Vendor/MSFT/"</span><span class="sxs-lookup"><span data-stu-id="3531b-185">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> <dt>

[<span data-ttu-id="3531b-186">Status</span><span class="sxs-lookup"><span data-stu-id="3531b-186">Status</span></span>](/windows/client-management/mdm/windowslicensing-csp#subscriptions-subscriptionid-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3531b-187">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3531b-187">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3531b-188">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3531b-188">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3531b-189">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3531b-189">Requirements</span></span>



| <span data-ttu-id="3531b-190">Requisito</span><span class="sxs-lookup"><span data-stu-id="3531b-190">Requirement</span></span> | <span data-ttu-id="3531b-191">Valore</span><span class="sxs-lookup"><span data-stu-id="3531b-191">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3531b-192">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3531b-192">Minimum supported client</span></span><br/> | <span data-ttu-id="3531b-193">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="3531b-193">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3531b-194">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3531b-194">Minimum supported server</span></span><br/> | <span data-ttu-id="3531b-195">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3531b-195">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="3531b-196">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3531b-196">Namespace</span></span><br/>                | <span data-ttu-id="3531b-197">\\ \\ DMMap MDM CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="3531b-197">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="3531b-198">MOF</span><span class="sxs-lookup"><span data-stu-id="3531b-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3531b-199"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3531b-199"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3531b-200">DLL</span><span class="sxs-lookup"><span data-stu-id="3531b-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3531b-201"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3531b-201"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3531b-202">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3531b-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3531b-203">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="3531b-203">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

