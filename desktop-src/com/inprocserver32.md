---
title: InprocServer32
description: Registra un server in-process a 32 bit e specifica il modello di threading dell'apartment in cui può essere eseguito il server.
ms.assetid: 4edbbd9d-7ea1-4476-aee7-eaf30e54db8d
keywords:
- InprocServer32 chiave del Registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9904aa636bbfb8dc0bc01cac85e041aedfcd34364bd62ac7b0e4e5a9f904750f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567821"
---
# <a name="inprocserver32"></a>InprocServer32

Registra un server in-process a 32 bit e specifica il modello di threading dell'apartment in cui può essere eseguito il server.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer32
         (Default) = path
         ThreadingModel = value
```

## <a name="remarks"></a>Commenti

**ThreadingModel** è un **valore \_ REG SZ** che specifica il modello di threading. I valori possibili sono indicati nella tabella seguente.



| Valore     | Descrizione                                |
|-----------|--------------------------------------------|
| Appartamento | Apartment a thread singolo                  |
| Entrambe      | Apartment a thread singolo o multithreading |
| Gratuito      | Apartment multithreading                    |
| Neutralità   | Apartment neutro                          |



 

È necessario usare lo stesso valore per ogni oggetto fornito dal server in-process.

Se **ThreadingModel** non è presente o non è impostato su un valore , il server viene caricato nel primo apartment inizializzato nel processo. Questo apartment viene talvolta definito apartment a thread singolo principale (STA). Se il primo STA in un processo viene inizializzato da COM, anziché da una chiamata esplicita a [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) o [**CoInitializeEx,**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)viene chiamato sta dell'host. Ad esempio, COM crea un'istanza STA dell'host se un server in-process da caricare richiede sta ma attualmente non è presente sta nel processo.

Quando possibile, il server in-process viene caricato nello stesso apartment del client che lo carica. Se il modello di threading dell'apartment client non è compatibile con il modello specificato, il server viene caricato come indicato nella tabella seguente.



| Modello di threading del server | Il server apartment viene eseguito in |
|---------------------------|----------------------------|
| <not specified>     | Sta principale                   |
| Entrambe                      | Stesso apartment del client   |
| Gratuito                      | Apartment multithreading    |
| Neutralità                   | Apartment neutro          |



 

Se il modello di threading del server è Apartment, l'apartment in cui viene caricato il server dipende dall'apartment in cui è in esecuzione il client, come indicato nella tabella seguente.



| Il client apartment viene eseguito in | Il server apartment viene eseguito in |
|----------------------------|----------------------------|
| Multithreading              | Host STA                   |
| Neutro (nel thread STA)    | Stesso apartment del client   |
| Neutro (nel thread MTA)    | Host STA                   |



 

COM può anche creare un apartment multithreading host (MTA). Se un client in un apartment a thread singolo richiede un server in-process il cui modello di threading è Gratuito quando non è presente alcun agente di trasferimento messaggi nel processo, COM crea un MTA host e vi carica il server.

Per un server in-process a 32 bit, è necessario registrare le chiavi [**InprocHandler32**](inprochandler32.md), [**InprocServer**](inprocserver.md), **InprocServer32** e [**Insertable.**](insertable.md) La **voce InprocServer** è necessaria solo per la compatibilità con le versioni precedenti. Se manca, la classe funziona ancora ma non può essere caricata nelle applicazioni a 16 bit.

Se un contenitore cerca un server in-process nel Registro di sistema, la versione a 16 bit ha la priorità con un contenitore a 16 bit e la versione a 32 bit ha la priorità con un contenitore a 32 bit.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**InprocServer**](inprocserver.md)
</dt> </dl>

 

 




