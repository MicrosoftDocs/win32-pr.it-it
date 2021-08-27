---
description: L'esempio di scripting in questo argomento illustra come usare Windows Update Agent (WUA) per analizzare, scaricare e installare un aggiornamento specifico. L'aggiornamento può essere specificato dal titolo.
ms.assetid: 4a5bb920-fc51-48a0-8f66-bb2fcc72589f
title: Ricerca, download e installazione di aggiornamenti specifici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c2da9569ed6fe34b18264ee59e91965877d63e422ae20e25fc27fbc025e812
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071286"
---
# <a name="searching-downloading-and-installing-specific-updates"></a>Ricerca, download e installazione di aggiornamenti specifici

L'esempio di scripting in questo argomento illustra come usare Windows Update Agent (WUA) per analizzare, scaricare e installare un aggiornamento specifico. L'aggiornamento può essere specificato dal titolo.

L'esempio cerca un aggiornamento software specifico, scarica l'aggiornamento e quindi installa l'aggiornamento. Ad esempio, un utente può usare questo metodo per determinare se un aggiornamento della sicurezza critico è installato in un computer. Se l'aggiornamento non è installato, l'utente può assicurarsi che l'aggiornamento sia scaricato e installato. L'utente può anche assicurarsi di ricevere una notifica sullo stato dell'installazione.

L'aggiornamento di esempio è identificato dal titolo dell'aggiornamento nella [**proprietà Title di IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_title). Il titolo dell'aggiornamento suggerito in questo esempio è "Update for Windows Rights Management client 1.0".

> [!Note]  
> Per informazioni su come cercare, scaricare e installare tutti gli aggiornamenti applicabili a un'applicazione specifica, vedere [Ricerca, download](searching--downloading--and-installing-updates.md)e installazione degli aggiornamenti .

 

Prima di provare a eseguire questo esempio, tenere presente quanto segue:

-   WUA deve essere installato nel computer. Per altre informazioni su come determinare la versione di WUA installata, vedere [Determinare la versione corrente di WUA.](determining-the-current-version-of-wua.md)
-   L'esempio non fornisce la propria interfaccia utente. WUA richiede all'utente di riavviare il computer se un aggiornamento richiede un riavvio.
-   L'esempio può scaricare gli aggiornamenti solo da WUA. Non è possibile scaricare gli aggiornamenti da un server SuS (Software Update Services) 1.0.
-   L'esecuzione di questo esempio richiede Windows Script Host (WSH). Per altre informazioni su WSH, vedere la sezione WSH di Platform Software Development Kit (SDK). Se l'esempio viene copiato in un file denominato WUASpecificUpdate.vbs, è possibile eseguirlo aprendo una finestra del prompt dei comandi e digitando questo \_ comando: **cscript WUA \_SpecificUpdate.vbs**  
    

## <a name="example"></a>Esempio

> [!IMPORTANT]
> Questo script ha lo scopo di illustrare l'uso delle API dell'Windows Update Agent e di fornire un esempio di come gli sviluppatori possono usare queste API per risolvere i problemi. Questo script non è inteso come codice di produzione e lo script stesso non è supportato da Microsoft (anche se sono supportate le API Windows Update Agent sottostanti).

 


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



 

 



