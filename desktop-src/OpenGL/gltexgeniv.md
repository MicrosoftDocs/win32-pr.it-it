---
title: Funzione glTexGeniv (Gl.h)
description: Controlla la generazione delle coordinate della trama. | Funzione glTexGeniv (Gl.h)
ms.assetid: e95f2844-414a-4fb2-944e-4d0b6e51bdd2
keywords:
- Funzione glTexGeniv OpenGL
topic_type:
- apiref
api_name:
- glTexGeniv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7caffbcf71b09f31fd05c1252471f7da2a66e5bc01e532dfb6c71563545779e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519751"
---
# <a name="gltexgeniv-function"></a>Funzione glTexGeniv

Controlla la generazione delle coordinate della trama.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glTexGeniv(
         GLenum coord,
         GLenum pname,
   const GLint  *params
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Coord* 
</dt> <dd>

Coordinata di trama. Deve essere uno dei seguenti: GL \_ S, GL \_ T, GL \_ R o GL \_ Q.

</dd> <dt>

**Pname** 
</dt> <dd>

Nome simbolico della funzione di generazione delle coordinate della trama.

</dd> <dt>

*params* 
</dt> <dd>

Matrice contenente i coefficienti per la funzione di generazione della trama corrispondente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl>      | *coord* o *pname* non è un valore definito accettato oppure *pname* è GL TEXTURE GEN MODE e params non è \_ un valore definito \_ \_ accettato. <br/> |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md). <br/>                 |



## <a name="remarks"></a>Commenti

La **funzione glTexGen** seleziona una funzione di generazione delle coordinate di trama o fornisce coefficienti per una delle funzioni. Il *parametro coord* fa nome a una delle coordinate di trama (s,t,r,q) e deve essere uno di questi simboli: GL \_ S, GL T, GL R o GL \_ \_ \_ Q. Il *parametro pname* deve essere una delle tre costanti simboliche: GL \_ TEXTURE GEN \_ \_ MODE, GL OBJECT PLANE o GL \_ EYE \_ \_ \_ PLANE. Se *pname è* GL OBJECT PLANE o GL EYE PLANE, il parametro contiene \_ \_ \_ \_ coefficienti per la funzione di generazione della trama corrispondente. 

Se la funzione di generazione della trama è GL \_ OBJECT \_ LINEAR, la funzione

! [Equazione che mostra la funzione glTexGen quando la funzione di generazione della trama GL_OBJECT_LINEAR.]

viene usato, dove g è il valore calcolato per la coordinata denominata in coord; p1, p2, p3 e p4 sono i quattro valori forniti in params. e x?, y?, z?e w? sono le coordinate dell'oggetto del vertice. È possibile usare questa funzione per mappare il terreno usando il livello del mare come piano di riferimento (definito da p1, p2, p3 e p4). La funzione gl OBJECT LINEAR coordinate generation calcola l'altitudine di un vertice del terreno come distanza dal livello del mare. Tale altitudine viene usata per indicizzare l'immagine della trama per mappare la neve bianca sulle cime e l'erboso verde sui pedoni, \_ \_ ad esempio.

Se la funzione di generazione della trama è GL \_ EYE \_ LINEAR, la funzione

! [Equazione che mostra la funzione glTexGen quando la funzione di generazione della trama GL_EYE_LINEAR.]

viene usato, dove

![Equazione che mostra le coordinate oculare del vertice.](images/tex03.png)

e x?, y?, z?e w? sono le coordinate oculare del vertice, p1, p2, p3 e p4 sono i valori forniti in *param* e M è la matrice modelview quando si chiama **glTexGen**. Se M è scarsamente condizionato o singolare, le coordinate di trama generate dalla funzione risultante possono essere imprecise o non definite.

Si noti che i valori in *param* definiscono un piano di riferimento in coordinate oculare. La matrice modelview applicata potrebbe non essere la stessa in vigore quando i vertici del poligono vengono trasformati. Questa funzione stabilisce un campo di coordinate di trama in grado di produrre linee di contorno dinamiche sugli oggetti in movimento.

Se *pname* è GL SPHERE MAP e \_ \_ *coord* è GL S o GL T, le coordinate di trama s e \_ t vengono generate come indicato di \_ seguito. Che u sia il vettore unità che punta dall'origine al vertice del poligono (in coordinate oculari). Lasciare che n sia la normale corrente, dopo la trasformazione in coordinate oculare. Let f = (fx ( ) fy ( ) fz)T essere il vettore di reflection in modo che

![Equazione che mostra il vettore di reflection come funzione del vettore unità e della normale corrente.](images/tex05.png)

Infine, lasciare

![Equazione che mostra m come funzione del vettore di reflection.](images/tex07.png)

I valori assegnati alle coordinate delle trame i e t sono quindi

![Equazione che mostra i valori assegnati alle coordinate delle trame i e t.](images/tex06.png)

È possibile abilitare o disabilitare una funzione di generazione delle coordinate di trama usando [**glEnable**](glenable.md) o [**glDisable**](gldisable.md) con uno dei nomi simbolici delle coordinate di trama (GL \_ TEXTURE GEN \_ \_ S, GL TEXTURE GEN T, GL TEXTURE GEN R o GL TEXTURE GEN Q) come \_ \_ \_ \_ \_ \_ \_ \_ \_ argomento. Quando questa funzione è abilitata, la coordinata di trama specificata viene calcolata in base alla funzione di generazione associata a tale coordinata. Quando questa funzione è disabilitata, i vertici successivi prendono la coordinata di trama specificata dal set corrente di coordinate della trama. Inizialmente, tutte le funzioni di generazione delle trame sono impostate su GL \_ EYE LINEAR e sono \_ disabilitate. Entrambe le equazioni del piano sono (1,0,0,0); entrambe le equazioni del piano t sono (0,1,0,0); e tutte le equazioni del piano r e q sono (0,0,0,0).

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

 

 





