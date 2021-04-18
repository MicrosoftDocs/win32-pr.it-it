---
title: Per identificare i numeri di output
description: Per identificare i numeri di output
ms.assetid: a2135a71-52e6-4f62-8be8-b9886be9b37c
keywords:
- Windows Media Format SDK, identificazione dei numeri di output
- ASF (Advanced Systems Format), identificazione dei numeri di output
- ASF (Advanced Systems Format), identificazione dei numeri di output
- ASF (Advanced Systems Format), numeri di output e formati
- ASF (formato avanzato dei sistemi), numeri e formati di output
- numeri e formati di output, identificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c08f8e9a49d672efe7c04ecdde11ca4ef297d552
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299401"
---
# <a name="to-identify-output-numbers"></a>Per identificare i numeri di output

Per identificare i numeri di output per un file caricato, seguire questa procedura. Queste procedure sono identiche sia per il lettore asincrono che per il lettore sincrono. Laddove i nomi di interfaccia variano, i metodi di lettura sincrona sono elencati tra parentesi dopo i metodi del lettore asincrono.

1.  Creare un oggetto Reader e caricare un file per la lettura. Per ulteriori informazioni, vedere [per creare un reader e aprire un file](to-create-a-reader-and-open-a-file.md) (o [per creare un reader sincrono e aprire un file](to-create-a-synchronous-reader-and-open-a-file.md)).
2.  Recuperare il numero totale di output per il file chiamando [**IWMReader:: GetOutputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputcount) (o [**IWMSyncReader:: GetOutputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputcount)).
3.  Scorrere gli output uno alla volta, eseguendo i passaggi seguenti per ognuno di essi:
    -   Recuperare l'interfaccia [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) per l'output corrente con una chiamata a [**IWMReader:: GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) o [**IWMSyncReader:: GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputprops).
    -   Recuperare la struttura del [**\_ \_ tipo di supporto WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) per l'output effettuando due chiamate a [**IWMMediaProps:: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype). Eseguire la prima chiamata per ottenere la dimensione della struttura, quindi allocare la memoria per l'oggetto e passare un puntatore alla memoria allocata alla seconda chiamata. In alternativa, è possibile chiamare [**IWMMediaProps:: GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-gettype), che fornisce il tipo principale senza che sia necessario allocare memoria per la struttura del **\_ \_ tipo di supporto WM** . È possibile ignorare gli output del tipo principale errato.
    -   Recuperare il tipo di supporto principale e il sottotipo di supporto dalla struttura del **\_ \_ tipo di supporto WM** . Questi valori vengono archiviati rispettivamente nei membri dati **majortype** e **sottotipo** .
    -   Controllare il valore di **WM \_ media \_ Type. formatType**. Consente di specificare il tipo di struttura contenuto nel buffer in **WM \_ media \_ Type. pbFormat**. Per ulteriori informazioni sui tipi di formato, vedere [tipi di supporto](media-types.md).
    -   Allocare memoria per conservare la struttura del tipo identificato nel passaggio precedente. Copiare la struttura nella memoria allocata. Per audio e video, questa struttura fornisce informazioni essenziali sulla modalità di rendering dei dati.

Il lettore sincrono fornisce anche metodi per recuperare le associazioni tra i numeri di output e i numeri di flusso. Per ulteriori informazioni, vedere [per trovare i numeri di flusso e i numeri di output](to-find-stream-numbers-and-output-numbers.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Input, flussi e output**](inputs-streams-and-outputs.md)
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

 

 




