---
description: Impostazione delle proprietà per effetti e transizioni
ms.assetid: ce773140-7e50-4b72-8cb5-e34cba51644d
title: Impostazione delle proprietà per effetti e transizioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4ddd129eb9d4ab24ebef6f5c760a4211f26c9a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303696"
---
# <a name="setting-properties-on-effects-and-transitions"></a>Impostazione delle proprietà per effetti e transizioni

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

Molti effetti e transizioni di [servizi di modifica DirectShow](directshow-editing-services.md) supportano le proprietà che ne controllano il comportamento. Un'applicazione può impostare il valore di una proprietà usando l'interfaccia [**IPropertySetter**](ipropertysetter.md) . L'oggetto Effect o Transition sottostante deve supportare **IDispatch** per l'impostazione delle proprietà. Con gli effetti video e le transizioni, l'applicazione può impostare un intervallo di valori che cambiano nel tempo. (Ad esempio, è possibile impostare una transizione di cancellazione per spostarsi avanti e indietro nel frame). Con gli effetti audio, il valore della proprietà è statico e non può essere modificato nel tempo. L'unica eccezione è l'effetto della [busta del volume](volume-envelope-effect.md) , che supporta una proprietà dinamica per il livello del volume.

Per impostare una proprietà, seguire questa procedura.

1.  Creare un'istanza del setter della proprietà (CLSID \_ PropertySetter).
2.  Riempire le strutture del [**\_ valore**](dexter-value.md) Dexter [**\_ param**](dexter-param.md) e Dexter con i dati della proprietà. Queste strutture sono descritte di seguito.
3.  Passare le strutture del [**\_ valore**](dexter-value.md) [**Dexter \_ param**](dexter-param.md) e Dexter al metodo [**IPropertySetter:: AddProp**](ipropertysetter-addprop.md) .
4.  Ripetere i passaggi 2 e 3 per ogni proprietà che si desidera impostare.
5.  Passare il puntatore all'interfaccia [**IPropertySetter**](ipropertysetter.md) al metodo [**IAMTimelineObj:: SetPropertySetter**](iamtimelineobj-setpropertysetter.md) .

La struttura del [**\_ param Dexter**](dexter-param.md) specifica quale proprietà viene impostata. Contiene i membri seguenti.

-   **Nome**: nome della proprietà
-   **DISPID**: riservato, deve essere zero
-   **nValori**: numero di valori

La \_ struttura del valore Dexter specifica il valore di una proprietà in un determinato momento. Contiene i membri seguenti.

-   **v**: tipo Variant che specifica un nuovo valore per la proprietà. Il membro **VT** di questa variante definisce il tipo di dati della proprietà. Per ulteriori informazioni sul tipo **Variant** , vedere la Windows SDK.
-   **RT**: ora di riferimento quando la proprietà presuppone questo valore, in relazione all'ora di inizio dell'effetto o della transizione. L'ora di inizio dell'effetto o della transizione è relativa all'ora di inizio dell'oggetto padre.
-   **dwInterp**: flag che specifica il modo in cui la proprietà cambia dal valore precedente al nuovo valore. Con il \_ flag jump DEXTERF, la proprietà passa immediatamente al nuovo valore all'ora specificata. Con il flag DEXTERF interpolate \_ , la proprietà viene interpolata in modo lineare rispetto al valore precedente.

Se si imposta il membro **VT** su VT \_ BSTR, il setter della proprietà esegue le conversioni necessarie. Per i valori a virgola mobile, includere lo zero iniziali prima della posizione decimale. Ad esempio, 0,3, not. 3.

> [!Note]  
> Le applicazioni devono evitare di basarsi sulla conversione da **BSTR** s a valori numerici. Se la proprietà ha un valore numerico, è possibile usare il tipo **Variant** numerico appropriato.

 

Il valore di una proprietà può variare nel tempo, quindi il metodo [**IPropertySetter:: AddProp**](ipropertysetter-addprop.md) accetta un'unica struttura di [**\_ parametri Dexter**](dexter-param.md) e un puntatore a una matrice di strutture di [**\_ valori Dexter**](dexter-value.md) . La matrice definisce un set di valori basati sul tempo per la proprietà. I membri della matrice devono essere in ordine di tempo crescente e il membro **nValori** della struttura del parametro Dexter \_ deve essere uguale alla lunghezza della matrice.

Nell'esempio di codice seguente vengono creati i dati delle proprietà per la transizione di [cancellazione SMPTE](smpte-wipe-transition.md) . Imposta il codice di cancellazione su 120, che crea una cancellazione ovale. Imposta la durata di riferimento su zero, che indica l'inizio della transizione.


```C++
IPropertySetter     *pProp;   // Property setter
IAMTimelineObj      *pTransObj;  // Transition object
// Create an SMPTE Wipe transition object. (Not shown)

hr = CoCreateInstance(CLSID_PropertySetter, NULL, CLSCTX_INPROC_SERVER,
    IID_IPropertySetter, (void**) &pProp);

// Error checking is omitted for clarity...

DEXTER_PARAM param;
DEXTER_VALUE *pValue = (DEXTER_VALUE*)CoTaskMemAlloc(sizeof(DEXTER_VALUE));

// Initialize the parameter. 
param.Name = SysAllocString(L"MaskNum");
param.dispID = 0;
param.nValues = 1;

// Initialize the value.
pValue->v.vt = VT_I4;
pValue->v.lVal = 120; // Oval
pValue->rt = 0;
pValue->dwInterp = DEXTERF_JUMP;

pProp->AddProp(param, pValue);

// Free allocated resources.
SysFreeString(param.Name);
VariantClear(&(pValue->v));
CoTaskMemFree(pValue);

// Set the property on the transition.
pTransObj->SetPropertySetter(pProp);
pProp->Release();
```



**Modifica dinamica delle proprietà**

Dopo aver eseguito il rendering di un progetto di modifica video, è possibile modificare le proprietà di un oggetto o di un effetto di transizione durante l'esecuzione del grafo. Questa operazione è tuttavia possibile solo se si impostano le proprietà di tale oggetto prima dell'applicazione denominata [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md). In tal caso, è possibile chiamare [**IAMTimelineObj:: GetPropertySetter**](iamtimelineobj-getpropertysetter.md) per effetto o transizione, cancellare o modificare le proprietà e le modifiche vengono eseguite in modo dinamico durante l'esecuzione del grafo. È possibile che si verifichino anomalie visive durante la modifica, quindi questa operazione è consigliata solo per l'anteprima. Non modificare le proprietà durante la scrittura del progetto in un file.

Se non sono state impostate proprietà nell'oggetto Effect o Transition prima di chiamare **ConnectFrontEnd**, non è possibile aggiungervi proprietà durante l'esecuzione del grafo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo degli effetti e delle transizioni](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



