---
title: Assegnazione di formati di output
description: Assegnazione di formati di output
ms.assetid: 47697ffb-51cb-44cd-a0b0-7d85625a38f9
keywords:
- Windows Media Format SDK, assegnazione di formati di output
- Formato di sistemi avanzati (ASF), assegnazione di formati di output
- ASF (Advanced Systems Format), assegnazione di formati di output
- ASF (Advanced Systems Format), numeri di output e formati
- ASF (formato avanzato dei sistemi), numeri e formati di output
- numeri e formati di output, assegnazione
- codec, numeri di output e formati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633673053a2b34a2f7aed5ed3f6ae66457a7ee13
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/21/2020
ms.locfileid: "106299506"
---
# <a name="assigning-output-formats"></a>Assegnazione di formati di output

Alcuni codec possono decomprimere i dati multimediali digitali in diversi formati non compressi. È possibile trovare tutti i formati supportati per un output specifico usando il Reader asincrono o il lettore sincrono.

Per esaminare tutti i formati disponibili per un output, seguire questa procedura. Queste procedure sono identiche sia per il lettore asincrono che per il lettore sincrono. Laddove i nomi di interfaccia variano, i metodi di lettura sincrona sono elencati tra parentesi dopo i metodi del lettore asincrono.

1.  Creare un oggetto Reader e caricare un file per la lettura. Per ulteriori informazioni, vedere [per creare un reader e aprire un file](to-create-a-reader-and-open-a-file.md) (o [per creare un reader sincrono e aprire un file](to-create-a-synchronous-reader-and-open-a-file.md)).
2.  Determinare l'output per il quale si desidera trovare i formati disponibili. Se non si conosce già l'output che si desidera utilizzare, è possibile identificare gli output nel file utilizzando le procedure descritte in [per identificare i numeri di output](to-identify-output-numbers.md).
3.  Recuperare il numero totale di formati disponibili per l'output desiderato chiamando [**IWMReader:: GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) (o [**IWMSyncReader:: GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformatcount)).
4.  Scorrere i formati disponibili uno alla volta, eseguendo i passaggi seguenti per ognuno di essi:
    -   Recuperare l'interfaccia [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) per il formato di output corrente chiamando [**IWMReader:: GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) o [**IWMSyncReader:: GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformat).
    -   Recuperare la struttura del [**\_ \_ tipo di supporto WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) per il formato di output effettuando due chiamate a [**IWMMediaProps:: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype). Eseguire la prima chiamata per ottenere la dimensione della struttura, quindi allocare la memoria per l'oggetto e passare un puntatore alla memoria allocata alla seconda chiamata.
    -   Trovare il sottotipo di supporto del formato di output in **WM \_ media \_ Type. sottotipo**.
    -   Per video, se il sottotipo corrente è il formato che si vuole usare per l'output, interrompere il ciclo. In caso contrario, passare all'iterazione successiva.

        Per l'audio, è necessario controllare i valori nella struttura **WAVEFORMATEX** in base ai requisiti. **WM \_ MEDIA \_ Type. pbFormat** punta alla struttura **WAVEFORMATEX** per gli output audio.

5.  Dopo aver individuato l'output desiderato, impostarlo per l'uso con il lettore chiamando [**IWMReader:: SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) (o [**IWMSyncReader:: SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputprops)). È necessario passare un puntatore all'interfaccia **IWMOutputMediaProps** ottenuta nel primo passaggio del ciclo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

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

 

 




