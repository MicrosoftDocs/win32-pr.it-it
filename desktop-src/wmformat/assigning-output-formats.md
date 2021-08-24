---
title: Assegnazione di formati di output
description: Assegnazione di formati di output
ms.assetid: 47697ffb-51cb-44cd-a0b0-7d85625a38f9
keywords:
- Windows Media Format SDK, assegnazione di formati di output
- Advanced Systems Format (ASF), assegnazione di formati di output
- ASF (Advanced Systems Format), assegnazione di formati di output
- Advanced Systems Format (ASF), numeri di output e formati
- ASF (Advanced Systems Format), numeri di output e formati
- numeri di output e formati, assegnazione
- codec, numeri di output e formati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80672419a032b2fff779259ffc6dcebfbe9e9a569f9d4b7afbb75ae5a84fac2c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659371"
---
# <a name="assigning-output-formats"></a>Assegnazione di formati di output

Alcuni codec possono decomprimere i dati multimediali digitali in diversi formati non compressi. È possibile trovare tutti i formati supportati per un output specifico usando il lettore asincrono o il lettore sincrono.

Per esaminare tutti i formati disponibili per un output, seguire questa procedura. Queste procedure sono identiche sia per il lettore asincrono che per il lettore sincrono. Se i nomi delle interfacce variano, i metodi del reader sincrono sono elencati tra parentesi dopo i metodi del lettore asincrono.

1.  Creare un oggetto lettore e caricare un file per la lettura. Per altre informazioni, vedere Per creare un lettore [e aprire un file](to-create-a-reader-and-open-a-file.md) (o Per creare un lettore [sincrono e aprire un file).](to-create-a-synchronous-reader-and-open-a-file.md)
2.  Determinare l'output per il quale si desidera trovare i formati disponibili. Se non si conosce già l'output da usare, è possibile identificare gli output nel file usando le procedure descritte in Per identificare [i numeri di output](to-identify-output-numbers.md).
3.  Recuperare il numero totale di formati disponibili per l'output desiderato chiamando [**IWMReader::GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) (o [**IWMSyncReader::GetOutputFormatCount).**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformatcount)
4.  Scorrere i formati disponibili uno alla volta, eseguendo i passaggi seguenti per ognuno:
    -   Recuperare [**l'interfaccia IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) per il formato di output corrente chiamando [**IWMReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) (o [**IWMSyncReader::GetOutputFormat).**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformat)
    -   Recuperare la [**struttura \_ WM MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) per il formato di output effettuando due chiamate a [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype). Eseguire la prima chiamata per ottenere le dimensioni della struttura , quindi allocare memoria per la struttura e passare un puntatore alla memoria allocata nella seconda chiamata.
    -   Trovare il sottotipo multimediale del formato di output in **WM \_ MEDIA \_ TYPE.subtype**.
    -   Per il video, se il sottotipo corrente è il formato che si vuole usare per l'output, interrompere il ciclo. In caso contrario, passare all'iterazione successiva.

        Per l'audio, è necessario controllare i valori nella **struttura WAVEFORMATEX** in base alle esigenze. **WM \_ MEDIA \_ TYPE.pbFormat punta** alla struttura **WAVEFORMATEX** per gli output audio.

5.  Dopo aver trovato l'output desiderato, impostarlo per l'uso con il lettore chiamando [**IWMReader::SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) (o [**IWMSyncReader::SetOutputProps).**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputprops) È necessario passare un puntatore **all'interfaccia IWMOutputMediaProps** ottenuta nel primo passaggio del ciclo.

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

 

 




