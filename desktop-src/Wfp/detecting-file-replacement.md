---
description: Windows Protezione risorse impedisce la sostituzione di file di sistema, cartelle e chiavi del Registro di sistema essenziali installati come parte di Windows Vista o Windows Server 2008.
ms.assetid: 1cb67b4a-dc75-4bd7-b314-d695c10d5558
title: Rilevamento della sostituzione delle risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e452b9fba0a8002e13d7fc309ff3c8a12ec114a6a33b1bd7d8d253d710ffa77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053221"
---
# <a name="detecting-resource-replacement"></a>Rilevamento della sostituzione delle risorse

Windows Protezione risorse impedisce la sostituzione di file di sistema, cartelle e chiavi del Registro di sistema essenziali installati come parte di Windows Vista o Windows Server 2008.

WRP protegge file, cartelle e chiavi del Registro di sistema in Windows Vista o Windows Server 2008 rilevando e impedendo i tentativi di sostituire le risorse protette. Questa protezione si basa su un elenco Windows di controllo di accesso discrezionale (DACL) e gli elenchi di controllo di accesso (ACL) definiti per le risorse protette. L'autorizzazione per l'accesso completo per modificare le risorse protette da WRP è limitata a TrustedInstaller. Le risorse protette da WRP [](supported-file-replacement-mechanisms.md) possono essere modificate solo usando i meccanismi di sostituzione delle risorse supportati con il Windows del programma di installazione dei moduli. Le applicazioni che tentano di modificare una risorsa protetta da WRP non modificano mai la risorsa e possono ricevere un messaggio di errore che indica che l'accesso alla risorsa è stato negato.

Le applicazioni e i programmi di installazione possono usare le [**funzioni SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) e [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) per determinare se un file o una chiave del Registro di sistema è protetta.

**Windows Server 2003 e Windows XP: **

Windows Protezione file protegge i file di sistema rilevando i tentativi di sostituire i file di sistema protetti. Questa protezione viene attivata dopo che WFP riceve una notifica di modifica della directory per un file in una directory protetta. Quando il WFP riceve questa notifica, determina quale file è stato modificato. Se il file è protetto, WFP cerca la firma del file in un file di catalogo per determinare se il nuovo file è la versione corretta. Se la versione del file non è corretta, il sistema sostituisce il file con la versione corretta dal supporto di cache o di distribuzione, a seconda che il file si trovi nella cache. Wfp cerca il file corretto nell'ordine seguente:

1.  Cercare nella directory della cache.
2.  Cercare il percorso di installazione di rete, se il sistema è stato installato usando l'installazione di rete.
3.  Cercare in un Windows CD-ROM, se il sistema è stato installato da CD-ROM.

Se WFP non riesce a trovare automaticamente il file nei primi due percorsi, viene visualizzato il messaggio seguente:

![Messaggio wfp visualizzato quando il file non viene trovato nella directory della cache o nel percorso di installazione di rete](images/wfp-1.png)

Se il sistema è stato installato usando un CD-ROM, wfp visualizza il messaggio seguente:

![Messaggio wfp visualizzato per richiedere all'utente di inserire cd-rom di Windows](images/wfp-2.png)

Se un amministratore non è connesso, WFP non può visualizzare una di queste finestre di dialogo. Wfp visualizza la finestra di dialogo dopo l'accesso di un amministratore.

Wfp registra anche il tentativo di sostituzione dei file nel registro eventi di sistema. Se l'amministratore ha annullato il ripristino del file corretto, WFP registra l'annullamento.

## <a name="retrieving-the-list-of-protected-files"></a>Recupero dell'elenco di file protetti

L'esempio seguente illustra come applicazioni e programmi di installazione possono usare la [**funzione SfcGetNextProtectedFile**](/windows/desktop/api/Sfc/nf-sfc-sfcgetnextprotectedfile) per ottenere l'elenco completo dei file protetti.


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



 

 



