---
title: Operazioni StoClien
description: L'esempio StoClien illustra come il client usa l'archiviazione strutturata. Di seguito vengono riepilogate le operazioni StoClien.
ms.assetid: 55498665-520b-4a83-a3d1-22d3ed15863e
keywords:
- Operazioni StoClien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1068fcf1e377456211e08020f41279be9b5e3b0b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729066"
---
# <a name="stoclien-operations"></a>Operazioni StoClien

L'esempio [StoClien](structured-storage-client-sample--stoclien-.md) illustra come il client usa l'archiviazione strutturata. Di seguito vengono riepilogate le operazioni StoClien.

L'area client della finestra dell'applicazione [StoClien](structured-storage-client-sample--stoclien-.md) viene utilizzata per la visualizzazione visiva del disegno FreeForm creato con un mouse o un dispositivo tablet. Per creare con il mouse, tenere premuto il pulsante sinistro del mouse mentre si muove il mouse. Il rilascio del pulsante sinistro del mouse termina il disegno di una linea.

Di seguito è riportato un riepilogo delle operazioni dal punto di vista del Stoclien.exe come client COM del server Stoserve.dll COM:

<dl> <dt>

<span id="File_Open"></span><span id="file_open"></span><span id="FILE_OPEN"></span>File/Apri
</dt> <dd>

Consente di visualizzare la finestra di dialogo Apri per ottenere un nome e un percorso per l'apertura di un file di disegno di carta esistente. Valore predefinito. Si presuppone l'estensione del nome di file PAP per questi file. Se sono state apportate modifiche al disegno esistente quando si sceglie questa voce di menu, viene prima visualizzata una finestra di dialogo che chiede all'utente se il disegno corrente deve essere salvato nel file composto associato.

</dd> <dt>

<span id="File_Save"></span><span id="file_save"></span><span id="FILE_SAVE"></span>File/Salva
</dt> <dd>

Salva il disegno corrente nel file composto associato.

</dd> <dt>

<span id="File_Save_As"></span><span id="file_save_as"></span><span id="FILE_SAVE_AS"></span>File/Salva con nome
</dt> <dd>

Mostra la finestra di dialogo Salva con nome per ottenere un nome e un percorso per un nuovo file di disegno carta da creare. Il disegno corrente diventa il contenuto salvato del nuovo file e il nuovo file diventa il nuovo file composto associato per il disegno.

</dd> <dt>

<span id="File_Exit"></span><span id="file_exit"></span><span id="FILE_EXIT"></span>File/uscita
</dt> <dd>

Esce da [StoClien](structured-storage-client-sample--stoclien-.md).

</dd> <dt>

<span id="Draw_Drawing_On"></span><span id="draw_drawing_on"></span><span id="DRAW_DRAWING_ON"></span>Disegno/disegno
</dt> <dd>

Attiva il disegno tra il client [StoClien](structured-storage-client-sample--stoclien-.md) e l'oggetto Copaper nel server. Questo comando blocca l'oggetto Copaper per l'uso esclusivo da parte del client e impedisce ad altri client di accedere alla stessa istanza della cocarta nel server.

</dd> <dt>

<span id="Draw_Drawing_Off"></span><span id="draw_drawing_off"></span><span id="DRAW_DRAWING_OFF"></span>Disegno/disegno disattivato
</dt> <dd>

Disattiva il disegno tra il client [StoClien](structured-storage-client-sample--stoclien-.md) e l'oggetto Copaper nel server. Questo comando Sblocca il Copaper per l'uso esclusivo da parte del client e consente ad altri client di accedere alla stessa istanza della cocarta nel server.

</dd> <dt>

<span id="Draw_Redraw"></span><span id="draw_redraw"></span><span id="DRAW_REDRAW"></span>Disegni/ridisegni
</dt> <dd>

Ridisegna nel client i dati di disegno correnti contenuti nell'oggetto Copaper nel server.

</dd> <dt>

<span id="Draw_Erase"></span><span id="draw_erase"></span><span id="DRAW_ERASE"></span>Estrai/Cancella
</dt> <dd>

