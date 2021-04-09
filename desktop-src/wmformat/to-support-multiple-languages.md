---
title: Per supportare più lingue
description: Per supportare più lingue
ms.assetid: b0061de4-d725-455f-9d9b-5bd0dbe8ff53
keywords:
- Windows Media Format SDK, supporto per più lingue
- Windows Media Format SDK, supporto per più lingue
- Windows Media Format SDK, supporto del linguaggio
- Advanced Systems Format (ASF), supporto per più lingue
- ASF (Advanced Systems Format), supporto per più lingue
- Advanced Systems Format (ASF), supporto per più lingue
- ASF (Advanced Systems Format), supporto per più lingue
- ASF (Advanced Systems Format), supporto per le lingue
- ASF (formato avanzato dei sistemi), supporto per le lingue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc070bda1cc25c6b7fd0fa583a8ac63a55fa603
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "103956264"
---
# <a name="to-support-multiple-languages"></a>Per supportare più lingue

È possibile supportare più lingue sia nei flussi che nei metadati. Il nucleo del supporto di più lingue in Windows Media Format SDK è l'interfaccia [**IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) , che mantiene un elenco delle lingue supportate. L'elenco di lingue fornisce a ogni lingua supportata un indice, che viene usato in vari oggetti nell'SDK quando si gestiscono più lingue.

Il metodo [**IWMLanguageList:: AddLanguageByRFC1766String**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-addlanguagebyrfc1766string) aggiunge un linguaggio all'elenco. È possibile identificare le lingue già presenti nell'elenco ottenendo il numero totale di lingue con [**IWMLanguageList:: GetLanguageCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagecount) e quindi scorrendo le lingue che chiamano [**IWMLanguageList:: GetLanguageDetails**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagedetails) per ciascuna. L'indice del linguaggio è in base zero.

## <a name="to-configure-mutual-exclusion-by-language"></a>Per configurare l'esclusione reciproca per lingua

La configurazione di un semplice oggetto di esclusione reciproca per lingua è molto semplice. Ogni flusso è ora associato a una lingua. Il linguaggio associato a un flusso può essere impostato usando [**IWMStreamConfig3:: tolanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig3-setlanguage). Una volta configurati tutti i flussi che si escludono a vicenda, è sufficiente creare un oggetto di esclusione reciproca come per qualsiasi altro tipo. Chiamare quindi [**IWMMutualExclusion:: seTYPE**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) passando \_ \_ la lingua WMMUTEX CLSID per il tipo.

I flussi che si escludono a vicenda dalla lingua diventano più complessi quando i flussi esclusivi si escludono a vicenda anche per velocità in bit. In questo caso è necessario usare record che si escludono a vicenda, eseguendo i passaggi seguenti:

1.  Creare un oggetto di esclusione reciproca per i flussi di velocità in bit diverse in ogni lingua. Per ulteriori informazioni sulla creazione di un oggetto di esclusione reciproca per velocità in bit, vedere [utilizzo dell'esclusione reciproca a più bit rate](using-multiple-bit-rate-mutual-exclusion.md).
2.  Creare un oggetto di esclusione reciproca. Chiamare [**IWMMutualExclusion:: seTYPE**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) e pass CLSID \_ WMMUTEX \_ Language per specificare l'esclusività in base alla lingua.
3.  Ottenere un puntatore all'interfaccia [**IWMMutualExclusion2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2) dell'oggetto di esclusione reciproca creato nel passaggio 2 chiamando il metodo **QueryInterface** di [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion).
4.  Chiamare il metodo [**IWMMutualExclusion2:: AddRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addrecord) una volta per ogni lingua, per creare record di flusso che si escludono a vicenda.
5.  Per ogni record creato nel passaggio 4, aggiungere i flussi della lingua appropriata con le chiamate a [**IWMMutualExclusion2:: AddStreamForRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addstreamforrecord).

## <a name="to-read-files-with-multiple-languages"></a>Per leggere file con più lingue

L'oggetto Reader fornisce metodi per identificare le lingue disponibili dei flussi in un file. È possibile recuperare il numero di lingue supportate per un output chiamando [**IWMReaderAdvanced4:: GetLanguageCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguagecount). È quindi possibile recuperare i dettagli relativi a ogni lingua con le chiamate a [**IWMReaderAdvanced4:: GetLanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguage).

È possibile specificare la lingua da riprodurre passando l'indice di tale lingua al Reader con una chiamata a [**IWMReaderAdvanced2:: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting). Verrà selezionata la lingua specificata mantenendo la selezione automatica dei flussi per tutti gli altri oggetti di esclusione reciproca del file.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Argomenti avanzati**](advanced-topics.md)
</dt> <dt>

[**Interfaccia IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist)
</dt> <dt>

[**Interfaccia IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)
</dt> <dt>

[**Interfaccia IWMMutualExclusion2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2)
</dt> <dt>

[**Interfaccia IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[**Interfaccia IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)
</dt> <dt>

[**Interfaccia IWMStreamConfig3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3)
</dt> </dl>

 

 




