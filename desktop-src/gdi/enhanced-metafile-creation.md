---
description: Per creare un metafile avanzato, è possibile usare la funzione CreateEnhMetaFile, fornendo gli argomenti appropriati.
ms.assetid: b012e50e-a7f5-4687-9833-38dacc113d77
title: Creazione di metafile migliorata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 080c350e41e895c5d4bf834a6f407cca5907743d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754415"
---
# <a name="enhanced-metafile-creation"></a>Creazione di metafile migliorata

Per creare un metafile avanzato, è possibile usare la funzione [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) , fornendo gli argomenti appropriati. Il sistema utilizza questi argomenti per mantenere le dimensioni immagine, determinare se il metafile deve essere archiviato in un disco o in memoria e così via.

Per gestire le dimensioni immagine tra dispositivi di output, [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) richiede la risoluzione del dispositivo di riferimento. Questo *dispositivo di riferimento* è il dispositivo in cui è apparsa la prima immagine e il controller di dominio di *riferimento* è il *contesto di dispositivo* associato al dispositivo di riferimento. Quando si chiama la funzione **CreateEnhMetaFile** , è necessario fornire un handle che identifichi il controller di dominio. È possibile ottenere questo handle chiamando la funzione [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) o [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) . È anche possibile specificare **null** come handle per usare il dispositivo di visualizzazione corrente per il dispositivo di riferimento.

La maggior parte delle applicazioni archivia le immagini in modo permanente e quindi crea un metafile migliorato archiviato in un disco; Tuttavia, in alcuni casi questa operazione non è necessaria. Ad esempio, un'applicazione per l'elaborazione di testi che fornisce funzionalità di disegno dei grafici può archiviare un grafico definito dall'utente in memoria come Enhanced Metafile, quindi copiare i bit di metafile avanzati dalla memoria nel file di documento dell'utente. Un'applicazione che richiede un metafile archiviato in modo permanente su un disco deve fornire il nome del file quando chiama [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea). Se non si specifica un nome di file, il sistema considera automaticamente il metafile come un file temporaneo e lo archivia in memoria.

È possibile aggiungere una descrizione di testo facoltativa a un metafile contenente le informazioni sull'immagine e sull'autore. Un'applicazione può visualizzare queste stringhe nella finestra di dialogo Apri file per fornire all'utente informazioni sul contenuto del metafile che consente di selezionare il file appropriato. Se un'applicazione include la descrizione del testo, deve fornire un puntatore alla stringa quando chiama [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea).

Quando [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) ha esito positivo, restituisce un handle che identifica un contesto di dispositivo metafile speciale. Un contesto di dispositivo metafile è univoco in quanto è associato a un file anziché a un dispositivo di output. Quando il sistema elabora una funzione GDI che ha ricevuto un handle per un contesto di dispositivo metafile, la funzione GDI viene convertita in un record Enhanced-Metafile e il record viene accodato alla fine del metafile avanzato.

Una volta completata un'immagine e l'ultimo record viene aggiunto al metafile avanzato, l'applicazione può chiudere il file chiamando la funzione [**CloseEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-closeenhmetafile) . Questa funzione chiude ed Elimina il contesto di dispositivo metafile speciale e restituisce un handle che identifica il metafile avanzato.

Per eliminare un metafile con formato avanzato o un handle di metafile in formato avanzato, chiamare la funzione [**DeleteEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-deleteenhmetafile) .

 

 



