---
title: Per supportare più lingue
description: Per supportare più lingue
ms.assetid: b0061de4-d725-455f-9d9b-5bd0dbe8ff53
keywords:
- Windows Media Format SDK, supporto di più lingue
- Windows Media Format SDK, supporto per più lingue
- Windows MEDIA Format SDK, supporto del linguaggio
- Advanced Systems Format (ASF), che supporta più lingue
- ASF (Advanced Systems Format), supporto di più lingue
- Advanced Systems Format (ASF), supporto per più lingue
- ASF (Advanced Systems Format), supporto per più lingue
- Advanced Systems Format (ASF), supporto della lingua
- ASF (Advanced Systems Format),supporto della lingua
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa610d5a9b0c92fb205ecdc234a18d816190223b5bca843a542e7222695fa24f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699102"
---
# <a name="to-support-multiple-languages"></a>Per supportare più lingue

È possibile supportare più linguaggi sia nei flussi che nei metadati. Il nucleo del supporto per più lingue in Windows Media Format SDK è [**l'interfaccia IWMLanguageList,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) che gestisce un elenco delle lingue supportate. L'elenco delle lingue fornisce a ogni lingua supportata un indice, che viene usato in vari oggetti nell'SDK quando si gestiscono più lingue.

Il [**metodo IWMLanguageList::AddLanguageByRFC1766String**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-addlanguagebyrfc1766string) aggiunge una lingua all'elenco. È possibile identificare le lingue già presenti nell'elenco ottenendo il numero totale di lingue con [**IWMLanguageList::GetLanguageCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagecount) e quindi scorrendo le lingue che chiamano [**IWMLanguageList::GetLanguageDetails**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagedetails) per ognuna. L'indice della lingua è in base zero.

## <a name="to-configure-mutual-exclusion-by-language"></a>Per configurare l'esclusione reciproca in base alla lingua

La configurazione di un semplice oggetto di esclusione reciproca in base al linguaggio è molto semplice. Ogni flusso è ora associato a un linguaggio. La lingua associata a un flusso può essere impostata [**usando IWMStreamConfig3::SetLanguage.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig3-setlanguage) Dopo aver configurato tutti i flussi che si escludono a vicenda, è sufficiente creare un oggetto di esclusione reciproca come per qualsiasi altro tipo. Chiamare quindi [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) passando clsID \_ WMMUTEX \_ Language per il tipo.

Flussi che si escludono a vicenda in base al linguaggio diventano più complicate quando anche i flussi esclusivi si escludono a vicenda in base alla velocità in bit. In questo caso è necessario usare record che si escludono a vicenda, seguendo questa procedura:

1.  Creare un oggetto di esclusione reciproca per i flussi di velocità in bit diverse in ogni linguaggio. Per altre informazioni sulla creazione di un oggetto di esclusione reciproca in base alla velocità in bit, vedere [Using Multiple Bit Rate Mutual Exclusion](using-multiple-bit-rate-mutual-exclusion.md).
2.  Creare un oggetto di esclusione reciproca. Chiamare [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) e passare il linguaggio WMMUTEX CLSID per specificare \_ \_ l'esclusività in base al linguaggio.
3.  Ottenere un puntatore [**all'interfaccia IWMMutualExclusion2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2) dell'oggetto di esclusione reciproca creato nel passaggio 2 chiamando il metodo **QueryInterface** di [**IWMMutualExclusion.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)
4.  Chiamare il [**metodo IWMMutualExclusion2::AddRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addrecord) una volta per ogni lingua, per creare record di flusso che si escludono a vicenda.
5.  Per ogni record creato nel passaggio 4, aggiungere i flussi della lingua appropriata con chiamate a [**IWMMutualExclusion2::AddStreamForRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addstreamforrecord).

## <a name="to-read-files-with-multiple-languages"></a>Per leggere file con più lingue

L'oggetto reader fornisce metodi per identificare le lingue disponibili dei flussi in un file. È possibile recuperare il numero di lingue supportate per un output chiamando [**IWMReaderAdvanced4::GetLanguageCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguagecount). È quindi possibile recuperare i dettagli su ogni lingua con chiamate a [**IWMReaderAdvanced4::GetLanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguage).

È possibile specificare la lingua da riprodurre passando l'indice della lingua al lettore con una chiamata a [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting). Verrà selezionata la lingua specificata mantenendo la selezione automatica del flusso per qualsiasi altro oggetto di esclusione reciproca nel file.

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

 

 




