---
title: Funzione glBlendFunc (Gl.h)
description: La funzione glBlendFunc specifica l'aritmetica dei pixel.
ms.assetid: 6756774b-5eef-419a-a653-0b251aed65a0
keywords:
- Funzione glBlendFunc OpenGL
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
ms.openlocfilehash: 2e4b079d0eb83f401eb7e906cb399fab18e5b2fd22f06299fcc62b1e6b4a02e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082131"
---
# <a name="glblendfunc-function"></a>Funzione glBlendFunc

La **funzione glBlendFunc** specifica l'aritmetica dei pixel.

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

Specifica il modo in cui vengono calcolati i fattori di fusione di origine rosso, verde, blu e alfa. Sono accettate nove costanti simboliche: GL \_ ZERO, GL \_ ONE, GL \_ \_ DST COLOR, GL \_ ONE MINUS \_ \_ DST \_ COLOR, GL \_ \_ SRC ALPHA, GL \_ ONE MINUS \_ \_ SRC \_ ALPHA, GL \_ DST \_ ALPHA, GL ONE MINUS DST ALPHA e GL \_ \_ \_ \_ \_ SRC \_ ALPHA \_ SATURATE.

</dd> <dt>

*dfactor* 
</dt> <dd>

Specifica il modo in cui vengono calcolati i fattori di fusione della destinazione rosso, verde, blu e alfa. Sono accettate otto costanti simboliche: GL \_ ZERO, GL \_ ONE, GL \_ SRC \_ COLOR, GL \_ ONE MINUS \_ \_ SRC \_ COLOR, GL \_ SRC \_ ALPHA, GL ONE MINUS \_ \_ \_ SRC \_ ALPHA, GL DST ALPHA e GL ONE MINUS \_ \_ \_ \_ \_ DST \_ ALPHA.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ \_ NON VALIDA**</dt> </dl>      | *Sfactor o* *dfactor* non è un valore accettato.<br/>                                                                   |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

In modalità RGB i pixel possono essere disegnati usando una funzione che combina i valori RGBA in ingresso (di origine) con i valori RGBA già presenti nel framebuffer (i valori di destinazione). Per impostazione predefinita, la fusione è disabilitata. Usare [**glEnable e**](glenable.md) [**glDisable con**](gldisable.md) l'argomento GL BLEND per abilitare e \_ disabilitare la fusione.

Se abilitata, **glBlendFunc** definisce l'operazione di fusione. Il *parametro sfactor* specifica quale dei nove metodi viene usato per ridimensionare i componenti di colore di origine. Il *parametro dfactor* specifica quale degli otto metodi viene usato per ridimensionare i componenti di colore di destinazione. Gli 11 metodi possibili sono descritti nella tabella seguente. Ogni metodo definisce quattro fattori di scala, uno per rosso, verde, blu e alfa.

Nella tabella e nelle equazioni successive i componenti dei colori di origine e di destinazione sono definiti (*R*? , *G*? , *B*? , *a*? ) e (*R*<sub>d</sub> , *G*<sub>d</sub> , *B*<sub>d</sub> , *A*<sub>d</sub> ). Si è compreso che hanno valori interi compresi tra zero e (*k*<sub>R</sub> , *k*<sub>G</sub> , *k*<sub>R</sub> , *k*<sub>A</sub> ), dove

*k*<sub>R</sub> = 2 <sup>m</sup>*R* - 1

*k*<sub>G</sub> = 2 <sup>m</sup>*G* - 1

*k*<sub>B</sub> = 2 <sup>m</sup>*B* - 1

*k*<sub>A</sub> = 2 <sup>m</sup>*A* - 1

e (*m*<sub>R</sub> , *m*<sub>G</sub> , *m*<sub>B</sub> , *m*<sub>A</sub> ) è il numero di bitplani rosso, verde, blu e alfa.

I fattori di scala di origine e destinazione sono definiti (*s*<sub>R</sub> , *s*<sub>G</sub> , *s*<sub>B</sub> , *s*<sub>A</sub> ) e (*d*<sub>R</sub> , *d*<sub>G</sub> , *d*<sub>B</sub> , *d*<sub>A</sub> ). I fattori di scala descritti nella tabella, indicato (*f*<sub>R</sub> , *f*<sub>G</sub> , *f*<sub>B</sub> , *f*<sub>A</sub> ), rappresentano i fattori di origine o di destinazione. Tutti i fattori di scala hanno un intervallo \[ di 0,1 \] .



