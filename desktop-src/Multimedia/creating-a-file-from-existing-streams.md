---
title: Creazione di un file da un Flussi
description: Creazione di un file da un Flussi
ms.assetid: 5149a766-7809-42b7-8e5c-b67b847b9218
keywords:
- Funzione AVISave
- Funzione AVISaveV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a15a6ad3770f93bc2fb77dcb79975e1e9aa1fc8da7319e34c140baf488a69554
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498011"
---
# <a name="creating-a-file-from-existing-streams"></a>Creazione di un file da un Flussi

Un modo per creare un file che contiene flussi di dati è combinare i flussi esistenti in un nuovo file. I flussi che forniscono dati per il nuovo file possono risiedere in memoria o in uno o più file.

È possibile compilare un file da diversi flussi usando la [**funzione AVISave.**](/windows/desktop/api/Vfw/nf-vfw-avisavea) Questa funzione crea un file e scrive nel file i flussi di dati specificati nella sequenza di chiamata. La sequenza di chiamata **per AVISave** usa un numero variabile di argomenti che includono interfacce per i flussi combinati nel nuovo file.

È anche possibile combinare flussi di dati in un nuovo file usando la [**funzione AVISaveV.**](/windows/desktop/api/Vfw/nf-vfw-avisaveva) Questa funzione fornisce la stessa funzionalità di **AVISave,** ma quando si usa **AVISaveV**, l'applicazione specifica i flussi di dati come matrice, non come numero variabile di argomenti.

È possibile creare una finestra di dialogo in cui l'utente può selezionare le impostazioni di compressione per il nuovo file usando la [**funzione AVISaveOptions.**](/windows/desktop/api/Vfw/nf-vfw-avisaveoptions) La finestra di dialogo visualizza le impostazioni di compressione correnti e consente all'utente di modificarle. Le modifiche alle impostazioni di compressione vengono archiviate in [**una struttura AVICOMPRESSOPTIONS.**](/windows/desktop/api/Vfw/ns-vfw-avicompressoptions)

È anche possibile includere una funzione di callback con [**AVISave**](/windows/desktop/api/Vfw/nf-vfw-avisavea) e [**AVISaveV**](/windows/desktop/api/Vfw/nf-vfw-avisaveva) che l'applicazione può usare per visualizzare lo stato di avanzamento della scrittura del file e, se necessario, consentire all'utente di annullare l'operazione di salvataggio. È possibile includere l'indirizzo della funzione di callback nella sequenza di chiamata di **AVISave** o **AVISaveV.**

È possibile consentire all'utente di selezionare un nome file per il nuovo file usando la [**funzione GetSaveFileNamePreview.**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa) Questa funzione visualizza la finestra di dialogo Salva con nome in cui l'utente può visualizzare in anteprima il primo flusso (in genere il flusso video) di un file AVI.

È possibile creare un puntatore a interfaccia file (e un file virtuale) per un gruppo di flussi usando la [**funzione AVIMakeFileFromStreams.**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) Altre funzioni AVIFile possono usare il puntatore di interfaccia file restituito da questa funzione per accedere ai flussi nel file virtuale. Dopo aver terminato di usare il file virtuale, eliminare il puntatore dell'interfaccia file usando la [**funzione AVIFileRelease.**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease)

> [!Note]  
> Per ridurre al minimo la riduzione delle prestazioni di immagini e audio, evitare di comprimere un file AVI più di una volta. Combinare parti di video non compresse nel sistema di modifica e quindi comprimere il prodotto finale. Per informazioni sulle opzioni di compressione, vedere [Gestione compressione video.](video-compression-manager.md)

 

 

 




