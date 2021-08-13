---
description: DMO Basi
ms.assetid: eaf453d2-69f8-432a-8a58-1ed70778f182
title: DMO Nozioni di base (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f24c7fb988d5e5225f292585a5562cce22e67c007175fa7ddc4cd86e40ec1d18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118742360"
---
# <a name="dmo-basics-microsoft-media-foundation"></a>DMO Nozioni di base (Microsoft Media Foundation)

In questo argomento viene fornita una breve panoramica degli oggetti DMO correlati Windows codec multimediali. Per altre informazioni sugli oggetti DMO, vedere [Oggetti multimediali DirectX.](../directshow/directx-media-objects.md)

Un DMO è un oggetto COM che trasforma i dati. Si passano i dati e vengono restituiti i dati trasformati. Nel caso di un codificatore di codec DMO dati multimediali non compressi vengono immessi e il DMO i dati multimediali compressi. Il vantaggio principale dell'uso degli oggetti DMO è che implementano tutti la stessa interfaccia di base, [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject), che semplifica l'uso di tali oggetti perché è possibile usare lo stesso oggetto, indipendentemente dal tipo di trasformazione eseguita.

Poiché sono presenti variabili coinvolte in qualsiasi tipo di trasformazione dei dati, la trasformazione audio e video deve prendere in considerazione l'ampia gamma di possibili configurazioni multimediali. I codec Windows audio e video multimediali supportano anche una serie di funzionalità speciali che è necessario configurare usando il DMO.

In generale, le informazioni sulle variabili necessarie ai DMO del codec per comprimere e decomprimere i supporti digitali vengono trasmesse in uno dei tre modi seguenti:

-   Impostare il tipo di input nel DMO per comunicare le caratteristiche dei supporti non compressi passati a un DMO del codificatore e le caratteristiche dei supporti compressi passati a un DMO.
-   Impostare il tipo di output sul DMO per comunicare le caratteristiche dei supporti compressi che vengono recapitati da un DMO di codificatore e le caratteristiche dei supporti non compressi che vengono recapitati da un DMO decodificatore.
-   Usando i metodi **dell'interfaccia IPropertyBag,** configurare altre impostazioni che supportano le varie funzionalità dei DMO del codec come proprietà. **IPropertyBag è** un'interfaccia COM standard supportata da tutti i DMO codec.

Inoltre, alcune funzionalità del codec vengono gestite usando altre interfacce specifiche per i DMO del codec. Queste interfacce sono elencate per ogni codec nella sezione [Oggetti codec](codecobjects.md).

I tipi di input e output sono specifici dei flussi di input e output. Ogni flusso rappresenta una rappresentazione discreta del contenuto. Ad esempio, il Windows Media Video DMO ha un singolo flusso di input e due flussi di output. Il flusso di input accetta esempi di video non compressi. Il primo dei due flussi di output fornisce esempi compressi. l'altro fornisce esempi non compressi. I singoli esempi in un flusso di output rappresentano lo stesso contenuto degli esempi corrispondenti nell'altro flusso, ma ogni flusso fornisce tali esempi in un formato diverso.

Ogni flusso (input o output) supporta uno o più tipi di supporti. Un tipo di supporto, o formato, viene descritto da una [**DMO \_ MEDIA \_ TYPE.**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) È possibile eseguire una query DMO i tipi supportati da un flusso di output chiamando [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype). Questo metodo restituisce un tipo di output valido (anche se in alcuni casi parzialmente incompleto) per il flusso. È possibile enumerare i tipi di supporti supportati per un flusso di output effettuando chiamate ripetute a **GetOutputType**, incrementando il parametro di tipo con ogni chiamata. Quando l'indice del tipo passato non rientra nei limiti, il metodo restituisce DMO **\_ E NO MORE \_ \_ \_ ITEMS**. I formati di input possono essere enumerati nello stesso modo usando il [**metodo IMediaObject::GetInputType.**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype)

I tipi enumerati dal DMO sono solo i tipi "preferiti", ma possono essere supportati altri tipi. È possibile convalidare un tipo di output chiamando [**IMediaObject::SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype). Usare [**IMediaObject::SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) per convalidare un tipo di input. Entrambi i metodi restituiranno **DMO E TYPE NOT \_ \_ \_ \_ ACCEPTED** se la [**DMO MEDIA \_ \_ TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) passata non è valida. Alcuni DMO richiedono l'impostazione di un tipo di output prima di enumerare qualsiasi tipo di input. I Windows di codec audio e video multimediali hanno tutti input e output con convalida interdipendente. Ciò significa che il tipo di output impostato imposta i criteri di convalida per il tipo di input. Esistono anche alcune proprietà che, se impostate, modificano i tipi di input e output validi. Per questo motivo, è necessario impostare tutte le proprietà desiderate nel DMO prima di enumerare i tipi.

Dopo aver impostato i tipi di output e di input per il DMO, è possibile iniziare a elaborare gli esempi. Ogni esempio di input viene passato al codec usando una chiamata a [**IMediaObject::P rocessInput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput)e ogni esempio di output viene recapitato dal codec quando si effettua una chiamata a [**IMediaObject::P rocessOutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso degli oggetti DMO codec](workingwithcodecdmos.md)
</dt> </dl>

 

 
