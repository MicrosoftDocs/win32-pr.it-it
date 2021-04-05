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
# <a name="stoclien-operations"></a><span data-ttu-id="3e807-105">Operazioni StoClien</span><span class="sxs-lookup"><span data-stu-id="3e807-105">StoClien Operations</span></span>

<span data-ttu-id="3e807-106">L'esempio [StoClien](structured-storage-client-sample--stoclien-.md) illustra come il client usa l'archiviazione strutturata.</span><span class="sxs-lookup"><span data-stu-id="3e807-106">The [StoClien](structured-storage-client-sample--stoclien-.md) sample demonstrates how the client uses structured storage.</span></span> <span data-ttu-id="3e807-107">Di seguito vengono riepilogate le operazioni StoClien.</span><span class="sxs-lookup"><span data-stu-id="3e807-107">The following summarizes the StoClien operations.</span></span>

<span data-ttu-id="3e807-108">L'area client della finestra dell'applicazione [StoClien](structured-storage-client-sample--stoclien-.md) viene utilizzata per la visualizzazione visiva del disegno FreeForm creato con un mouse o un dispositivo tablet.</span><span class="sxs-lookup"><span data-stu-id="3e807-108">The [StoClien](structured-storage-client-sample--stoclien-.md) application window client area is used for visual display of freeform drawing created with a mouse or tablet device.</span></span> <span data-ttu-id="3e807-109">Per creare con il mouse, tenere premuto il pulsante sinistro del mouse mentre si muove il mouse.</span><span class="sxs-lookup"><span data-stu-id="3e807-109">To draw with the mouse, press and hold the left mouse button while moving the mouse.</span></span> <span data-ttu-id="3e807-110">Il rilascio del pulsante sinistro del mouse termina il disegno di una linea.</span><span class="sxs-lookup"><span data-stu-id="3e807-110">Releasing the left mouse button ends the drawing of a line.</span></span>

<span data-ttu-id="3e807-111">Di seguito è riportato un riepilogo delle operazioni dal punto di vista del Stoclien.exe come client COM del server Stoserve.dll COM:</span><span class="sxs-lookup"><span data-stu-id="3e807-111">Here is a summary of operations from the standpoint of Stoclien.exe as a COM client of the Stoserve.dll COM server:</span></span>

<dl> <dt>

<span data-ttu-id="3e807-112"><span id="File_Open"></span><span id="file_open"></span><span id="FILE_OPEN"></span>File/Apri</span><span class="sxs-lookup"><span data-stu-id="3e807-112"><span id="File_Open"></span><span id="file_open"></span><span id="FILE_OPEN"></span>File/Open</span></span>
</dt> <dd>

<span data-ttu-id="3e807-113">Consente di visualizzare la finestra di dialogo Apri per ottenere un nome e un percorso per l'apertura di un file di disegno di carta esistente.</span><span class="sxs-lookup"><span data-stu-id="3e807-113">Shows the Open dialog box to obtain a name and path for an existing paper drawing file to open.</span></span> <span data-ttu-id="3e807-114">Valore predefinito. Si presuppone l'estensione del nome di file PAP per questi file.</span><span class="sxs-lookup"><span data-stu-id="3e807-114">A default .PAP file name extension for these files is assumed.</span></span> <span data-ttu-id="3e807-115">Se sono state apportate modifiche al disegno esistente quando si sceglie questa voce di menu, viene prima visualizzata una finestra di dialogo che chiede all'utente se il disegno corrente deve essere salvato nel file composto associato.</span><span class="sxs-lookup"><span data-stu-id="3e807-115">If changes were made to the existing drawing when this menu item is chosen, a separate dialog will first be shown asking the user if the current drawing should be saved into its associated compound file.</span></span>

</dd> <dt>

<span data-ttu-id="3e807-116"><span id="File_Save"></span><span id="file_save"></span><span id="FILE_SAVE"></span>File/Salva</span><span class="sxs-lookup"><span data-stu-id="3e807-116"><span id="File_Save"></span><span id="file_save"></span><span id="FILE_SAVE"></span>File/Save</span></span>
</dt> <dd>

