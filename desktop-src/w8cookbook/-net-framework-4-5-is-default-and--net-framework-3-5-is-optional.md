---
title: Impostazioni predefinite .NET Framework
description: .NET Framework 4,5 è il valore predefinito e .NET Framework 3,5 è facoltativo
ms.assetid: 19B53C82-812A-49AC-87C6-C08E7C199208
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab1f91acc8739b2c660bfb1ba1392ea192511d1c
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/10/2020
ms.locfileid: "106300636"
---
# <a name="net-framework-45-is-default-and-net-framework-35-is-optional"></a><span data-ttu-id="4e950-103">.NET Framework 4,5 è il valore predefinito e .NET Framework 3,5 è facoltativo</span><span class="sxs-lookup"><span data-stu-id="4e950-103">.NET Framework 4.5 is default and .NET Framework 3.5 is optional</span></span>

## <a name="platforms"></a><span data-ttu-id="4e950-104">Piattaforme</span><span class="sxs-lookup"><span data-stu-id="4e950-104">Platforms</span></span>

<span data-ttu-id="4e950-105">**Client**   di   Windows 8</span><span class="sxs-lookup"><span data-stu-id="4e950-105">**Clients**   Windows 8</span></span>  
<span data-ttu-id="4e950-106">**Server**   di   Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4e950-106">**Servers**   Windows Server 2012</span></span>  

## <a name="description"></a><span data-ttu-id="4e950-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e950-107">Description</span></span>

<span data-ttu-id="4e950-108">.NET Framework 4,5 è abilitato per impostazione predefinita in Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4e950-108">.NET Framework 4.5 is enabled by default in Windows 8.</span></span> <span data-ttu-id="4e950-109">Windows 8 non include .NET 3,5 per impostazione predefinita, ma i file per .NET 3,5 sono disponibili nel supporto di installazione di Windows 8 come funzionalità facoltativa.</span><span class="sxs-lookup"><span data-stu-id="4e950-109">Windows 8 does not include .NET 3.5 by default, but the files for .NET 3.5 are available on the Windows 8 installation media as an optional feature.</span></span>

<span data-ttu-id="4e950-110">Se l'utente sta eseguendo l'aggiornamento da Windows 7 a Windows 8, .NET Framework 3,5 è completamente abilitato per assicurarsi che tutte le app nel computer continuino a funzionare correttamente.</span><span class="sxs-lookup"><span data-stu-id="4e950-110">If the user is upgrading from Windows 7 to Windows 8, .NET Framework 3.5 is fully enabled to ensure that any apps on the computer continue to work correctly.</span></span>

## <a name="manifestation"></a><span data-ttu-id="4e950-111">Manifestazione</span><span class="sxs-lookup"><span data-stu-id="4e950-111">Manifestation</span></span>

<span data-ttu-id="4e950-112">Se l'utente esegue un'installazione pulita di Windows 8, quindi installa app che richiedono .NET Framework 3,5 (o 2,0), attiverà una richiesta per i file .NET 3,5 necessari.</span><span class="sxs-lookup"><span data-stu-id="4e950-112">If the user performs a clean installation of Windows 8, and then installs apps that require .NET Framework 3.5 (or 2.0), they will trigger a request for the necessary .NET 3.5 files.</span></span> <span data-ttu-id="4e950-113">In genere i file mancanti verranno scaricati da Windows Update (dopo aver chiesto all'utente l'autorizzazione), ma se non è possibile accedere a Windows Update, l'abilitazione di .NET Framework 3,5 avrà esito negativo a meno che non sia stata specificata un'origine alternativa per i file mancanti.</span><span class="sxs-lookup"><span data-stu-id="4e950-113">Normally the missing files will be downloaded from Windows Update (after asking the user for permission), but if access to Windows Update is not possible, enabling .NET Framework 3.5 will fail unless an alternate source for the missing files has been specified.</span></span>

## <a name="mitigation"></a><span data-ttu-id="4e950-114">Strategia di riduzione del rischio</span><span class="sxs-lookup"><span data-stu-id="4e950-114">Mitigation</span></span>

<span data-ttu-id="4e950-115">Per abilitare .NET Framework 3,5 solo nei computer di test con installazioni pulite di Windows 8:</span><span class="sxs-lookup"><span data-stu-id="4e950-115">To enable .NET Framework 3.5 on only test machines with clean installs of Windows 8:</span></span>

