---
description: Utilizzato per proteggere le singole parti di un'applicazione in un ambiente bloccato. Può essere usato con l'installazione di file, chiavi del registro di sistema e cartelle create.
ms.assetid: 7c20e211-7704-49c2-a0c5-aaa695a09764
title: Tabella LockPermissions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c07402b80caec7beff68083567f2ff2fb9bf5eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311734"
---
# <a name="lockpermissions-table"></a><span data-ttu-id="793e3-104">Tabella LockPermissions</span><span class="sxs-lookup"><span data-stu-id="793e3-104">LockPermissions Table</span></span>

<span data-ttu-id="793e3-105">La tabella LockPermissions viene utilizzata per proteggere le singole parti di un'applicazione in un ambiente bloccato.</span><span class="sxs-lookup"><span data-stu-id="793e3-105">The LockPermissions Table is used to secure individual portions of an application in a locked-down environment.</span></span> <span data-ttu-id="793e3-106">Può essere usato con l'installazione di file, chiavi del registro di sistema e cartelle create.</span><span class="sxs-lookup"><span data-stu-id="793e3-106">It can be used with the installation of files, registry keys, and created folders.</span></span>

<span data-ttu-id="793e3-107">Un pacchetto progettato per l'installazione in Windows Server 2008 R2 o Windows 7 deve usare la [tabella MsiLockPermissionsEx](msilockpermissionsex-table.md) anziché la tabella LockPermissions.</span><span class="sxs-lookup"><span data-stu-id="793e3-107">A package intended for installation in Windows Server 2008 R2 or Windows 7 should use the [MsiLockPermissionsEx Table](msilockpermissionsex-table.md) rather than the LockPermissions Table.</span></span> <span data-ttu-id="793e3-108">Windows Installer versioni precedenti alla Windows Installer 5,0 ignorano la tabella MsiLockPermissionsEx.</span><span class="sxs-lookup"><span data-stu-id="793e3-108">Windows Installer versions earlier than Windows Installer 5.0 ignore the MsiLockPermissionsEx Table.</span></span> <span data-ttu-id="793e3-109">Windows Installer 5,0 può installare un pacchetto che contiene la tabella LockPermissions.</span><span class="sxs-lookup"><span data-stu-id="793e3-109">Windows Installer 5.0 can install an package that contains the LockPermissions Table.</span></span> <span data-ttu-id="793e3-110">A partire da Windows Installer 5,0, l'installazione di un pacchetto che contiene sia la tabella MsiLockPermissionsEx che la tabella LockPermissions ha esito negativo e restituisce Windows Installer messaggio di errore 1941.</span><span class="sxs-lookup"><span data-stu-id="793e3-110">Beginning with Windows Installer 5.0, installation of a package that contains both the MsiLockPermissionsEx Table and the LockPermissions Table fails and returns Windows Installer error message 1941.</span></span>

<span data-ttu-id="793e3-111">La tabella LockPermissions include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="793e3-111">The LockPermissions Table has the following columns.</span></span>



