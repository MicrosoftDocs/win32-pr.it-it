---
title: Per eseguire ricerche in base al tempo tramite il Reader asincrono
description: Per eseguire ricerche in base al tempo tramite il Reader asincrono
ms.assetid: 731b0a6e-1472-45a7-998c-e395be86036f
keywords:
- Formato Advanced Systems (ASF), ricerca per ora
- ASF (Advanced Systems Format), ricerca per ora
- ASF (Advanced Systems Format), Reader asincroni
- ASF (formato avanzato dei sistemi), Reader asincroni
- lettori asincroni, ricerca per ora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f3e24c04d75d762aef6bac498d4b4c8dfa9552
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723566"
---
# <a name="to-seek-by-time-using-the-asynchronous-reader"></a>Per eseguire ricerche in base al tempo tramite il Reader asincrono

Se si desidera eseguire la ricerca di un'ora di presentazione specifica in un file ASF, il file deve essere configurato correttamente. Per impostazione predefinita, è possibile cercare solo nei file audio, ma è necessario indicizzare i file video prima di cercare. Se non si è certi della modalità di creazione di un file, è possibile controllare l' \_ attributo g wszWMSeekable nell'intestazione del file chiamando [**IWMHeaderInfo:: GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).

Per cercare i dati in un file ASF in base all'ora di presentazione utilizzando il lettore asincrono, chiamare [**IWMReader:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start), passando il tempo e la durata desiderati della parte del file che si desidera leggere rispettivamente come *cnsStart* e *cnsDuration* .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Lettura di file con il lettore asincrono**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Lettura dei metadati durante la riproduzione**](reading-metadata-at-playback.md)
</dt> <dt>

[**Operazioni con gli indici**](working-with-indexes.md)
</dt> </dl>

 

 




