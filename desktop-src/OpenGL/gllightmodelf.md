---
title: Funzione glLightModelf (Gl.h)
description: La funzione glLightModelf imposta i parametri del modello di illuminazione.
ms.assetid: 7002c157-514e-4102-93f7-21a0df97a5c2
keywords:
- Funzione glLightModelf OpenGL
topic_type:
- apiref
api_name:
- glLightModelf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1b413f4cd3daa1eeeaeaf1857018cae21edf5b4ab36bea7474bfd6bcd7e64ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493261"
---
# <a name="gllightmodelf-function"></a>Funzione glLightModelf

La **funzione glLightModelf** imposta i parametri del modello di illuminazione.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glLightModelf(
   GLenum  pname,
   GLfloat *param
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pname* 
</dt> <dd>

Parametro del modello di illuminazione a valore singolo. Vengono accettati i valori seguenti.



| Valore                                                                                                                                                                                                      | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span><dl> <dt>**VISUALIZZATORE \_ LOCALE \_ DEL \_ MODELLO \_ GL LIGHT**</dt> </dl> | Il *parametro param* è un singolo valore a virgola mobile che specifica come vengono calcolati gli angoli di reflection speculari. Se *param* è 0 (o 0,0), gli angoli di reflection speculari prendono la direzione di visualizzazione per essere paralleli a e nella direzione dell'asse -*z,* indipendentemente dalla posizione del vertice nelle coordinate oculari. In caso contrario, i riflessi speculari vengono calcolati dall'origine del sistema di coordinate oculari. Il valore predefinito è 0. <br/>                                                                                                                                                                                                                                                                                                                |
| <span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span><dl> <dt>**GL \_ LIGHT \_ MODEL \_ TWO \_ SIDE**</dt> </dl>             | Il *parametro param* è un singolo valore a virgola mobile che specifica se per i poligoni vengono emersi calcoli di illuminazione a uno o a due lati. Non ha alcun effetto sui calcoli di illuminazione per punti, linee o bitmap. Se *param è* 0 (o 0,0), viene specificata l'illuminazione a un lato e nell'equazione di illuminazione vengono usati solo i parametri del materiale anteriore. In caso contrario, viene specificata l'illuminazione a due lati. <br/> In questo caso, i vertici dei poligoni rivolti all'indietro vengono illuminati usando i parametri del materiale posteriore e le normali vengono invertete prima che venga valutata l'equazione di illuminazione. I vertici dei poligoni frontali vengono sempre illuminati usando i parametri del materiale anteriore, senza modificare le normali. Il valore predefinito è 0.<br/> |



 

</dd> <dt>

*param* 
</dt> <dd>

Valore sul quale *verrà impostato il* parametro.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl>      | *pname* non è un valore accettato.<br/>                                                                                         |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glLightModelf** imposta il parametro del modello di illuminazione. Il *parametro pname* assegna un nome a un parametro e *param* restituisce il nuovo valore. Il valore o i valori dei singoli parametri di sorgente di luce.

In modalità RGBA, il colore illuminato di un vertice è la somma dell'intensità di emissione del materiale, del prodotto della riflettenza dell'ambiente materiale e dell'intensità dell'ambiente della scena completa del modello di illuminazione e del contributo di ogni sorgente di luce abilitata. Ogni sorgente di luce contribuisce alla somma di tre termini: ambiente, diffusione e speculare.

-   Il contributo della sorgente di luce ambientale è il prodotto della riflettenza dell'ambiente materiale e dell'intensità ambientale della luce.
-   Il contributo della sorgente di luce diffusa è il prodotto della riflessione diffusa del materiale, dell'intensità diffusa della luce e del prodotto del punto della normale del vertice con il vettore normalizzato dal vertice alla sorgente di luce.
-   Il contributo della sorgente di luce speculare è il prodotto della riflettenza speculare del materiale, dell'intensità speculare della luce e del prodotto del punto dei vettori vertice-occhio e vertice-luce normalizzati, alzati alla potenza della lucentezza del materiale.

Tutti e tre i contributi alla sorgente di luce vengono attenuati in modo uniforme in base alla distanza dal vertice alla sorgente di luce e alla direzione della sorgente di luce, all'esponente diffusione e all'angolo di taglio della distribuzione. Tutti i prodotti punto vengono sostituiti con zero se restituiscono un valore negativo.

Il componente alfa del colore illuminato risultante viene impostato sul valore alfa della riflessione diffusa del materiale.

In modalità color-index, il valore dell'indice illuminato di un vertice varia dall'ambiente ai valori speculari passati a [**glMaterial**](glmaterial-functions.md) usando GL \_ COLOR \_ INDEXES. I coefficienti diffusi e speculari, calcolati con una ponderazione (.30, .59, .11) dei colori della luce, la luminosità del materiale e le stesse equazioni di reflection e attenuazione del caso RGBA, determinano quanto al di sopra dell'ambiente si trova l'indice risultante.

Le funzioni seguenti recuperano informazioni correlate alla **funzione glLightModelf:**

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ LIGHT MODEL LOCAL \_ \_ \_ VIEWER

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ LIGHT MODEL TWO \_ \_ \_ SIDE

[**glIsEnabled con**](glisenabled.md) l'argomento GL \_ LIGHTING

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Libreria<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> </dl>

 

 





