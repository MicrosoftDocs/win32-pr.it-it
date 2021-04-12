---
description: Nell'esempio di scripting in questo argomento viene illustrato come utilizzare l'agente di Windows Update (WUA) per analizzare, scaricare e installare un aggiornamento specifico. L'aggiornamento può essere specificato in base al titolo.
ms.assetid: 4a5bb920-fc51-48a0-8f66-bb2fcc72589f
title: Ricerca, download e installazione di aggiornamenti specifici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aadd7903303356c3937f41e44aa7a47e71192409
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343806"
---
# <a name="searching-downloading-and-installing-specific-updates"></a><span data-ttu-id="b2f5c-104">Ricerca, download e installazione di aggiornamenti specifici</span><span class="sxs-lookup"><span data-stu-id="b2f5c-104">Searching, Downloading, and Installing Specific Updates</span></span>

<span data-ttu-id="b2f5c-105">Nell'esempio di scripting in questo argomento viene illustrato come utilizzare l'agente di Windows Update (WUA) per analizzare, scaricare e installare un aggiornamento specifico.</span><span class="sxs-lookup"><span data-stu-id="b2f5c-105">The scripting sample in this topic shows you how to use the Windows Update Agent (WUA) to scan, download, and install a specific update.</span></span> <span data-ttu-id="b2f5c-106">L'aggiornamento può essere specificato in base al titolo.</span><span class="sxs-lookup"><span data-stu-id="b2f5c-106">The update can be specified by its title.</span></span>

<span data-ttu-id="b2f5c-107">Nell'esempio viene eseguita la ricerca di un aggiornamento software specifico, viene scaricato l'aggiornamento, quindi viene installato l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="b2f5c-107">The sample searches for a specific software update, downloads the update, and then installs the update.</span></span> <span data-ttu-id="b2f5c-108">Un utente, ad esempio, può utilizzare questo metodo per determinare se un aggiornamento critico della sicurezza è installato in un computer.</span><span class="sxs-lookup"><span data-stu-id="b2f5c-108">For example, a user can use this method to determine if a critical security update is installed on a computer.</span></span> <span data-ttu-id="b2f5c-109">Se l'aggiornamento non è installato, l'utente può verificare che l'aggiornamento venga scaricato e installato.</span><span class="sxs-lookup"><span data-stu-id="b2f5c-109">If the update isn't installed, the user can ensure that the update is downloaded and installed.</span></span> <span data-ttu-id="b2f5c-110">L'utente può inoltre assicurarsi di ricevere una notifica sullo stato dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="b2f5c-110">The user can also ensure that they are notified about the status of the installation.</span></span>

<span data-ttu-id="b2f5c-111">L'aggiornamento di esempio è identificato dal titolo dell'aggiornamento nella [**proprietà title di IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_title).</span><span class="sxs-lookup"><span data-stu-id="b2f5c-111">The sample update is identified by the update title in [**Title Property of IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_title).</span></span> <span data-ttu-id="b2f5c-112">Il titolo dell'aggiornamento suggerito in questo esempio è "Update for Windows Rights Management Client 1,0".</span><span class="sxs-lookup"><span data-stu-id="b2f5c-112">The title of the update that is suggested in this sample is "Update for Windows Rights Management client 1.0."</span></span>

> [!Note]  
> <span data-ttu-id="b2f5c-113">Per informazioni su come cercare, scaricare e installare tutti gli aggiornamenti applicabili a un'applicazione specifica, vedere [ricerca, download e installazione degli aggiornamenti](searching--downloading--and-installing-updates.md).</span><span class="sxs-lookup"><span data-stu-id="b2f5c-113">For info about how to search, download, and install all the updates that apply to a specific application, see [Searching, Downloading, and Installing Updates](searching--downloading--and-installing-updates.md).</span></span>

 

<span data-ttu-id="b2f5c-114">Prima di provare a eseguire l'esempio, tenere presente quanto segue:</span><span class="sxs-lookup"><span data-stu-id="b2f5c-114">Before you attempt to run this sample, note the following:</span></span>

