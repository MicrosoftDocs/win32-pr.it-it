---
title: Funzione glTexGenf (Gl.h)
description: Controlla la generazione delle coordinate della trama. | Funzione glTexGenf (Gl.h)
ms.assetid: 43439d34-46df-49c6-8c19-09db9f005520
keywords:
- Funzione glTexGenf OpenGL
topic_type:
- apiref
api_name:
- glTexGenf
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1198da9d87e79f8e3abb923ac2f5ce48ad5afc8cb06d4d97bcf40a3153367e72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119490381"
---
# <a name="gltexgenf-function"></a>Funzione glTexGenf

Controlla la generazione delle coordinate della trama.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glTexGenf(
   GLenum  coord,
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Coord* 
</dt> <dd>

Coordinata della trama. Deve essere uno dei seguenti: GL \_ S, GL \_ T, GL \_ R o GL \_ Q.

</dd> <dt>

**Pname** 
</dt> <dd>

Nome simbolico della funzione di generazione delle coordinate di trama.

</dd> <dt>

*param* 
</dt> <dd>

Un singolo parametro di generazione della trama con valore, uno tra GL \_ OBJECT \_ LINEAR, GL \_ EYE LINEAR o GL SPHERE \_ \_ \_ MAP.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ \_ NON VALIDA**</dt> </dl>      | *coord* o *pname* non è un valore definito accettato oppure *pname* è GL TEXTURE GEN MODE e params non è \_ un valore definito \_ \_ accettato. <br/> |
| <dl> <dt>**ENUMERAZIONE GL \_ \_ NON VALIDA**</dt> </dl>      | *pname* era GL \_ TEXTURE \_ GEN \_ MODE, *params* era GL \_ SPHERE MAP e \_ *coord* era GL \_ R o GL \_ Q<br/>                                     |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md). <br/>                 |



## <a name="remarks"></a>Commenti

La **funzione glTexGen** seleziona una funzione di generazione delle coordinate della trama o fornisce i coefficienti per una delle funzioni. Il *parametro coord* specifica una delle coordinate di trama (s,t,r,q) e deve essere uno di questi simboli: GL \_ S, GL T, GL R o GL \_ \_ \_ Q. Il *parametro pname* deve essere una delle tre costanti simboliche seguenti: GL \_ TEXTURE GEN \_ \_ MODE, GL OBJECT PLANE o GL \_ EYE \_ \_ \_ PLANE. Se *pname* è GL TEXTURE GEN MODE, param specifica una modalità, una tra \_ GL OBJECT \_ \_  \_ \_ LINEAR, GL EYE LINEAR o GL \_ SPHERE \_ \_ \_ MAP. Se *pname* è GL \_ OBJECT PLANE o GL EYE \_ \_ \_ PLANE, il *parametro* contiene i coefficienti per la funzione di generazione della trama corrispondente.

Se la funzione di generazione della trama è GL \_ OBJECT \_ LINEAR, la funzione

! [Equazione che mostra la funzione glTexGen quando la funzione di generazione della trama è GL_OBJECT_LINEAR.]

viene usato , dove g è il valore calcolato per la coordinata denominata in coord; p1, p2, p3 e p4 sono i quattro valori specificati in params; e x?, y?, z? e w? sono le coordinate dell'oggetto del vertice. È possibile usare questa funzione per mappare il terreno usando il livello del mare come piano di riferimento (definito da p1, p2, p3 e p4). La funzione di generazione delle coordinate GL OBJECT LINEAR calcola l'altitudine di un vertice del terreno come distanza dal livello del mare. Tale altitudine viene usata, ad esempio, per indicizzare l'immagine della trama per mappare la nevicata bianca sui picchi e il terreno verde sui \_ \_ pedoni.

Se la funzione di generazione della trama è GL \_ EYE \_ LINEAR, la funzione

! [Equazione che mostra la funzione glTexGen quando la funzione di generazione della trama è GL_EYE_LINEAR.]

