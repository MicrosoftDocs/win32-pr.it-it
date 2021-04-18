---
description: Il metodo EnableLog dell'oggetto Installer consente la registrazione del tipo di messaggio selezionato per tutte le sessioni di installazione successive nello spazio di processo corrente.
ms.assetid: eb384587-0870-4812-866c-b483c1dfa841
title: Installer. EnableLog, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.EnableLog
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 573b56dda0479f58595b0849f6443fd8a2e67e71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324645"
---
# <a name="installerenablelog-method"></a><span data-ttu-id="df751-103">Installer. EnableLog, metodo</span><span class="sxs-lookup"><span data-stu-id="df751-103">Installer.EnableLog method</span></span>

<span data-ttu-id="df751-104">Il metodo **EnableLog** dell'oggetto [**Installer**](installer-object.md) consente la registrazione del tipo di messaggio selezionato per tutte le sessioni di installazione successive nello spazio di processo corrente.</span><span class="sxs-lookup"><span data-stu-id="df751-104">The **EnableLog** method of the [**Installer**](installer-object.md) object enables logging of the selected message type for all subsequent installation sessions in the current process space.</span></span>

## <a name="syntax"></a><span data-ttu-id="df751-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="df751-105">Syntax</span></span>


```JScript
Installer.EnableLog(
  logMode,
  logFile
)
```



## <a name="parameters"></a><span data-ttu-id="df751-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="df751-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df751-107">*logMode*</span><span class="sxs-lookup"><span data-stu-id="df751-107">*logMode*</span></span> 
</dt> <dd>

<span data-ttu-id="df751-108">Stringa obbligatoria che contiene le lettere che rappresentano i tipi di messaggio da registrare.</span><span class="sxs-lookup"><span data-stu-id="df751-108">A required string that contains letters representing the message types to log.</span></span> <span data-ttu-id="df751-109">La stringa può essere una combinazione dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="df751-109">The string can be a combination of the following values.</span></span>