1.  <span data-ttu-id="4e950-116">Copiare \\ \\ le origini SxS \\ dall'immagine ISO di compilazione del sistema operativo montata in dotnet35 o in una cartella simile.</span><span class="sxs-lookup"><span data-stu-id="4e950-116">Copy \\sources\\sxs\\ from the mounted operating system build ISO image to dotnet35 or similar folder.</span></span> <span data-ttu-id="4e950-117">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="4e950-117">For example:</span></span>
    ```
    xcopy e:\sources\sxs\*.* c:\dotnet35 /s
    ```



2.  <span data-ttu-id="4e950-118">Eseguire questa riga di comando con privilegi di amministratore:</span><span class="sxs-lookup"><span data-stu-id="4e950-118">Execute this command line using admin privileges:</span></span>
    ```
    Dism.exe /online /enable-feature /featurename:NetFX3 /All /Source:c:\dotnet35 /LimitAccess

    ```



> [!Note]  
> <span data-ttu-id="4e950-119">La \\ cartella SxS di origine non deve essere utilizzata come meccanismo di ridistribuzione poiché non si tratta di un meccanismo supportato.</span><span class="sxs-lookup"><span data-stu-id="4e950-119">The sources\\SxS folder must not be used as a redistribution mechanism since this is not a supported mechanism.</span></span>



## <a name="solution"></a><span data-ttu-id="4e950-120">Soluzione</span><span class="sxs-lookup"><span data-stu-id="4e950-120">Solution</span></span>

<span data-ttu-id="4e950-121">**Per i consumer:**</span><span class="sxs-lookup"><span data-stu-id="4e950-121">**For consumers:**</span></span>

<span data-ttu-id="4e950-122">Windows 8 include un meccanismo che abilita automaticamente .NET Framework 3,5 quando si tenta di installare il pacchetto ridistribuibile o quando un programma di installazione dell'applicazione che richiede .NET 3,5 richiama il ridistribuibile.</span><span class="sxs-lookup"><span data-stu-id="4e950-122">Windows 8 includes a mechanism that automatically enables .NET Framework 3.5 when attempting to install the redistributable package or when an application installer that needs .NET 3.5 invokes the redistributable.</span></span>

<span data-ttu-id="4e950-123">**Per gli sviluppatori di app e gli amministratori IT:**</span><span class="sxs-lookup"><span data-stu-id="4e950-123">**For App developers (and IT Administrators):**</span></span>

<span data-ttu-id="4e950-124">Gli amministratori IT possono configurare le app .NET 3,5 per l'esecuzione in .NET 3,5 o .NET 4,5 (a seconda degli elementi già installati).</span><span class="sxs-lookup"><span data-stu-id="4e950-124">IT administrators can configure .NET 3.5 apps to run on either .NET 3.5 or .NET 4.5 (depending on what's already installed).</span></span> <span data-ttu-id="4e950-125">Per eseguire un'app gestita in 3,5 o 4,5, è sufficiente aggiungere una sezione nel file di configurazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4e950-125">In order to run a managed app on either 3.5 or 4.5, just add a section in the application configuration file.</span></span> <span data-ttu-id="4e950-126">In questo modo si garantisce che se è installato .NET 3,5, l'app verrà eseguita in .NET 3,5; in caso contrario, l'app viene eseguita in .NET 4,5.</span><span class="sxs-lookup"><span data-stu-id="4e950-126">This will ensure that if .NET 3.5 is installed, the app will run on .NET 3.5; otherwise the app will run on .NET 4.5.</span></span> <span data-ttu-id="4e950-127">Di seguito è riportato un esempio della sezione aggiuntiva nel file di configurazione:</span><span class="sxs-lookup"><span data-stu-id="4e950-127">An example of the additional section in the configuration file is provided below:</span></span>


```
<configuration>
   <startup>
      <supportedRuntime version="v2.0.50727"/>
      <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.5"/>
   </startup>
</configuration>
```



<span data-ttu-id="4e950-128">**Per gli OEM aziendali:**</span><span class="sxs-lookup"><span data-stu-id="4e950-128">**For enterprise OEMs:**</span></span>

<span data-ttu-id="4e950-129">Per abilitare .NET Framework 3,5 per le compilazioni PAEE e per le applicazioni che non hanno accesso ai Windows Update:</span><span class="sxs-lookup"><span data-stu-id="4e950-129">To enable .NET Framework 3.5 for EEAP builds and for applications that do not have access to Windows Update:</span></span>