viene usato , dove

![Equazione che mostra le coordinate oculare del vertice.](images/tex03.png)

e x?, y?, z? e w? sono le coordinate oculare del vertice, p1, p2, p3 e p4 sono i valori forniti nel *parametro* e M è la matrice della visualizzazione modelli quando si chiama **glTexGen.** Se M è scarsamente condizionato o singolare, le coordinate di trama generate dalla funzione risultante possono essere imprecise o indefinite.

Si noti che i valori nel *parametro definiscono* un piano di riferimento nelle coordinate oculare. La matrice della visualizzazione modello applicata potrebbe non essere la stessa in vigore quando i vertici del poligono vengono trasformati. Questa funzione stabilisce un campo di coordinate di trama in grado di produrre linee di contorno dinamiche sugli oggetti in movimento.

Se *pname* è GL \_ SPHERE MAP e \_ *coord* è GL S o GL T, le coordinate di trama s e \_ t vengono generate come \_ segue. Lasciare che u sia il vettore unità che punta dall'origine al vertice poligono (nelle coordinate oculari). Lasciare che n sia la normale corrente, dopo la trasformazione in coordinate oculare. Lasciare che f = (fx ( ) fy ( ) fz)T sia il vettore di reflection in modo che

![Equazione che mostra il vettore di reflection come funzione del vettore unità e della normale corrente.](images/tex05.png)

Infine,

![Equazione che mostra m come funzione del vettore di reflection.](images/tex07.png)

I valori assegnati alle coordinate delle trame i e t sono quindi

![Equazione che mostra i valori assegnati alle coordinate delle trame i e t.](images/tex06.png)

È possibile abilitare o disabilitare una funzione di generazione delle coordinate di trama usando [**glEnable**](glenable.md) o [**glDisable**](gldisable.md) con uno dei nomi simbolici delle coordinate di trama (GL \_ TEXTURE GEN \_ \_ S, GL TEXTURE GEN T, GL TEXTURE GEN R o \_ GL TEXTURE GEN \_ \_ \_ \_ \_ \_ \_ \_ Q) come argomento. Quando questa funzione è abilitata, la coordinata di trama specificata viene calcolata in base alla funzione di generazione associata a tale coordinata. Quando questa funzione è disabilitata, i vertici successivi prendono la coordinata di trama specificata dal set corrente di coordinate della trama. Inizialmente, tutte le funzioni di generazione della trama sono impostate su GL \_ EYE LINEAR e sono \_ disabilitate. Entrambe le equazioni del piano sono (1,0,0,0); entrambe le equazioni del piano t sono (0,1,0,0); e tutte le equazioni del piano r e q sono (0,0,0,0).

Le funzioni seguenti recuperano informazioni correlate a glTexGen:

<dl>

[**glGetTexGen**](glgettexgen.md)  
[**glIsEnabled con**](glisenabled.md) argomento GL \_ TEXTURE GEN \_ \_ S  
[**glIsEnabled con**](glisenabled.md) argomento GL \_ TEXTURE GEN \_ \_ T  
[**glIsEnabled con**](glisenabled.md) argomento GL \_ TEXTURE GEN \_ \_ R  
[**glIsEnabled con**](glisenabled.md) argomento GL \_ TEXTURE GEN \_ \_ Q  
</dl>

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

[**glCopyTexImage2D**](glcopyteximage2d.md)
</dt> <dt>

[**glCopyTexSubImage2D**](glcopytexsubimage2d.md)
</dt> <dt>

[**glGetTexGen**](glgettexgen.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[glTexEnv](gltexenv-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[glTexParameter](gltexparameter-functions.md)
</dt> <dt>

[**glTexSubImage1D**](gltexsubimage1d.md)
</dt> <dt>

[**glTexSubImage2D**](gltexsubimage2d.md)
</dt> </dl>

 

 





