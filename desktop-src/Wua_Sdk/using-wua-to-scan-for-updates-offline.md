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
# <a name="using-wua-to-scan-for-updates-offline"></a><span data-ttu-id="64270-104">Utilizzo di WUA per la ricerca di aggiornamenti offline</span><span class="sxs-lookup"><span data-stu-id="64270-104">Using WUA to Scan for Updates Offline</span></span>

<span data-ttu-id="64270-105">Windows Update Agent (WUA) può essere utilizzato per analizzare i computer per gli aggiornamenti della sicurezza senza connettersi a Windows Update o a un server Windows Server Update Services (WSUS), che consente di analizzare gli aggiornamenti della sicurezza nei computer che non sono connessi a Internet.</span><span class="sxs-lookup"><span data-stu-id="64270-105">Windows Update Agent (WUA) can be used to scan computers for security updates without connecting to Windows Update or to a Windows Server Update Services (WSUS) server, which enables computers that are not connected to the Internet to be scanned for security updates.</span></span>

<span data-ttu-id="64270-106">L'analisi offline per gli aggiornamenti richiede il download di un file firmato, Wsusscn2.cab, da Windows Update.</span><span class="sxs-lookup"><span data-stu-id="64270-106">Offline scanning for updates requires the download of a signed file, Wsusscn2.cab, from Windows Update.</span></span>

<span data-ttu-id="64270-107">Il file di Wsusscn2.cab è un file CAB firmato da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="64270-107">The Wsusscn2.cab file is a cabinet file that is signed by Microsoft.</span></span> <span data-ttu-id="64270-108">Questo file contiene informazioni sugli aggiornamenti relativi alla sicurezza pubblicati da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="64270-108">This file contains info about security-related updates that are published by Microsoft.</span></span> <span data-ttu-id="64270-109">I computer che non sono connessi a Internet possono essere analizzati per verificare se questi aggiornamenti correlati alla sicurezza sono presenti o richiesti.</span><span class="sxs-lookup"><span data-stu-id="64270-109">Computers that aren't connected to the Internet can be scanned to see whether these security-related updates are present or required.</span></span> <span data-ttu-id="64270-110">Il file di Wsusscn2.cab non contiene gli aggiornamenti della sicurezza, pertanto è necessario ottenere e installare gli aggiornamenti relativi alla sicurezza necessari in altri modi.</span><span class="sxs-lookup"><span data-stu-id="64270-110">The Wsusscn2.cab file doesn't contain the security updates themselves so you must obtain and install any needed security-related updates through other means.</span></span> <span data-ttu-id="64270-111">Le nuove versioni del file di Wsusscn2.cab vengono rilasciate periodicamente quando gli aggiornamenti relativi alla sicurezza vengono rilasciati, rimossi o rivisti nel sito Windows Update.</span><span class="sxs-lookup"><span data-stu-id="64270-111">New versions of the Wsusscn2.cab file are released periodically as security-related updates are released, removed, or revised on the Windows Update site.</span></span> <span data-ttu-id="64270-112">Il file di Wsusscn2.cab più recente è disponibile per il download nel percorso seguente: [download Wsusscn2.cab](http://download.windowsupdate.com/microsoftupdate/v6/wsusscan/wsusscn2.cab)</span><span class="sxs-lookup"><span data-stu-id="64270-112">The latest Wsusscn2.cab file is available for download at the following location: [Download Wsusscn2.cab](http://download.windowsupdate.com/microsoftupdate/v6/wsusscan/wsusscn2.cab)</span></span>

<span data-ttu-id="64270-113">Dopo aver scaricato la Wsusscn2.cab più recente, il file può essere fornito al metodo [**AddScanPackageService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addscanpackageservice) e l'API WUA può essere usata per cercare gli aggiornamenti della sicurezza nel computer offline.</span><span class="sxs-lookup"><span data-stu-id="64270-113">After you download the latest Wsusscn2.cab, the file can be provided to the [**AddScanPackageService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addscanpackageservice) method, and the WUA API can be used to search the offline computer for security updates.</span></span> <span data-ttu-id="64270-114">WUA verifica che il Wsusscn2.cab sia firmato da un certificato Microsoft valido prima di eseguire un'analisi offline.</span><span class="sxs-lookup"><span data-stu-id="64270-114">WUA validates that the Wsusscn2.cab is signed by a valid Microsoft certificate before running an offline scan.</span></span>

> [!NOTE]
> <span data-ttu-id="64270-115">In conformità con l' [iniziativa di deprecazione SHA-1](https://aka.ms/sha1deprecation), il file di Wsusscn2.cab non è più firmato a doppio usando SHA-1 e la suite SHA-2 di algoritmi hash (in particolare sha-256).</span><span class="sxs-lookup"><span data-stu-id="64270-115">In accordance with our [SHA-1 deprecation initiative](https://aka.ms/sha1deprecation), the Wsusscn2.cab file is no longer dual-signed using both SHA-1 and the SHA-2 suite of hash algorithms (specifically SHA-256).</span></span> <span data-ttu-id="64270-116">Questo file è ora firmato solo con SHA-256.</span><span class="sxs-lookup"><span data-stu-id="64270-116">This file is now signed using only SHA-256.</span></span> <span data-ttu-id="64270-117">Gli amministratori che verificano le firme digitali in questo file dovrebbero ora prevedere solo firme SHA-256 singole.</span><span class="sxs-lookup"><span data-stu-id="64270-117">Administrators who verify digital signatures on this file should now expect only single SHA-256 signatures.</span></span>

## <a name="example"></a><span data-ttu-id="64270-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="64270-118">Example</span></span>

<span data-ttu-id="64270-119">Nell'esempio seguente viene usato il file di Wsusscn2.cab per eseguire la scansione di un computer e visualizzare gli aggiornamenti mancanti.</span><span class="sxs-lookup"><span data-stu-id="64270-119">The following example uses the Wsusscn2.cab file to scan a computer and displays updates that are missing.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="64270-120">Questo script ha lo scopo di illustrare l'uso delle API dell'agente Windows Update e fornisce un esempio di come gli sviluppatori possono usare queste API per risolvere i problemi.</span><span class="sxs-lookup"><span data-stu-id="64270-120">This script is intended to demonstrate the use of the Windows Update Agent APIs, and provide an example of how developers can use these APIs to solve problems.</span></span> <span data-ttu-id="64270-121">Questo script non è destinato al codice di produzione e lo script non è supportato da Microsoft (anche se sono supportate le API di Windows Update Agent sottostanti).</span><span class="sxs-lookup"><span data-stu-id="64270-121">This script is not intended as production code, and the script itself is not supported by Microsoft (though the underlying Windows Update Agent APIs are supported).</span></span>

 


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



 

 



