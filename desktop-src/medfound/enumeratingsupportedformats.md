---
description: Configurazione degli oggetti DMO codec
ms.assetid: 431b33f1-ceb0-4f1b-a9f2-72e88b63f973
title: Configurazione degli oggetti DMO codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4040c0a16c0311d14b0553336e1d9b70a7a6c1fd28a0f01277c955eea55ec7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958331"
---
# <a name="configuring-codec-dmos"></a>Configurazione degli oggetti DMO codec

Questo argomento descrive il processo di configurazione degli oggetti DMO del codec. Ogni codec ha procedure specifiche, ma le informazioni comuni a tutti sono descritte qui.

## <a name="configuring-dmo-inputs-and-outputs"></a>Configurazione DMO input e output

Ogni DMO supporta tipi di input e output specifici. È possibile recuperare i tipi supportati per input e output chiamando [**IMediaObject::GetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype) per gli input e [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype) per gli output. È possibile enumerare i formati supportati effettuando chiamate ripetute a uno dei due metodi, incrementando l'indice del tipo con ogni chiamata. Quando l'indice supera quello del tipo supportato finale, la chiamata restituisce DMO \_ E \_ NO MORE \_ \_ ITEMS.

Per i codec video, viene enumerato un solo tipo di output o di input per un determinato sottotipo multimediale. Per i codec audio, viene enumerato ogni singolo tipo supportato. Per altre informazioni sui tipi supportati per i singoli codec, vedere [Uso dell'audio](workingwithaudio.md) e [Uso di video.](workingwithvideo.md)

Dopo aver configurato i tipi di supporti per i flussi di input e output, impostarli chiamando [**rispettivamente IMediaObject::SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) e [**IMediaObject::SetOutputType.**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) Entrambi questi metodi restituiscono **DMO E TYPE NOT \_ \_ \_ \_ ACCEPTED** se il tipo specificato non è valido.

## <a name="configuring-the-codec-dmos-for-encoding"></a>Configurazione dei DMO codec per la codifica

Tutti i codec Windows audio e video supportano un'ampia gamma di funzionalità di codifica. Queste funzionalità vengono in genere configurate impostando le proprietà DMO usando i metodi **dell'interfaccia IPropertyBag.** Alcune proprietà vengono configurate usando interfacce codec specializzate. Queste interfacce sono elencate per ogni codec nella sezione [Oggetti codec](codecobjects.md).

L'ordine generale delle operazioni per la configurazione di un DMO codifica è il seguente:

1.  Configurare le funzionalità del codec in base alle esigenze usando i metodi **di IPropertyBag.**
2.  Usare le interfacce DMO codec per configurare funzionalità aggiuntive, se necessario.
3.  Configurare i tipi di input e output. L'ordine in cui devono essere configurati i tipi varia per i singoli codec. Per altre informazioni, vedere [Working with Audio (Uso dell'audio)](workingwithaudio.md) [e Working with Video (Uso di video).](workingwithvideo.md)

## <a name="configuring-the-codec-dmos-for-decoding"></a>Configurazione dei DMO codec per la decodifica

La decodifica è più semplice della codifica, poiché sono supportate meno funzionalità del decodificatore.

L'ordine generale delle operazioni per la configurazione di un DMO decodifica è il seguente:

1.  Configurare le funzionalità del decodificatore in base alle esigenze usando i metodi **di IPropertyBag.**
2.  Impostare il tipo di input sul tipo usato per l'output del codificatore.
3.  Configurare il tipo di output. I tipi di output supportati sono diversi per input diversi.

> [!Note]  
> È importante usare lo stesso tipo di supporto per l'input del decodificatore usato per l'output del codificatore. Ciò è dovuto al fatto che Windows codec Audio e Video multimediali usano formati multimediali con dati aggiuntivi. Questi dati vengono aggiunti alla struttura a cui punta il membro **pbFormat** della [**struttura DMO MEDIA \_ \_ TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) (in genere [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) o [**WAVEFORMATEX).**](/previous-versions/dd757713(v=vs.85)) Per alcuni tipi, i dati aggiuntivi fanno parte del tipo di output del codificatore enumerato. Altri tipi richiedono l'aggiunta manuale di questi dati. Senza i dati in formato esteso, non è possibile decodificare il contenuto compresso.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso degli oggetti DMO codec](workingwithcodecdmos.md)
</dt> </dl>

 

 
