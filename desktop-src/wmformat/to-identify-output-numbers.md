---
title: Per identificare i numeri di output
description: Per identificare i numeri di output
ms.assetid: a2135a71-52e6-4f62-8be8-b9886be9b37c
keywords:
- Windows Media Format SDK, identificazione dei numeri di output
- Advanced Systems Format (ASF), identificazione dei numeri di output
- ASF (Advanced Systems Format), identificazione dei numeri di output
- Advanced Systems Format (ASF), numeri di output e formati
- ASF (Advanced Systems Format), numeri di output e formati
- numeri e formati di output, identificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c601481520632806ac56e12e16e1474336897d1be341c9d19df8e235d6355ab1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699381"
---
# <a name="to-identify-output-numbers"></a>Per identificare i numeri di output

Per identificare i numeri di output per un file caricato, seguire questa procedura. Queste procedure sono identiche sia per il lettore asincrono che per il lettore sincrono. Se i nomi delle interfacce variano, i metodi del reader sincrono sono elencati tra parentesi dopo i metodi del lettore asincrono.

1.  Creare un oggetto lettore e caricare un file per la lettura. Per altre informazioni, vedere Per creare un lettore [e aprire un file](to-create-a-reader-and-open-a-file.md) (o Per creare un lettore [sincrono e aprire un file).](to-create-a-synchronous-reader-and-open-a-file.md)
2.  Recuperare il numero totale di output per il file chiamando [**IWMReader::GetOutputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputcount) (o [**IWMSyncReader::GetOutputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputcount)).
3.  Scorrere gli output uno alla volta, eseguendo i passaggi seguenti per ognuno:
    -   Recuperare [**l'interfaccia IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) per l'output corrente con una chiamata a [**IWMReader::GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) (o [**IWMSyncReader::GetOutputProps).**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputprops)
    -   Recuperare la [**struttura \_ MEDIA \_ TYPE WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) per l'output effettuando due chiamate a [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype). Eseguire la prima chiamata per ottenere le dimensioni della struttura , quindi allocare memoria per la struttura e passare un puntatore alla memoria allocata nella seconda chiamata. In alternativa, è possibile chiamare [**IWMMediaProps::GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-gettype), che fornisce il tipo principale senza che sia necessario allocare memoria per la **struttura WM MEDIA \_ \_ TYPE.** È possibile ignorare gli output del tipo principale errato.
    -   Recuperare il tipo di supporto principale e il sottotipo multimediale dalla **struttura WM \_ MEDIA \_ TYPE.** Questi valori vengono archiviati rispettivamente nei membri dati **majortype** **e subtype.**
    -   Controllare il valore di **WM \_ MEDIA \_ TYPE.formattype**. Specifica il tipo di struttura contenuto nel buffer in **WM \_ MEDIA \_ TYPE.pbFormat.** Per altre informazioni sui tipi di formato, vedere [Tipi di supporto.](media-types.md)
    -   Allocare memoria per contenere la struttura del tipo identificato nel passaggio precedente. Copiare la struttura nella memoria allocata. Per audio e video, questa struttura offre informazioni essenziali su come eseguire il rendering dei dati.

Il lettore sincrono fornisce anche metodi per recuperare le associazioni tra i numeri di output e i numeri di flusso. Per altre informazioni, vedere [Per trovare i numeri di flusso e i numeri di output.](to-find-stream-numbers-and-output-numbers.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Input, Flussi e output**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Interfaccia IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[**Interfaccia IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)
</dt> <dt>

[**Interfaccia IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Interfaccia IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Uso degli output**](working-with-outputs.md)
</dt> </dl>

 

 




