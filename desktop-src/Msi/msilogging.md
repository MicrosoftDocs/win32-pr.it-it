---
description: La proprietà MsiLogging imposta la modalità di registrazione predefinita per il pacchetto di Windows Installer.
ms.assetid: f5ae389e-bc27-465d-886b-4f4f41d49118
title: Proprietà MsiLogging
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97e53df57723157f7184a904e512aac9035a9f53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332615"
---
# <a name="msilogging-property"></a><span data-ttu-id="48c32-103">Proprietà MsiLogging</span><span class="sxs-lookup"><span data-stu-id="48c32-103">MsiLogging property</span></span>

<span data-ttu-id="48c32-104">La proprietà **MsiLogging** imposta la modalità di registrazione predefinita per il pacchetto di Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="48c32-104">The **MsiLogging** property sets the default logging mode for the Windows Installer package.</span></span> <span data-ttu-id="48c32-105">Se questa proprietà facoltativa è presente nella [tabella delle proprietà](property-table.md), il programma di installazione genera un file di log denominato MSI \* . LOG.</span><span class="sxs-lookup"><span data-stu-id="48c32-105">If this optional property is present in the [Property table](property-table.md), the installer generates a log file named MSI\*.LOG.</span></span> <span data-ttu-id="48c32-106">Il percorso completo del file di log viene fornito dal valore della proprietà [**MsiLogFileLocation**](msilogfilelocation.md) .</span><span class="sxs-lookup"><span data-stu-id="48c32-106">The full path to the log file is given by the value of the [**MsiLogFileLocation**](msilogfilelocation.md) property.</span></span>

## <a name="value"></a><span data-ttu-id="48c32-107">Valore</span><span class="sxs-lookup"><span data-stu-id="48c32-107">Value</span></span>

<span data-ttu-id="48c32-108">Il valore di questa proprietà deve essere una stringa dei caratteri seguenti che specificano la modalità di registrazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="48c32-108">The value of this property should be a string of the following characters that specify the default logging mode.</span></span>



| <span data-ttu-id="48c32-109">Valore</span><span class="sxs-lookup"><span data-stu-id="48c32-109">Value</span></span>                                                                        | <span data-ttu-id="48c32-110">Significato</span><span class="sxs-lookup"><span data-stu-id="48c32-110">Meaning</span></span>                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="48c32-111"><dt>I</dt></span><span class="sxs-lookup"><span data-stu-id="48c32-111"><dt>I</dt></span></span> </dl> | <span data-ttu-id="48c32-112">Messaggi di stato.</span><span class="sxs-lookup"><span data-stu-id="48c32-112">Status messages.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="48c32-113"><dt>w</dt></span><span class="sxs-lookup"><span data-stu-id="48c32-113"><dt>w</dt></span></span> </dl> | <span data-ttu-id="48c32-114">Avvisi non irreversibili.</span><span class="sxs-lookup"><span data-stu-id="48c32-114">Nonfatal warnings.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="48c32-115"><dt>e</dt></span><span class="sxs-lookup"><span data-stu-id="48c32-115"><dt>e</dt></span></span> </dl> | <span data-ttu-id="48c32-116">Tutti i messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="48c32-116">All error messages.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="48c32-117"><dt>un</dt></span><span class="sxs-lookup"><span data-stu-id="48c32-117"><dt>a</dt></span></span> </dl> | <span data-ttu-id="48c32-118">Avvio delle azioni.</span><span class="sxs-lookup"><span data-stu-id="48c32-118">Start up of actions.</span></span><br/>                                                |
| <dl> <span data-ttu-id="48c32-119"><dt>r</dt></span><span class="sxs-lookup"><span data-stu-id="48c32-119"><dt>r</dt></span></span> </dl> | <span data-ttu-id="48c32-120">Record specifici dell'azione.</span><span class="sxs-lookup"><span data-stu-id="48c32-120">Action-specific records.</span></span><br/>                                            |
| <dl> <span data-ttu-id="48c32-121"><dt>u</dt></span><span class="sxs-lookup"><span data-stu-id="48c32-121"><dt>u</dt></span></span> </dl> | <span data-ttu-id="48c32-122">Richieste dell'utente.</span><span class="sxs-lookup"><span data-stu-id="48c32-122">User requests.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="48c32-123"><dt>c</dt></span><span class="sxs-lookup"><span data-stu-id="48c32-123"><dt>c</dt></span></span> </dl> | <span data-ttu-id="48c32-124">Parametri iniziali dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="48c32-124">Initial UI parameters.</span></span><br/>                                              |
| <dl> <span data-ttu-id="48c32-125"><dt>m</dt></span><span class="sxs-lookup"><span data-stu-id="48c32-125"><dt>m</dt></span></span> </dl> | <span data-ttu-id="48c32-126">Informazioni sulla memoria insufficiente o sull'uscita fatale.</span><span class="sxs-lookup"><span data-stu-id="48c32-126">Out-of-memory or fatal exit information.</span></span><br/>                            |
| <dl> <span data-ttu-id="48c32-127"><dt>o</dt></span><span class="sxs-lookup"><span data-stu-id="48c32-127"><dt>o</dt></span></span> </dl> | <span data-ttu-id="48c32-128">Messaggi di spazio fuori disco.</span><span class="sxs-lookup"><span data-stu-id="48c32-128">Out-of-disk-space messages.</span></span><br/>                                         |
| <dl> <span data-ttu-id="48c32-129"><dt>p</dt></span><span class="sxs-lookup"><span data-stu-id="48c32-129"><dt>p</dt></span></span> </dl> | <span data-ttu-id="48c32-130">Proprietà del terminale.</span><span class="sxs-lookup"><span data-stu-id="48c32-130">Terminal properties.</span></span><br/>                                                |
| <dl> <span data-ttu-id="48c32-131"><dt>v</dt></span><span class="sxs-lookup"><span data-stu-id="48c32-131"><dt>v</dt></span></span> </dl> | <span data-ttu-id="48c32-132">Output dettagliato.</span><span class="sxs-lookup"><span data-stu-id="48c32-132">Verbose output.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="48c32-133"><dt>x</dt></span><span class="sxs-lookup"><span data-stu-id="48c32-133"><dt>x</dt></span></span> </dl> | <span data-ttu-id="48c32-134">Informazioni di debug aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="48c32-134">Extra debugging information.</span></span> <span data-ttu-id="48c32-135">Disponibile solo in Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="48c32-135">Only available on Windows Server 2003.</span></span><br/> |
| <dl> <span data-ttu-id="48c32-136"><dt>!</dt></span><span class="sxs-lookup"><span data-stu-id="48c32-136"><dt>!</dt></span></span> </dl> | <span data-ttu-id="48c32-137">Scaricare ogni riga nel log.</span><span class="sxs-lookup"><span data-stu-id="48c32-137">Flush each line to the log.</span></span><br/>                                         |



 

