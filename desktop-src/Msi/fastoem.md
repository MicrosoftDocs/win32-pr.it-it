---
description: La proprietà FASTOEM è progettata per consentire agli OEM di ridurre il tempo necessario per l'installazione di applicazioni Windows Installer per uno scenario specifico.
ms.assetid: 4c0af524-eb2e-4d64-bb25-3dae488d236d
title: Proprietà FASTOEM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78993a4affed62baf7e15a2b7787d83cabb9429e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332956"
---
# <a name="fastoem-property"></a><span data-ttu-id="61ff1-103">Proprietà FASTOEM</span><span class="sxs-lookup"><span data-stu-id="61ff1-103">FASTOEM property</span></span>

<span data-ttu-id="61ff1-104">La proprietà **FASTOEM** è progettata per consentire agli OEM di ridurre il tempo necessario per l'installazione di applicazioni Windows Installer per uno scenario specifico.</span><span class="sxs-lookup"><span data-stu-id="61ff1-104">The **FASTOEM** property is designed to enable OEMs to reduce the time it takes to install Windows Installer applications for a specific scenario.</span></span> <span data-ttu-id="61ff1-105">Non creare la proprietà **FASTOEM** nella tabella delle [Proprietà](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="61ff1-105">Do not author the **FASTOEM** property into the [Property Table](property-table.md).</span></span>

<span data-ttu-id="61ff1-106">La proprietà **FASTOEM** è applicabile solo se si verificano tutte le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="61ff1-106">The **FASTOEM** property is only applicable if all of these conditions are true:</span></span>

-   <span data-ttu-id="61ff1-107">L'applicazione viene installata nello stesso volume della cartella che contiene i file di origine.</span><span class="sxs-lookup"><span data-stu-id="61ff1-107">The application is being installed on the same volume as the folder containing the source files.</span></span>
-   <span data-ttu-id="61ff1-108">I file di origine vengono eliminati dopo l'installazione.</span><span class="sxs-lookup"><span data-stu-id="61ff1-108">The source files are deleted after the installation.</span></span>
-   <span data-ttu-id="61ff1-109">Durante l'installazione non viene visualizzata alcuna interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="61ff1-109">No user interface is displayed during the installation.</span></span> <span data-ttu-id="61ff1-110">Il [livello dell'interfaccia utente](user-interface-levels.md) è None.</span><span class="sxs-lookup"><span data-stu-id="61ff1-110">The [user interface level](user-interface-levels.md) is none.</span></span>
-   <span data-ttu-id="61ff1-111">L'installazione viene eseguita nel [contesto di installazione](installation-context.md)per computer.</span><span class="sxs-lookup"><span data-stu-id="61ff1-111">The installation is performed in the per-machine [installation context](installation-context.md).</span></span>
-   <span data-ttu-id="61ff1-112">Lo spazio disponibile nel computer è sufficiente per una corretta installazione.</span><span class="sxs-lookup"><span data-stu-id="61ff1-112">There is enough space on the computer for a successful installation.</span></span>
-   <span data-ttu-id="61ff1-113">Questa è la prima volta che si installa.</span><span class="sxs-lookup"><span data-stu-id="61ff1-113">This is first time installation.</span></span> <span data-ttu-id="61ff1-114">L'installazione non sta annunciando, reinstallando, rimuovendo o eseguendo un'installazione amministrativa.</span><span class="sxs-lookup"><span data-stu-id="61ff1-114">The installation is not advertising, reinstalling, removing, or doing an administrative installation.</span></span>
-   <span data-ttu-id="61ff1-115">Nessuna funzionalità installata per l'esecuzione dall'origine.</span><span class="sxs-lookup"><span data-stu-id="61ff1-115">No features are installed to run from source.</span></span>
-   <span data-ttu-id="61ff1-116">Il pacchetto di installazione non contiene [componenti isolati](isolated-components.md).</span><span class="sxs-lookup"><span data-stu-id="61ff1-116">The installation package contains no [isolated components](isolated-components.md).</span></span> <span data-ttu-id="61ff1-117">Poiché i componenti isolati richiedono che i file di origine rimangano nell'origine, non è attualmente possibile utilizzare la proprietà **FASTOEM** con componenti isolati.</span><span class="sxs-lookup"><span data-stu-id="61ff1-117">Because isolated components require source files to remain located at the source, the **FASTOEM** property cannot currently be used with isolated components.</span></span>

