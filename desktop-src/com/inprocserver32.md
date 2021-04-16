---
title: InprocServer32
description: Registra un server in-process a 32 bit e specifica il modello di threading dell'Apartment in cui è possibile eseguire il server.
ms.assetid: 4edbbd9d-7ea1-4476-aee7-eaf30e54db8d
keywords:
- InprocServer32 chiave del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0daae9d495ad588e0dc710b63fe7d7ae9f48c11d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515961"
---
# <a name="inprocserver32"></a>InprocServer32

Registra un server in-process a 32 bit e specifica il modello di threading dell'Apartment in cui è possibile eseguire il server.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer32
         (Default) = path
         ThreadingModel = value
```

## <a name="remarks"></a>Commenti

**ThreadingModel** è un valore **reg \_ SZ** che specifica il modello di Threading. I valori possibili sono illustrati nella tabella seguente.



| Valore     | Descrizione                                |
|-----------|--------------------------------------------|
| Apartment | Apartment a thread singolo                  |
| Entrambi      | Apartment a thread singolo o a thread multipli |
| Gratuito      | Apartment a thread multipli                    |
| Neutralità   | Apartment neutro                          |



 

È necessario utilizzare lo stesso valore per ogni oggetto fornito dal server in-process.

Se **ThreadingModel** non è presente o non è impostato su un valore, il server viene caricato nel primo Apartment inizializzato nel processo. Questo Apartment viene talvolta definito Apartment a thread singolo principale (STA). Se il primo STA in un processo inizializzato da COM, anziché da una chiamata esplicita a [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) o [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), viene chiamato sta per essere host. Ad esempio, COM crea un'host STA se un server in-process da caricare richiede un STA ma attualmente non è presente alcun STA nel processo.

Laddove possibile, il server in-process viene caricato nello stesso apartment del client che lo carica. Se il modello di threading dell'Apartment client non è compatibile con il modello specificato, il server viene caricato come indicato nella tabella seguente.



| Modello di threading del server | Il server Apartment viene eseguito in |
|---------------------------|----------------------------|
| <not specified>     | STA principale                   |
| Entrambi                      | Stesso apartment del client   |
| Gratuito                      | Apartment a thread multipli    |
| Neutralità                   | Apartment neutro          |



 

Se il modello di threading del server è Apartment, l'Apartment in cui viene caricato il server dipende dall'Apartment in cui è in esecuzione il client, come indicato nella tabella seguente.



| Il client Apartment viene eseguito in | Il server Apartment viene eseguito in |
|----------------------------|----------------------------|
| Multithreading              | Host STA                   |
| Neutro (sul thread STA)    | Stesso apartment del client   |
| Neutro (su thread MTA)    | Host STA                   |



 

COM è inoltre in grado di creare un Apartment a thread multipli (MTA) host. Se un client in un Apartment a thread singolo richiede un server in-process il cui modello di threading è gratuito quando non è presente alcun MTA nel processo, COM crea un MTA host e lo carica nel server.

Per un server in-process a 32 bit, è necessario registrare le chiavi [**InprocHandler32**](inprochandler32.md), [**InprocServer**](inprocserver.md), **InprocServer32** e [**Insertable**](insertable.md) . La voce **InprocServer** è necessaria solo per la compatibilità con le versioni precedenti. Se non è presente, la classe funziona ancora, ma non può essere caricata in applicazioni a 16 bit.

Se un contenitore esegue una ricerca nel registro di sistema per un server in-process, la versione a 16 bit ha la priorità con un contenitore a 16 bit e la versione a 32 bit ha la priorità con un contenitore a 32 bit.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**InprocServer**](inprocserver.md)
</dt> </dl>

 

 




