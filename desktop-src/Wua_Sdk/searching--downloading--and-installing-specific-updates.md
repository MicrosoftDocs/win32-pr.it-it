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
# <a name="searching-downloading-and-installing-specific-updates"></a>Ricerca, download e installazione di aggiornamenti specifici

Nell'esempio di scripting in questo argomento viene illustrato come utilizzare l'agente di Windows Update (WUA) per analizzare, scaricare e installare un aggiornamento specifico. L'aggiornamento può essere specificato in base al titolo.

Nell'esempio viene eseguita la ricerca di un aggiornamento software specifico, viene scaricato l'aggiornamento, quindi viene installato l'aggiornamento. Un utente, ad esempio, può utilizzare questo metodo per determinare se un aggiornamento critico della sicurezza è installato in un computer. Se l'aggiornamento non è installato, l'utente può verificare che l'aggiornamento venga scaricato e installato. L'utente può inoltre assicurarsi di ricevere una notifica sullo stato dell'installazione.

L'aggiornamento di esempio è identificato dal titolo dell'aggiornamento nella [**proprietà title di IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_title). Il titolo dell'aggiornamento suggerito in questo esempio è "Update for Windows Rights Management Client 1,0".

> [!Note]  
> Per informazioni su come cercare, scaricare e installare tutti gli aggiornamenti applicabili a un'applicazione specifica, vedere [ricerca, download e installazione degli aggiornamenti](searching--downloading--and-installing-updates.md).

 

Prima di provare a eseguire l'esempio, tenere presente quanto segue:

-   WUA deve essere installato nel computer. Per ulteriori informazioni su come determinare la versione di WUA installata, vedere [determinazione della versione corrente di WUA](determining-the-current-version-of-wua.md).
-   L'esempio non fornisce una propria interfaccia utente. WUA chiede all'utente di riavviare il computer se è necessario riavviare un aggiornamento.
-   L'esempio può scaricare gli aggiornamenti solo da WUA. Non è possibile scaricare gli aggiornamenti da un server di servizi di aggiornamento software (SUS) 1,0.
-   Per eseguire questo esempio è necessario Windows script host (WSH). Per ulteriori informazioni su WSH, vedere la sezione WSH della piattaforma Software Development Kit (SDK). Se l'esempio viene copiato in un file denominato WUA \_SpecificUpdate.vbs, è possibile eseguirlo aprendo una finestra del prompt dei comandi e digitando il comando seguente: **cscript WUA \_SpecificUpdate.vbs**  
    

## <a name="example"></a>Esempio

> [!IMPORTANT]
> Questo script ha lo scopo di illustrare l'uso delle API dell'agente Windows Update e fornisce un esempio di come gli sviluppatori possono usare queste API per risolvere i problemi. Questo script non è destinato al codice di produzione e lo script non è supportato da Microsoft (anche se sono supportate le API di Windows Update Agent sottostanti).

 


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



 

 