Cancella il contenuto del disegno corrente e cancella l'immagine della finestra. Selezione menu: penna/colore consente di visualizzare la finestra di dialogo Scegli colore per ottenere un nuovo colore della penna per il disegno.

</dd> <dt>

<span id="Pen_Medium"></span><span id="pen_medium"></span><span id="PEN_MEDIUM"></span>Penna/media
</dt> <dd>

Sceglie la larghezza media per il disegno. Un segno di spunta in questa scelta di menu indica che media è la larghezza corrente della penna.

</dd> <dt>

<span id="Pen_Thick"></span><span id="pen_thick"></span><span id="PEN_THICK"></span>Penna/spessore
</dt> <dd>

Sceglie la larghezza spessa per il disegno. Un segno di spunta in questa scelta di menu indica che lo spessore è la larghezza corrente della penna.

</dd> <dt>

<span id="Pen_Thin"></span><span id="pen_thin"></span><span id="PEN_THIN"></span>Penna/thin
</dt> <dd>

Sceglie la larghezza sottile per il disegno. Un segno di spunta in questa scelta di menu indica che la larghezza corrente della penna è sottile.

</dd> <dt>

<span id="Sink_Connect"></span><span id="sink_connect"></span><span id="SINK_CONNECT"></span>Sink/connessione
</dt> <dd>

Connette l'interfaccia IPaperSink di COPaperSink al punto di connessione PaperSink dell'oggetto Copaper. Il ridisegno dell'immagine del disegno corrente in [StoClien](structured-storage-client-sample--stoclien-.md) si basa sulla connessione del sink. Un segno di spunta in questa scelta di menu indica che la ridisegno è connessa.

</dd> <dt>

<span id="Sink_Disconnect"></span><span id="sink_disconnect"></span><span id="SINK_DISCONNECT"></span>Sink/disconnessione
</dt> <dd>

Disconnette l'interfaccia COPaperSink IPaperSink dal punto di connessione PaperSink dell'oggetto Copaper. Il ridisegno dell'immagine del disegno corrente in [StoClien](structured-storage-client-sample--stoclien-.md) si basa sulla connessione del sink. Un segno di spunta in questa scelta di menu indica che la ridisegno è disconnessa.

</dd> <dt>

<span id="Help_StoClien_Tutorial"></span><span id="help_stoclien_tutorial"></span><span id="HELP_STOCLIEN_TUTORIAL"></span>Esercitazione guida/StoClien
</dt> <dd>

Apre il file dell'esercitazione STOCLIEN.HTM nel Web browser.

</dd> <dt>

<span id="Help_StoServe_Tutorial"></span><span id="help_stoserve_tutorial"></span><span id="HELP_STOSERVE_TUTORIAL"></span>Esercitazione guida/StoServe
</dt> <dd>

Apre il file dell'esercitazione STOSERVE.HTM nel Web browser.

</dd> <dt>

<span id="Help_Read_Source_File"></span><span id="help_read_source_file"></span><span id="HELP_READ_SOURCE_FILE"></span>Guida/Leggi file di origine
</dt> <dd>

Consente di visualizzare la finestra di dialogo Apri in cui è possibile aprire un file di origine da questa lezione o da un altro nel blocco note di Windows.

</dd> <dt>

<span id="Help_About_StoClien"></span><span id="help_about_stoclien"></span><span id="HELP_ABOUT_STOCLIEN"></span>Guida/informazioni su StoClien
</dt> <dd>

Consente di visualizzare la finestra di dialogo informazioni su per questa applicazione.

</dd> </dl>

L'esempio [StoClien](structured-storage-client-sample--stoclien-.md) usa molte delle classi e dei servizi di utilità forniti da [APPUTIL](./using-visual-studio.md). Per ulteriori informazioni su [APPUTIL](./using-visual-studio.md), vedere il codice sorgente della libreria [APPUTIL](./using-visual-studio.md) nella directory di pari livello [APPUTIL](./using-visual-studio.md) e apputil.MD nella directory principale dell'esercitazione. Per ulteriori informazioni su [APPUTIL](./using-visual-studio.md), vedere [How to Build Samples](how-to-build-samples.md).

 

 