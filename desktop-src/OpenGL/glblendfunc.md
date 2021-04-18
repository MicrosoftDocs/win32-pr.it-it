---
title: funzione glBlendFunc (GL. h)
description: La funzione glBlendFunc specifica l'aritmetica dei pixel.
ms.assetid: 6756774b-5eef-419a-a653-0b251aed65a0
keywords:
- funzione glBlendFunc OpenGL
topic_type:
- apiref
api_name:
- glBlendFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6300543bbf589c704da6d941bd743f693e0ed5fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301801"
---
# <a name="glblendfunc-function"></a>glBlendFunc (funzione)

La funzione **glBlendFunc** specifica l'aritmetica dei pixel.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glBlendFunc(
   GLenum sfactor,
   GLenum dfactor
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sfactor* 
</dt> <dd>

Specifica il modo in cui vengono calcolati i fattori di fusione del codice sorgente rosso, verde, blu e alfa. Sono accettate nove costanti simboliche: GL \_ zero, GL \_ One, GL \_ DST \_ color, GL a \_ \_ meno \_ DST \_ color, GL \_ src \_ Alpha, GL \_ One \_ meno \_ src \_ Alpha, GL \_ DST Alpha, \_ GL \_ One \_ meno \_ DST \_ Alpha e GL \_ src \_ Alpha \_ satura.

</dd> <dt>

*dfactor* 
</dt> <dd>

Specifica il modo in cui vengono calcolati i fattori di fusione di destinazione rosso, verde, blu e alfa. Sono accettate otto costanti simboliche: GL \_ zero, GL \_ One, GL \_ src \_ color, GL a \_ \_ meno \_ src \_ color, GL \_ src \_ Alpha, GL \_ One \_ meno \_ src \_ Alpha, GL \_ DST \_ Alpha e GL \_ 1 \_ meno \_ DST \_ alpha.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | *Sfactor* o *dfactor* non è un valore accettato.<br/>                                                                   |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

In modalità RGB, i pixel possono essere disegnati usando una funzione che combina i valori RGBA in ingresso (di origine) con i valori RGBA già presenti nel framebuffer (valori di destinazione). Per impostazione predefinita, la fusione è disabilitata. Usare [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) con l' \_ argomento di Blend GL per abilitare e disabilitare la fusione.

Se abilitata, **glBlendFunc** definisce l'operazione di fusione. Il parametro *sfactor* specifica quale dei nove metodi viene usato per ridimensionare i componenti del colore di origine. Il parametro *dfactor* specifica quale di otto metodi viene utilizzato per ridimensionare i componenti del colore di destinazione. Nella tabella seguente sono descritti gli undici metodi possibili. Ogni metodo definisce quattro fattori di scala ognuno per rosso, verde, blu e alfa.

Nella tabella e nelle equazioni successive, i componenti dei colori di origine e di destinazione sono detti (*R*? , *G*? , *B*? , *A*? ) e (*R*<sub>d</sub> , *G*<sub>d</sub> , *B*<sub>d</sub> , *A*<sub>d</sub> ). Hanno valori integer compresi tra zero e (*k*<sub>r</sub> , *k*<sub>G</sub> , *k*<sub>r</sub> , *k*<sub>a</sub> ), dove

*k*<sub>r</sub> = 2 <sup>m</sup>*r* -1

*k*<sub>g</sub> = 2 <sup>m</sup>*g* -1

*k*<sub>b</sub> = 2 <sup>m</sup>*b* -1

*k*<sub>a</sub> = 2 <sup>m</sup>*a* -1

e (*m*<sub>R</sub> , *m*<sub>G</sub> , *m*<sub>B</sub> , *m*<sub>A</sub> ) è il numero di bitplane rosso, verde, blu e alfa.

I fattori di scala di origine e di destinazione sono detti (*s*<sub>R</sub> , *s*<sub>G</sub> , *s*<sub>B</sub> , *s*<sub>A</sub> ) e (*d*<sub>R</sub> , *d*<sub>G</sub> , *d*<sub>B</sub> , *d*<sub>A</sub> ). I fattori di scala descritti nella tabella, denotati (*f*<sub>R</sub> , *f*<sub>G</sub> , *f*<sub>B</sub> , *f*<sub>A</sub> ), rappresentano i fattori di origine o di destinazione. Tutti i fattori di scala hanno un intervallo compreso tra \[ 0 e 1 \] .