| Parametro                  | (*f*<sub>R</sub>  , *f*<sub>G</sub>  , *f*<sub>B</sub>  , *f*<sub>A</sub>  )                                                                                 |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GL \_ ZERO                   | (0,0,0,0)                                                                                                                                                    |
| GL \_ ONE                    | (1,1,1,1)                                                                                                                                                    |
| COLORE \_ GL \_ SRC             | (*R*? / *k*<sub>R</sub> , *G*? / *k*<sub>G</sub> , *B*? / *k*<sub>B</sub> , *A*? / *k*<sub>A</sub> )                                                         |
| GL \_ ONE \_ MINUS \_ SRC \_ COLOR | (1,1,1,1) - (*R*? / *k*<sub>R</sub> , *G*? / *k*<sub>G</sub> , *B*? / *k*<sub>B</sub> , *A*? / *k*<sub>A</sub> )                                             |
| COLORE \_ ORA LEGALE GL \_             | (*R*<sub>d</sub>  /  *k*<sub>R</sub> , *G*<sub>d</sub>  /  *k*<sub>G</sub> , *B*<sub>d</sub>  /  *k*<sub>B</sub> , *A*<sub>d</sub>  /  *k*<sub>A</sub> )             |
| GL \_ ONE \_ MINUS \_ DST \_ COLOR | (1,1,1,1) - (*R*<sub>d</sub>  /  *k*<sub>R</sub> , *G*<sub>d</sub>  /  *k*<sub>G</sub> , *B*<sub>d</sub>  /  *k*<sub>B</sub> , *A*<sub>d</sub>  /  *k*<sub>A</sub> ) |
| GL \_ SRC \_ ALPHA             | (*A*? / *k*<sub>A</sub> , *A*? / *k*<sub>A</sub> , *A*? / *k*<sub>A</sub> , *A*? / *k*<sub>A</sub> )                                                         |
| GL \_ ONE \_ MINUS \_ SRC \_ ALPHA | (1,1,1,1) - (*A*? / *k*<sub>A</sub> , *A*? / *k*<sub>A</sub> , *A*? / *k*<sub>A</sub> , *A*? / *k*<sub>A</sub> )                                             |
| GL \_ DST \_ ALPHA             | (*A*<sub>d</sub>  /  *k*<sub>A</sub> , *A*<sub>d</sub>  /  *k*<sub>A</sub> , *A*<sub>d</sub>  /  *k*<sub>A</sub> , *A*<sub>d</sub>  /  *k*<sub>A</sub> )             |
| GL \_ ONE \_ MINUS \_ DST \_ ALPHA | (1,1,1,1) - (*A*<sub>d</sub>  /  *k*<sub>A</sub> , *A*<sub>d</sub>  /  *k*<sub>A</sub> , *A*<sub>d</sub>k A , A d  /  *k*<sub>A</sub> , *A*<sub>d</sub>  /  *k*<sub>A</sub> ) |
| GL \_ SRC \_ ALPHA \_ SATURATE   | (*i,i,i,* 1)                                                                                                                                                 |



 

Nella tabella,

*i* = min (*A*? , *k*<sub>A</sub>   -  *d*<sub></sub> ) / *k*<sub>A</sub>

Per determinare i valori RGBA misti di un pixel durante il disegno in modalità RGBA, il sistema usa le equazioni seguenti:

*R* (*d*) = min( *k*<sub>R</sub> , *R*? *s*<sub>R</sub>  +  *d*<sub>d</sub> <sub>R</sub> )

*G* (*d*) = min( *k*<sub>G</sub> , *G*? *s*<sub>G</sub>  +  *G*<sub>d</sub> <sub>G )</sub>

*B* (*d*) = min( *k*<sub>B</sub> *, B*? *s*<sub>B</sub>  +  <sub>d</sub> *d*<sub>B</sub> )

*A* (*d*) = min( *k*<sub>A</sub> , *A*? *s*<sub>A</sub>  +  *D*<sub>d</sub> <sub>A )</sub>

Nonostante l'apparente precisione delle equazioni precedenti, la fusione aritmetica non è esattamente specificata, perché la fusione funziona con valori di colore integer imprecisi. Tuttavia, un fattore di blend che deve essere uguale a uno non ne modifica la moltiplicazione e un fattore di blend uguale a zero ne riduce la moltiplicazione a zero. Di conseguenza, ad esempio, quando *sfactor* è GL \_ SRC \_ ALPHA, *dfactor* è GL \_ ONE MINUS \_ SRC ALPHA e A ? è \_ uguale \_  <sub></sub>a k A , le equazioni si riducono alla sostituzione semplice:

*R*<sub>d</sub>  =  *R*?

*G*<sub>d</sub>  =  *G*?

B <sub>d</sub>  =  *B*?

*A*<sub>d</sub>  =  *A*?

## <a name="examples"></a>Esempio

La trasparenza è implementata meglio usando **glBlendFunc**(GL \_ SRC \_ ALPHA, GL \_ ONE MINUS \_ SRC ALPHA) con \_ primitive ordinate dal più lontano \_ al più vicino. Si noti che questo calcolo della trasparenza non richiede la presenza di bitplane alfa nel buffer frame.

È anche possibile usare **glBlendFunc**(GL SRC ALPHA, GL ONE MINUS SRC ALPHA) per il rendering di punti e linee \_ \_ \_ \_ \_ \_ antialias in ordine arbitrario.

Per ottimizzare l'antialiasing dei poligoni, usare **glBlendFunc**(GL \_ SRC \_ ALPHA \_ SATURATE, GL ONE) con i poligoni ordinati dal più vicino al più \_ lontano. (Vedere il gl \_ Argomento POLYGON \_ SMOOTH in [**glEnable per**](glenable.md) informazioni sull'antialiasing dei poligoni. I bitplani alfa di destinazione, che devono essere presenti per il corretto funzionamento di questa funzione blend, archiviano la copertura accumulata.

Il valore alfa in ingresso (di origine) è un'opacità materiale, compresa tra 1,0 *(K*<sub>A),</sub> che rappresenta l'opacità completa, e 0,0 (0), che rappresenta la trasparenza completa.

Quando si abilita più di un buffer colori per il disegno, ogni buffer abilitato viene misto separatamente e il contenuto del buffer viene utilizzato per il colore di destinazione. Vedere [**glDrawBuffer.**](gldrawbuffer.md)

La fusione influisce solo sul rendering RGBA. Viene ignorato dai renderer dell'indice colori.

Le funzioni seguenti recuperano informazioni correlate **a glBlendFunc:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ BLEND \_ SRC

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ BLEND \_ DST

[**glIsEnabled con**](glisenabled.md) argomento GL \_ BLEND

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

 

 