| <span data-ttu-id="793e3-112">Colonna</span><span class="sxs-lookup"><span data-stu-id="793e3-112">Column</span></span>     | <span data-ttu-id="793e3-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="793e3-113">Type</span></span>                               | <span data-ttu-id="793e3-114">Chiave</span><span class="sxs-lookup"><span data-stu-id="793e3-114">Key</span></span> | <span data-ttu-id="793e3-115">Nullable</span><span class="sxs-lookup"><span data-stu-id="793e3-115">Nullable</span></span> |
|------------|------------------------------------|-----|----------|
| <span data-ttu-id="793e3-116">LockObject</span><span class="sxs-lookup"><span data-stu-id="793e3-116">LockObject</span></span> | [<span data-ttu-id="793e3-117">Identificatore</span><span class="sxs-lookup"><span data-stu-id="793e3-117">Identifier</span></span>](identifier.md)       | <span data-ttu-id="793e3-118">S</span><span class="sxs-lookup"><span data-stu-id="793e3-118">Y</span></span>   | <span data-ttu-id="793e3-119">N</span><span class="sxs-lookup"><span data-stu-id="793e3-119">N</span></span>        |
| <span data-ttu-id="793e3-120">Tabella</span><span class="sxs-lookup"><span data-stu-id="793e3-120">Table</span></span>      | [<span data-ttu-id="793e3-121">Text</span><span class="sxs-lookup"><span data-stu-id="793e3-121">Text</span></span>](text.md)                   | <span data-ttu-id="793e3-122">S</span><span class="sxs-lookup"><span data-stu-id="793e3-122">Y</span></span>   | <span data-ttu-id="793e3-123">N</span><span class="sxs-lookup"><span data-stu-id="793e3-123">N</span></span>        |
| <span data-ttu-id="793e3-124">Dominio</span><span class="sxs-lookup"><span data-stu-id="793e3-124">Domain</span></span>     | [<span data-ttu-id="793e3-125">Formattato</span><span class="sxs-lookup"><span data-stu-id="793e3-125">Formatted</span></span>](formatted.md)         | <span data-ttu-id="793e3-126">S</span><span class="sxs-lookup"><span data-stu-id="793e3-126">Y</span></span>   | <span data-ttu-id="793e3-127">S</span><span class="sxs-lookup"><span data-stu-id="793e3-127">Y</span></span>        |
| <span data-ttu-id="793e3-128">User</span><span class="sxs-lookup"><span data-stu-id="793e3-128">User</span></span>       | [<span data-ttu-id="793e3-129">Formattato</span><span class="sxs-lookup"><span data-stu-id="793e3-129">Formatted</span></span>](formatted.md)         | <span data-ttu-id="793e3-130">S</span><span class="sxs-lookup"><span data-stu-id="793e3-130">Y</span></span>   | <span data-ttu-id="793e3-131">N</span><span class="sxs-lookup"><span data-stu-id="793e3-131">N</span></span>        |
| <span data-ttu-id="793e3-132">Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="793e3-132">Permission</span></span> | [<span data-ttu-id="793e3-133">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="793e3-133">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="793e3-134">N</span><span class="sxs-lookup"><span data-stu-id="793e3-134">N</span></span>   | <span data-ttu-id="793e3-135">S</span><span class="sxs-lookup"><span data-stu-id="793e3-135">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="793e3-136">Colonne</span><span class="sxs-lookup"><span data-stu-id="793e3-136">Columns</span></span>

<dl> <dt>

<span data-ttu-id="793e3-137"><span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject</span><span class="sxs-lookup"><span data-stu-id="793e3-137"><span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject</span></span>
</dt> <dd>

<span data-ttu-id="793e3-138">Questa colonna e la colonna della tabella specificano insieme il file, la directory o la chiave del registro di sistema da proteggere.</span><span class="sxs-lookup"><span data-stu-id="793e3-138">This column and the Table column together specify the file, directory, or registry key that is to be secured.</span></span> <span data-ttu-id="793e3-139">La colonna LockObject è una chiave esterna che punta alla chiave primaria della tabella specificata dalla colonna della tabella.</span><span class="sxs-lookup"><span data-stu-id="793e3-139">The LockObject column is a foreign key that points to the primary key of the table specified by the Table column.</span></span>

</dd> <dt>

<span data-ttu-id="793e3-140"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>tavolo</span><span class="sxs-lookup"><span data-stu-id="793e3-140"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="793e3-141">Questa colonna e la colonna LockObject specificano il file, la directory o la chiave del registro di sistema da proteggere.</span><span class="sxs-lookup"><span data-stu-id="793e3-141">This column and the LockObject column specify the file, directory, or registry key that is to be secured.</span></span> <span data-ttu-id="793e3-142">Nella colonna della tabella immettere file, Registry o CreateFolder per specificare un LockObject elencato nella tabella [file](file-table.md), nella [tabella del registro di sistema](registry-table.md)o nella [tabella CreateFolder](createfolder-table.md).</span><span class="sxs-lookup"><span data-stu-id="793e3-142">In the Table column, enter File, Registry, or CreateFolder to specify a LockObject listed in the [File Table](file-table.md), [Registry Table](registry-table.md), or [CreateFolder Table](createfolder-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="793e3-143"><span id="Domain"></span><span id="domain"></span><span id="DOMAIN"></span>Dominio</span><span class="sxs-lookup"><span data-stu-id="793e3-143"><span id="Domain"></span><span id="domain"></span><span id="DOMAIN"></span>Domain</span></span>
</dt> <dd>

<span data-ttu-id="793e3-144">Colonna che identifica il dominio dell'utente per il quale devono essere impostate le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="793e3-144">The column that identifies the domain of the user for which permissions are to be set.</span></span> <span data-ttu-id="793e3-145">Si tratta del nome di un computer autonomo o di un nome di dominio.</span><span class="sxs-lookup"><span data-stu-id="793e3-145">This is the name of a stand-alone machine or a domain name.</span></span> <span data-ttu-id="793e3-146">Il tipo di dati della colonna è [formattato](formatted.md)ed è possibile usare la stringa \[ % UserDomain \] in questo campo per ottenere il valore della variabile di ambiente UserDomain per il dominio corrente.</span><span class="sxs-lookup"><span data-stu-id="793e3-146">The column data type is [Formatted](formatted.md), and you may use the string \[%USERDOMAIN\] in this field to get the value of the USERDOMAIN environment variable for the current domain.</span></span> <span data-ttu-id="793e3-147">Per ottenere qualsiasi altro dominio, è necessario usare [azioni personalizzate](custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="793e3-147">To get any other domain requires using [Custom Actions](custom-actions.md).</span></span> <span data-ttu-id="793e3-148">Per ulteriori informazioni, vedere la tabella delle azioni personalizzata.</span><span class="sxs-lookup"><span data-stu-id="793e3-148">For more information, see the Custom Action Table.</span></span>

</dd> <dt>

<span data-ttu-id="793e3-149"><span id="User"></span><span id="user"></span><span id="USER"></span>Utente</span><span class="sxs-lookup"><span data-stu-id="793e3-149"><span id="User"></span><span id="user"></span><span id="USER"></span>User</span></span>
</dt> <dd>

<span data-ttu-id="793e3-150">Colonna che identifica il nome localizzato dell'utente per il quale devono essere impostate le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="793e3-150">The column that identifies the localized name of the user for which permissions are to be set.</span></span> <span data-ttu-id="793e3-151">Questo nome deve trovarsi nel computer o nel dominio.</span><span class="sxs-lookup"><span data-stu-id="793e3-151">This name must be located on the machine or domain.</span></span> <span data-ttu-id="793e3-152">L'installazione non riesce se il computer o il controller di dominio non riconosce la combinazione di dominio e utente o se non è possibile recuperare l'ID di sicurezza (SID) dell'utente.</span><span class="sxs-lookup"><span data-stu-id="793e3-152">The installation fails if the machine or domain controller does not recognize the domain and user combination or if the user's security identifier (SID) cannot be retrieved.</span></span> <span data-ttu-id="793e3-153">È possibile specificare più utenti per un singolo LockObject.</span><span class="sxs-lookup"><span data-stu-id="793e3-153">Multiple users can be specified for a single LockObject.</span></span>

<span data-ttu-id="793e3-154">I nomi utente comuni "Everyone" e "Administrators" possono essere immessi in inglese e sono mappati a SID noti.</span><span class="sxs-lookup"><span data-stu-id="793e3-154">The common user names "Everyone" and "Administrators" may be entered in English and are mapped to well-known SIDs.</span></span> <span data-ttu-id="793e3-155">Per LocalSystem viene fornito il controllo completo in tutti i descrittori di sicurezza creati tramite la tabella LockPermissions.</span><span class="sxs-lookup"><span data-stu-id="793e3-155">LocalSystem is given full control in all security descriptors created through the LockPermissions Table.</span></span> <span data-ttu-id="793e3-156">È possibile usare la proprietà [**ComputerName**](computername.md), la proprietà [**LogonUser**](logonuser.md) o la [**proprietà UserName**](username.md) in questo campo per ottenere l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="793e3-156">You can use the [**ComputerName Property**](computername.md), [**LogonUser Property**](logonuser.md) or [**USERNAME Property**](username.md) in this field to get the current user.</span></span> <span data-ttu-id="793e3-157">Per immettere il nome localizzato di un altro utente o gruppo, è necessaria un'azione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="793e3-157">A custom action is required to enter the localized name of any other user or group.</span></span>

<span data-ttu-id="793e3-158">Per specificare gli elenchi di controllo di accesso per più utenti, è possibile usare più record con LockObject e voci di tabella identici (ma con voci utente diverse).</span><span class="sxs-lookup"><span data-stu-id="793e3-158">You can use multiple records with identical LockObject and Table entries (but different User entries) to specify access control lists for multiple users.</span></span>

</dd> <dt>

<span data-ttu-id="793e3-159"><span id="Permission"></span><span id="permission"></span><span id="PERMISSION"></span>Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="793e3-159"><span id="Permission"></span><span id="permission"></span><span id="PERMISSION"></span>Permission</span></span>
</dt> <dd>

<span data-ttu-id="793e3-160">Colonna che identifica la descrizione intera dei privilegi di sistema.</span><span class="sxs-lookup"><span data-stu-id="793e3-160">The column that identifies the integer description of system privileges.</span></span> <span data-ttu-id="793e3-161">Di seguito sono riportati i valori usati più di frequente (un elenco completo esiste in Winnt. h).</span><span class="sxs-lookup"><span data-stu-id="793e3-161">The following gives the most commonly used values (a complete list exists in Winnt.h).</span></span>



| <span data-ttu-id="793e3-162">Privilege</span><span class="sxs-lookup"><span data-stu-id="793e3-162">Privilege</span></span>                                                              | <span data-ttu-id="793e3-163">Descrizione</span><span class="sxs-lookup"><span data-stu-id="793e3-163">Description</span></span>                     |
|------------------------------------------------------------------------|---------------------------------|
| <span data-ttu-id="793e3-164">tutti GENERIci \_</span><span class="sxs-lookup"><span data-stu-id="793e3-164">GENERIC\_ALL</span></span><br/> <span data-ttu-id="793e3-165">0X10000000</span><span class="sxs-lookup"><span data-stu-id="793e3-165">0X10000000</span></span><br/> <span data-ttu-id="793e3-166">268435456</span><span class="sxs-lookup"><span data-stu-id="793e3-166">268435456</span></span><br/>     | <span data-ttu-id="793e3-167">Accesso in lettura, scrittura ed esecuzione</span><span class="sxs-lookup"><span data-stu-id="793e3-167">Read, write, and execute access</span></span> |
| <span data-ttu-id="793e3-168">esecuzione GENERIca \_</span><span class="sxs-lookup"><span data-stu-id="793e3-168">GENERIC\_EXECUTE</span></span><br/> <span data-ttu-id="793e3-169">0X20000000</span><span class="sxs-lookup"><span data-stu-id="793e3-169">0X20000000</span></span><br/> <span data-ttu-id="793e3-170">536870912</span><span class="sxs-lookup"><span data-stu-id="793e3-170">536870912</span></span><br/> | <span data-ttu-id="793e3-171">Esegui accesso</span><span class="sxs-lookup"><span data-stu-id="793e3-171">Execute access</span></span>                  |
| <span data-ttu-id="793e3-172">scrittura GENERIca \_</span><span class="sxs-lookup"><span data-stu-id="793e3-172">GENERIC\_WRITE</span></span><br/> <span data-ttu-id="793e3-173">0X40000000</span><span class="sxs-lookup"><span data-stu-id="793e3-173">0X40000000</span></span><br/> <span data-ttu-id="793e3-174">1073741824</span><span class="sxs-lookup"><span data-stu-id="793e3-174">1073741824</span></span><br/>  | <span data-ttu-id="793e3-175">Accesso in scrittura</span><span class="sxs-lookup"><span data-stu-id="793e3-175">Write access</span></span>                    |



 

<span data-ttu-id="793e3-176">Non è possibile specificare \_ la lettura generica nella colonna autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="793e3-176">You cannot specify GENERIC\_READ in the Permission column.</span></span> <span data-ttu-id="793e3-177">Il tentativo di eseguire questa operazione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="793e3-177">Attempting to do so will fail.</span></span> <span data-ttu-id="793e3-178">Al contrario, è necessario specificare un valore, ad esempio lettura chiave \_ o \_ lettura file generica \_ .</span><span class="sxs-lookup"><span data-stu-id="793e3-178">Instead, you must specify a value such as KEY\_READ or FILE\_GENERIC\_READ.</span></span>

<span data-ttu-id="793e3-179">Il valore null immesso in questa colonna è riservato per un utilizzo futuro.</span><span class="sxs-lookup"><span data-stu-id="793e3-179">Null entered in this column is reserved for future use.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="793e3-180">Commenti</span><span class="sxs-lookup"><span data-stu-id="793e3-180">Remarks</span></span>

<span data-ttu-id="793e3-181">Le azioni [InstallFiles](installfiles-action.md), [WriteRegistryValori consente](writeregistryvalues-action.md)e [CreateFolders](createfolders-action.md) nelle [*tabelle di sequenza*](s-gly.md) elaborano le informazioni contenute in questa tabella.</span><span class="sxs-lookup"><span data-stu-id="793e3-181">The [InstallFiles](installfiles-action.md), [WriteRegistryValues](writeregistryvalues-action.md), and [CreateFolders](createfolders-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="793e3-182">Per informazioni sull'utilizzo di *tabelle di sequenza*, vedere [utilizzo di una tabella di sequenza](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="793e3-182">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

<span data-ttu-id="793e3-183">L'autorizzazione può essere impostata solo nella tabella LockPermissions per gli utenti già presenti nel computer o nel dominio.</span><span class="sxs-lookup"><span data-stu-id="793e3-183">Permission can only be set in the LockPermissions Table for users that already exist on the computer or domain.</span></span> <span data-ttu-id="793e3-184">Il tentativo di impostare le autorizzazioni per un utente sconosciuto comporta l'esito negativo dell'installazione, anche se tale account utente viene creato durante l'installazione mediante un'azione personalizzata posticipata.</span><span class="sxs-lookup"><span data-stu-id="793e3-184">An attempt to set permissions for an unknown user causes the installation to fail, even if that user account is created during the installation by a deferred custom action.</span></span>

<span data-ttu-id="793e3-185">Si consiglia di includere il gruppo locale dell'amministratore di sistema in tutti gli elenchi di controllo di accesso (ACL).</span><span class="sxs-lookup"><span data-stu-id="793e3-185">It is recommended that the system administrator's local group be included in all access control lists (ACL).</span></span> <span data-ttu-id="793e3-186">Ciò garantisce che l'amministratore di sistema possa accedere e gestire gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="793e3-186">This ensures that the system administrator can access and maintain objects.</span></span>

<span data-ttu-id="793e3-187">Ogni file, chiave del registro di sistema o directory elencato nella tabella LockPermissions riceve un descrittore di sicurezza esplicito, indipendentemente dal fatto che venga sostituito o meno un oggetto esistente.</span><span class="sxs-lookup"><span data-stu-id="793e3-187">Every file, registry key, or directory that is listed in the LockPermissions Table receives an explicit security descriptor, whether it replaces an existing object or not.</span></span> <span data-ttu-id="793e3-188">Il Windows Installer tenta di mantenere la sicurezza per gli oggetti già presenti nel sistema.</span><span class="sxs-lookup"><span data-stu-id="793e3-188">The Windows Installer attempts to preserve the security on objects that already exist on the system.</span></span> <span data-ttu-id="793e3-189">Se un oggetto non è elencato nella tabella LockPermissions e sostituisce un oggetto esistente, la sostituzione ottiene le impostazioni di sicurezza dell'oggetto che sostituisce.</span><span class="sxs-lookup"><span data-stu-id="793e3-189">If an object is not listed in the LockPermissions Table, and replaces an existing object, the replacement gets the security settings of the object that it replaces.</span></span>

<span data-ttu-id="793e3-190">Se un oggetto non è elencato nella tabella LockPermissions e non sostituisce un oggetto esistente, non riceve alcun descrittore di sicurezza esplicito.</span><span class="sxs-lookup"><span data-stu-id="793e3-190">If an object is not listed in the LockPermissions Table, and does not replace an existing object, it receives no explicit security descriptor.</span></span> <span data-ttu-id="793e3-191">L'accesso al nuovo oggetto si basa sugli attributi del relativo oggetto padre o contenitore.</span><span class="sxs-lookup"><span data-stu-id="793e3-191">The access to the new object is based on the attributes of its parent or container object.</span></span> <span data-ttu-id="793e3-192">Se un oggetto non è elencato nella tabella e sostituisce un oggetto senza descrittore di sicurezza esplicito, l'accesso al nuovo oggetto si basa sugli attributi del relativo oggetto padre o contenitore.</span><span class="sxs-lookup"><span data-stu-id="793e3-192">If an object is not listed in the table, and replaces an object with no explicit security descriptor, the access to the new object is based on the attributes of its parent or container object.</span></span>

<span data-ttu-id="793e3-193">Il Windows Installer imposta la proprietà [**UserSID**](usersid.md) sull'ID di sicurezza (SID) o sull'utente che esegue l'installazione.</span><span class="sxs-lookup"><span data-stu-id="793e3-193">The Windows Installer sets the [**UserSID**](usersid.md) property to the security identifier (SID) or the user running the installation.</span></span>

## <a name="validation"></a><span data-ttu-id="793e3-194">Convalida</span><span class="sxs-lookup"><span data-stu-id="793e3-194">Validation</span></span>

<dl>

[<span data-ttu-id="793e3-195">ICE03</span><span class="sxs-lookup"><span data-stu-id="793e3-195">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="793e3-196">ICE06</span><span class="sxs-lookup"><span data-stu-id="793e3-196">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="793e3-197">ICE46</span><span class="sxs-lookup"><span data-stu-id="793e3-197">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="793e3-198">ICE55</span><span class="sxs-lookup"><span data-stu-id="793e3-198">ICE55</span></span>](ice55.md)  
</dl>

 

 




