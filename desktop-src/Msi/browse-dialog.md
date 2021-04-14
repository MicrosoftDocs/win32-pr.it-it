---
description: Una finestra di dialogo Sfoglia consente all'utente di selezionare una directory. La directory non deve esistere e può essere creata tramite questo controllo.
ms.assetid: 35b991b8-d291-44ef-b1c0-8128bed3c3c8
title: Sfoglia finestra di dialogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3f6d3c3d95caec7e9a439621f6741b0dceb0c83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401703"
---
# <a name="browse-dialog"></a>Sfoglia finestra di dialogo

Una finestra di dialogo Sfoglia consente all'utente di selezionare una directory. La directory non deve esistere e può essere creata tramite questo controllo.

Questo tipo di finestra di dialogo contiene in genere i tre controlli seguenti. Questi controlli sono connessi alla stessa proprietà. Tale proprietà è il percorso selezionato.

-   [Controllo PathEdit](pathedit-control.md) per selezionare la sezione finale del percorso. Questo controllo non può perdere lo stato attivo se la coda immessa non è valida nel volume presente.
-   [Controllo DirectoryCombo](directorycombo-control.md) per visualizzare il percorso attualmente selezionato visualizzato dal controllo PathEdit. Questo controllo non Mostra l'ultimo segmento del percorso.
-   Un [controllo Directory](directorylist-control.md) per visualizzare le cartelle sotto la directory attualmente visualizzata dal DirectoryCombo. È anche possibile visualizzare una cartella che non è ancora stata creata.

Una finestra di dialogo Sfoglia contiene in genere anche un [controllo DirectoryCombo](directorycombo-control.md) che specifica i tipi di volume da visualizzare. È comune che tutti i tipi di volume vengano visualizzati in una finestra di dialogo Sfoglia.

Le finestre di dialogo di esplorazione contengono in genere tre [controlli pulsante](pushbutton-control.md). Questi pulsanti sono collegati ai rispettivi ControlEvents nella [tabella ControlEvent](controlevent-table.md). Questi pulsanti vengono usati per attivare le opzioni di controllo seguenti.



| Opzione di controllo | ControlEvent                                            |
|----------------|---------------------------------------------------------|
| Livello superiore   | [DirectoryListUp](directorylistup-controlevent.md)     |
| Nuova cartella     | [DirectoryListNew](directorylistnew-controlevent.md)   |
| Apri           | [DirectoryListOpen](directorylistopen-controlevent.md) |



 

Affinché l'opzione nuova cartella funzioni con un nome di cartella non predefinito, è necessario specificare il percorso della nuova cartella nella [tabella UIText](uitext-table.md). Per il nome del file, la stringa di percorso deve usare il formato "nome file breve nome file \| lungo". Ad esempio, usare un nome file, ad esempio "Prod ~ 1 \| My Fabulous Product". Per ulteriori informazioni sul formato del nome file, vedere il tipo di dati della colonna [filename](filename.md) . Se il percorso non è presente nella tabella UIText o se è impostato su un valore non valido, per impostazione predefinita viene impostato sul valore "FLDR \| New Folder". Il pulsante **nuova cartella** può essere omesso se la finestra di dialogo deve solo cercare le cartelle esistenti.

 

 