<span data-ttu-id="3e807-117">Salva il disegno corrente nel file composto associato.</span><span class="sxs-lookup"><span data-stu-id="3e807-117">Saves the current drawing into its associated compound file.</span></span>

</dd> <dt>

<span data-ttu-id="3e807-118"><span id="File_Save_As"></span><span id="file_save_as"></span><span id="FILE_SAVE_AS"></span>File/Salva con nome</span><span class="sxs-lookup"><span data-stu-id="3e807-118"><span id="File_Save_As"></span><span id="file_save_as"></span><span id="FILE_SAVE_AS"></span>File/Save As</span></span>
</dt> <dd>

<span data-ttu-id="3e807-119">Mostra la finestra di dialogo Salva con nome per ottenere un nome e un percorso per un nuovo file di disegno carta da creare.</span><span class="sxs-lookup"><span data-stu-id="3e807-119">Shows the Save As dialog box to obtain a name and path for a new paper drawing file to create.</span></span> <span data-ttu-id="3e807-120">Il disegno corrente diventa il contenuto salvato del nuovo file e il nuovo file diventa il nuovo file composto associato per il disegno.</span><span class="sxs-lookup"><span data-stu-id="3e807-120">The current drawing becomes the saved content of the new file, and the new file becomes the new associated compound file for the drawing.</span></span>

</dd> <dt>

<span data-ttu-id="3e807-121"><span id="File_Exit"></span><span id="file_exit"></span><span id="FILE_EXIT"></span>File/uscita</span><span class="sxs-lookup"><span data-stu-id="3e807-121"><span id="File_Exit"></span><span id="file_exit"></span><span id="FILE_EXIT"></span>File/Exit</span></span>
</dt> <dd>