## <a name="remarks"></a><span data-ttu-id="48c32-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="48c32-138">Remarks</span></span>

<span data-ttu-id="48c32-139">Questa proprietà è disponibile a partire da Windows Installer 4,0.</span><span class="sxs-lookup"><span data-stu-id="48c32-139">This property is available starting with Windows Installer 4.0.</span></span>

<span data-ttu-id="48c32-140">Non è possibile usare i valori "+" e " \* " dell'opzione/l nel valore della proprietà **MsiLogging** .</span><span class="sxs-lookup"><span data-stu-id="48c32-140">You cannot use the "+" and "\*" values of the /L option in the value of the **MsiLogging** property.</span></span>

<span data-ttu-id="48c32-141">La modalità di registrazione può essere impostata tramite criteri, un'opzione della riga di comando o a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="48c32-141">The logging mode can be set using policy, a command-line option, or programmatically.</span></span> <span data-ttu-id="48c32-142">Viene eseguito l'override della modalità di registrazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="48c32-142">This overrides the default logging mode.</span></span> <span data-ttu-id="48c32-143">Per ulteriori informazioni su tutti i metodi disponibili per l'impostazione della modalità di registrazione, vedere [registrazione normale](normal-logging.md) nella sezione [registrazione Windows Installer](windows-installer-logging.md) .</span><span class="sxs-lookup"><span data-stu-id="48c32-143">For more information about all the methods that are available for setting the logging mode, see [Normal Logging](normal-logging.md) in the [Windows Installer Logging](windows-installer-logging.md) section.</span></span>

<span data-ttu-id="48c32-144">Se la proprietà **MsiLogging** è presente nella [tabella delle proprietà](property-table.md), è possibile modificare la modalità di registrazione predefinita del pacchetto modificando il valore di questa proprietà utilizzando una [trasformazione del database](database-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="48c32-144">If the **MsiLogging** property is present in the [Property table](property-table.md), the default logging mode of the package can be modified by changing the value of this property using a [database transform](database-transforms.md).</span></span> <span data-ttu-id="48c32-145">Non è possibile modificare la modalità di registrazione predefinita utilizzando un [pacchetto di patch](patch-packages.md) , ovvero un file con estensione msp.</span><span class="sxs-lookup"><span data-stu-id="48c32-145">The default logging mode cannot be changed using a [Patch Package](patch-packages.md) (a .msp file.)</span></span>

<span data-ttu-id="48c32-146">Se la proprietà **MsiLogging** è stata impostata nella [tabella delle proprietà](property-table.md), è possibile specificare la modalità di registrazione predefinita per tutti gli utenti del computer impostando il criterio [DisableLoggingFromPackage](disableloggingfrompackage.md) e i criteri di [registrazione](logging.md) .</span><span class="sxs-lookup"><span data-stu-id="48c32-146">If the **MsiLogging** property has been set in the [Property table](property-table.md), the default logging mode for all users of the computer can be specified by setting both the [DisableLoggingFromPackage](disableloggingfrompackage.md) policy and [Logging](logging.md) policy.</span></span> <span data-ttu-id="48c32-147">L'impostazione del criterio DisableLoggingFromPackage e dei criteri di registrazione eseguirà l'override della proprietà **MsiLogging** per tutti i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="48c32-147">Setting both the DisableLoggingFromPackage policy and Logging policy will override the **MsiLogging** property for all packages.</span></span>

## <a name="requirements"></a><span data-ttu-id="48c32-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="48c32-148">Requirements</span></span>



| <span data-ttu-id="48c32-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="48c32-149">Requirement</span></span> | <span data-ttu-id="48c32-150">Valore</span><span class="sxs-lookup"><span data-stu-id="48c32-150">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48c32-151">Versione</span><span class="sxs-lookup"><span data-stu-id="48c32-151">Version</span></span><br/> | <span data-ttu-id="48c32-152">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="48c32-152">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="48c32-153">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="48c32-153">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="48c32-154">Windows Installer 4,5 in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="48c32-154">Windows Installer 4.5 on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="48c32-155">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="48c32-155">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="48c32-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="48c32-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48c32-157">Proprietà</span><span class="sxs-lookup"><span data-stu-id="48c32-157">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="48c32-158">Non supportato in Windows Installer 3,1 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="48c32-158">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