1.  <span data-ttu-id="4e950-130">Copiare \\ \\ le origini SxS \\ dall'immagine ISO di compilazione del sistema operativo montata in dotnet35 o in una cartella simile.</span><span class="sxs-lookup"><span data-stu-id="4e950-130">Copy \\sources\\sxs\\ from the mounted OS build ISO image to the dotnet35 or similar folder.</span></span> <span data-ttu-id="4e950-131">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="4e950-131">For example:</span></span>
    ```
    xcopy e:\sources\sxs\*.* c:\dotnet35 /s
    ```



2.  <span data-ttu-id="4e950-132">Impostare il chiave:</span><span class="sxs-lookup"><span data-stu-id="4e950-132">Set the regkey:</span></span>
    ```
    [HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Servicing]
     LocalSourcePath = c:\dotnet35
    ```



<span data-ttu-id="4e950-133">**Per le aziende:**</span><span class="sxs-lookup"><span data-stu-id="4e950-133">**For enterprises:**</span></span>

<span data-ttu-id="4e950-134">Per i computer configurati per l'utilizzo di WSUS per la manutenzione, è possibile impostare una voce del registro di sistema per consentire al computer di utilizzare Windows Update per l'abilitazione di .NET 3,5 anziché WSUS (la manutenzione verrà comunque eseguita da WSUS, se si esegue questa operazione).</span><span class="sxs-lookup"><span data-stu-id="4e950-134">For machines that are configured to use WSUS for servicing, you can set a registry entry to allow the machine to use Windows Update for enabling .NET 3.5 instead of WSUS (servicing will still be done from WSUS if you do this).</span></span>

-   <span data-ttu-id="4e950-135">Impostare il chiave:</span><span class="sxs-lookup"><span data-stu-id="4e950-135">Set the regkey:</span></span>
    ```
    [HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Servicing]  RepairContentServerSource =DWORD(2)
    ```



