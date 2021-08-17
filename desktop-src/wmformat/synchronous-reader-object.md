---
title: Oggetto lettore sincrono
description: Oggetto lettore sincrono
ms.assetid: 52a4891f-03bf-4d8a-ab7b-e9739db30bc3
keywords:
- Windows Media Format SDK, oggetti lettore sincrono
- Advanced Systems Format (ASF), oggetti lettore sincrono
- ASF (Advanced Systems Format), oggetti lettore sincrono
- oggetti, oggetti reader sincroni
- lettori sincroni,oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 629f08684f996a611acaf00b913eaa8715869bdfd0219ea27994e2f8faf7c896
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197061"
---
# <a name="synchronous-reader-object"></a>Oggetto lettore sincrono

L'oggetto lettore sincrono viene usato per leggere i file multimediali digitali tramite chiamate sincrone.

L'oggetto lettore sincrono viene creato dalla funzione [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader), che imposta un puntatore a **un'interfaccia IWMSyncReader.** Le altre interfacce supportate dall'interfaccia del lettore sincrono possono essere ottenute chiamando il **metodo QueryInterface.**

Le interfacce seguenti sono supportate dall'oggetto reader sincrono.



| Interfaccia                                | Descrizione                                                                                                                                                        |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)   | Imposta e recupera informazioni sull'intestazione, ad esempio metadati, [*marcatori*](wmformat-glossary.md)e così via.                                            |
| [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) | Enumera le informazioni sul codec disponibili. Eredita tutti i metodi di **IWMHeaderInfo.**                                                                      |
| [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) | Supporta attributi di grandi dimensioni, nomi di attributi duplicati e supporto per più lingue. Eredita tutti i metodi di **IWMHeaderInfo e** **IWMHeaderInfo2.** |
| [**IWMProfile**](iwmprofile.md)         | Fornisce l'accesso alle informazioni sul profilo del Windows file multimediale caricato nel lettore.                                                                       |
| [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)       | Recupera l'identificatore univoco globale (GUID), se presente, associato al profilo. Eredita tutti i metodi di **IWMProfile.**                               |
| [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)       | Supporta la condivisione della larghezza di banda e le informazioni di definizione delle priorità del flusso nel profilo. Eredita tutti i metodi di **IWMProfile** e **IWMProfile2.**                |
| [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)   | Fornisce funzionalità di lettura sincrona per i file multimediali digitali.                                                                                                 |
| [**IWMSyncReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader2) | Fornisce il supporto per la ricerca di codici temporità SMPTE e per l'allocazione manuale dei campioni. Eredita tutti i metodi di **IWMSyncReader.**                            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Oggetti**](objects.md)
</dt> <dt>

[**Oggetto Lettore**](reader-object.md)
</dt> <dt>

[**Lettura di file con il lettore sincrono**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




