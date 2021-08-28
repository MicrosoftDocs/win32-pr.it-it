---
description: Per creare un metafile avanzato, usare la funzione CreateEnhMetaFile, fornendo gli argomenti appropriati.
ms.assetid: b012e50e-a7f5-4687-9833-38dacc113d77
title: Creazione avanzata di metafile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c89a4a05a18ecce4bc1b1fe3689e4f7a8dc64c833db4eac937da4f9a290dd3ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831991"
---
# <a name="enhanced-metafile-creation"></a>Creazione avanzata di metafile

Per creare un metafile avanzato, usare la [**funzione CreateEnhMetaFile,**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) fornendo gli argomenti appropriati. Il sistema usa questi argomenti per mantenere le dimensioni dell'immagine, determinare se il metafile deve essere archiviato su disco o in memoria e così via.

Per mantenere le dimensioni dell'immagine nei dispositivi di output, [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) richiede la risoluzione del dispositivo di riferimento. Questo *dispositivo di riferimento* è il dispositivo in  cui è stata apparsa per la prima volta l'immagine e il controller di dominio di riferimento è il contesto di *dispositivo* associato al dispositivo di riferimento. Quando si chiama **la funzione CreateEnhMetaFile,** è necessario fornire un handle che identifica questo controller di dominio. È possibile ottenere questo handle chiamando la [**funzione GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) [**o CreateDC.**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) È anche possibile specificare **NULL** come handle per usare il dispositivo di visualizzazione corrente per il dispositivo di riferimento.

La maggior parte delle applicazioni archivia le immagini in modo permanente e quindi crea un metafile avanzato archiviato su disco. Tuttavia, esistono alcuni casi in cui questa operazione non è necessaria. Ad esempio, un'applicazione di elaborazione di testo che fornisce funzionalità di disegno di grafici può archiviare un grafico definito dall'utente in memoria come metafile avanzato e quindi copiare i bit di metafile migliorati dalla memoria nel file di documento dell'utente. Un'applicazione che richiede un metafile archiviato in modo permanente su un disco deve fornire il nome del file quando chiama [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea). Se non si specifica un nome file, il sistema considera automaticamente il metafile come file temporaneo e lo archivia in memoria.

È possibile aggiungere una descrizione di testo facoltativa a un metafile contenente informazioni sull'immagine e sull'autore. Un'applicazione può visualizzare queste stringhe nella finestra di dialogo Apri file per fornire all'utente informazioni sul contenuto del metafile che consentono di selezionare il file appropriato. Se un'applicazione include la descrizione testuale, deve fornire un puntatore alla stringa quando chiama [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea).

Quando [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) ha esito positivo, restituisce un handle che identifica un contesto di dispositivo metafile speciale. Un contesto di dispositivo metafile è univoco perché è associato a un file anziché a un dispositivo di output. Quando il sistema elabora una funzione GDI che ha ricevuto un handle in un contesto di dispositivo metafile, converte la funzione GDI in un record metafile avanzato e aggiunge il record alla fine del metafile avanzato.

Dopo aver completato un'immagine e aggiunto l'ultimo record al metafile avanzato, l'applicazione può chiudere il file chiamando la [**funzione CloseEnhMetaFile.**](/windows/desktop/api/Wingdi/nf-wingdi-closeenhmetafile) Questa funzione chiude ed elimina il contesto di dispositivo metafile speciale e restituisce un handle che identifica il metafile avanzato.

Per eliminare un metafile di formato avanzato o un handle di metafile in formato avanzato, chiamare la [**funzione DeleteEnhMetaFile.**](/windows/desktop/api/Wingdi/nf-wingdi-deleteenhmetafile)

 

 



