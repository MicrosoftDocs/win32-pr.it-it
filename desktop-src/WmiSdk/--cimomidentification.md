---
description: Descrive l'installazione locale di WMI.
ms.assetid: 907b65b2-a853-40f4-8b36-5a05a2b1cf85
ms.tgt_platform: multiple
title: Classe __CIMOMIdentification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __CIMOMIdentification
- Root.__CIMOMIdentification.SetupDateTime
- Root.__CIMOMIdentification.VersionCurrentlyRunning
- Root.__CIMOMIdentification.VersionUsedToCreateDB
- Root.__CIMOMIdentification.WorkingDirectory
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: a8590a2a83cdbc9bd06575cf17ddbe65138a4a31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314096"
---
# <a name="__cimomidentification-class"></a><span data-ttu-id="06370-103">\_\_Classe CIMOMIdentification</span><span class="sxs-lookup"><span data-stu-id="06370-103">\_\_CIMOMIdentification class</span></span>

<span data-ttu-id="06370-104">La classe di sistema **\_ \_ CIMOMIdentification** descrive l'installazione locale di WMI.</span><span class="sxs-lookup"><span data-stu-id="06370-104">The **\_\_CIMOMIdentification** system class describes the local installation of WMI.</span></span> <span data-ttu-id="06370-105">Si tratta di una classe singleton; esiste una sola istanza.</span><span class="sxs-lookup"><span data-stu-id="06370-105">This is a singleton class; there is only one instance.</span></span> <span data-ttu-id="06370-106">La classe **\_ \_ CIMOMIdentification** è disponibile solo negli spazi dei nomi **\\ predefiniti** **radice** e radice.</span><span class="sxs-lookup"><span data-stu-id="06370-106">The **\_\_CIMOMIdentification** class is available only in the **Root** and **Root\\Default** namespaces.</span></span> <span data-ttu-id="06370-107">Gli utenti eseguono una query per l'istanza di per ottenere informazioni sull'installazione di WMI.</span><span class="sxs-lookup"><span data-stu-id="06370-107">Users query for the instance to obtain information about the WMI installation.</span></span>

<span data-ttu-id="06370-108">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="06370-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="06370-109">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="06370-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="06370-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="06370-110">Syntax</span></span>

``` syntax
[singleton]
class __CIMOMIdentification : __SystemClass
{
  string SetupDateTime;
  string VersionCurrentlyRunning;
  string VersionUsedToCreateDB;
  string WorkingDirectory;
};
```

## <a name="members"></a><span data-ttu-id="06370-111">Members</span><span class="sxs-lookup"><span data-stu-id="06370-111">Members</span></span>

<span data-ttu-id="06370-112">La classe **\_ \_ CIMOMIdentification** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="06370-112">The **\_\_CIMOMIdentification** class has these types of members:</span></span>

