---
description: La tabella MsiLockPermissionsEx può essere utilizzata per proteggere servizi, file, chiavi del registro di sistema e cartelle create.
ms.assetid: c642f02d-07fa-463f-8151-769c28a71a5c
title: Tabella MsiLockPermissionsEx
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63d7c63e27d7a9c390e6015eb0ebe5f663de5b4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317124"
---
# <a name="msilockpermissionsex-table"></a><span data-ttu-id="ddc0f-103">Tabella MsiLockPermissionsEx</span><span class="sxs-lookup"><span data-stu-id="ddc0f-103">MsiLockPermissionsEx Table</span></span>

<span data-ttu-id="ddc0f-104">La tabella MsiLockPermissionsEx può essere utilizzata per proteggere servizi, file, chiavi del registro di sistema e cartelle create.</span><span class="sxs-lookup"><span data-stu-id="ddc0f-104">The MsiLockPermissionsEx Table can be used to secure services, files, registry keys, and created folders.</span></span>

<span data-ttu-id="ddc0f-105">Un pacchetto non deve contenere sia la tabella MsiLockPermissionsEx che la [tabella LockPermissions](lockpermissions-table.md).</span><span class="sxs-lookup"><span data-stu-id="ddc0f-105">A package should not contain both the MsiLockPermissionsEx Table and the [LockPermissions Table](lockpermissions-table.md).</span></span>

<span data-ttu-id="ddc0f-106">**[Windows Installer 4,5 o versioni precedenti](not-supported-in-windows-installer-4-5.md):** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="ddc0f-106">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="ddc0f-107">Questa tabella è consigliata per i pacchetti destinati all'installazione con Windows Installer 5,0 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="ddc0f-107">This table is recommended for packages intended for installation with Windows Installer 5.0 or later.</span></span>

<span data-ttu-id="ddc0f-108">La tabella MsiLockPermissionsEx include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="ddc0f-108">The MsiLockPermissionsEx Table has the following columns.</span></span>



| <span data-ttu-id="ddc0f-109">Colonna</span><span class="sxs-lookup"><span data-stu-id="ddc0f-109">Column</span></span>               | <span data-ttu-id="ddc0f-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="ddc0f-110">Type</span></span>                                       | <span data-ttu-id="ddc0f-111">Chiave</span><span class="sxs-lookup"><span data-stu-id="ddc0f-111">Key</span></span> | <span data-ttu-id="ddc0f-112">Nullable</span><span class="sxs-lookup"><span data-stu-id="ddc0f-112">Nullable</span></span> |
|----------------------|--------------------------------------------|-----|----------|
| <span data-ttu-id="ddc0f-113">MsiLockPermissionsEx</span><span class="sxs-lookup"><span data-stu-id="ddc0f-113">MsiLockPermissionsEx</span></span> | [<span data-ttu-id="ddc0f-114">Text</span><span class="sxs-lookup"><span data-stu-id="ddc0f-114">Text</span></span>](text.md)                           | <span data-ttu-id="ddc0f-115">S</span><span class="sxs-lookup"><span data-stu-id="ddc0f-115">Y</span></span>   | <span data-ttu-id="ddc0f-116">N</span><span class="sxs-lookup"><span data-stu-id="ddc0f-116">N</span></span>        |
| <span data-ttu-id="ddc0f-117">LockObject</span><span class="sxs-lookup"><span data-stu-id="ddc0f-117">LockObject</span></span>           | [<span data-ttu-id="ddc0f-118">Identificatore</span><span class="sxs-lookup"><span data-stu-id="ddc0f-118">Identifier</span></span>](identifier.md)               | <span data-ttu-id="ddc0f-119">N</span><span class="sxs-lookup"><span data-stu-id="ddc0f-119">N</span></span>   | <span data-ttu-id="ddc0f-120">N</span><span class="sxs-lookup"><span data-stu-id="ddc0f-120">N</span></span>        |
| <span data-ttu-id="ddc0f-121">Tabella</span><span class="sxs-lookup"><span data-stu-id="ddc0f-121">Table</span></span>                | [<span data-ttu-id="ddc0f-122">Text</span><span class="sxs-lookup"><span data-stu-id="ddc0f-122">Text</span></span>](text.md)                           | <span data-ttu-id="ddc0f-123">N</span><span class="sxs-lookup"><span data-stu-id="ddc0f-123">N</span></span>   | <span data-ttu-id="ddc0f-124">N</span><span class="sxs-lookup"><span data-stu-id="ddc0f-124">N</span></span>        |
| <span data-ttu-id="ddc0f-125">SDDLText</span><span class="sxs-lookup"><span data-stu-id="ddc0f-125">SDDLText</span></span>             | [<span data-ttu-id="ddc0f-126">FormattedSDDLText</span><span class="sxs-lookup"><span data-stu-id="ddc0f-126">FormattedSDDLText</span></span>](formattedsddltext.md) | <span data-ttu-id="ddc0f-127">N</span><span class="sxs-lookup"><span data-stu-id="ddc0f-127">N</span></span>   | <span data-ttu-id="ddc0f-128">N</span><span class="sxs-lookup"><span data-stu-id="ddc0f-128">N</span></span>        |
| <span data-ttu-id="ddc0f-129">Condizione</span><span class="sxs-lookup"><span data-stu-id="ddc0f-129">Condition</span></span>            | [<span data-ttu-id="ddc0f-130">Condition</span><span class="sxs-lookup"><span data-stu-id="ddc0f-130">Condition</span></span>](condition.md)                 | <span data-ttu-id="ddc0f-131">N</span><span class="sxs-lookup"><span data-stu-id="ddc0f-131">N</span></span>   | <span data-ttu-id="ddc0f-132">S</span><span class="sxs-lookup"><span data-stu-id="ddc0f-132">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="ddc0f-133">Colonne</span><span class="sxs-lookup"><span data-stu-id="ddc0f-133">Columns</span></span>

