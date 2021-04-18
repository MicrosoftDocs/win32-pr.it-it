---
description: Funzioni di output di debug
ms.assetid: dfe44c8c-43ec-461f-952f-b87256b82ee6
title: Funzioni di output di debug
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87470b44717bb76c1a029bd885bb9149a4636b5d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304318"
---
# <a name="debug-output-functions"></a>Funzioni di output di debug

Le [classi base di DirectShow](directshow-base-classes.md) forniscono diverse macro per la visualizzazione delle informazioni di debug.



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
| [**GuidNames**](guidnames.md)                         | Matrice globale che contiene le stringhe che rappresentano i GUID definiti in UUIDs. h.                        |
| [**NOME**](name.md)                                   | Genera una stringa di solo debug.                                                                       |
| [**Si noti**](note.md)                                   | Invia una stringa al percorso di output di debug.                                                         |
| [**RICORDARE**](remind.md)                               | Genera un promemoria in fase di compilazione.                                                                |



 

**Chiavi del registro di sistema**

La funzione di output di debug in DirectShow usa un set di chiavi del registro di sistema. Il percorso di queste chiavi del registro di sistema dipende dalla versione di Windows.

*Prima di Windows Vista*, le chiavi di debug si trovano nel percorso seguente:

**HKEY \_ Debug \_ del software del computer locale** \\  \\ 

In Windows Vista o versioni successive si trovano nel percorso seguente:

**HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **DirectShow** \\ **debug**

Per i filtri di terze parti, la posizione dipende dalla versione delle [classi di base di DirectShow](directshow-base-classes.md) utilizzata per compilare il filtro. La versione inclusa nel Windows SDK per Windows Vista usa il percorso più recente. Le versioni precedenti usavano il percorso precedente.

Nelle osservazioni che seguono, l'etichetta *<DebugRoot>* viene usata per indicare questi due percorsi. Sostituire il percorso corretto, a seconda della versione di Windows o della versione delle classi di base.

**Registrazione debug**

DirectShow definisce diversi tipi di messaggi, illustrati nella tabella seguente.



| Valore                   | Descrizione                                             |
|-------------------------|---------------------------------------------------------|
| errore di registrazione \_              | Notifica di errore.                                     |
| blocco del LOG \_            | Blocco e sblocco di sezioni critiche.             |
| \_memoria log             | Allocazione di memoria e creazione e distruzione di oggetti. |
| \_temporizzazione log             | Misurazione delle prestazioni e delle tempistiche.                    |
| traccia del LOG \_              | Traccia generale delle chiamate.                                   |
| Da PERSONALIZZATA1 a CUSTOM5 | Disponibile per i messaggi di debug personalizzati                     |



 

Ogni funzione di registrazione del debug DirectShow specifica un tipo di messaggio e un livello di registrazione. Il messaggio di debug viene visualizzato solo quando il livello di debug corrente per quel tipo di messaggio è uguale o maggiore del livello specificato nella funzione di registrazione. In caso contrario, il messaggio viene ignorato.

Il codice seguente, ad esempio, restituisce la stringa "questo è un messaggio di debug" Se il livello di traccia del LOG \_ è 3 o superiore:

``` syntax
DbgLog((LOG_TRACE, 3, TEXT("This is a debug message")));
```

Ogni modulo può impostare il proprio livello di debug per ogni tipo di messaggio. Un *modulo* è un file eseguibile o dll che è possibile caricare utilizzando la funzione **LoadLibrary** . I livelli di debug di un modulo vengono visualizzati nel registro di sistema nella chiave seguente:

**\_computer locale \_ HKEY**\\**<DebugRoot>**\\**<ModuleName>**\\**<MessageType>**

dove *<Message Type>* è il tipo di messaggio meno il "log \_ " iniziale, ad esempio il **blocco** per \_ i messaggi di blocco del log. Quando viene caricato un modulo, la libreria di debug trova i livelli di registrazione del modulo nel registro di sistema. Se le chiavi del registro di sistema non esistono, vengono create dalla libreria di debug.

Un modulo può inoltre impostare i propri livelli in fase di esecuzione tramite la funzione [**DbgSetModuleLevel**](dbgsetmodulelevel.md) . Per inviare un messaggio all'output di debug, chiamare la macro [**DbgLog**](dbglog.md) . Nell'esempio seguente viene creato un messaggio di livello 3 di tipo \_ traccia log:

È anche possibile specificare i livelli di registrazione globali, con la chiave del registro di sistema seguente:


```C++
\HKEY_LOCAL_MACHINE\<DebugRoot>\GLOBAL\<Message Type>
```



La libreria di debug usa qualsiasi livello maggiore, il livello globale o il livello del modulo.

**Percorso di output di debug**

Il percorso di output di debug è determinato da un'altra chiave del registro di sistema:

**HKEY \_ LogToFile \_ computer locale** \\ **<DebugRoot>** \\ **<Modile Name>** \\ 

Se il valore di questa chiave è `Console` , l'output passa alla finestra della console. Se il valore è `Deb` , `Debug` , `Debugger` o una stringa vuota, l'output passa alla finestra del debugger. In caso contrario, l'output viene scritto in un file specificato dalla chiave del registro di sistema.

Prima che un eseguibile usi la libreria di debug DirectShow, deve chiamare la funzione [**DbgInitialise**](dbginitialise.md) . Successivamente, deve chiamare la funzione [**DbgTerminate**](dbgterminate.md) . Le dll non devono chiamare queste funzioni, perché il punto di ingresso della DLL (definito nella libreria di classi base) li chiama automaticamente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilità di debug](debugging-utilities.md)
</dt> </dl>

 

 



