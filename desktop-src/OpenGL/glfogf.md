---
title: funzione glFogf (GL. h)
description: GlFogf e Function specificano i parametri di nebbia.
ms.assetid: 69961d8f-385c-4353-aef3-38fb654c44f8
keywords:
- funzione glFogf OpenGL
topic_type:
- apiref
api_name:
- glFogf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfe0509b30e91797752604110068701fcedaa266
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "104058399"
---
# <a name="glfogf-function"></a>glFogf (funzione)

**GlFogf** e Function specificano i parametri di nebbia.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glFogf(
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pname* 
</dt> <dd>

Specifica un parametro di nebbia a valore singolo.

Accetta uno dei valori seguenti.



| Valore                                                                                                                                                             | Significato                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_MODE"></span><span id="gl_fog_mode"></span><dl> <dt>**\_modalità di nebbia GL \_**</dt> </dl>          | Il parametro *params* è un singolo valore a virgola mobile che specifica l'equazione da usare per calcolare il fattore di Blend di nebbia, *f*. Sono accettate tre costanti simboliche: GL \_ Linear, GL \_ exp e GL \_ exp2. Le equazioni corrispondenti a queste costanti simboliche sono definite nella sezione Osservazioni riportata di seguito. La modalità di nebbia predefinita è GL \_ Exp.<br/> |
| <span id="GL_FOG_DENSITY"></span><span id="gl_fog_density"></span><dl> <dt>**\_densità di nebbia GL \_**</dt> </dl> | Il parametro *params* è un singolo valore a virgola mobile che specifica la *densità*, la densità di nebbia usata in entrambe le equazioni di nebbia esponenziale. Vengono accettate solo le densità non negative. La densità di nebbia predefinita è 1,0.<br/>                                                                                                                                    |
| <span id="GL_FOG_START"></span><span id="gl_fog_start"></span><dl> <dt>**\_inizio di nebbia GL \_**</dt> </dl>       | Il parametro *params* è un singolo valore a virgola mobile che specifica *Start*, la distanza vicina utilizzata nell'equazione Linear Fog. La distanza quasi predefinita è 0,0.<br/>                                                                                                                                                                                  |
| <span id="GL_FOG_END"></span><span id="gl_fog_end"></span><dl> <dt>**\_fine nebbia \_ GL**</dt> </dl>             | Il parametro *params* è un singolo valore a virgola mobile che specifica *end*, la distanza massima utilizzata nell'equazione Linear Fog. La distanza predefinita è 1,0.<br/>                                                                                                                                                                                      |
| <span id="GL_FOG_INDEX"></span><span id="gl_fog_index"></span><dl> <dt>**\_indice di nebbia GL \_**</dt> </dl>       | Il parametro *params* è un singolo valore a virgola mobile che specifica *i*<sub>f</sub> , ovvero l'indice dei colori di nebbia. L'indice di nebbia predefinito è 0,0.<br/>                                                                                                                                                                                                           |



 

</dd> <dt>

*param* 
</dt> <dd>

Specifica il valore su cui verrà impostato *pname* .

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

Per abilitare e disabilitare Fog con [**glEnable**](glenable.md) e [**glDisable**](gldisable.md), è possibile usare l'argomento per la \_ nebbia. Se abilitata, la nebbia interessa la geometria rasterizzata, le bitmap e i blocchi pixel, ma non le operazioni di cancellazione del buffer.

La funzione **glFogf** assegna il valore o i valori in *params* al parametro Fog specificato da *pname*.

Nebbia combina un colore di nebbia con ogni colore di post-texturing del frammento di pixel rasterizzato usando un fattore di fusione *f*. Il fattore *f* viene calcolato in uno dei tre modi seguenti, a seconda della modalità di nebbia. Lasciare che *z* sia la distanza nelle coordinate oculari dall'origine al frammento a cui si sta eseguendo la nebbia. L'equazione per GL \_ Linear Fog è:

![Equazione che mostra il valore di GL_LINEAR nebbia.](images/fog01.png)

L'equazione per GL \_ Exp Fog è:

![Equazione che mostra il valore del fattore di fusione in modalità GL_EXP nebbia.](images/fog02.png)

L'equazione per GL \_ exp2 Fog è:

![Equazione che mostra il valore del fattore di fusione in modalità GL_EXP2 nebbia.](images/fog03.png)

Indipendentemente dalla modalità di nebbia, *f* viene bloccato nell'intervallo \[ 0, 1 dopo il \] calcolo. Quindi, se OpenGL è in modalità colore RGBA, il colore *C*<sub>r</sub> del frammento viene sostituito da

![Equazione che mostra il colore del frammento offuscato come funzione di combinazione del fattore e del colore nebbia.](images/fog04.png)

In modalità di indice dei colori, l'indice di colore del frammento *i*<sub>r</sub> viene sostituito da

![Equazione che mostra l'indice dei colori del frammento con offuscamento come funzione del fattore di fusione e del colore indicizzato.](images/fog05.png)

Le funzioni seguenti consentono di recuperare informazioni correlate alle funzioni **glFog** :

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento del \_ colore della nebbia GL \_

**glGet** con argument GL \_ Fog \_ index

**glGet** con densità di \_ nebbia argomento GL \_

**glGet** con argument GL \_ Fog \_ Start

**glGet** con argomento di \_ \_ fine nebbia

**glGet** con argomento della \_ modalità di nebbia GL \_

[**glIsEnabled**](glisenabled.md) con argomento GL \_ Fog

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

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





