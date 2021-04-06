---
description: Protezione risorse di Windows (WRP) impedisce la sostituzione di file di sistema, cartelle e chiavi del registro di sistema essenziali installati come parte di Windows Vista o Windows Server 2008.
ms.assetid: 1cb67b4a-dc75-4bd7-b314-d695c10d5558
title: Rilevamento della sostituzione delle risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62dc1855b98ca5834ef9e13e2f48bf7cca492e94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759011"
---
# <a name="detecting-resource-replacement"></a><span data-ttu-id="901c5-103">Rilevamento della sostituzione delle risorse</span><span class="sxs-lookup"><span data-stu-id="901c5-103">Detecting Resource Replacement</span></span>

<span data-ttu-id="901c5-104">Protezione risorse di Windows (WRP) impedisce la sostituzione di file di sistema, cartelle e chiavi del registro di sistema essenziali installati come parte di Windows Vista o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="901c5-104">Windows Resource Protection (WRP) prevents the replacement of essential system files, folders, and registry keys that are installed as part of Windows Vista or Windows Server 2008.</span></span>

<span data-ttu-id="901c5-105">WRP protegge i file, le cartelle e le chiavi del registro di sistema in Windows Vista o Windows Server 2008 individuando e impedendo i tentativi di sostituzione delle risorse protette.</span><span class="sxs-lookup"><span data-stu-id="901c5-105">WRP protects files, folders, and registry keys on Windows Vista or Windows Server 2008 by detecting and preventing attempts to replace protected resources.</span></span> <span data-ttu-id="901c5-106">Questa protezione si basa su un elenco di controllo di accesso discrezionale (DACL) e sugli elenchi di controllo di accesso (ACL) di Windows definiti per le risorse protette.</span><span class="sxs-lookup"><span data-stu-id="901c5-106">This protection is based on a Windows discretionary access control list (DACL) and access control lists (ACL) defined for protected resources.</span></span> <span data-ttu-id="901c5-107">L'autorizzazione per l'accesso completo per modificare le risorse protette con WRP è limitata a TrustedInstaller.</span><span class="sxs-lookup"><span data-stu-id="901c5-107">Permission for full access to modify WRP-protected resources is restricted to TrustedInstaller.</span></span> <span data-ttu-id="901c5-108">Le risorse protette da WRP possono essere modificate solo usando i [meccanismi di sostituzione delle risorse supportati](supported-file-replacement-mechanisms.md) con il servizio moduli di installazione di Windows.</span><span class="sxs-lookup"><span data-stu-id="901c5-108">WRP-protected resources can only be changed using the [Supported Resource Replacement Mechanisms](supported-file-replacement-mechanisms.md) with the Windows Modules Installer service.</span></span> <span data-ttu-id="901c5-109">Le applicazioni che tentano di modificare una risorsa protetta da WRP non modificano mai la risorsa e possono ricevere un messaggio di errore che indica che l'accesso alla risorsa è stato negato.</span><span class="sxs-lookup"><span data-stu-id="901c5-109">Applications attempting to modify a WRP-protected resource never change the resource and may receive an error message that states that access to the resource was denied.</span></span>

<span data-ttu-id="901c5-110">Le applicazioni e i programmi di installazione possono utilizzare le funzioni [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) e [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) per determinare se un file o una chiave del registro di sistema è protetta.</span><span class="sxs-lookup"><span data-stu-id="901c5-110">Applications and installers can use the [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) and [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) functions to determine whether a file or registry key is protected.</span></span>

<span data-ttu-id="901c5-111">\* \* Windows Server 2003 e Windows XP: \* \*</span><span class="sxs-lookup"><span data-stu-id="901c5-111">\*\*Windows Server 2003 and Windows XP:  \*\*</span></span>

<span data-ttu-id="901c5-112">Protezione file Windows consente di proteggere i file di sistema rilevando i tentativi di sostituzione dei file di sistema protetti.</span><span class="sxs-lookup"><span data-stu-id="901c5-112">Windows File Protection (WFP) protects system files by detecting attempts to replace protected system files.</span></span> <span data-ttu-id="901c5-113">Questa protezione viene attivata dopo che PAM riceve una notifica di modifica della directory per un file in una directory protetta.</span><span class="sxs-lookup"><span data-stu-id="901c5-113">This protection is triggered after WFP receives a directory change notification for a file in a protected directory.</span></span> <span data-ttu-id="901c5-114">Quando PAM riceve questa notifica, determina quale file è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="901c5-114">When WFP receives this notification, it determines which file has changed.</span></span> <span data-ttu-id="901c5-115">Se il file è protetto, PAM cerca la firma del file in un file di catalogo per determinare se il nuovo file è la versione corretta.</span><span class="sxs-lookup"><span data-stu-id="901c5-115">If the file is protected, WFP looks up the file signature in a catalog file to determine if the new file is the correct version.</span></span> <span data-ttu-id="901c5-116">Se la versione del file non è corretta, il sistema sostituisce il file con la versione corretta dalla cache o dal supporto di distribuzione, a seconda che il file si trovi nella cache.</span><span class="sxs-lookup"><span data-stu-id="901c5-116">If the file version is not correct, the system replaces the file with the correct version from either the cache or distribution media, depending on whether the file is located in the cache.</span></span> <span data-ttu-id="901c5-117">PAM cerca il file corretto nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="901c5-117">WFP searches for the correct file in the following order:</span></span>

