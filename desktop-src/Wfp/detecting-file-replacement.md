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
# <a name="detecting-resource-replacement"></a>Rilevamento della sostituzione delle risorse

Protezione risorse di Windows (WRP) impedisce la sostituzione di file di sistema, cartelle e chiavi del registro di sistema essenziali installati come parte di Windows Vista o Windows Server 2008.

WRP protegge i file, le cartelle e le chiavi del registro di sistema in Windows Vista o Windows Server 2008 individuando e impedendo i tentativi di sostituzione delle risorse protette. Questa protezione si basa su un elenco di controllo di accesso discrezionale (DACL) e sugli elenchi di controllo di accesso (ACL) di Windows definiti per le risorse protette. L'autorizzazione per l'accesso completo per modificare le risorse protette con WRP è limitata a TrustedInstaller. Le risorse protette da WRP possono essere modificate solo usando i [meccanismi di sostituzione delle risorse supportati](supported-file-replacement-mechanisms.md) con il servizio moduli di installazione di Windows. Le applicazioni che tentano di modificare una risorsa protetta da WRP non modificano mai la risorsa e possono ricevere un messaggio di errore che indica che l'accesso alla risorsa è stato negato.

Le applicazioni e i programmi di installazione possono utilizzare le funzioni [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) e [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) per determinare se un file o una chiave del registro di sistema è protetta.

* * Windows Server 2003 e Windows XP: * *

Protezione file Windows consente di proteggere i file di sistema rilevando i tentativi di sostituzione dei file di sistema protetti. Questa protezione viene attivata dopo che PAM riceve una notifica di modifica della directory per un file in una directory protetta. Quando PAM riceve questa notifica, determina quale file è stato modificato. Se il file è protetto, PAM cerca la firma del file in un file di catalogo per determinare se il nuovo file è la versione corretta. Se la versione del file non è corretta, il sistema sostituisce il file con la versione corretta dalla cache o dal supporto di distribuzione, a seconda che il file si trovi nella cache. PAM cerca il file corretto nell'ordine seguente:

1.  Eseguire una ricerca nella directory della cache.
2.  Cercare il percorso di installazione della rete, se il sistema è stato installato con l'installazione di rete.
3.  Eseguire una ricerca in un CD-ROM di Windows, se il sistema è stato installato da CD-ROM.

Se WFP non riesce a trovare automaticamente il file nelle prime due posizioni, viene visualizzato il messaggio seguente:

![messaggio WFP visualizzato quando il file non è stato trovato nella directory della cache o nel percorso di installazione di rete](images/wfp-1.png)

Se il sistema è stato installato usando un CD-ROM, WFP Visualizza il messaggio seguente:

![messaggio WFP visualizzato per richiedere all'utente di inserire CD-ROM di Windows](images/wfp-2.png)

Se un amministratore non è connesso, non è possibile visualizzare nessuna di queste finestre di dialogo. Pam Visualizza la finestra di dialogo dopo che un amministratore ha eseguito l'accesso.

Pam registra inoltre il tentativo di sostituzione del file nel registro eventi di sistema. Se l'amministratore ha annullato il ripristino del file corretto, WFP registra l'annullamento.

## <a name="retrieving-the-list-of-protected-files"></a>Recupero dell'elenco di file protetti

Nell'esempio seguente viene illustrato come le applicazioni e i programmi di installazione possono utilizzare la funzione [**SfcGetNextProtectedFile**](/windows/desktop/api/Sfc/nf-sfc-sfcgetnextprotectedfile) per ottenere l'elenco completo dei file protetti.


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



 

 



