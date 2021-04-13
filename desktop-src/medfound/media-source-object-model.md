---
description: Modello a oggetti di origine multimediale
ms.assetid: 88373028-8a34-4bf1-8300-d1a7e4c7dd75
title: Modello a oggetti di origine multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0d05cc9d5341bff433d6276b5ee67505361b78f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351531"
---
# <a name="media-source-object-model"></a>Modello a oggetti di origine multimediale

Questo argomento descrive il modello a oggetti per le origini multimediali in Microsoft Media Foundation. Un'origine multimediale deve implementare due oggetti:

-   Descrittore di presentazione che descrive il contenuto dell'origine, inclusi il numero di flussi e il formato di ogni flusso. Per ulteriori informazioni sui descrittori di presentazione, vedere [descrittori di presentazione](presentation-descriptors.md).
-   Uno o più flussi multimediali, che generano i dati di origine.

L'origine non crea i flussi fino a quando non viene avviata la riproduzione.

## <a name="media-source-interfaces"></a>Interfacce di origine dei supporti

Un'origine multimediale deve esporre le interfacce seguenti tramite **QueryInterface**.



| Interfaccia                                                | Descrizione                                                                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                 | Obbligatorio per tutte le origini supporti.                                                                                 |
| [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | Obbligatorio per tutte le origini supporti. L'interfaccia [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) eredita questa interfaccia. |



 

Facoltativamente, un'origine multimediale può implementare l'interfaccia [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) e implementare una delle interfacce seguenti come servizi:



| Interfaccia del servizio                                  | Descrizione                                                       |
|----------------------------------------------------|-------------------------------------------------------------------|
| [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)           | Controlla la velocità di riproduzione.                                       |
| [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)           | Segnala l'intervallo di frequenze di riproduzione supportate.           |
| [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)       | Consente al gestore della qualità di regolare la qualità audio o video. |
| [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) | Fornisce i metadati.                                                |



 

Se l'origine supporto può essere riprodotto a frequenze diverse dalla velocità normale (1,0), deve esporre il servizio di controllo della velocità ([**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) e [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)). In caso contrario, si presuppone che l'origine supporti solo la riproduzione alla velocità normale. Per ulteriori informazioni, vedere [implementazione del controllo della frequenza](implementing-rate-control.md).

Per ulteriori informazioni sulle interfacce del servizio e [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice), vedere [interfacce di servizio](service-interfaces.md).

## <a name="media-stream-interfaces"></a>Interfacce del flusso multimediale

I flussi multimediali devono implementare le interfacce seguenti.



| Interfaccia                                                | Descrizione                                                                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)                 | Obbligatorio per tutti i flussi multimediali.                                                                                 |
| [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | Obbligatorio per tutti i flussi multimediali. L'interfaccia [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) eredita questa interfaccia. |



 

Attualmente non sono definite interfacce del servizio per flussi multimediali.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Origini supporti](media-sources.md)
</dt> </dl>

 

 