1.  <span data-ttu-id="901c5-118">Eseguire una ricerca nella directory della cache.</span><span class="sxs-lookup"><span data-stu-id="901c5-118">Search the cache directory.</span></span>
2.  <span data-ttu-id="901c5-119">Cercare il percorso di installazione della rete, se il sistema è stato installato con l'installazione di rete.</span><span class="sxs-lookup"><span data-stu-id="901c5-119">Search the network install path, if the system was installed using network install.</span></span>
3.  <span data-ttu-id="901c5-120">Eseguire una ricerca in un CD-ROM di Windows, se il sistema è stato installato da CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="901c5-120">Search on a Windows CD-ROM, if the system was installed from CD-ROM.</span></span>

<span data-ttu-id="901c5-121">Se WFP non riesce a trovare automaticamente il file nelle prime due posizioni, viene visualizzato il messaggio seguente:</span><span class="sxs-lookup"><span data-stu-id="901c5-121">If WFP cannot automatically find the file in the first two locations, it displays the following message:</span></span>

![messaggio WFP visualizzato quando il file non è stato trovato nella directory della cache o nel percorso di installazione di rete](images/wfp-1.png)

<span data-ttu-id="901c5-123">Se il sistema è stato installato usando un CD-ROM, WFP Visualizza il messaggio seguente:</span><span class="sxs-lookup"><span data-stu-id="901c5-123">If the system was installed using a CD-ROM, WFP displays the following message:</span></span>

![messaggio WFP visualizzato per richiedere all'utente di inserire CD-ROM di Windows](images/wfp-2.png)

<span data-ttu-id="901c5-125">Se un amministratore non è connesso, non è possibile visualizzare nessuna di queste finestre di dialogo.</span><span class="sxs-lookup"><span data-stu-id="901c5-125">If an administrator is not logged on, WFP cannot display either of these dialog boxes.</span></span> <span data-ttu-id="901c5-126">Pam Visualizza la finestra di dialogo dopo che un amministratore ha eseguito l'accesso.</span><span class="sxs-lookup"><span data-stu-id="901c5-126">WFP will display the dialog box after an administrator logs on.</span></span>

<span data-ttu-id="901c5-127">Pam registra inoltre il tentativo di sostituzione del file nel registro eventi di sistema.</span><span class="sxs-lookup"><span data-stu-id="901c5-127">WFP also logs the file replacement attempt in the system event log.</span></span> <span data-ttu-id="901c5-128">Se l'amministratore ha annullato il ripristino del file corretto, WFP registra l'annullamento.</span><span class="sxs-lookup"><span data-stu-id="901c5-128">If the administrator canceled restoration of the correct file, WFP logs the cancellation.</span></span>

## <a name="retrieving-the-list-of-protected-files"></a><span data-ttu-id="901c5-129">Recupero dell'elenco di file protetti</span><span class="sxs-lookup"><span data-stu-id="901c5-129">Retrieving the List of Protected Files</span></span>

<span data-ttu-id="901c5-130">Nell'esempio seguente viene illustrato come le applicazioni e i programmi di installazione possono utilizzare la funzione [**SfcGetNextProtectedFile**](/windows/desktop/api/Sfc/nf-sfc-sfcgetnextprotectedfile) per ottenere l'elenco completo dei file protetti.</span><span class="sxs-lookup"><span data-stu-id="901c5-130">The following example shows how applications and installers can use the [**SfcGetNextProtectedFile**](/windows/desktop/api/Sfc/nf-sfc-sfcgetnextprotectedfile) function to get the complete list of protected files.</span></span>


```C++
#include <windows.h>
#include <sfc.h>
#include <stdio.h>

#pragma comment(lib, "sfc")

void wmain (int argc, WCHAR ** argv)
{  UNREFERENCED_PARAMETER(argc);    
   PROTECTED_FILE_DATA pfd = {0};
   BOOL fResult;

   wprintf (L"List of protected files:\n\n", argv[1]);

   while (FALSE != (fResult = SfcGetNextProtectedFile (NULL, &pfd)))
   {
      wprintf (L"   %lu   %s\n", pfd.FileNumber, pfd.FileName);
   }

   if (GetLastError() == ERROR_NO_MORE_FILES)
   {
      wprintf (L"\nAll %lu protected files listed\n", pfd.FileNumber);
   }
   else
   {
      wprintf (L"\nerror %lu: SfcGetNextProtectedFile() failed unexpectedly\n", GetLastError());
   }

}
```



 

 



