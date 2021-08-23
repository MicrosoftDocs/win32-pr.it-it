---
description: Funzioni di output di debug
ms.assetid: dfe44c8c-43ec-461f-952f-b87256b82ee6
title: Funzioni di output di debug
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 252e1020ca99bd5b4f2f46d7f2169fa6835dea83a25d599dba142f370bb794f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537741"
---
# <a name="debug-output-functions"></a>Funzioni di output di debug

Le [DirectShow base forniscono](directshow-base-classes.md) diverse macro per la visualizzazione di informazioni di debug.



| Funzione                                               | Descrizione                                                                                          |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**DbgCheckModuleLevel**](dbgcheckmodulelevel.md)     | Controlla se la registrazione è abilitata per i tipi di messaggio e il livello specificati.                             |
| [**DbgDumpObjectRegister**](dbgdumpobjectregister.md) | Visualizza informazioni sugli oggetti attivi.                                                           |
| [**DbgInitialise**](dbginitialise.md)                 | Inizializza la libreria di debug.                                                                       |
| [**DbgLog**](dbglog.md)                               | Invia una stringa al percorso di output di debug, se la registrazione è abilitata per il tipo e il livello specificati. |
| [**DbgOutString**](dbgoutstring.md)                   | Invia una stringa al percorso di output di debug.                                                         |
| [**DbgSetModuleLevel**](dbgsetmodulelevel.md)         | Imposta il livello di registrazione per uno o più tipi di messaggio.                                                |
| [**DbgTerminate**](dbgterminate.md)                   | Pulisce la libreria di debug.                                                                         |
| [**DisplayType**](displaytype.md)                     | Invia informazioni su un tipo di supporto al percorso di output di debug.                                   |
| [**DumpGraph**](dumpgraph.md)                         | Invia informazioni su un grafico di filtro al percorso di output di debug.                                 |
| [**GuidNames**](guidnames.md)                         | Matrice globale contenente stringhe che rappresentano i GUID definiti in Uuids.h.                        |
| [**Nome**](name.md)                                   | Genera una stringa di solo debug.                                                                       |
| [**Nota**](note.md)                                   | Invia una stringa al percorso di output di debug.                                                         |
| [**Ricordare**](remind.md)                               | Genera un promemoria in fase di compilazione.                                                                |



 

**Chiavi del Registro di sistema**

La funzione di output di debug in DirectShow un set di chiavi del Registro di sistema. Il percorso di queste chiavi del Registro di sistema dipende dalla versione di Windows.

*Prima di Windows Vista*, le chiavi di debug si trovano nel percorso seguente:

**HKEY \_ Debug \_ DEL** \\ **SOFTWARE DEL COMPUTER** \\ **LOCALE**

In Windows Vista o versioni successive, si trovano nel percorso seguente:

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **DirectShow** \\ **Debug**

Per i filtri di terze parti, il percorso dipende dalla versione del DirectShow [di base](directshow-base-classes.md) usata per compilare il filtro. La versione inclusa in Windows SDK per Windows Vista usa il percorso più recente. Nelle versioni precedenti è stato usato il percorso precedente.

Nelle osservazioni seguenti, l'etichetta *<DebugRoot>* viene usata per indicare questi due percorsi. Sostituire il percorso corretto, a seconda della versione di Windows o della versione delle classi di base.

**Registrazione di debug**

DirectShow definisce diversi tipi di messaggio, illustrati nella tabella seguente.



| Valore                   | Descrizione                                             |
|-------------------------|---------------------------------------------------------|
| LOG \_ ERROR              | Notifica di errore.                                     |
| BLOCCO \_ DEL LOG            | Blocco e sblocco delle sezioni critiche.             |
| LOG \_ MEMORY             | Allocazione di memoria e creazione e distruzione di oggetti. |
| LOG \_ TIMING             | Misurazioni di temporizzazione e prestazioni.                    |
| LOG \_ TRACE              | Traccia generale delle chiamate.                                   |
| Da CUSTOM1 a CUSTOM5 | Disponibile per i messaggi di debug personalizzati                     |



 

Ogni funzione di DirectShow di registrazione di debug specifica un tipo di messaggio e un livello di log. Il messaggio di debug viene visualizzato solo quando il livello di debug corrente per quel tipo di messaggio è uguale o maggiore del livello specificato nella funzione di registrazione. In caso contrario, il messaggio viene ignorato.

Ad esempio, il codice seguente restituisce la stringa "This is a debug message" se il livello LOG \_ TRACE è 3 o superiore:

``` syntax
DbgLog((LOG_TRACE, 3, TEXT("This is a debug message")));
```

Ogni modulo può impostare il proprio livello di debug per ogni tipo di messaggio. Un *modulo è* una DLL o un eseguibile che può essere caricato usando la **funzione LoadLibrary.** I livelli di debug di un modulo vengono visualizzati nel Registro di sistema sotto la chiave seguente:

**HKEY \_ LOCAL \_ MACHINE**\\**<DebugRoot>**\\**<ModuleName>**\\**<MessageType>**

dove *<Message Type>* è il tipo di messaggio meno il valore iniziale di "LOG", ad esempio \_ **LOCKING** per i messaggi LOG \_ LOCKING. Quando viene caricato un modulo, la libreria di debug trova i livelli di registrazione del modulo nel Registro di sistema. Se le chiavi del Registro di sistema non esistono, vengono create dalla libreria di debug.

Un modulo può anche impostare i propri livelli in fase di esecuzione, usando la [**funzione DbgSetModuleLevel.**](dbgsetmodulelevel.md) Per inviare un messaggio all'output di debug, chiamare la macro [**DbgLog.**](dbglog.md) Nell'esempio seguente viene creato un messaggio di livello 3 di tipo LOG \_ TRACE:

È anche possibile specificare livelli di registrazione globali, con la chiave del Registro di sistema seguente:


```C++
\HKEY_LOCAL_MACHINE\<DebugRoot>\GLOBAL\<Message Type>
```



La libreria di debug usa il livello maggiore, il livello globale o il livello del modulo.

**Percorso di output del debug**

Il percorso di output di debug è determinato da un'altra chiave del Registro di sistema:

**HKEY \_ Local \_ MACHINE** \\ **<DebugRoot>** \\ **<Modile Name>** \\ **LogToFile**

Se il valore di questa chiave è `Console` , l'output passa alla finestra della console. Se il valore è `Deb` , , o una stringa `Debug` `Debugger` vuota, l'output viene visualizzato nella finestra del debugger. In caso contrario, l'output viene scritto in un file specificato dalla chiave del Registro di sistema.

Prima che un eseguibile usi DirectShow libreria di debug, deve chiamare la [**funzione DbgInitialise.**](dbginitialise.md) Successivamente, deve chiamare la [**funzione DbgTerminate.**](dbgterminate.md) Non è necessario che le DLL chiamino queste funzioni, perché il punto di ingresso della DLL (definito nella libreria di classi base) le chiama automaticamente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilità di debug](debugging-utilities.md)
</dt> </dl>

 

 



