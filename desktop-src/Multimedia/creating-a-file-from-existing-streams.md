---
title: Creazione di un file da flussi esistenti
description: Creazione di un file da flussi esistenti
ms.assetid: 5149a766-7809-42b7-8e5c-b67b847b9218
keywords:
- AVISave (funzione)
- AVISaveV (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bc422d2170ccd49b8a9746666db7ebbcd7dff14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955391"
---
# <a name="creating-a-file-from-existing-streams"></a>Creazione di un file da flussi esistenti

Un modo per creare un file che contiene flussi di dati consiste nel combinare i flussi esistenti in un nuovo file. I flussi che forniscono i dati per il nuovo file possono risiedere in memoria o in uno o più file.

È possibile compilare un file da più flussi usando la funzione [**AVISave**](/windows/desktop/api/Vfw/nf-vfw-avisavea) . Questa funzione crea un file e scrive nel file i flussi di dati specificati nella sequenza chiamante. La sequenza chiamante per **AVISave** usa un numero variabile di argomenti che includono interfacce per i flussi combinati nel nuovo file.

È anche possibile combinare i flussi di dati in un nuovo file usando la funzione [**AVISaveV**](/windows/desktop/api/Vfw/nf-vfw-avisaveva) . Questa funzione fornisce la stessa funzionalità di **AVISave**, ma quando si usa **AVISaveV**, l'applicazione specifica i flussi di dati come una matrice, non come un numero variabile di argomenti.

È possibile creare una finestra di dialogo in cui l'utente può selezionare le impostazioni di compressione per il nuovo file tramite la funzione [**AVISaveOptions**](/windows/desktop/api/Vfw/nf-vfw-avisaveoptions) . Nella finestra di dialogo vengono visualizzate le impostazioni di compressione correnti e l'utente viene modificato. Le modifiche delle impostazioni di compressione vengono archiviate in una struttura [**AVICOMPRESSOPTIONS**](/windows/desktop/api/Vfw/ns-vfw-avicompressoptions) .

È anche possibile includere una funzione di callback con [**AVISave**](/windows/desktop/api/Vfw/nf-vfw-avisavea) e [**AVISaveV**](/windows/desktop/api/Vfw/nf-vfw-avisaveva) che l'applicazione può usare per visualizzare lo stato di avanzamento della scrittura del file e, se necessario, consentire all'utente di annullare l'operazione di salvataggio. È possibile includere l'indirizzo della funzione di callback nella sequenza chiamante di **AVISave** o **AVISaveV**.

È possibile consentire all'utente di selezionare un nome file per il nuovo file usando la funzione [**GetSaveFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa) . Questa funzione Visualizza la finestra di dialogo Salva con nome in cui l'utente può visualizzare l'anteprima del primo flusso, in genere il flusso video, di un file AVI.

È possibile creare un puntatore a interfaccia file (e un file virtuale) per un gruppo di flussi usando la funzione [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) . Altre funzioni AVIFile possono usare il puntatore di interfaccia file restituito da questa funzione per accedere ai flussi nel file virtuale. Al termine dell'utilizzo del file virtuale, eliminare il puntatore all'interfaccia di file utilizzando la funzione [**AVIFileRelease**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease) .

> [!Note]  
> Per ridurre al minimo la riduzione di immagini e audio, evitare di comprimere un file AVI più di una volta. Combinare parti del video non compresse nel sistema di modifica e quindi comprimere il prodotto finale. Per informazioni sulle opzioni di compressione, vedere [Video Compression Manager](video-compression-manager.md).

 

 

 




