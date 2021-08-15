---
description: Una finestra di dialogo Sfoglia consente all'utente di selezionare una directory. La directory non deve esistere e può essere creata usando questo controllo.
ms.assetid: 35b991b8-d291-44ef-b1c0-8128bed3c3c8
title: Finestra di dialogo Sfoglia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7caceb8e10bc99a9edd8fa5b828efa2e5cbc8b4ed7164d40e2235e19c098199
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118380715"
---
# <a name="browse-dialog"></a>Finestra di dialogo Sfoglia

Una finestra di dialogo Sfoglia consente all'utente di selezionare una directory. La directory non deve esistere e può essere creata usando questo controllo.

Questo tipo di finestra di dialogo contiene in genere i tre controlli seguenti. Questi controlli sono connessi alla stessa proprietà. Tale proprietà è il percorso selezionato.

-   Controllo [PathEdit per](pathedit-control.md) selezionare la sezione finale del percorso. Questo controllo non può perdere lo stato attivo se la coda immessa non è valida nel volume presente.
-   Controllo [DirectoryCombo per](directorycombo-control.md) visualizzare il percorso attualmente selezionato visualizzato dal controllo PathEdit. Questo controllo non mostra l'ultimo segmento del percorso.
-   Controllo [DirectoryList per](directorylist-control.md) visualizzare le cartelle sotto la directory attualmente visualizzata da DirectoryCombo. Può anche visualizzare una cartella che non è ancora stata creata.

Una finestra di dialogo Sfoglia contiene in genere anche un [controllo DirectoryCombo](directorycombo-control.md) che specifica i tipi di volume da visualizzare. È comune che tutti i tipi di volume siano visualizzati in una finestra di dialogo Sfoglia.

Le finestre di dialogo Sfoglia contengono in genere [tre controlli PushButton.](pushbutton-control.md) Questi pulsanti sono collegati ai rispettivi ControlEvent nella [tabella ControlEvent](controlevent-table.md). Questi pulsanti vengono usati per attivare le opzioni di controllo seguenti.



| Opzione di controllo | ControlEvent                                            |
|----------------|---------------------------------------------------------|
| Livello superiore   | [DirectoryListUp](directorylistup-controlevent.md)     |
| Nuova cartella     | [DirectoryListNew](directorylistnew-controlevent.md)   |
| Apri           | [DirectoryListOpen](directorylistopen-controlevent.md) |



 

Perché l'opzione Nuova cartella funzioni con un nome di cartella non predefinito, è necessario specificare il percorso della nuova cartella nella [tabella UIText](uitext-table.md). La stringa di percorso deve usare il formato "nome file breve \| nome file lungo" per il nome file. Ad esempio, usare un nome file, ad esempio "MyProd~1 \| My Fantastic Product". Per altre [informazioni sul formato](filename.md) del nome file, vedere Il tipo di dati della colonna Nome file. Se il percorso non è presente nella tabella UIText o se è impostato su un valore non valido, viene impostato sul valore "Fldr New Folder" per \| impostazione predefinita. Il **pulsante Nuova** cartella può essere omesso se la finestra di dialogo deve solo cercare cartelle esistenti.

 

 



