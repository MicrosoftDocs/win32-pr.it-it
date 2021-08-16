---
title: Funzione glFogiv (Gl.h)
description: La funzione glFogiv specifica i parametri della nebbia. | Funzione glFogiv (Gl.h)
ms.assetid: 8d920ddc-6155-412d-af10-585932cb149f
keywords:
- Funzione glFogiv OpenGL
topic_type:
- apiref
api_name:
- glFogiv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd4e22fddbd6c89a219c296c4fa0161f3992be195a91b38ab512c493241430fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061711"
---
# <a name="glfogiv-function"></a>Funzione glFogiv

La **funzione glFogfv** specifica i parametri di osa.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glFogiv(
         GLenum pname,
   const GLint  *params
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pname* 
</dt> <dd>

Specifica un parametro di nebbia.

Accetta uno dei valori seguenti.



| Valore                                                                                                                                                             | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_MODE"></span><span id="gl_fog_mode"></span><dl> <dt>**MODALITÀ \_ GL \_ OSA**</dt> </dl>          | Il *parametro params* è un singolo valore integer che specifica l'equazione da usare per calcolare il fattore di fusione della nebbia, *f*. Sono accettate tre costanti simboliche: GL \_ LINEAR, GL \_ EXP e GL \_ EXP2. Le equazioni corrispondenti a queste costanti simboliche sono definite nella sezione Osservazioni seguente. La modalità predefinita è GL \_ EXP.<br/>                                                                                      |
| <span id="GL_FOG_DENSITY"></span><span id="gl_fog_density"></span><dl> <dt>**DENSITÀ \_ DELLA DENSITÀ DELLA \_ NEBBIA GL**</dt> </dl> | Il *parametro params* è un singolo valore intero che specifica *la* densità , la densità della nebbia usata in entrambe le equazioni esponenziali della nebbia. Vengono accettate solo densità non neghe. La densità di nebbia predefinita è 1,0.<br/>                                                                                                                                                                                                                         |
| <span id="GL_FOG_START"></span><span id="gl_fog_start"></span><dl> <dt>**GL \_ \_ OSA INIZIO**</dt> </dl>       | Il *parametro params* è un singolo valore intero che specifica *start,* la distanza vicina usata nell'equazione lineare della nebbia. La distanza minima predefinita è 0,0.<br/>                                                                                                                                                                                                                                                                       |
| <span id="GL_FOG_END"></span><span id="gl_fog_end"></span><dl> <dt>**FINE \_ DELLA NEBBIA \_ GL**</dt> </dl>             | Il *parametro params* è un singolo valore intero che specifica *end*, la distanza lontana usata nell'equazione lineare della nebbia. La distanza predefinita è 1,0.<br/>                                                                                                                                                                                                                                                                           |
| <span id="GL_FOG_INDEX"></span><span id="gl_fog_index"></span><dl> <dt>**INDICE \_ GL FOG \_**</dt> </dl>       | Il *parametro params* è un singolo valore integer che specifica *i*<sub>f</sub> , l'indice dei colori della nebbia. L'indice predefinito della nebbia è 0,0.<br/>                                                                                                                                                                                                                                                                                                |
| <span id="GL_FOG_COLOR"></span><span id="gl_fog_color"></span><dl> <dt>**COLORE \_ GL \_ OSANNA**</dt> </dl>       | Il *parametro params* contiene quattro valori integer o a virgola mobile che *specificano C*<sub>f</sub> , il colore della nebbia. I valori interi vengono mappati in modo lineare in modo che il valore rappresentabile più positivo sia mappato a 1,0 e il valore rappresentabile più negativo a -1,0. I valori a virgola mobile vengono mappati direttamente. Dopo la conversione, tutti i componenti di colore vengono ancorati all'intervallo \[ 0,1. \] Il colore predefinito della nebbia è (0,0,0,0).<br/> |



 

</dd> <dt>

*params* 
</dt> <dd>

Specifica il valore o i valori da assegnare a *pname*. GL \_ FOG COLOR richiede una matrice di quattro \_ valori. Tutti gli altri parametri accettano una matrice contenente un solo valore.

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

Abilitare e disabilitare la frodi [**con glEnable**](glenable.md) [**e glDisable**](gldisable.md)usando l'argomento GL \_ FOG. Se abilitata, la nebbia influisce sulla geometria rasterizzata, sulle bitmap e sui blocchi di pixel, ma non sulle operazioni di cancellazione del buffer.

La **funzione glFogiv** assegna il valore o i valori in *params* al parametro osa specificato da *pname*.

La sfumatura combina un colore osanna con il colore posttexturing di ogni frammento di pixel rasterizzato usando un fattore di fusione *f*. Il *fattore f* viene calcolato in uno dei tre modi seguenti, a seconda della modalità nebbia. Che *z* sia la distanza in coordinate oculari dall'origine al frammento in fase di foro. L'equazione per GL \_ LINEAR è:

![Equazione che mostra il valore del fattore di fusione GL_LINEAR modalità nebbia come funzione della distanza.](images/fog01.png)

L'equazione per gl \_ EXP exp è:

![Equazione che mostra il valore del fattore di fusione in GL_EXP modalità nebbia.](images/fog02.png)

L'equazione per gl \_ EXP2 exp2 è:

![Equazione che mostra il valore del fattore di fusione in GL_EXP2 modalità nebbia.](images/fog03.png)

Indipendentemente dalla modalità osanna, *f* viene ancorato all'intervallo \[ 0,1 \] dopo il calcolo. Quindi, se OpenGL è in modalità colore RGBA, il colore *C*<sub>r</sub> del frammento viene sostituito da

![Equazione che mostra il colore del frammento irregolare in funzione del fattore di fusione e del colore della nebbia.](images/fog04.png)

In modalità color-index, l'indice colori del frammento *i*<sub>r</sub> viene sostituito da

![Equazione che mostra l'indice dei colori del frammento dentellato in funzione del fattore di fusione e del colore indicizzato.](images/fog05.png)

Le funzioni seguenti recuperano informazioni correlate alle **funzioni glFog:**

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ FOG \_ COLOR

**glGet con** argomento GL \_ FOG \_ INDEX

**glGet con** argomento GL \_ FOG \_ DENSITY

**glGet con** argomento GL \_ FOG \_ START

**glGet con** argomento GL \_ \_ FEB END

**glGet con** argomento GL \_ FOG \_ MODE

[**glIsEnabled con**](glisenabled.md) argomento GL \_ FOG

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

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