<dl> <dt>

<span data-ttu-id="ddc0f-134"><span id="MsiLockPermissionsEx"></span><span id="msilockpermissionsex"></span><span id="MSILOCKPERMISSIONSEX"></span>MsiLockPermissionsEx</span><span class="sxs-lookup"><span data-stu-id="ddc0f-134"><span id="MsiLockPermissionsEx"></span><span id="msilockpermissionsex"></span><span id="MSILOCKPERMISSIONSEX"></span>MsiLockPermissionsEx</span></span>
</dt> <dd>

<span data-ttu-id="ddc0f-135">Si tratta della chiave primaria della tabella.</span><span class="sxs-lookup"><span data-stu-id="ddc0f-135">This is the primary key of this table.</span></span>

</dd> <dt>

<span data-ttu-id="ddc0f-136"><span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject</span><span class="sxs-lookup"><span data-stu-id="ddc0f-136"><span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject</span></span>
</dt> <dd>

<span data-ttu-id="ddc0f-137">Questa colonna e la colonna della tabella consentono di specificare il file, la directory, la chiave del registro di sistema o il servizio che deve essere protetto.</span><span class="sxs-lookup"><span data-stu-id="ddc0f-137">This column and the Table column together specify the file, directory, registry key, or service that is to be secured.</span></span> <span data-ttu-id="ddc0f-138">La colonna LockObject è una chiave esterna che punta alla chiave primaria della tabella specificata dalla colonna della tabella.</span><span class="sxs-lookup"><span data-stu-id="ddc0f-138">The LockObject column is a foreign key that points to the primary key of the table specified by the Table column.</span></span>

</dd> <dt>

