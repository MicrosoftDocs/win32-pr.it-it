---
description: Nozioni fondamentali su DMO
ms.assetid: eaf453d2-69f8-432a-8a58-1ed70778f182
title: Nozioni di base su DMO (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b1aca2fcd7e70cf78e2e95135aee73c454b910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225806"
---
# <a name="dmo-basics-microsoft-media-foundation"></a>Nozioni di base su DMO (Microsoft Media Foundation)

In questo argomento viene fornita una breve panoramica di DMOs in relazione ai codec Windows Media. Per altre informazioni su DMOs, vedere [oggetti multimediali DirectX](../directshow/directx-media-objects.md).

Un DMO è un oggetto COM che trasforma i dati. I dati vengono passati e vengono restituiti i dati trasformati. Nel caso di un codec Encoder DMO, è possibile inserire dati multimediali non compressi e DMO recapita dati multimediali compressi. Il vantaggio principale dell'utilizzo di DMOs consiste nel fatto che tutti implementano la stessa interfaccia di base, [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject), che semplifica l'utilizzo di tali interfacce, in quanto è possibile utilizzare lo stesso oggetto, indipendentemente dal tipo di trasformazione eseguito.

Poiché sono presenti variabili che coinvolgono qualsiasi tipo di trasformazione dei dati, la trasformazione audio e video deve tenere conto dell'ampia gamma di possibili configurazioni multimediali. I codec Windows Media Audio e video supportano anche una serie di funzionalità speciali che è necessario poter configurare usando DMO.

In generale, le informazioni sulle variabili necessarie per il codec DMOs per comprimere e decomprimere i supporti digitali vengono fornite in uno dei tre modi seguenti:

-   Impostare il tipo di input in DMO per fornire le caratteristiche del supporto non compresso passato a un codificatore DMO e le caratteristiche del supporto compresso passato a un decodificatore DMO.
-   Impostare il tipo di output su DMO per fornire le caratteristiche dei supporti compressi che vengono recapitati da un codificatore DMO e le caratteristiche del supporto non compresso che vengono recapitati da un decodificatore DMO.
-   Usando i metodi dell'interfaccia **IPropertyBag** , configurare altre impostazioni che supportano le varie funzionalità del codec DMOS come proprietà. **IPropertyBag** è un'interfaccia com standard supportata da tutti i codec DMOS.

Inoltre, alcune funzionalità di codec vengono gestite usando altre interfacce specifiche per il codec DMOs. Queste interfacce sono elencate per ogni codec nella sezione [oggetti codec](codecobjects.md).

I tipi di input e di output sono specifici per i flussi di input e di output. Ogni flusso rappresenta una rappresentazione discreta del contenuto. Ad esempio, il Windows Media Video Encoder DMO dispone di un singolo flusso di input e di due flussi di output. Il flusso di input accetta esempi video non compressi. Il primo dei due flussi di output fornisce esempi compressi; l'altra fornisce esempi non compressi. I singoli esempi in un flusso di output rappresentano lo stesso contenuto degli esempi corrispondenti nell'altro flusso, ma ogni flusso recapita questi esempi in un formato diverso.

Ogni flusso (input o output) supporta uno o più tipi di supporto. Un tipo di supporto, o format, è descritto da una struttura del [**\_ \_ tipo di supporto DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) . È possibile eseguire una query su DMO per i tipi supportati da un flusso di output chiamando [**IMediaObject:: GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype). Questo metodo restituisce un tipo di output valido, sebbene in alcuni casi parzialmente incompleto, per quel flusso. È possibile enumerare i tipi di supporto supportati per un flusso di output effettuando chiamate ripetute a **GetOutputType**, incrementando il parametro di tipo a ogni chiamata. Quando l'indice del tipo passato non è più limitato, il metodo restituisce **DMO \_ E \_ non \_ più \_ elementi**. I formati di input possono essere enumerati nello stesso modo usando il metodo [**IMediaObject:: GetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype) .

I tipi enumerati da DMO sono solo i tipi "Preferiti", tuttavia potrebbero essere supportati altri tipi. È possibile convalidare un tipo di output chiamando [**IMediaObject:: SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype). Usare [**IMediaObject:: SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) per convalidare un tipo di input. Entrambi i metodi restituiscono **DMO \_ E \_ Type \_ non \_ accettati** se la struttura del [**\_ \_ tipo di supporto DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) passata non è valida. Per alcuni DMOs è necessario impostare un tipo di output prima di enumerare tutti i tipi di input. Il Windows Media Audio e il codec video DMOs includono tutti gli input e gli output con convalida interdipendente. Ovvero il tipo di output impostato imposta i criteri di convalida per il tipo di input. Sono inoltre presenti alcune proprietà che, se impostate, modificano i tipi di input e di output validi. Per questo motivo, è necessario impostare tutte le proprietà desiderate su DMO prima di enumerare i tipi.

Dopo aver impostato i tipi di output e di input per DMO, è possibile iniziare l'elaborazione degli esempi. Ogni esempio di input viene passato al codec usando una chiamata a [**IMediaObject::P rocessinput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput)e ogni esempio di output viene recapitato dal codec quando si effettua una chiamata a [**IMediaObject::P rocessoutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di codec DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 
