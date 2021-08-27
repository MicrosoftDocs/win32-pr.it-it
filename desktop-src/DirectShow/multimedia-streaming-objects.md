---
description: Oggetti di streaming multimediali
ms.assetid: 4f5460db-2670-41af-a57f-20cf706827e6
title: Oggetti di streaming multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bfefd7d16c832dc168204df771ff8f925bec3f1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471947"
---
# <a name="multimedia-streaming-objects"></a>Oggetti di streaming multimediali

> [!Note]  
> Questa API è deprecata. Le nuove applicazioni non devono usarlo.

 

Nella tabella seguente vengono descritti gli oggetti di streaming multimediale.




| CLSID | Descrizione | Interfacce supportate | 
|-------|-------------|----------------------|
| CLSID_AMMediaTypeStream | Può creare esempi multimediali per qualsiasi DirectShow di dati supportato | <ul><li><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>IAMMediaStream</strong></a></li><li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>IMediaStream</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li></ul> | 
| CLSID_AMAudioData | Implementazione <a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>dell'oggetto contenitore audio IAudioData.</strong></a> | <ul><li><a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>IAudioData</strong></a></li></ul> | 
| CLSID_AMDirectDrawStream | Flusso multimediale DirectDraw che può essere aggiunto a un DirectShow multimediale. | <ul><li><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>IAMMediaStream</strong></a></li><li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>IMediaStream</strong></a></li><li><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream"><strong>IDirectDrawMediaStream</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li></ul> | 
| CLSID_AMMultiMediaStream | DirectShow'implementazione del flusso multimediale. | <ul><li><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>IAMMultiMediaStream</strong></a></li><li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream"><strong>IMultiMediaStream</strong></a></li></ul> | 
| CLSID_MediaStreamFilter | Fornisce funzionalità di streaming multimediale per CLSID_AMMultiMediaStream'oggetto tramite <a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>l'interfaccia IAMMultiMediaStream.</strong></a> | <ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></li></ul> | 
| N/A | Esempi creati dall'oggetto CLSID_AMMediaTypeStream. | <ul><li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>IStreamSample</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>IMediaSample</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample2"><strong>IMediaSample2</strong></a></li></ul> | 
| N/A | Esempi creati dal flusso DirectDraw. | <ul><li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>IStreamSample</strong></a></li><li><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample"><strong>IDirectDrawStreamSample</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>IMediaSample</strong></a></li></ul> | 




 

 

 



