---
description: Configurazione del codec DMOs
ms.assetid: 431b33f1-ceb0-4f1b-a9f2-72e88b63f973
title: Configurazione del codec DMOs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 564c0e6c566d9f583a495238f3ea6f0716d7adde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484084"
---
# <a name="configuring-codec-dmos"></a>Configurazione del codec DMOs

Questo argomento descrive il processo di configurazione del codec DMOs. Ogni codec ha procedure specifiche, ma le informazioni comuni a tutte sono descritte qui.

## <a name="configuring-dmo-inputs-and-outputs"></a>Configurazione di input e output DMO

Ogni DMO supporta tipi di input e output specifici. È possibile recuperare i tipi supportati per gli input e gli output chiamando [**IMediaObject:: GetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype) per gli input e [**IMediaObject:: GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype) per gli output. È possibile enumerare i formati supportati effettuando chiamate ripetute a uno dei metodi, incrementando l'indice del tipo con ogni chiamata. Quando l'indice supera quello del tipo supportato finale, la chiamata restituisce DMO \_ E \_ non \_ più \_ elementi.

Per i codec video, viene enumerato solo un tipo di output o un tipo di input per un sottotipo di supporto specifico. Per i codec audio, ogni singolo tipo supportato viene enumerato. Per ulteriori informazioni sui tipi supportati per i singoli codec, vedere [utilizzo di audio](workingwithaudio.md) e [utilizzo di video](workingwithvideo.md).

Dopo aver configurato i tipi di supporto per i flussi di input e di output, impostarli chiamando [**IMediaObject:: SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) e [**IMediaObject:: SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) rispettivamente. Entrambi questi metodi restituiscono **DMO \_ E \_ Type \_ non \_ accettati** se il tipo specificato non è valido.

## <a name="configuring-the-codec-dmos-for-encoding"></a>Configurazione del codec DMOs per la codifica

Tutti i codec Windows Media Audio e video supportano un'ampia gamma di funzionalità di codifica. Queste funzionalità vengono in genere configurate impostando le proprietà di DMO usando i metodi dell'interfaccia **IPropertyBag** . Alcune proprietà vengono configurate utilizzando interfacce di codec specializzate. Queste interfacce sono elencate per ogni codec nella sezione [oggetti codec](codecobjects.md).

L'ordine generale delle operazioni per la configurazione di una DMO di codifica è il seguente:

1.  Configurare le funzionalità di codec come desiderato usando i metodi di **IPropertyBag**.
2.  Usare le interfacce codec DMO per configurare le funzionalità aggiuntive, se necessario.
3.  Configurare i tipi di input e di output. L'ordine in cui devono essere configurati i tipi varia per i singoli codec. Per ulteriori informazioni, vedere [utilizzo di audio](workingwithaudio.md) e [utilizzo di video](workingwithvideo.md).

## <a name="configuring-the-codec-dmos-for-decoding"></a>Configurazione del codec DMOs per la decodifica

La decodifica è più semplice della codifica, in quanto sono supportate meno funzionalità di decodificatore.

L'ordine generale delle operazioni per la configurazione di un DMO di decodifica è il seguente:

1.  Configurare le funzionalità del decodificatore come desiderato usando i metodi di **IPropertyBag**.
2.  Impostare il tipo di input sul tipo usato per l'output del codificatore.
3.  Configurare il tipo di output. I tipi di output supportati sono diversi per gli input diversi.

> [!Note]  
> È importante usare lo stesso tipo di supporto per l'input del decodificatore usato per l'output del codificatore. Ciò è dovuto al fatto che i codec Windows Media Audio e video usano formati multimediali con dati aggiuntivi. Questi dati vengono aggiunti alla struttura a cui punta il membro **pbFormat** della struttura del [**tipo di \_ supporto \_ DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) (in genere [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) o [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))). Per alcuni tipi i dati aggiuntivi fanno parte del tipo di output del codificatore enumerato. Per altri tipi è necessario aggiungere manualmente questi dati. Senza i dati di formato esteso, non è possibile decodificare il contenuto compresso.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di codec DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 
