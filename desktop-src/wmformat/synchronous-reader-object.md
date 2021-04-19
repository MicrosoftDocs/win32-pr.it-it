---
title: Oggetto lettore sincrono
description: Oggetto lettore sincrono
ms.assetid: 52a4891f-03bf-4d8a-ab7b-e9739db30bc3
keywords:
- Windows Media Format SDK, oggetti Reader sincroni
- ASF (Advanced Systems Format), oggetti Reader sincroni
- ASF (Advanced Systems Format), oggetti Reader sincroni
- oggetti, oggetti Reader sincroni
- lettori sincroni, oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 491fed915a049dbfc52acc24d06a0344d8e3109c
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "106299516"
---
# <a name="synchronous-reader-object"></a>Oggetto lettore sincrono

L'oggetto Reader sincrono viene usato per leggere i file multimediali digitali usando chiamate sincrone.

L'oggetto Reader sincrono viene creato dalla funzione [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader), che imposta un puntatore a un'interfaccia **IWMSyncReader** . Le altre interfacce supportate dall'interfaccia di lettura sincrona possono essere ottenute chiamando il metodo **QueryInterface** .

Le interfacce seguenti sono supportate dall'oggetto Reader sincrono.



| Interfaccia                                | Descrizione                                                                                                                                                        |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)   | Imposta e recupera le informazioni di intestazione, ad esempio i metadati, i [*marcatori*](wmformat-glossary.md)e così via.                                            |
| [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) | Enumera le informazioni sui codec disponibili. Eredita tutti i metodi di **IWMHeaderInfo**.                                                                      |
| [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) | Supporta le dimensioni degli attributi grandi, i nomi di attributi duplicati e il supporto di più lingue. Eredita tutti i metodi di **IWMHeaderInfo** e **IWMHeaderInfo2**. |
| [**IWMProfile**](iwmprofile.md)         | Consente di accedere alle informazioni sul profilo del file Windows Media caricato nel lettore.                                                                       |
| [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)       | Recupera l'identificatore univoco globale (GUID), se presente, associato al profilo. Eredita tutti i metodi di **IWMProfile**.                               |
| [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)       | Supporta la condivisione della larghezza di banda e le informazioni relative alla priorità del flusso nel profilo. Eredita tutti i metodi di **IWMProfile** e **IWMProfile2**.                |
| [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)   | Fornisce funzionalità di lettura sincrona per i file multimediali digitali.                                                                                                 |
| [**IWMSyncReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader2) | Fornisce supporto per la ricerca di codici temporali SMPTE e per l'allocazione manuale di campioni. Eredita tutti i metodi di **IWMSyncReader**.                            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Oggetti**](objects.md)
</dt> <dt>

[**Oggetto Lettore**](reader-object.md)
</dt> <dt>

[**Lettura di file con il lettore sincrono**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