<span data-ttu-id="61ff1-118">Se tutte le condizioni precedenti sono vere, l'impostazione della proprietà **FASTOEM** consente Windows Installer per migliorare le prestazioni effettuando le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="61ff1-118">If all of the previous conditions are true, setting the **FASTOEM** property enables Windows Installer to improve performance by doing the following:</span></span>

-   <span data-ttu-id="61ff1-119">Spostare invece di copiare i file nello stesso volume.</span><span class="sxs-lookup"><span data-stu-id="61ff1-119">Move rather than copy files on the same volume.</span></span> <span data-ttu-id="61ff1-120">Ciò non garantisce che tutti i file vengano spostati anziché copiati.</span><span class="sxs-lookup"><span data-stu-id="61ff1-120">This does not guarantee that all files are moved rather than copied.</span></span> <span data-ttu-id="61ff1-121">Si noti che se il computer dispone di più dischi rigidi, è necessario inizializzare la proprietà [**ROOTDRIVE**](rootdrive.md) nella riga di comando nella stessa unità contenente l'origine dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="61ff1-121">Note that if the computer has multiple hard drives, you must initialize the [**ROOTDRIVE**](rootdrive.md) property on the command line to the same drive containing the installation source.</span></span>
-   <span data-ttu-id="61ff1-122">Omettere questa origine dall'elenco di origine dell'applicazione in modo che le installazioni successive di reinstallazione o manutenzione siano predefinite per le origini CD-ROM specificate nella [tabella media](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="61ff1-122">Omit this source from the application's source list so that subsequent reinstallation or maintenance installations default to the CD-ROM sources specified in the [Media Table](media-table.md).</span></span>
-   <span data-ttu-id="61ff1-123">Semplifica il [costo del file](file-costing.md).</span><span class="sxs-lookup"><span data-stu-id="61ff1-123">Streamline [file costing](file-costing.md).</span></span>
-   <span data-ttu-id="61ff1-124">Non visualizzare i messaggi di stato inviati dal Windows Installer al client.</span><span class="sxs-lookup"><span data-stu-id="61ff1-124">Suppress progress messages sent from Windows Installer to the client.</span></span>

## <a name="remarks"></a><span data-ttu-id="61ff1-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="61ff1-125">Remarks</span></span>

<span data-ttu-id="61ff1-126">Poiché non vengono inviati messaggi di stato quando viene impostato **FASTOEM** , è consigliabile che gli autori scrivano manualmente un valore di 1800 per il timeout nella chiave</span><span class="sxs-lookup"><span data-stu-id="61ff1-126">Because no progress messages are sent when **FASTOEM** is set, it is recommended that authors manually write a value of 1800 for Timeout into the key</span></span>

<span data-ttu-id="61ff1-127">**HKLM** \\ **Software** \\ di **Criteri** \\ di **Microsoft** \\ **Windows** \\ **Programma di installazione** \\ **Timeout**</span><span class="sxs-lookup"><span data-stu-id="61ff1-127">**HKLM**\\**SoftWare**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**\\**Timeout**</span></span>

<span data-ttu-id="61ff1-128">Timeout è un tipo **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="61ff1-128">Timeout is a **REG\_DWORD** type.</span></span>

<span data-ttu-id="61ff1-129">Per visualizzare le dimensioni dell'applicazione in Installazione applicazioni nel pannello di controllo di Windows 2000, è necessario scrivere manualmente il valore di EstimatedSize nella chiave</span><span class="sxs-lookup"><span data-stu-id="61ff1-129">To display the size of the application in Add or Remove Programs in the Windows 2000 Control Panel, you must manually write the value of EstimatedSize into the key</span></span>

<span data-ttu-id="61ff1-130">**HKLM** \\ **Software** \\ di **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Disinstalla** \\ **<  Codice > prodotto**</span><span class="sxs-lookup"><span data-stu-id="61ff1-130">**HKLM**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Uninstall**\\**<*Product Code*>**</span></span>

<span data-ttu-id="61ff1-131">Si tratta di un tipo **reg \_ DWORD** ed è uguale alla dimensione dell'applicazione in Kbyte.</span><span class="sxs-lookup"><span data-stu-id="61ff1-131">This is a **REG\_DWORD** type and equals to the size of the application in Kbytes.</span></span> <span data-ttu-id="61ff1-132">Il programma di installazione non scrive automaticamente questo valore.</span><span class="sxs-lookup"><span data-stu-id="61ff1-132">The installer does not automatically write this value.</span></span>

<span data-ttu-id="61ff1-133">Usare la riga di comando di esempio seguente se il CD-ROM spedito agli utenti finali archivia il pacchetto di installazione dell'applicazione nella directory principale del CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="61ff1-133">Use the following example command line if the CD-ROM shipped to end users stores the application's installation package at the root of the CD-ROM.</span></span> <span data-ttu-id="61ff1-134">Si noti che l'etichetta del volume nella [tabella media](media-table.md) del file con estensione msi deve corrispondere all'etichetta del volume del CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="61ff1-134">Note that the volume label in the [Media Table](media-table.md) of the .msi file must match the volume label of the CD-ROM.</span></span>

<span data-ttu-id="61ff1-135">**Msiexec/I C: \\ TempImage \\package.msi/qn/le logfile.txt ALLUSERS = 1 FASTOEM = 1 DisableRollback = 1 ROOTDRIVE = C:\\**</span><span class="sxs-lookup"><span data-stu-id="61ff1-135">**Msiexec /I C:\\TempImage\\package.msi /qn /le logfile.txt ALLUSERS=1 FASTOEM=1 DISABLEROLLBACK=1 ROOTDRIVE=C:\\**</span></span>

<span data-ttu-id="61ff1-136">Usare la riga di comando di esempio seguente se il pacchetto di installazione non si trova nella directory principale del CD-ROM spedito agli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="61ff1-136">Use the following example command line if the installation package is not located at the root of the CD-ROM shipped to end users.</span></span> <span data-ttu-id="61ff1-137">È necessario impostare la proprietà [**MEDIAPACKAGEPATH**](mediapackagepath.md) in questo caso sul percorso del pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="61ff1-137">You must set the [**MEDIAPACKAGEPATH**](mediapackagepath.md) property in this case to the path to the installation package.</span></span> <span data-ttu-id="61ff1-138">L'etichetta del volume nella [tabella media](media-table.md) del file con estensione msi deve corrispondere all'etichetta del volume del CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="61ff1-138">The volume label in the [Media Table](media-table.md) of the .msi file must match the volume label of the CD-ROM.</span></span> <span data-ttu-id="61ff1-139">In questo caso, seguire questo esempio.</span><span class="sxs-lookup"><span data-stu-id="61ff1-139">In this case follow this example.</span></span>

<span data-ttu-id="61ff1-140">**Msiexec/I C: \\ TempImage \\package.msi/qn/le logfile.txt ALLUSERS = 1 FASTOEM = 1 DisableRollback = 1 MEDIAPACKAGEPATH = c: \\ TempImage \\package.msi ROOTDRIVE = c:\\**</span><span class="sxs-lookup"><span data-stu-id="61ff1-140">**Msiexec /I C:\\TempImage\\package.msi /qn /le logfile.txt ALLUSERS=1 FASTOEM=1 DISABLEROLLBACK=1 MEDIAPACKAGEPATH=C:\\TempImage\\package.msi ROOTDRIVE=C:\\**</span></span>

## <a name="requirements"></a><span data-ttu-id="61ff1-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="61ff1-141">Requirements</span></span>



| <span data-ttu-id="61ff1-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="61ff1-142">Requirement</span></span> | <span data-ttu-id="61ff1-143">Valore</span><span class="sxs-lookup"><span data-stu-id="61ff1-143">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61ff1-144">Versione</span><span class="sxs-lookup"><span data-stu-id="61ff1-144">Version</span></span><br/> | <span data-ttu-id="61ff1-145">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="61ff1-145">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="61ff1-146">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="61ff1-146">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="61ff1-147">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="61ff1-147">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="61ff1-148">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="61ff1-148">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="61ff1-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="61ff1-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61ff1-150">Proprietà</span><span class="sxs-lookup"><span data-stu-id="61ff1-150">Properties</span></span>](properties.md)
</dt> </dl>

 

 