| <span data-ttu-id="df751-110">Valore</span><span class="sxs-lookup"><span data-stu-id="df751-110">Value</span></span> | <span data-ttu-id="df751-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df751-111">Description</span></span>                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df751-112">I</span><span class="sxs-lookup"><span data-stu-id="df751-112">I</span></span>     | <span data-ttu-id="df751-113">Messaggi di sola informazione.</span><span class="sxs-lookup"><span data-stu-id="df751-113">Information-only messages.</span></span>                                                                             |
| <span data-ttu-id="df751-114">w</span><span class="sxs-lookup"><span data-stu-id="df751-114">w</span></span>     | <span data-ttu-id="df751-115">Messaggi di avviso non irreversibili.</span><span class="sxs-lookup"><span data-stu-id="df751-115">Non-fatal warning messages.</span></span>                                                                            |
| <span data-ttu-id="df751-116">h</span><span class="sxs-lookup"><span data-stu-id="df751-116">e</span></span>     | <span data-ttu-id="df751-117">Messaggi di errore che potrebbero essere errori irreversibili.</span><span class="sxs-lookup"><span data-stu-id="df751-117">Error messages that may be fatal errors.</span></span>                                                               |
| <span data-ttu-id="df751-118">f</span><span class="sxs-lookup"><span data-stu-id="df751-118">f</span></span>     | <span data-ttu-id="df751-119">Elenco di file in uso che devono essere sostituiti.</span><span class="sxs-lookup"><span data-stu-id="df751-119">List of files in use that need to be replaced.</span></span>                                                         |
| <span data-ttu-id="df751-120">a</span><span class="sxs-lookup"><span data-stu-id="df751-120">a</span></span>     | <span data-ttu-id="df751-121">Inizio della notifica dell'azione.</span><span class="sxs-lookup"><span data-stu-id="df751-121">Start of action notification.</span></span>                                                                          |
| <span data-ttu-id="df751-122">r</span><span class="sxs-lookup"><span data-stu-id="df751-122">r</span></span>     | <span data-ttu-id="df751-123">Record di dati azione che contiene contenuto specifico per l'azione.</span><span class="sxs-lookup"><span data-stu-id="df751-123">Action data record containing content specific to action.</span></span>                                              |
| <span data-ttu-id="df751-124">u</span><span class="sxs-lookup"><span data-stu-id="df751-124">u</span></span>     | <span data-ttu-id="df751-125">Messaggi di richiesta dell'utente.</span><span class="sxs-lookup"><span data-stu-id="df751-125">User request messages.</span></span>                                                                                 |
| <span data-ttu-id="df751-126">c</span><span class="sxs-lookup"><span data-stu-id="df751-126">c</span></span>     | <span data-ttu-id="df751-127">Parametri di inizializzazione dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="df751-127">UI initialization parameters.</span></span>                                                                          |
| <span data-ttu-id="df751-128">m</span><span class="sxs-lookup"><span data-stu-id="df751-128">m</span></span>     | <span data-ttu-id="df751-129">Messaggio di memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="df751-129">Out-of-memory message.</span></span>                                                                                 |
| <span data-ttu-id="df751-130">v</span><span class="sxs-lookup"><span data-stu-id="df751-130">v</span></span>     | <span data-ttu-id="df751-131">Invia grandi quantità di informazioni al file di log non in genere utile agli utenti.</span><span class="sxs-lookup"><span data-stu-id="df751-131">Sends large amounts of information to log file not generally useful to users.</span></span> <span data-ttu-id="df751-132">Può essere utilizzato per il supporto.</span><span class="sxs-lookup"><span data-stu-id="df751-132">May be used for support.</span></span> |
| <span data-ttu-id="df751-133">p</span><span class="sxs-lookup"><span data-stu-id="df751-133">p</span></span>     | <span data-ttu-id="df751-134">Dump della tabella delle proprietà; "Property = Value" alla chiusura del motore</span><span class="sxs-lookup"><span data-stu-id="df751-134">Dump property table; "property = value" at engine termination</span></span>                                          |
| \+    | <span data-ttu-id="df751-135">Accoda a un file di log esistente.</span><span class="sxs-lookup"><span data-stu-id="df751-135">Append to existing log file.</span></span>                                                                           |
| <span data-ttu-id="df751-136">!</span><span class="sxs-lookup"><span data-stu-id="df751-136">!</span></span>     | <span data-ttu-id="df751-137">Scaricare ogni riga nel file di log.</span><span class="sxs-lookup"><span data-stu-id="df751-137">Flush each line to the log file.</span></span>                                                                       |
| <span data-ttu-id="df751-138">x</span><span class="sxs-lookup"><span data-stu-id="df751-138">x</span></span>     | <span data-ttu-id="df751-139">Informazioni di debug aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="df751-139">Extra debugging information.</span></span> <span data-ttu-id="df751-140">Questa opzione è disponibile solo con Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="df751-140">This option only available with Windows Server 2003.</span></span>                      |
| <span data-ttu-id="df751-141">o</span><span class="sxs-lookup"><span data-stu-id="df751-141">o</span></span>     | <span data-ttu-id="df751-142">Messaggi di spazio fuori disco.</span><span class="sxs-lookup"><span data-stu-id="df751-142">Out-of-disk-space messages.</span></span>                                                                            |



 

</dd> <dt>

<span data-ttu-id="df751-143">*logFile*</span><span class="sxs-lookup"><span data-stu-id="df751-143">*logFile*</span></span> 
</dt> <dd>

<span data-ttu-id="df751-144">Stringa obbligatoria contenente il percorso del file di log da creare.</span><span class="sxs-lookup"><span data-stu-id="df751-144">Required string containing the path to the log file to be created.</span></span> <span data-ttu-id="df751-145">Usare una stringa vuota ("") per disattivare la registrazione.</span><span class="sxs-lookup"><span data-stu-id="df751-145">Use an empty string ("") to turn off logging.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df751-146">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="df751-146">Return value</span></span>