<span data-ttu-id="3e807-122">Esce da [StoClien](structured-storage-client-sample--stoclien-.md).</span><span class="sxs-lookup"><span data-stu-id="3e807-122">Exits [StoClien](structured-storage-client-sample--stoclien-.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e807-123"><span id="Draw_Drawing_On"></span><span id="draw_drawing_on"></span><span id="DRAW_DRAWING_ON"></span>Disegno/disegno</span><span class="sxs-lookup"><span data-stu-id="3e807-123"><span id="Draw_Drawing_On"></span><span id="draw_drawing_on"></span><span id="DRAW_DRAWING_ON"></span>Draw/Drawing On</span></span>
</dt> <dd>

<span data-ttu-id="3e807-124">Attiva il disegno tra il client [StoClien](structured-storage-client-sample--stoclien-.md) e l'oggetto Copaper nel server.</span><span class="sxs-lookup"><span data-stu-id="3e807-124">Turns on drawing between the [StoClien](structured-storage-client-sample--stoclien-.md) client and the COPaper object in the server.</span></span> <span data-ttu-id="3e807-125">Questo comando blocca l'oggetto Copaper per l'uso esclusivo da parte del client e impedisce ad altri client di accedere alla stessa istanza della cocarta nel server.</span><span class="sxs-lookup"><span data-stu-id="3e807-125">This command locks the COPaper object for exclusive use by this client and prevents other clients from accessing the same COPaper instance in the server.</span></span>

</dd> <dt>

<span data-ttu-id="3e807-126"><span id="Draw_Drawing_Off"></span><span id="draw_drawing_off"></span><span id="DRAW_DRAWING_OFF"></span>Disegno/disegno disattivato</span><span class="sxs-lookup"><span data-stu-id="3e807-126"><span id="Draw_Drawing_Off"></span><span id="draw_drawing_off"></span><span id="DRAW_DRAWING_OFF"></span>Draw/Drawing Off</span></span>
</dt> <dd>

<span data-ttu-id="3e807-127">Disattiva il disegno tra il client [StoClien](structured-storage-client-sample--stoclien-.md) e l'oggetto Copaper nel server.</span><span class="sxs-lookup"><span data-stu-id="3e807-127">Turns off drawing between the [StoClien](structured-storage-client-sample--stoclien-.md) client and the COPaper object in the server.</span></span> <span data-ttu-id="3e807-128">Questo comando Sblocca il Copaper per l'uso esclusivo da parte del client e consente ad altri client di accedere alla stessa istanza della cocarta nel server.</span><span class="sxs-lookup"><span data-stu-id="3e807-128">This command unlocks the COPaper for exclusive use by this client and allows other clients to access the same COPaper instance in the server.</span></span>

</dd> <dt>

<span data-ttu-id="3e807-129"><span id="Draw_Redraw"></span><span id="draw_redraw"></span><span id="DRAW_REDRAW"></span>Disegni/ridisegni</span><span class="sxs-lookup"><span data-stu-id="3e807-129"><span id="Draw_Redraw"></span><span id="draw_redraw"></span><span id="DRAW_REDRAW"></span>Draw/Redraw</span></span>
</dt> <dd>

<span data-ttu-id="3e807-130">Ridisegna nel client i dati di disegno correnti contenuti nell'oggetto Copaper nel server.</span><span class="sxs-lookup"><span data-stu-id="3e807-130">Redraws in the client the current drawing data held in the COPaper object in the server.</span></span>

</dd> <dt>

<span data-ttu-id="3e807-131"><span id="Draw_Erase"></span><span id="draw_erase"></span><span id="DRAW_ERASE"></span>Estrai/Cancella</span><span class="sxs-lookup"><span data-stu-id="3e807-131"><span id="Draw_Erase"></span><span id="draw_erase"></span><span id="DRAW_ERASE"></span>Draw/Erase</span></span>
</dt> <dd>

<span data-ttu-id="3e807-132">Cancella il contenuto del disegno corrente e cancella l'immagine della finestra.</span><span class="sxs-lookup"><span data-stu-id="3e807-132">Erases the current drawing content and clears the window image.</span></span> <span data-ttu-id="3e807-133">Selezione menu: penna/colore consente di visualizzare la finestra di dialogo Scegli colore per ottenere un nuovo colore della penna per il disegno.</span><span class="sxs-lookup"><span data-stu-id="3e807-133">Menu Selection: Pen/Color Shows the Choose Color dialog box to obtain a new pen color for drawing.</span></span>

</dd> <dt>

<span data-ttu-id="3e807-134"><span id="Pen_Medium"></span><span id="pen_medium"></span><span id="PEN_MEDIUM"></span>Penna/media</span><span class="sxs-lookup"><span data-stu-id="3e807-134"><span id="Pen_Medium"></span><span id="pen_medium"></span><span id="PEN_MEDIUM"></span>Pen/Medium</span></span>
</dt> <dd>

<span data-ttu-id="3e807-135">Sceglie la larghezza media per il disegno.</span><span class="sxs-lookup"><span data-stu-id="3e807-135">Chooses the medium width for drawing.</span></span> <span data-ttu-id="3e807-136">Un segno di spunta in questa scelta di menu indica che media è la larghezza corrente della penna.</span><span class="sxs-lookup"><span data-stu-id="3e807-136">A check mark on this menu choice indicates that medium is the current pen width.</span></span>

</dd> <dt>

<span data-ttu-id="3e807-137"><span id="Pen_Thick"></span><span id="pen_thick"></span><span id="PEN_THICK"></span>Penna/spessore</span><span class="sxs-lookup"><span data-stu-id="3e807-137"><span id="Pen_Thick"></span><span id="pen_thick"></span><span id="PEN_THICK"></span>Pen/Thick</span></span>
</dt> <dd>

<span data-ttu-id="3e807-138">Sceglie la larghezza spessa per il disegno.</span><span class="sxs-lookup"><span data-stu-id="3e807-138">Chooses the thick width for drawing.</span></span> <span data-ttu-id="3e807-139">Un segno di spunta in questa scelta di menu indica che lo spessore è la larghezza corrente della penna.</span><span class="sxs-lookup"><span data-stu-id="3e807-139">A check mark on this menu choice indicates that thick is the current pen width.</span></span>

</dd> <dt>

<span data-ttu-id="3e807-140"><span id="Pen_Thin"></span><span id="pen_thin"></span><span id="PEN_THIN"></span>Penna/thin</span><span class="sxs-lookup"><span data-stu-id="3e807-140"><span id="Pen_Thin"></span><span id="pen_thin"></span><span id="PEN_THIN"></span>Pen/Thin</span></span>
</dt> <dd>

<span data-ttu-id="3e807-141">Sceglie la larghezza sottile per il disegno.</span><span class="sxs-lookup"><span data-stu-id="3e807-141">Chooses the thin width for drawing.</span></span> <span data-ttu-id="3e807-142">Un segno di spunta in questa scelta di menu indica che la larghezza corrente della penna è sottile.</span><span class="sxs-lookup"><span data-stu-id="3e807-142">A check mark on this menu choice indicates that thin is the current pen width.</span></span>

</dd> <dt>

<span data-ttu-id="3e807-143"><span id="Sink_Connect"></span><span id="sink_connect"></span><span id="SINK_CONNECT"></span>Sink/connessione</span><span class="sxs-lookup"><span data-stu-id="3e807-143"><span id="Sink_Connect"></span><span id="sink_connect"></span><span id="SINK_CONNECT"></span>Sink/Connect</span></span>
</dt> <dd>

<span data-ttu-id="3e807-144">Connette l'interfaccia IPaperSink di COPaperSink al punto di connessione PaperSink dell'oggetto Copaper.</span><span class="sxs-lookup"><span data-stu-id="3e807-144">Connects the COPaperSink IPaperSink interface to the COPaper object PaperSink connection point.</span></span> <span data-ttu-id="3e807-145">Il ridisegno dell'immagine del disegno corrente in [StoClien](structured-storage-client-sample--stoclien-.md) si basa sulla connessione del sink.</span><span class="sxs-lookup"><span data-stu-id="3e807-145">Repainting of the current drawing image in [StoClien](structured-storage-client-sample--stoclien-.md) relies on the sink connection.</span></span> <span data-ttu-id="3e807-146">Un segno di spunta in questa scelta di menu indica che la ridisegno è connessa.</span><span class="sxs-lookup"><span data-stu-id="3e807-146">A check mark on this menu choice indicates that repainting is connected.</span></span>

</dd> <dt>

<span data-ttu-id="3e807-147"><span id="Sink_Disconnect"></span><span id="sink_disconnect"></span><span id="SINK_DISCONNECT"></span>Sink/disconnessione</span><span class="sxs-lookup"><span data-stu-id="3e807-147"><span id="Sink_Disconnect"></span><span id="sink_disconnect"></span><span id="SINK_DISCONNECT"></span>Sink/Disconnect</span></span>
</dt> <dd>

<span data-ttu-id="3e807-148">Disconnette l'interfaccia COPaperSink IPaperSink dal punto di connessione PaperSink dell'oggetto Copaper.</span><span class="sxs-lookup"><span data-stu-id="3e807-148">Disconnects the COPaperSink IPaperSink interface from the COPaper object PaperSink connection point.</span></span> <span data-ttu-id="3e807-149">Il ridisegno dell'immagine del disegno corrente in [StoClien](structured-storage-client-sample--stoclien-.md) si basa sulla connessione del sink.</span><span class="sxs-lookup"><span data-stu-id="3e807-149">Repainting of the current drawing image in [StoClien](structured-storage-client-sample--stoclien-.md) relies on the sink connection.</span></span> <span data-ttu-id="3e807-150">Un segno di spunta in questa scelta di menu indica che la ridisegno è disconnessa.</span><span class="sxs-lookup"><span data-stu-id="3e807-150">A check mark on this menu choice indicates that repainting is disconnected.</span></span>

</dd> <dt>

<span data-ttu-id="3e807-151"><span id="Help_StoClien_Tutorial"></span><span id="help_stoclien_tutorial"></span><span id="HELP_STOCLIEN_TUTORIAL"></span>Esercitazione guida/StoClien</span><span class="sxs-lookup"><span data-stu-id="3e807-151"><span id="Help_StoClien_Tutorial"></span><span id="help_stoclien_tutorial"></span><span id="HELP_STOCLIEN_TUTORIAL"></span>Help/StoClien Tutorial</span></span>
</dt> <dd>

<span data-ttu-id="3e807-152">Apre il file dell'esercitazione STOCLIEN.HTM nel Web browser.</span><span class="sxs-lookup"><span data-stu-id="3e807-152">Opens the STOCLIEN.HTM tutorial file in the Web browser.</span></span>

</dd> <dt>

<span data-ttu-id="3e807-153"><span id="Help_StoServe_Tutorial"></span><span id="help_stoserve_tutorial"></span><span id="HELP_STOSERVE_TUTORIAL"></span>Esercitazione guida/StoServe</span><span class="sxs-lookup"><span data-stu-id="3e807-153"><span id="Help_StoServe_Tutorial"></span><span id="help_stoserve_tutorial"></span><span id="HELP_STOSERVE_TUTORIAL"></span>Help/StoServe Tutorial</span></span>
</dt> <dd>

<span data-ttu-id="3e807-154">Apre il file dell'esercitazione STOSERVE.HTM nel Web browser.</span><span class="sxs-lookup"><span data-stu-id="3e807-154">Opens the STOSERVE.HTM tutorial file in the Web browser.</span></span>

</dd> <dt>

<span data-ttu-id="3e807-155"><span id="Help_Read_Source_File"></span><span id="help_read_source_file"></span><span id="HELP_READ_SOURCE_FILE"></span>Guida/Leggi file di origine</span><span class="sxs-lookup"><span data-stu-id="3e807-155"><span id="Help_Read_Source_File"></span><span id="help_read_source_file"></span><span id="HELP_READ_SOURCE_FILE"></span>Help/Read Source File</span></span>
</dt> <dd>

<span data-ttu-id="3e807-156">Consente di visualizzare la finestra di dialogo Apri in cui è possibile aprire un file di origine da questa lezione o da un altro nel blocco note di Windows.</span><span class="sxs-lookup"><span data-stu-id="3e807-156">Displays the Open dialog box so you can open a source file from this lesson or another one in the Windows Notepad.</span></span>

</dd> <dt>

<span data-ttu-id="3e807-157"><span id="Help_About_StoClien"></span><span id="help_about_stoclien"></span><span id="HELP_ABOUT_STOCLIEN"></span>Guida/informazioni su StoClien</span><span class="sxs-lookup"><span data-stu-id="3e807-157"><span id="Help_About_StoClien"></span><span id="help_about_stoclien"></span><span id="HELP_ABOUT_STOCLIEN"></span>Help/About StoClien</span></span>
</dt> <dd>

<span data-ttu-id="3e807-158">Consente di visualizzare la finestra di dialogo informazioni su per questa applicazione.</span><span class="sxs-lookup"><span data-stu-id="3e807-158">Displays the About dialog box for this application.</span></span>

</dd> </dl>

<span data-ttu-id="3e807-159">L'esempio [StoClien](structured-storage-client-sample--stoclien-.md) usa molte delle classi e dei servizi di utilità forniti da [APPUTIL](./using-visual-studio.md).</span><span class="sxs-lookup"><span data-stu-id="3e807-159">The [StoClien](structured-storage-client-sample--stoclien-.md) sample uses many of the utility classes and services provided by [APPUTIL](./using-visual-studio.md).</span></span> <span data-ttu-id="3e807-160">Per ulteriori informazioni su [APPUTIL](./using-visual-studio.md), vedere il codice sorgente della libreria [APPUTIL](./using-visual-studio.md) nella directory di pari livello [APPUTIL](./using-visual-studio.md) e apputil.MD nella directory principale dell'esercitazione.</span><span class="sxs-lookup"><span data-stu-id="3e807-160">For more information about [APPUTIL](./using-visual-studio.md), see the [APPUTIL](./using-visual-studio.md) library source code in the sibling [APPUTIL](./using-visual-studio.md) directory and Apputil.md in the main tutorial directory.</span></span> <span data-ttu-id="3e807-161">Per ulteriori informazioni su [APPUTIL](./using-visual-studio.md), vedere [How to Build Samples](how-to-build-samples.md).</span><span class="sxs-lookup"><span data-stu-id="3e807-161">For more information about [APPUTIL](./using-visual-studio.md), see [How to Build Samples](how-to-build-samples.md).</span></span>

 

 