-   [<span data-ttu-id="06370-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="06370-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="06370-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="06370-114">Properties</span></span>

<span data-ttu-id="06370-115">La classe **\_ \_ CIMOMIdentification** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="06370-115">The **\_\_CIMOMIdentification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="06370-116">**SetupDateTime**</span><span class="sxs-lookup"><span data-stu-id="06370-116">**SetupDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06370-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06370-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06370-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06370-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06370-119">Data e ora dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="06370-119">Date and time of installation.</span></span> <span data-ttu-id="06370-120">Questa proprietà è vuota dopo l'installazione del sistema operativo per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="06370-120">This property is empty after the operating system is installed for the first time.</span></span>

<span data-ttu-id="06370-121">Se il repository WMI è stato eliminato e quindi creato nuovamente, questa proprietà contiene la data e l'ora di creazione del repository.</span><span class="sxs-lookup"><span data-stu-id="06370-121">If the WMI repository has been deleted and then created again, this property contains the date and time that the repository is created again.</span></span>

</dd> <dt>

<span data-ttu-id="06370-122">**VersionCurrentlyRunning**</span><span class="sxs-lookup"><span data-stu-id="06370-122">**VersionCurrentlyRunning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06370-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06370-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06370-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06370-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06370-125">Indica la versione dell'immagine effettiva contenente il servizio WMI che ha creato il repository di Common Information Model (CIM).</span><span class="sxs-lookup"><span data-stu-id="06370-125">Indicates the version of the actual image containing the WMI service that created the Common Information Model (CIM) repository.</span></span> <span data-ttu-id="06370-126">Poiché il formato del repository può variare tra le versioni di WMI, questa proprietà consente aggiornamenti WMI futuri per determinare se è necessario aggiornare il database.</span><span class="sxs-lookup"><span data-stu-id="06370-126">Because the repository format may change between versions of WMI, this property allows future WMI upgrades to determine whether the database must be upgraded.</span></span> <span data-ttu-id="06370-127">Il formato è:</span><span class="sxs-lookup"><span data-stu-id="06370-127">The format is:</span></span>

<span data-ttu-id="06370-128">"1.00.183.0000"</span><span class="sxs-lookup"><span data-stu-id="06370-128">"1.00.183.0000"</span></span>

<span data-ttu-id="06370-129">Se la prima cifra è la versione principale, le due cifre successive sono le versioni secondarie e le tre cifre successive corrispondono al numero di Build.</span><span class="sxs-lookup"><span data-stu-id="06370-129">where the first digit is the major version, the next two digits are minor versions, and the next three digits are the build number.</span></span> <span data-ttu-id="06370-130">Le cifre rimanenti non vengono utilizzate.</span><span class="sxs-lookup"><span data-stu-id="06370-130">The remaining digits are not used.</span></span>

</dd> <dt>

<span data-ttu-id="06370-131">**VersionUsedToCreateDB**</span><span class="sxs-lookup"><span data-stu-id="06370-131">**VersionUsedToCreateDB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06370-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06370-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06370-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06370-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06370-134">Indica la versione dell'immagine effettiva contenente il servizio WMI che ha creato il repository CIM.</span><span class="sxs-lookup"><span data-stu-id="06370-134">Indicates the version of the actual image containing the WMI service that created the CIM repository.</span></span> <span data-ttu-id="06370-135">Poiché il formato del repository può variare tra le versioni di WMI, questa proprietà consente aggiornamenti WMI futuri per determinare se è necessario aggiornare il database.</span><span class="sxs-lookup"><span data-stu-id="06370-135">Because the repository format may change between versions of WMI, this property allows future WMI upgrades to determine whether the database must be upgraded.</span></span> <span data-ttu-id="06370-136">Il formato è:</span><span class="sxs-lookup"><span data-stu-id="06370-136">The format is:</span></span>

<span data-ttu-id="06370-137">"1.00.183.0000"</span><span class="sxs-lookup"><span data-stu-id="06370-137">"1.00.183.0000"</span></span>

<span data-ttu-id="06370-138">Se la prima cifra è la versione principale, le due cifre successive sono le versioni secondarie e le tre cifre successive corrispondono al numero di Build.</span><span class="sxs-lookup"><span data-stu-id="06370-138">where the first digit is the major version, the next two digits are minor versions, and the next three digits are the build number.</span></span> <span data-ttu-id="06370-139">Le cifre rimanenti non vengono utilizzate.</span><span class="sxs-lookup"><span data-stu-id="06370-139">The remaining digits are not used.</span></span>

</dd> <dt>

<span data-ttu-id="06370-140">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="06370-140">**WorkingDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06370-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06370-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06370-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06370-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06370-143">Directory di installazione.</span><span class="sxs-lookup"><span data-stu-id="06370-143">Installation directory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="06370-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="06370-144">Remarks</span></span>

<span data-ttu-id="06370-145">La classe **\_ \_ CIMOMIdentification** deriva da [**\_ \_ SystemClass**](--systemclass.md), che non dispone di proprietà.</span><span class="sxs-lookup"><span data-stu-id="06370-145">The **\_\_CIMOMIdentification** class is derived from [**\_\_SystemClass**](--systemclass.md), which has no properties.</span></span>

## <a name="examples"></a><span data-ttu-id="06370-146">Esempio</span><span class="sxs-lookup"><span data-stu-id="06370-146">Examples</span></span>

<span data-ttu-id="06370-147">Nell'esempio di codice VBScript riportato di seguito viene descritto come visualizzare le informazioni di identificazione del modello a oggetti CIM ed è stato ricavato dalla directory di esempio in \\ \\ programmi \\ Microsoft SDK \\ Windows \\ v 7.0 \\ esempi \\ sysmgmt di \\ \\ script WMI.</span><span class="sxs-lookup"><span data-stu-id="06370-147">The following VBScript code sample describes how to display CIM object model identification information, and was taken from the sample directory at \\\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\sysmgmt\\wmi\\scripting.</span></span>


```VB
on error resume next 
set cimomid = GetObject("winmgmts:root\default:__cimomidentification=@")

if err <> 0 then
 WScript.Echo ErrNumber, Err.Source, Err.Description
else
 WScript.Echo cimomid.path_.displayname
 WScript.Echo cimomid.versionusedtocreatedb
end if
```



<span data-ttu-id="06370-148">Nell'esempio di codice Perl seguente viene descritto come visualizzare le informazioni di identificazione del modello a oggetti CIM ed è stato ricavato dalla directory di esempio in \\ \\ programmi \\ Microsoft SDK \\ Windows \\ v 7.0 \\ esempi \\ sysmgmt di \\ \\ script WMI.</span><span class="sxs-lookup"><span data-stu-id="06370-148">The following Perl code sample describes how to display CIM object model identification information, and was taken from the sample directory at \\\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\sysmgmt\\wmi\\scripting.</span></span>


```Perl
use strict;
use Win32::OLE;

my ($Cimomid, $locator, $services);

eval { $Cimomid = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\default")->
 Get("__CIMOMIdentification=@"); };

unless ($@)
{
 print "\n", $Cimomid->Path_()->{displayname}, "\n";
 print $Cimomid->{versionusedtocreatedb}, "\n";
}
else
{ 
 print STDERR "\n", Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="06370-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06370-149">Requirements</span></span>



| <span data-ttu-id="06370-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="06370-150">Requirement</span></span> | <span data-ttu-id="06370-151">Valore</span><span class="sxs-lookup"><span data-stu-id="06370-151">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="06370-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06370-152">Minimum supported client</span></span><br/> | <span data-ttu-id="06370-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="06370-153">Windows Vista</span></span><br/>       |
| <span data-ttu-id="06370-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06370-154">Minimum supported server</span></span><br/> | <span data-ttu-id="06370-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="06370-155">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="06370-156">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="06370-156">Namespace</span></span><br/>                | <span data-ttu-id="06370-157">Radice</span><span class="sxs-lookup"><span data-stu-id="06370-157">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="06370-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="06370-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06370-159">**\_\_SystemClass**</span><span class="sxs-lookup"><span data-stu-id="06370-159">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="06370-160">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="06370-160">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

