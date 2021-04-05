---
title: Utilizzo dell'applicazione desktop di esempio
description: Utilizzo dell'applicazione desktop di esempio
ms.assetid: 5e3e5283-9e27-4f6a-93a9-84d84f2e875a
keywords:
- Windows Media Gestione dispositivi, esempi
- Gestione dispositivi, esempi
- applicazioni desktop, esempi
- Windows Media Gestione dispositivi, esempio di applicazione desktop
- Esempio di Gestione dispositivi, applicazione desktop
- esempi, applicazioni desktop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd511ea5241f458d2cd926dc8fb2f3681757ff8b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708746"
---
# <a name="using-the-sample-desktop-application"></a>Utilizzo dell'applicazione desktop di esempio

L'applicazione desktop di esempio è una finestra di base a due riquadri, come Esplora risorse. Consente di esplorare il contenuto di un dispositivo, usando una visualizzazione albero delle cartelle nel riquadro sinistro e i file nel riquadro di destra. La radice di ogni albero di cartelle viene considerata logicamente un dispositivo diverso, anche se alcuni dispositivi potrebbero rappresentarsi come diversi oggetti (uno per ogni archiviazione radice). Per leggere le proprietà di base di una cartella o di un file, fare clic con il pulsante destro del mouse sull'oggetto e scegliere **Proprietà**.

È possibile eliminare i file nel dispositivo selezionando un file nel riquadro destro e selezionando **Elimina** dal menu **file** . Per aggiungere file multimediali al dispositivo, è possibile trascinare i file dal desktop nel riquadro destro del programma. Si noti che i file devono essere di un formato multimediale supportato dal dispositivo. i file di formati non accettabili (file non multimediali, ad esempio file con estensione txt o formati multimediali non supportati dal dispositivo) non verranno inviati al dispositivo. (Si noti che questa restrizione è il programma; Windows Media Gestione dispositivi consente di inviare qualsiasi file a un dispositivo se viene accettato dal dispositivo.

Per acquisire gli eventi di callback inviati all'interfaccia [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) , è necessario selezionare l'opzione "utilizza interfaccia operativa" nel menu **Opzioni** .

Il menu **Opzioni** consente inoltre di scegliere se utilizzare più interfacce avanzate con le funzionalità supportate dai dispositivi avanzati.

Nel menu **contenitori** sono disponibili opzioni che consentono di creare una playlist o un album. Per creare una playlist, selezionare uno o più brani sul dispositivo e fare clic su **Crea playlist** nel menu **contenitori** . Questa funzionalità funziona solo nei dispositivi MTP, perché il codice supporta solo la creazione di un file di playlist "virtuale". Una playlist virtuale è una playlist specificata solo dai valori dei metadati, anziché da un file fisico, ad esempio un file WPL. Per usare questa funzionalità, il dispositivo deve supportare playlist vuote.

Per creare un album (una playlist con un'immagine associata), selezionare uno o più brani sul dispositivo e fare clic su **Crea album** nel menu **contenitori** . Una finestra di dialogo consente di selezionare un file di immagine nel computer da associare all'album. Analogamente al modo in cui vengono create le playlist, l'applicazione crea un file di album "vuoto"; Se il dispositivo non supporta gli album vuoti, la funzionalità non funzionerà.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Applicazione desktop di esempio**](sample-desktop-application.md)
</dt> </dl>

 

 




