---
description: Impostazione delle proprietà su effetti e transizioni
ms.assetid: ce773140-7e50-4b72-8cb5-e34cba51644d
title: Impostazione delle proprietà su effetti e transizioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1305eb7860b5519b14cfeebc349643c2662db3f133c0bf3424d1d71ccf85753c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904261"
---
# <a name="setting-properties-on-effects-and-transitions"></a>Impostazione delle proprietà su effetti e transizioni

\[Questa API non è supportata e potrebbe essere modificata o non disponibile in futuro.\]

Molti [DirectShow effetti e](directshow-editing-services.md) transizioni di Servizi di modifica supportano proprietà che ne controllano il comportamento. Un'applicazione può impostare il valore di una proprietà usando [**l'interfaccia IPropertySetter.**](ipropertysetter.md) L'effetto o l'oggetto transizione sottostante deve **supportare IDispatch per** l'impostazione delle proprietà. Con gli effetti video e le transizioni, l'applicazione può impostare un intervallo di valori che cambiano nel tempo. Ad esempio, è possibile impostare una transizione di cancellazione per spostarsi avanti e indietro nel frame. Con gli effetti audio, il valore della proprietà è statico e non può cambiare nel tempo. L'unica eccezione è [l'effetto Volume Envelope,](volume-envelope-effect.md) che supporta una proprietà dinamica per il livello di volume.

Per impostare una proprietà, seguire questa procedura.

1.  Creare un'istanza del setter di proprietà (CLSID \_ PropertySetter).
2.  Inserire i dati delle proprietà nelle strutture [**\_ PARAM**](dexter-param.md) [**e FILL \_ VALUE.**](dexter-value.md) Queste strutture sono illustrate di seguito.
3.  Passare le [**\_ strutture PARAM e**](dexter-param.md) [**\_ UNEMETE AL**](dexter-value.md) metodo [**IPropertySetter::AddProp.**](ipropertysetter-addprop.md)
4.  Ripetere i passaggi 2 e 3 per ogni proprietà che si vuole impostare.
5.  Passare il puntatore di interfaccia [**IPropertySetter**](ipropertysetter.md) al [**metodo IAMTimelineObj::SetPropertySetter.**](iamtimelineobj-setpropertysetter.md)

La [**struttura \_ PARAM DELL'ARGOMENTO**](dexter-param.md) SPECIFICA la proprietà da impostare. Contiene i membri seguenti.

-   **Name:** nome della proprietà
-   **dispID:** Riservato, deve essere zero
-   **nValues:** numero di valori

La struttura DI \_ TIPO VALUE specifica il valore di una proprietà in un determinato momento. Contiene i membri seguenti.

-   **v:** tipo VARIANT che specifica un nuovo valore per la proprietà. Il **membro vt** di questa variante definisce il tipo di dati della proprietà. Per altre informazioni sul tipo **VARIANT,** vedere Windows SDK.
-   **rt**: ora di riferimento in cui la proprietà assume questo valore, rispetto all'ora di inizio dell'effetto o della transizione. L'ora di inizio dell'effetto o della transizione è relativa all'ora di inizio dell'oggetto padre.
-   **dwInterp:** flag che specifica il modo in cui la proprietà viene modificata dal valore precedente al nuovo valore. Con il flag JUMP DI TIPO JUMP, la proprietà passa immediatamente \_ al nuovo valore all'ora specificata. Con il flag INTERPOLATE DELLA FUNZIONE DI \_ INTERPOLAZIONE, la proprietà viene interpolata in modo lineare rispetto al valore precedente.

Se si imposta il **membro vt** su VT BSTR, il setter di proprietà \_ esegue le conversioni necessarie. Per i valori a virgola mobile, includere lo zero iniziale prima della posizione decimale. Ad esempio, 0.3, non .3.

> [!Note]  
> Le applicazioni devono evitare di basarsi sulla conversione **da BSTR** a valori numerici. Se la proprietà ha un valore numerico, è possibile usare il tipo **VARIANT** numerico appropriato.

 

Il valore di una proprietà può cambiare nel tempo, quindi il metodo [**IPropertySetter::AddProp**](ipropertysetter-addprop.md) accetta una singola struttura [**\_ PARAM DELL'istruzione e**](dexter-param.md) un puntatore a una matrice di strutture DI TIPO [**VALUE. \_**](dexter-value.md) La matrice definisce un set di valori basati sul tempo per la proprietà . I membri della matrice devono essere in ordine di tempo crescente e il membro **nValues** della struttura PARAM DELL'ARGOMENTO DEVE essere uguale alla \_ lunghezza della matrice.

Nell'esempio di codice seguente vengono creati i dati delle proprietà per [la transizione di cancellazione SMPTE.](smpte-wipe-transition.md) Imposta il codice di cancellazione su 120, che crea una cancellazione ovale. Imposta l'ora di riferimento su zero, che indica l'inizio della transizione.


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

Dopo aver eseguito il rendering di un progetto di modifica video, è possibile modificare le proprietà di un oggetto effetto o transizione mentre il grafico è in esecuzione. Tuttavia, ciò è possibile solo se si impostano le proprietà su tale oggetto prima che l'applicazione chiama [**IRenderEngine::ConnectFrontEnd.**](irenderengine-connectfrontend.md) In questo caso, è possibile chiamare [**IAMTimelineObj::GetPropertySetter**](iamtimelineobj-getpropertysetter.md) per l'effetto o la transizione, cancellare o modificare le proprietà e le modifiche verranno apportate dinamicamente durante l'esecuzione del grafico. Potrebbero verificarsi anomalie visive durante la modifica, quindi questa opzione è consigliata solo per l'anteprima. Non modificare le proprietà durante la scrittura del progetto in un file.

Se non è stata impostata alcuna proprietà sull'oggetto effetto o transizione prima di **chiamare ConnectFrontEnd,** non è possibile aggiungervi proprietà mentre il grafico è in esecuzione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di effetti e transizioni](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