<span data-ttu-id="ddc0f-139"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>tavolo</span><span class="sxs-lookup"><span data-stu-id="ddc0f-139"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="ddc0f-140">Questa colonna e la colonna LockObject specificano il file, la directory, la chiave del registro di sistema o il servizio che deve essere protetto.</span><span class="sxs-lookup"><span data-stu-id="ddc0f-140">This column and the LockObject column specify the file, directory, registry key, or service that is to be secured.</span></span> <span data-ttu-id="ddc0f-141">Nella colonna della tabella immettere file, Registry, CreateFolder o ServiceInstall per specificare un LockObject elencato nella tabella [file](file-table.md), tabella Registro di [sistema](registry-table.md), tabella [CreateFolder](createfolder-table.md)o [tabella ServiceInstall](serviceinstall-table.md).</span><span class="sxs-lookup"><span data-stu-id="ddc0f-141">In the Table column, enter File, Registry, CreateFolder, or ServiceInstall to specify a LockObject listed in the [File Table](file-table.md), [Registry Table](registry-table.md), [CreateFolder Table](createfolder-table.md), or [ServiceInstall Table](serviceinstall-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddc0f-142"><span id="SDDLText"></span><span id="sddltext"></span><span id="SDDLTEXT"></span>SDDLText</span><span class="sxs-lookup"><span data-stu-id="ddc0f-142"><span id="SDDLText"></span><span id="sddltext"></span><span id="SDDLTEXT"></span>SDDLText</span></span>
</dt> <dd>

<span data-ttu-id="ddc0f-143">Immettere la stringa SDDL per indicare le autorizzazioni da applicare all'oggetto selezionato.</span><span class="sxs-lookup"><span data-stu-id="ddc0f-143">Enter the SDDL string to indicate permissions to apply to selected object.</span></span> <span data-ttu-id="ddc0f-144">L'SDDL deve essere specificato nel [formato stringa del descrittore di sicurezza](../secauthz/security-descriptor-string-format.md).</span><span class="sxs-lookup"><span data-stu-id="ddc0f-144">The SDDL must be provided in [Security Descriptor String Format](../secauthz/security-descriptor-string-format.md).</span></span>

<span data-ttu-id="ddc0f-145">Questo non supporta le proprietà private o Public.</span><span class="sxs-lookup"><span data-stu-id="ddc0f-145">This does not support private or public properties.</span></span>

</dd> <dt>

<span data-ttu-id="ddc0f-146"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condizione</span><span class="sxs-lookup"><span data-stu-id="ddc0f-146"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="ddc0f-147">Questa colonna contiene un'espressione condizionale utilizzata per determinare se applicare l'autorizzazione specificata.</span><span class="sxs-lookup"><span data-stu-id="ddc0f-147">This column contains a conditional expression used to determine whether to apply the specified permission.</span></span> <span data-ttu-id="ddc0f-148">Se la condizione restituisce **false**, l'autorizzazione non viene applicata.</span><span class="sxs-lookup"><span data-stu-id="ddc0f-148">If the condition evaluates to **FALSE**, the permission is not applied.</span></span> <span data-ttu-id="ddc0f-149">Se la condizione restituisce **true**, viene applicata l'autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="ddc0f-149">If the condition evaluates to **TRUE**, the permission is applied.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ddc0f-150">Commenti</span><span class="sxs-lookup"><span data-stu-id="ddc0f-150">Remarks</span></span>

<span data-ttu-id="ddc0f-151">Per ulteriori informazioni sulla protezione di servizi, file, chiavi del registro di sistema e cartelle create, vedere la pagina relativa alla [protezione delle risorse](securing-resources-.md).</span><span class="sxs-lookup"><span data-stu-id="ddc0f-151">See [Securing Resources](securing-resources-.md)for more information about securing services, files, registry keys, and created folders.</span></span>

<span data-ttu-id="ddc0f-152">Usare la tabella MsiLockPermissionsEx per proteggere gli oggetti per un account utente che viene creato durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="ddc0f-152">Use the MsiLockPermissionsEx Table to secure objects for a user account that is being created during the installation.</span></span> <span data-ttu-id="ddc0f-153">L'account utente deve esistere già quando l'installazione protegge l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ddc0f-153">The user account must already exist when the installation secures the object.</span></span> <span data-ttu-id="ddc0f-154">Creare l'account utente prima di installare il file, la chiave del registro di sistema, la cartella o il servizio protetto.</span><span class="sxs-lookup"><span data-stu-id="ddc0f-154">Create the user account before installing the file, registry key, folder or service being secured.</span></span>

<span data-ttu-id="ddc0f-155">Se una LockObject e una coppia di tabelle in questa tabella hanno più di un'espressione condizionale che restituisce true, l'installazione non riesce e Windows Installer restituisce un messaggio di errore 1942.</span><span class="sxs-lookup"><span data-stu-id="ddc0f-155">If a LockObject and Table pair in this table has more than one conditional expression that evaluates to true, the installation fails and Windows Installer returns an error message 1942.</span></span>

<span data-ttu-id="ddc0f-156">Se la stringa [FormattedSDDLText](formattedsddltext.md) nel campo SDDLText non può essere risolta in una stringa SDDL valida, l'installazione non riesce e Windows Installer restituisce un messaggio di errore 1943.</span><span class="sxs-lookup"><span data-stu-id="ddc0f-156">If the [FormattedSDDLText](formattedsddltext.md) string in the SDDLText field cannot be resolved into a valid SDDL string, the installation fails and Windows Installer returns an error message 1943.</span></span>

<span data-ttu-id="ddc0f-157">Se l'utente non dispone di privilegi sufficienti per impostare il descrittore di sicurezza specificato dal campo SDDLText in un file o una cartella, l'installazione non riesce e Windows Installer restituisce un messaggio di errore 1926.</span><span class="sxs-lookup"><span data-stu-id="ddc0f-157">If the user does not have sufficient privileges to set the security descriptor specified by the SDDLText field on a file or folder, the installation fails and Windows Installer returns an error message 1926.</span></span>

<span data-ttu-id="ddc0f-158">Se l'utente non dispone di privilegi sufficienti per impostare il descrittore di sicurezza specificato dal campo SDDLText in una chiave del registro di sistema, l'installazione non riesce e Windows Installer restituisce un messaggio di errore 1401.</span><span class="sxs-lookup"><span data-stu-id="ddc0f-158">If the user does not have sufficient privileges to set the security descriptor specified by the SDDLText field on a registry key, the installation fails and Windows Installer returns an error message 1401.</span></span>

<span data-ttu-id="ddc0f-159">Se l'utente non dispone di privilegi sufficienti per impostare il descrittore di sicurezza specificato dal campo SDDLText in un servizio, l'installazione non riesce e Windows Installer restituisce un messaggio di errore 1944.</span><span class="sxs-lookup"><span data-stu-id="ddc0f-159">If the user does not have sufficient privileges to set the security descriptor specified by the SDDLText field on a service, the installation fails and Windows Installer returns an error message 1944.</span></span>

## <a name="validation"></a><span data-ttu-id="ddc0f-160">Convalida</span><span class="sxs-lookup"><span data-stu-id="ddc0f-160">Validation</span></span>

<dl>

[<span data-ttu-id="ddc0f-161">ICE104</span><span class="sxs-lookup"><span data-stu-id="ddc0f-161">ICE104</span></span>](ice-104.md)  
[<span data-ttu-id="ddc0f-162">ICE03</span><span class="sxs-lookup"><span data-stu-id="ddc0f-162">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="ddc0f-163">ICE06</span><span class="sxs-lookup"><span data-stu-id="ddc0f-163">ICE06</span></span>](ice06.md)  
</dl>

 

 
