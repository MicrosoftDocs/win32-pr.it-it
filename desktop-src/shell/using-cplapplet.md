---
description: Prima di Windows Vista, è stato creato un elemento del pannello di controllo creando un file dll e definendolo con estensione CPL.
ms.assetid: 258dae28-c054-4392-b0e9-99493f23c814
title: Uso di CPLApplet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1e59b29dd7c082822ed63d425dd4967a542b5d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979479"
---
# <a name="using-cplapplet"></a>Uso di CPLApplet

Prima di Windows Vista, è stato creato un elemento del pannello di controllo creando un file dll e definendolo con estensione CPL. Questo file ha esportato la funzione [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) . Questo schema è ancora supportato in Windows Vista e versioni successive e viene illustrato in questo argomento. Tuttavia, le linee guida per i nuovi elementi del pannello di controllo consigliano un approccio più semplice con l'elemento del pannello di controllo compilato come file con estensione exe che usa un layout del flusso di attività.

Quando il pannello di controllo carica un file dll (o CPL), chiama la funzione [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) per ottenere informazioni come il numero di elementi del pannello di controllo che ospita il file, nonché informazioni su ogni elemento. Il pannello di controllo chiama anche la funzione quando la finestra dell'elemento è inizializzata, aperta o chiusa.

Quando Windows carica innanzitutto l'elemento del pannello di controllo, recupera l'indirizzo della funzione [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) e successivamente lo usa per chiamare la funzione e passare i messaggi it. Potrebbe inviare i messaggi seguenti.



| Message                                     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_DBLCLK cpl**](cpl-dblclk.md)           | Inviato per notificare a [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) che l'utente ha scelto l'icona associata a un elemento del pannello di controllo specificato. **CPlApplet** dovrebbe visualizzare la finestra di dialogo per l'elemento specificato ed eseguire tutte le attività specificate dall'utente. Il parametro **CPlApplet** *lParam1* è un numero intero che rappresenta l'indice in base zero dell'elemento del pannello di controllo. Il parametro *lParam2* è il puntatore **lpData** restituito nella struttura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) o [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) nel messaggio [**cpl \_ Inquirer**](cpl-inquire.md) o [**cpl \_ NEWINQUIRE**](cpl-newinquire.md) . Il valore restituito viene ignorato.                                                                |
| [**\_uscita cpl**](cpl-exit.md)               | Inviato dopo l'ultimo \_ messaggio di arresto cpl e immediatamente prima che Windows usi la funzione [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) per liberare la dll che contiene l'elemento del pannello di controllo. [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) deve liberare la memoria rimanente e prepararsi alla chiusura. Il valore restituito viene ignorato.                                                                                                                                                                                                                                                                                                                                                                                                |
| [**\_conteggio cpl**](cpl-getcount.md)       | Inviato dopo il \_ messaggio cpl init per richiedere a [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) di restituire un numero che indichi il numero di sottoprogrammi supportati.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**\_init cpl**](cpl-init.md)               | Inviato immediatamente dopo che la DLL contenente l'elemento del pannello di controllo è stata caricata. Il messaggio richiede a [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) di eseguire le procedure di inizializzazione, inclusa l'allocazione della memoria.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**domande su CPL \_**](cpl-inquire.md)         | Inviato dopo il \_ messaggio cpl GetCount per richiedere a [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) di fornire informazioni su un sottoprogramma specificato. Il valore *lParam1* è un numero intero che rappresenta l'indice in base zero del sottoprogramma su cui vengono richieste informazioni. Il parametro *lParam2* di **CPlApplet** punta a una struttura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) . Il valore restituito viene ignorato.                                                                                                                                                                                                                                                                                                    |
| [**\_NEWINQUIRE cpl**](cpl-newinquire.md)   | Inviato dopo il \_ messaggio cpl GetCount per richiedere [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) per fornire informazioni su un elemento del pannello di controllo specificato. Il valore *lParam1* è un numero intero che rappresenta l'indice in base zero del sottoprogramma su cui vengono richieste informazioni. Il parametro *lParam2* è un puntatore a una struttura [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) . CPL \_ NEWINQUIRE in genere deve essere ignorato. L'applicazione deve elaborare solo CPL \_ Inquirer su Windows 95, Microsoft Windows NT 4,0 e versioni successive, perché le prestazioni del pannello di controllo soffrono quando \_ si usa cpl NEWINQUIRE. Questo perché le stringhe e le icone restituite non possono essere memorizzate nella cache. Il valore restituito viene ignorato. |
| [**\_selezione cpl**](cpl-select.md)           | Obsoleta. Le versioni correnti di Windows non inviano questo messaggio.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**\_STARTWPARMS cpl**](cpl-startwparms.md) | Inviato per notificare a [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) che l'utente ha scelto l'icona associata a una determinata finestra di dialogo. **CPlApplet** dovrebbe visualizzare la finestra di dialogo corrispondente ed eseguire tutte le attività specificate dall'utente. Questo messaggio è simile a CPL \_ DblClk, ma potrebbero esserci alcune informazioni aggiuntive. Il parametro *lParam1* è il numero dell'elemento del pannello di controllo e *LParam2* è un **LPCTSTR** a tutte le direzioni aggiuntive che potrebbero essere necessarie. Restituisce **true** se il messaggio è gestito; in caso contrario, **false**. Questo messaggio è valido per la [versione 5,00](versions.md) e successive di Shell32.dll.                                                                                         |
| [**\_arresto cpl**](cpl-stop.md)               | Inviato una volta per ogni elemento del pannello di controllo nel file. cpl prima che Windows Scarica l'estensione del pannello di controllo. [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) deve liberare la memoria associata al numero di elemento fornito in *lParam1*. Il parametro *lParam2* è **lpData** puntatore restituito nella struttura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) o [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) nel messaggio [**cpl \_ Inquirer**](cpl-inquire.md) o [**cpl \_ NEWINQUIRE**](cpl-newinquire.md) . Il valore restituito viene ignorato.                                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Elementi del pannello di controllo](control-panel-applications.md)
</dt> <dt>

[Linee guida sull'esperienza utente](user-experience-guidelines.md)
</dt> <dt>

[Registrazione degli elementi del pannello di controllo](registering-control-panel-items.md)
</dt> <dt>

[Elaborazione del messaggio del pannello di controllo](message-processing.md)
</dt> <dt>

[Esecuzione degli elementi del pannello di controllo](executing-control-panel-items.md)
</dt> <dt>

[Estensione degli elementi del pannello di controllo di sistema](extending-system-control-panel-items.md)
</dt> <dt>

[Assegnazione delle categorie del pannello di controllo](assigning-control-panel-categories.md)
</dt> <dt>

[Creazione di collegamenti alle attività ricercabili per un elemento del pannello di controllo](creating-searchable-task-links.md)
</dt> <dt>

[Accesso al pannello di controllo in modalità provvisoria in Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