<span data-ttu-id="df751-147">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="df751-147">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="df751-148">Commenti</span><span class="sxs-lookup"><span data-stu-id="df751-148">Remarks</span></span>

<span data-ttu-id="df751-149">Il percorso del file di log deve esistere già quando si usa questo metodo.</span><span class="sxs-lookup"><span data-stu-id="df751-149">The path to the logfile location must already exist when using this method.</span></span> <span data-ttu-id="df751-150">Il programma di installazione non crea la struttura di directory per il file di log.</span><span class="sxs-lookup"><span data-stu-id="df751-150">The Installer does not create the directory structure for the logfile.</span></span>

<span data-ttu-id="df751-151">Le opzioni di registrazione impostate utilizzando **EnableLog** sostituiscono le impostazioni dei criteri di registrazione Windows Installer esistenti.</span><span class="sxs-lookup"><span data-stu-id="df751-151">The logging options set using **EnableLog** override any existing Windows Installer logging policy settings.</span></span>

<span data-ttu-id="df751-152">Per impostazione predefinita, la registrazione sovrascrive un file di log esistente.</span><span class="sxs-lookup"><span data-stu-id="df751-152">Logging overwrites an existing log file by default.</span></span> <span data-ttu-id="df751-153">Per aggiungere un file di log esistente, è necessario utilizzare la lettera "+" nella modalità di registrazione.</span><span class="sxs-lookup"><span data-stu-id="df751-153">You must use the '+' letter in the logging mode to append to an existing log file.</span></span>

<span data-ttu-id="df751-154">L'opzione '!' non è consigliata perché può rallentare notevolmente l'installazione.</span><span class="sxs-lookup"><span data-stu-id="df751-154">The '!' option is not recommended because it can significantly slow installation.</span></span> <span data-ttu-id="df751-155">Questa opzione può essere utile quando si esegue il debug di un'installazione.</span><span class="sxs-lookup"><span data-stu-id="df751-155">This option may be useful when debugging an installation.</span></span>

<span data-ttu-id="df751-156">Lo script di esempio seguente attiva la registrazione dettagliata per un'installazione.</span><span class="sxs-lookup"><span data-stu-id="df751-156">The following sample script turns on verbose logging for an installation.</span></span> <span data-ttu-id="df751-157">Al termine dell'installazione, il file di log generato sarà in c: \\ temp \\ Install. log.</span><span class="sxs-lookup"><span data-stu-id="df751-157">At the end of the installation, the generated log file will be at c:\\temp\\install.log.</span></span>


```VB
    Dim Installer
    Set Installer = CreateObject("WindowsInstaller.Installer")
    Installer.EnableLog "voicewarmup", "c:\temp\install.log"
    Installer.InstallProduct "\\server\share\products\sample\sample.msi"
```



## <a name="requirements"></a><span data-ttu-id="df751-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df751-158">Requirements</span></span>



| <span data-ttu-id="df751-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="df751-159">Requirement</span></span> | <span data-ttu-id="df751-160">Valore</span><span class="sxs-lookup"><span data-stu-id="df751-160">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df751-161">Versione</span><span class="sxs-lookup"><span data-stu-id="df751-161">Version</span></span><br/> | <span data-ttu-id="df751-162">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="df751-162">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="df751-163">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="df751-163">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="df751-164">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="df751-164">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="df751-165">DLL</span><span class="sxs-lookup"><span data-stu-id="df751-165">DLL</span></span><br/>     | <dl> <span data-ttu-id="df751-166"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df751-166"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="df751-167">IID</span><span class="sxs-lookup"><span data-stu-id="df751-167">IID</span></span><br/>     | <span data-ttu-id="df751-168">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="df751-168">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="df751-169">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df751-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df751-170">Registrazione Windows Installer</span><span class="sxs-lookup"><span data-stu-id="df751-170">Windows Installer Logging</span></span>](windows-installer-logging.md)
</dt> </dl>

 

 