<span data-ttu-id="4e950-136">Questa voce del registro di sistema può essere impostata anche tramite Criteri di gruppo (criterio computer locale-> configurazione computer-> sistema Modelli amministrativi->.</span><span class="sxs-lookup"><span data-stu-id="4e950-136">This registry entry can also be set via Group Policy (Local Computer Policy -> Computer Configuration -> Administrative Templates -> System.</span></span> <span data-ttu-id="4e950-137">Selezionare l'impostazione specificare le impostazioni per l'installazione e il ripristino dei componenti facoltativi.</span><span class="sxs-lookup"><span data-stu-id="4e950-137">Select the setting  Specify settings for optional component installation and component repair .</span></span>

<span data-ttu-id="4e950-138">Se si seleziona Contact Windows Update direttamente per scaricare il contenuto di ripristino anziché Windows Server Update Services (WSUS), qualsiasi tentativo di aggiungere funzionalità di Windows (ad esempio, .NET Framework 3,5) o di ripristinare funzionalità attiverà i download di file da Windows Update.</span><span class="sxs-lookup"><span data-stu-id="4e950-138">If you select  Contact Windows Update directly to download repair content instead of Windows Server Update Services (WSUS) , any attempts to add Windows features (for example, .NET Framework 3.5) or repair features will trigger file downloads from Windows Update.</span></span> <span data-ttu-id="4e950-139">I computer di destinazione richiedono l'accesso a Internet e a WU per questa opzione.</span><span class="sxs-lookup"><span data-stu-id="4e950-139">Target computers require Internet and WU access for this option.</span></span> <span data-ttu-id="4e950-140">Le normali operazioni di manutenzione continuano a usare WSUS se è stato configurato come origine.</span><span class="sxs-lookup"><span data-stu-id="4e950-140">Normal servicing operations continue to use WSUS if it has been configured as a source.</span></span>

<span data-ttu-id="4e950-141">**Nota sull'impostazione del percorso di origine locale tramite le voci del registro di sistema**</span><span class="sxs-lookup"><span data-stu-id="4e950-141">**A note regarding setting local source location via registry entries**</span></span>

<span data-ttu-id="4e950-142">Gli amministratori IT possono impostare i percorsi di origine locali per i file .NET 3,5 tramite una voce del registro di sistema, in modo che gli utenti possano utilizzare la finestra di dialogo Aggiungi/Rimuovi funzionalità Windows per abilitare le funzionalità con payload mancante senza dover specificare un percorso di origine.</span><span class="sxs-lookup"><span data-stu-id="4e950-142">IT administrators can set local source location(s) for .NET 3.5 files via a registry entry, so that users can use the Add/Remove Windows Features dialog to enable features with missing payload without having to specify a source location.</span></span> <span data-ttu-id="4e950-143">Il valore della voce del registro di sistema può essere controllato tramite criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="4e950-143">The value of the registry entry can be controlled via group policy.</span></span>

<span data-ttu-id="4e950-144">Questa voce del registro di sistema è supportata:</span><span class="sxs-lookup"><span data-stu-id="4e950-144">This registry entry is supported:</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4e950-145">Voce</span><span class="sxs-lookup"><span data-stu-id="4e950-145">Entry</span></span></th>
<th><span data-ttu-id="4e950-146">Tipo</span><span class="sxs-lookup"><span data-stu-id="4e950-146">Type</span></span></th>
<th><span data-ttu-id="4e950-147">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e950-147">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4e950-148">Percorso di origine locale</span><span class="sxs-lookup"><span data-stu-id="4e950-148">Local Source Path</span></span></td>
<td><span data-ttu-id="4e950-149">REG_EXPAND_SZ</span><span class="sxs-lookup"><span data-stu-id="4e950-149">REG_EXPAND_SZ</span></span></td>
<td><span data-ttu-id="4e950-150">Percorsi di origine locali da utilizzare per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="4e950-150">Local source path(s) to be used by default.</span></span> <span data-ttu-id="4e950-151">È possibile specificare più percorsi; devono essere separate da.</span><span class="sxs-lookup"><span data-stu-id="4e950-151">Multiple paths can be specified; they should be separated by  ; .</span></span> <span data-ttu-id="4e950-152">Le località verranno ricercate nell'ordine in cui sono specificate.</span><span class="sxs-lookup"><span data-stu-id="4e950-152">Locations will be searched in the order they are specified.</span></span> <br/> <span data-ttu-id="4e950-153">I percorsi di origine locali specificati nella riga di comando DISM hanno la precedenza su quelli specificati in questa voce del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="4e950-153">Local source location(s) that are specified on the DISM command line, take precedence over locations specified in this registry entry.</span></span> <span data-ttu-id="4e950-154">I percorsi delle cartelle possono essere specificati in questa voce del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="4e950-154">Folder locations can be specified in this registry entry.</span></span> <br/> <span data-ttu-id="4e950-155">È possibile utilizzare WIMs, ma il percorso deve essere nel file WIM. non è necessario montarlo, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="4e950-155">WIMs can be used, but the path must be to the WIM file; there is no need to mount it, for example:</span></span> <br/> <dl> <span data-ttu-id="4e950-156">Wim: \\ machine\share\file.wim: 1</span><span class="sxs-lookup"><span data-stu-id="4e950-156">wim:\\machine\share\file.wim:1</span></span><br />
</dl> <span data-ttu-id="4e950-157">Si noti il 1 alla fine.</span><span class="sxs-lookup"><span data-stu-id="4e950-157">Notice the  1  at the end.</span></span> <span data-ttu-id="4e950-158">È necessario specificare l'indice numerico dell'immagine che si desidera utilizzare nel file WIM.</span><span class="sxs-lookup"><span data-stu-id="4e950-158">You must specify the numerical index of the image you want to use in the WIM file.</span></span> <br/> <span data-ttu-id="4e950-159">Per un file WIM montato, il percorso di origine deve fare riferimento alla directory di Windows dell'immagine montata, anziché al punto di montaggio, ad esempio:/Source: <mount_point> \Windows anziché/Source: <mount_point> .</span><span class="sxs-lookup"><span data-stu-id="4e950-159">For a mounted WIM, the source path needs to refer to the windows directory of the mounted image, rather than to the mount point (for example: /source:<mount_point>\windows rather than /source:<mount_point>).</span></span> <br/></td>
</tr>
</tbody>
</table>





## <a name="resources"></a><span data-ttu-id="4e950-160">Risorse</span><span class="sxs-lookup"><span data-stu-id="4e950-160">Resources</span></span>

<dl>

[<span data-ttu-id="4e950-161">Implementazione dei criteri basati sul Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="4e950-161">Implementing Registry-based Policy</span></span>](/previous-versions/windows/desktop/Policy/implementing-registry-based-policy)  
</dl>