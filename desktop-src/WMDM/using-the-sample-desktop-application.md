---
title: Uso dell'applicazione desktop di esempio
description: Uso dell'applicazione desktop di esempio
ms.assetid: 5e3e5283-9e27-4f6a-93a9-84d84f2e875a
keywords:
- Windows Gestione dispositivi multimediali, esempi
- Gestione dispositivi, esempi
- applicazioni desktop, esempi
- Windows Media Device Manager, esempio di applicazione desktop
- Gestione dispositivi, esempio di applicazione desktop
- esempi, applicazioni desktop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91b418458c9e6091b3e2002a30afb95abb77919d062667a9667a3aac9d4dad6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118584167"
---
# <a name="using-the-sample-desktop-application"></a>Uso dell'applicazione desktop di esempio

L'applicazione desktop di esempio è una finestra a due panoramica di base simile a Windows Explorer. Consente di esplorare il contenuto di un dispositivo, usando una visualizzazione albero delle cartelle nel riquadro sinistro e dei file nel riquadro destro. La radice di ogni albero di cartelle viene considerata logicamente un dispositivo diverso, anche se alcuni dispositivi potrebbero rappresentare se stessi come diversi oggetti (uno per ogni archiviazione radice). Per leggere le proprietà di base di una cartella o di un file, fare clic con il pulsante destro del mouse sull'oggetto e **scegliere Proprietà**.

È possibile eliminare i file nel dispositivo selezionando un file nel riquadro destro e **scegliendo Elimina** dal menu **File.** Per aggiungere file multimediali al dispositivo, è possibile trascinare i file dal desktop al riquadro destro del programma. Si noti che i file devono essere in un formato multimediale supportato dal dispositivo. I file con formati non accettabili (file non multimediali come .txt o formati multimediali non supportati dal dispositivo) non verranno inviati al dispositivo. Si noti che questa restrizione è del programma. Windows Gestione dispositivi multimediali consente di inviare qualsiasi file a un dispositivo se il dispositivo lo accetterà.

Per acquisire gli eventi di callback inviati [**all'interfaccia IWMDMOperation,**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) è necessario selezionare l'opzione "Usa interfaccia operazione" **nel** menu Opzioni.

Il  menu Opzioni consente anche di scegliere se usare diverse interfacce più avanzate con le funzionalità supportate dai dispositivi avanzati.

Il menu **Contenitori** include opzioni che consentono di creare una playlist o un album. Per creare una playlist, selezionare uno o più brani nel dispositivo e fare clic **su Crea playlist** nel menu **Contenitori.** Questa funzionalità funziona solo nei dispositivi MTP, perché il codice supporta solo la creazione di un file di playlist "virtuale". Una playlist virtuale è una playlist specificata solo dai valori dei metadati, anziché da un file fisico, ad esempio un file WPL. Per usare questa funzionalità, il dispositivo deve supportare playlist vuote.

Per creare un album (una playlist con un'immagine associata), selezionare uno o più brani nel dispositivo e fare clic su Create Album (Crea **album)** nel menu **Containers (Contenitori).** Una finestra di dialogo consente di selezionare un file di immagine nel computer da associare all'album. Analogamente al modo in cui crea le playlist, l'applicazione crea un file di album "vuoto". Se il dispositivo non supporta album vuoti, questa funzionalità non funzionerà.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Applicazione desktop di esempio**](sample-desktop-application.md)
</dt> </dl>

 

 




