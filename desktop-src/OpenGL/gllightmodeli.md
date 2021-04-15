---
title: funzione glLightModeli (GL. h)
description: La funzione glLightModeli imposta i parametri del modello di illuminazione.
ms.assetid: 49975166-b2b3-47f9-8305-aea2ba364546
keywords:
- funzione glLightModeli OpenGL
topic_type:
- apiref
api_name:
- glLightModeli
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7ae32e91e62a5341ceb0fc3fc4b16b0e7cfbae0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400253"
---
# <a name="gllightmodeli-function"></a>glLightModeli (funzione)

La funzione [**glLightModeli**](gllightf.md) imposta i parametri del modello di illuminazione.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glLightModeli(
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pname* 
</dt> <dd>

Parametro del modello di illuminazione a valore singolo. Vengono accettati i valori seguenti.



| Valore                                                                                                                                                                                                      | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span><dl> <dt>**\_ \_ \_ Visualizzatore locale del modello GL Light \_**</dt> </dl> | Il parametro *param* è un singolo valore integer che specifica il modo in cui vengono calcolati gli angoli di Reflection speculare. Se *param* è 0 (o 0,0), gli angoli di Reflection speculari prendono la direzione di visualizzazione parallela a e nella direzione dell'asse-*z* , indipendentemente dalla posizione del vertice nelle coordinate oculari. In caso contrario, le riflessioni speculari vengono calcolate dall'origine del sistema di coordinate oculari. Il valore predefinito è 0. <br/>                                                                                                                                                                                                                                                                                                                |
| <span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span><dl> <dt>**\_modello GL Light \_ Two- \_ \_ Side**</dt> </dl>             | Il parametro *param* è un singolo valore integer che specifica se vengono eseguiti calcoli di illuminazione unilaterali o bilaterali per i poligoni. Non ha alcun effetto sui calcoli di illuminazione per punti, linee o bitmap. Se *param* è 0 (o 0,0), viene specificata un'illuminazione unilaterale e vengono usati solo i parametri del materiale anteriore nell'equazione di illuminazione. In caso contrario, viene specificata l'illuminazione a due lati. <br/> In questo caso, i vertici dei poligoni sottoposti a riattivazione vengono illuminati usando i parametri del materiale di back-end e le normali annullate prima della valutazione dell'equazione di illuminazione. I vertici dei poligoni in primo piano sono sempre illuminati usando i parametri del materiale anteriore, senza apportare modifiche alle normali. Il valore predefinito è 0.<br/> |



 

</dd> <dt>

*param* 
</dt> <dd>

Valore in cui verrà impostato *param* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | *pname* non è un valore accettato.<br/>                                                                                         |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glLightModeli** imposta il parametro del modello di illuminazione. Il parametro *pname* denomina un parametro e *param* fornisce il nuovo valore. il valore o i valori dei singoli parametri della sorgente di luce.

In modalità RGBA, il colore chiaro di un vertice è costituito dalla somma dell'intensità di emissione del materiale, dal prodotto della riflettenza dell'ambiente del materiale e dall'intensità dell'ambiente a scena completa del modello di illuminazione e dal contributo di ogni sorgente di luce abilitata. Ogni sorgente di luce contribuisce alla somma di tre termini: ambiente, diffuso e speculare.

-   Il contributo di origine luce di ambiente è il prodotto della riflettenza dell'ambiente del materiale e l'intensità di ambiente della luce.
-   Il contributo Diffusion Light Source è il prodotto della riflettenza diffusa del materiale, l'intensità diffusa della luce e il prodotto punto della normale del vertice con il vettore normalizzato dal vertice alla sorgente di luce.
-   Il contributo della sorgente di luce speculare è il prodotto della riflettenza speculare del materiale, l'intensità speculare della luce e il prodotto a virgola dei vettori normalizzati da vertice a occhio e da vertice a chiaro, elevato alla potenza del lucentezza del materiale.

Tutti e tre i contributi della sorgente di luce vengono attenuati in modo uniforme in base alla distanza dal vertice alla sorgente di luce e alla direzione della sorgente di luce, all'esponente spread e all'angolo di taglio. Tutti i prodotti a virgola vengono sostituiti da zero se restituiscono un valore negativo.

Il componente alfa del colore chiaro risultante viene impostato sul valore alfa della riflettenza diffusa del materiale.

In modalità di indice dei colori, il valore dell'indice illuminato di un vertice spazia dall'ambiente ai valori speculari passati a [**glMaterial**](glmaterial-functions.md) usando gli \_ indici dei colori GL \_ . Coefficienti, diffusi e speculari, calcolati con un valore (30, 59, .11) ponderazione dei colori della luce, il lucentezza del materiale e le stesse equazioni di reflection e attenuazione come nel caso di RGBA, determinano la quantità di spazio sopra l'indice risultante.

Le funzioni seguenti consentono di recuperare informazioni correlate alla funzione **glLightModeli** :

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Light \_ Model \_ \_ Visualizzatore locale

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Light \_ Model \_ Two \_ Side

[**glIsEnabled**](glisenabled.md) con illuminazione GL argomento \_

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Libreria<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> </dl>

 

 