-   <span data-ttu-id="b2f5c-115">WUA deve essere installato nel computer.</span><span class="sxs-lookup"><span data-stu-id="b2f5c-115">WUA must be installed on the computer.</span></span> <span data-ttu-id="b2f5c-116">Per ulteriori informazioni su come determinare la versione di WUA installata, vedere [determinazione della versione corrente di WUA](determining-the-current-version-of-wua.md).</span><span class="sxs-lookup"><span data-stu-id="b2f5c-116">For more info about how to determine the version of WUA that is installed, see [Determining the Current Version of WUA](determining-the-current-version-of-wua.md).</span></span>
-   <span data-ttu-id="b2f5c-117">L'esempio non fornisce una propria interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="b2f5c-117">The sample doesn't provide its own user interface.</span></span> <span data-ttu-id="b2f5c-118">WUA chiede all'utente di riavviare il computer se è necessario riavviare un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="b2f5c-118">WUA prompts the user to restart the computer if an update requires a restart.</span></span>
-   <span data-ttu-id="b2f5c-119">L'esempio può scaricare gli aggiornamenti solo da WUA.</span><span class="sxs-lookup"><span data-stu-id="b2f5c-119">The sample can download updates only from WUA.</span></span> <span data-ttu-id="b2f5c-120">Non è possibile scaricare gli aggiornamenti da un server di servizi di aggiornamento software (SUS) 1,0.</span><span class="sxs-lookup"><span data-stu-id="b2f5c-120">It can't download updates from a Software Update Services (SUS) 1.0 server.</span></span>
-   <span data-ttu-id="b2f5c-121">Per eseguire questo esempio è necessario Windows script host (WSH).</span><span class="sxs-lookup"><span data-stu-id="b2f5c-121">Running this sample requires Windows Script Host (WSH).</span></span> <span data-ttu-id="b2f5c-122">Per ulteriori informazioni su WSH, vedere la sezione WSH della piattaforma Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="b2f5c-122">For more info about WSH, see the WSH section of the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="b2f5c-123">Se l'esempio viene copiato in un file denominato WUA \_SpecificUpdate.vbs, è possibile eseguirlo aprendo una finestra del prompt dei comandi e digitando il comando seguente: **cscript WUA \_SpecificUpdate.vbs**</span><span class="sxs-lookup"><span data-stu-id="b2f5c-123">If the sample is copied to a file named WUA\_SpecificUpdate.vbs, you can run it by opening a Command Prompt window and by typing this command: **cscript WUA\_SpecificUpdate.vbs**</span></span>  
    

## <a name="example"></a><span data-ttu-id="b2f5c-124">Esempio</span><span class="sxs-lookup"><span data-stu-id="b2f5c-124">Example</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b2f5c-125">Questo script ha lo scopo di illustrare l'uso delle API dell'agente Windows Update e fornisce un esempio di come gli sviluppatori possono usare queste API per risolvere i problemi.</span><span class="sxs-lookup"><span data-stu-id="b2f5c-125">This script is intended to demonstrate the use of the Windows Update Agent APIs, and provide an example of how developers can use these APIs to solve problems.</span></span> <span data-ttu-id="b2f5c-126">Questo script non è destinato al codice di produzione e lo script non è supportato da Microsoft (anche se sono supportate le API di Windows Update Agent sottostanti).</span><span class="sxs-lookup"><span data-stu-id="b2f5c-126">This script is not intended as production code, and the script itself is not supported by Microsoft (though the underlying Windows Update Agent APIs are supported).</span></span>

 


```VB
Set updateSession = CreateObject("Microsoft.Update.Session")
updateSession.ClientApplicationID = "MSDN Sample Script"

'Get update title to search for
WScript.Echo "Enter the title of the update: " & _
"(for example, Update for Windows Rights Management client 1.0)"
updateTitle = WScript.StdIn.Readline

WScript.Echo vbCRLF & "Searching for: " & updateTitle & "..."

Set updateSearcher = updateSession.CreateupdateSearcher()

'Search for all software updates, already installed and not installed
Set searchResult = _
updateSearcher.Search("Type='Software'")

Set updateToInstall = CreateObject("Microsoft.Update.UpdateColl")

updateIsApplicable = False

'Cycle through search results to look for the update title
For i = 0 To searchResult.Updates.Count-1
   Set update = searchResult.Updates.Item(i)
   If UCase(update.Title) = UCase(updateTitle) Then
   'Update in list of applicable updates 
   'Determine if it is already installed or not
      If update.IsInstalled = False Then
         WScript.Echo vbCRLF & _
         "Result: Update applicable, not installed."
         updateIsApplicable = True
         updateToInstall.Add(update)
      Else 
         'Update is installed so notify user and quit
         WScript.Echo vbCRLF & _
         "Result: Update applicable, already installed."
         updateIsApplicable = True
         WScript.Quit 
      End If
   End If 
Next

If updateIsApplicable = False Then
   WScript.Echo "Result: Update is not applicable to this machine."
   WScript.Quit
End If

WScript.Echo vbCRLF & "Would you like to install now? (Y/N)"
stdInput = WScript.StdIn.Readline
 
If (strInput = "N" or strInput = "n") Then 
   WScript.Quit
ElseIf  (stdInput = "Y" OR stdInput = "y") Then
   'Download update
   Set downloader = updateSession.CreateUpdateDownloader() 
   downloader.Updates = updateToInstall
   WScript.Echo vbCRLF & "Downloading..."
   Set downloadResult = downloader.Download()
   WScript.Echo "Download Result: " & downloadResult.ResultCode
  
   'Install Update
   Set installer = updateSession.CreateUpdateInstaller()
   WScript.Echo vbCRLF & "Installing..."
   installer.Updates = updateToInstall
   Set installationResult = installer.Install()
  
   'Output the result of the installation
   WScript.Echo "Installation Result: " & _
   installationResult.ResultCode
   WScript.Echo "Reboot Required: " & _
   installationResult.RebootRequired 
End If
```



 

 



