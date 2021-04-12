---
description: Windows Update Agent (WUA) può essere utilizzato per analizzare i computer per gli aggiornamenti della sicurezza senza connettersi a Windows Update o a un server Windows Server Update Services (WSUS), che consente di analizzare gli aggiornamenti della sicurezza nei computer che non sono connessi a Internet. L'analisi offline per gli aggiornamenti richiede il download di un file firmato, Wsusscn2.cab, da Windows Update.
ms.assetid: 452b53af-0f7b-435e-bf12-dd9d84cbd564
title: Utilizzo di WUA per la ricerca di aggiornamenti offline
ms.topic: article
ms.date: 07/23/2020
ms.openlocfilehash: 242ff3655f4ab469d8d768a94f8dc8e529e0da74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342721"
---
# <a name="using-wua-to-scan-for-updates-offline"></a>Utilizzo di WUA per la ricerca di aggiornamenti offline

Windows Update Agent (WUA) può essere utilizzato per analizzare i computer per gli aggiornamenti della sicurezza senza connettersi a Windows Update o a un server Windows Server Update Services (WSUS), che consente di analizzare gli aggiornamenti della sicurezza nei computer che non sono connessi a Internet.

L'analisi offline per gli aggiornamenti richiede il download di un file firmato, Wsusscn2.cab, da Windows Update.

Il file di Wsusscn2.cab è un file CAB firmato da Microsoft. Questo file contiene informazioni sugli aggiornamenti relativi alla sicurezza pubblicati da Microsoft. I computer che non sono connessi a Internet possono essere analizzati per verificare se questi aggiornamenti correlati alla sicurezza sono presenti o richiesti. Il file di Wsusscn2.cab non contiene gli aggiornamenti della sicurezza, pertanto è necessario ottenere e installare gli aggiornamenti relativi alla sicurezza necessari in altri modi. Le nuove versioni del file di Wsusscn2.cab vengono rilasciate periodicamente quando gli aggiornamenti relativi alla sicurezza vengono rilasciati, rimossi o rivisti nel sito Windows Update. Il file di Wsusscn2.cab più recente è disponibile per il download nel percorso seguente: [download Wsusscn2.cab](http://download.windowsupdate.com/microsoftupdate/v6/wsusscan/wsusscn2.cab)

Dopo aver scaricato la Wsusscn2.cab più recente, il file può essere fornito al metodo [**AddScanPackageService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addscanpackageservice) e l'API WUA può essere usata per cercare gli aggiornamenti della sicurezza nel computer offline. WUA verifica che il Wsusscn2.cab sia firmato da un certificato Microsoft valido prima di eseguire un'analisi offline.

> [!NOTE]
> In conformità con l' [iniziativa di deprecazione SHA-1](https://aka.ms/sha1deprecation), il file di Wsusscn2.cab non è più firmato a doppio usando SHA-1 e la suite SHA-2 di algoritmi hash (in particolare sha-256). Questo file è ora firmato solo con SHA-256. Gli amministratori che verificano le firme digitali in questo file dovrebbero ora prevedere solo firme SHA-256 singole.

## <a name="example"></a>Esempio

Nell'esempio seguente viene usato il file di Wsusscn2.cab per eseguire la scansione di un computer e visualizzare gli aggiornamenti mancanti.

> [!IMPORTANT]
> Questo script ha lo scopo di illustrare l'uso delle API dell'agente Windows Update e fornisce un esempio di come gli sviluppatori possono usare queste API per risolvere i problemi. Questo script non è destinato al codice di produzione e lo script non è supportato da Microsoft (anche se sono supportate le API di Windows Update Agent sottostanti).

 


```VB
Set UpdateSession = CreateObject("Microsoft.Update.Session")
Set UpdateServiceManager = CreateObject("Microsoft.Update.ServiceManager")
Set UpdateService = UpdateServiceManager.AddScanPackageService("Offline Sync Service", "c:\wsusscn2.cab", 1)
Set UpdateSearcher = UpdateSession.CreateUpdateSearcher()

WScript.Echo "Searching for updates..." & vbCRLF

UpdateSearcher.ServerSelection = 3 ' ssOthers

UpdateSearcher.ServiceID = UpdateService.ServiceID

Set SearchResult = UpdateSearcher.Search("IsInstalled=0")

Set Updates = SearchResult.Updates

If searchResult.Updates.Count = 0 Then
    WScript.Echo "There are no applicable updates."
    WScript.Quit
End If

WScript.Echo "List of applicable items on the machine when using wssuscan.cab:" & vbCRLF

For I = 0 to searchResult.Updates.Count-1
    Set update = searchResult.Updates.Item(I)
    WScript.Echo I + 1 & "> " & update.Title
Next

WScript.Quit
```



 

 