| Parametro                  | (*f*<sub>R</sub>  , *f*<sub>G</sub>  , *f*<sub>B</sub>  , *f*<sub>A</sub>  )                                                                                 |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_zero GL                   | (0, 0, 0, 0)                                                                                                                                                    |
| GL \_ uno                    | (1, 1, 1, 1)                                                                                                                                                    |
| \_colore GL src \_             | (*R*? / *k*<sub>R</sub> , *G*? / *k*<sub>G</sub> , *B*? / *k*<sub>B</sub> , *A*? / *k*<sub>A</sub> )                                                         |
| GL \_ uno \_ meno \_ il \_ colore src | (1, 1, 1, 1)-(*R*? / *k*<sub>R</sub> , *G*? / *k*<sub>G</sub> , *B*? / *k*<sub>B</sub> , *A*? / *k*<sub>A</sub> )                                             |
| \_colore GL DST \_             | (*R*<sub>d</sub>  /  *k*<sub>R</sub> , *g*<sub>d</sub>  /  *k*<sub>g</sub> , *b*<sub>d</sub>  /  *k*<sub>b</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> )             |
| GL \_ uno \_ meno \_ il \_ colore DST | (1, 1, 1, 1)-(*r*<sub>d</sub>  /  *k*<sub>r</sub> , *g*<sub>d</sub>  /  *k*<sub>g</sub> , *b*<sub>d</sub>  /  *k*<sub>b</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> ) |
| \_alfa src \_ GL             | (*A*? / *k*<sub>a</sub> , *a*? / *k*<sub>a</sub> , *a*? / *k*<sub>a</sub> , *a*? / *k*<sub>A</sub> )                                                         |
| GL \_ 1 \_ meno \_ src \_ Alpha | (1, 1, 1, 1)-(*A*? / *k*<sub>a</sub> , *a*? / *k*<sub>a</sub> , *a*? / *k*<sub>a</sub> , *a*? / *k*<sub>A</sub> )                                             |
| \_alfa del DST GL \_             | (*A*<sub>d</sub>  /  *k*<sub>a</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> )             |
| GL \_ 1 \_ meno \_ DST \_ Alpha | (1, 1, 1, 1)-(*a*<sub>d</sub>  /  *k*<sub>a</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> ) |
| \_ \_ satura Alpha di GL src \_   | (*i, i, i,* 1)                                                                                                                                                 |



 

Nella tabella,

*i* = min (*A*? , *k*<sub>a</sub>   -  *a*<sub>d</sub> )/ *k*<sub>a</sub>

Per determinare i valori RGBA di Blend di un pixel durante il disegno in modalità RGBA, il sistema usa le equazioni seguenti:

*R* (*d*) = min ( *k*<sub>r</sub> , *r*? *s*<sub>r</sub>  +  *r*<sub>d</sub> *d*<sub>r</sub> )

*G* (*d*) = min ( *k*<sub>g</sub> , *g*? *s*<sub>g</sub>  +  *g*<sub>d</sub> <sub>g</sub> )

*B* (*d*) = min ( *k*<sub>b</sub> *, b*? *s*<sub>b</sub>  +  *b*<sub>d</sub> *d*<sub>b</sub> )

*A* (*d*) = min ( *k*<sub>a</sub> , *a*? *s*<sub>a</sub>  +  <sub>d</sub> *d*<sub>a</sub> )

Nonostante la precisione apparente delle equazioni precedenti, la fusione aritmetica non è esattamente specificata, perché la fusione opera con valori di colore integer imprecisi. Tuttavia, un fattore di Blend che deve essere uguale a uno non modifica la relativa multiplicand e un fattore di fusione uguale a zero riduce il multiplicand a zero. Pertanto, ad esempio, quando *sfactor* è GL \_ src \_ Alpha, *dfactor* è GL \_ One \_ meno \_ src \_ Alpha e *a*? è uguale a *k*<sub>a</sub>, le equazioni riducono alla sostituzione semplice:

*R*<sub>d</sub>  =  *r*?

*G*<sub>d</sub>  =  *g*?

B <sub>d</sub>  =  *b*?

<sub>D</sub>  =  *a*?

## <a name="examples"></a>Esempio

La trasparenza è implementata in modo ottimale usando **glBlendFunc**(GL \_ src \_ Alpha, GL \_ One \_ meno \_ src \_ Alpha) con primitive ordinate dal più lontano al più vicino. Si noti che questo calcolo della trasparenza non richiede la presenza di Alpha bitplane nel framebuffer.

È anche possibile usare **glBlendFunc**(GL \_ src \_ Alpha, GL \_ One \_ meno \_ src \_ Alpha) per il rendering di punti e righe con antialias in ordine arbitrario.

Per ottimizzare l'anti-aliasing poligono, usare **glBlendFunc**(GL \_ src \_ Alpha \_ saturate, GL \_ One) con poligoni ordinati dal più vicino al più lontano. (Vedere GL \_ \_Argomento smussato del poligono in [**glenble**](glenable.md) per informazioni sull'anti-aliasing del poligono. Bitplane alfa di destinazione, che deve essere presente affinché questa funzione di Blend funzioni correttamente, archiviare la copertura accumulata.

In ingresso (origine) Alfa è un'opacità del materiale, che va da 1,0 (*K*<sub>a</sub> ), che rappresenta l'opacità completa, a 0,0 (0), che rappresenta la trasparenza completa.

Quando si Abilita più di un buffer di colore per il disegno, ogni buffer abilitato viene mescolato separatamente e il contenuto del buffer viene utilizzato per il colore di destinazione. Vedere [**glDrawBuffer**](gldrawbuffer.md).

La fusione ha effetto solo sul rendering RGBA. Viene ignorato dai renderer di indice dei colori.

Le funzioni seguenti consentono di recuperare informazioni correlate a **glBlendFunc**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Blend \_ src

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Blend \_ DST

[**glIsEnabled**](glisenabled.md) con argument GL \_ Blend

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

[**glAlphaFunc**](glalphafunc.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glClear**](glclear.md)
</dt> <dt>

[**glDisable**](gldisable.md)
</dt> <dt>

[**glDrawBuffer**](gldrawbuffer.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glLogicOp**](gllogicop.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> </dl>

 

 





