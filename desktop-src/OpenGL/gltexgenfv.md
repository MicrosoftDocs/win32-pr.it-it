---
title: funzione glTexGenfv (GL. h)
description: Controlla la generazione delle coordinate di trama. | funzione glTexGenfv (GL. h)
ms.assetid: d5454d6f-16bb-47d9-9c52-da2daf491224
keywords:
- funzione glTexGenfv OpenGL
topic_type:
- apiref
api_name:
- glTexGenfv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4d5394b6385246f296a472ce51f2727e2738845
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104561039"
---
# <a name="gltexgenfv-function"></a>glTexGenfv (funzione)

Controlla la generazione delle coordinate di trama.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glTexGenfv(
         GLenum  coord,
         GLenum  pname,
   const GLfloat *params
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Coord* 
</dt> <dd>

Coordinata di trama. Deve essere uno dei seguenti: GL \_ S, GL \_ T, GL \_ R o GL \_ Q.

</dd> <dt>

**pname** 
</dt> <dd>

Nome simbolico della funzione di generazione delle coordinate di trama.

</dd> <dt>

*params* 
</dt> <dd>

Matrice di float che contiene i coefficienti per la funzione di generazione della trama corrispondente.

``` syntax
GLfloat zPlane[] = { 0.0f, 0.0f, 1.0f, 0.0f };
```

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | *Coord* o *pname* non è un valore definito accettato oppure *pname* è la \_ \_ modalità di generazione della trama GL \_ e *params* non è un valore definito accettato.<br/> |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md). <br/>                 |



## <a name="remarks"></a>Commenti

La funzione **glTexGen** seleziona una funzione di generazione della coordinata di trama o fornisce coefficienti per una delle funzioni. Il parametro *Coord* denomina una delle coordinate di trama (s, t, r, q) e deve essere uno dei simboli seguenti: GL \_ s, GL \_ t, GL \_ r o GL \_ q. Il parametro *pname* deve essere una delle tre costanti simboliche, ovvero la \_ modalità gen della trama GL, il piano dell' \_ \_ oggetto GL o il \_ \_ piano GL \_ Eye \_ . Se *pname* è un piano \_ di oggetti GL \_ o \_ \_ un piano con occhio GL, *param* contiene coefficienti per la funzione di generazione della trama corrispondente.

Se la funzione di generazione della trama è un \_ oggetto GL \_ lineare, la funzione

! [Equazione che mostra la funzione glTexGen quando la funzione di generazione della trama è GL_OBJECT_LINEAR.]

viene usato, dove g è il valore calcolato per la coordinata denominata in Coord; P1, P2, P3 e P4 sono i quattro valori specificati nei parametri; e x?, y?, z? e w? sono le coordinate dell'oggetto del vertice. È possibile usare questa funzione per mappare il terreno usando il livello Sea come piano di riferimento (definito da P1, P2, P3 e P4). La \_ \_ funzione di generazione delle coordinate lineari dell'oggetto GL calcola l'altitudine di un vertice del terreno come distanza dal livello Sea. tale altitudine viene utilizzata per indicizzare l'immagine della trama per eseguire il mapping della neve bianca ai picchi e all'erba verde sui piedi, ad esempio.

Se la funzione di generazione della trama è GL \_ Eye \_ lineare, la funzione

! [Equazione che mostra la funzione glTexGen quando la funzione di generazione della trama è GL_EYE_LINEAR.]

viene usato, dove

![Equazione che mostra le coordinate oculari del vertice.](images/tex03.png)

e x?, y?, z? e w? sono le coordinate oculari dei vertici, P1, P2, P3 e P4 sono i valori specificati in *param* e M è la matrice Modelview quando si chiama **glTexGen**. Se M è scarsamente condizionato o singolare, le coordinate di trama generate dalla funzione risultante possono non essere accurate o indefinite.

Si noti che i valori in *param* definiscono un piano di riferimento in coordinate oculari. La matrice Modelview applicata a esse potrebbe non essere la stessa in vigore quando i vertici del poligono sono trasformati. Questa funzione stabilisce un campo di coordinate di trama che può produrre linee di contorno dinamiche sullo stato degli oggetti.

Se *pname* è \_ \_ una mappa GL Sphere e *Coord* è GL \_ S o GL \_ T, le coordinate di trama S e T vengono generate come indicato di seguito. Consentire a u il vettore di unità che punta dall'origine al vertice del poligono (in coordinate oculari). Let n è il normale corrente, dopo la trasformazione in coordinate oculari. Let f = (FX () FY () FZ) T è il vettore di reflection in modo che

![Equazione che mostra il vettore di reflection come funzione del vettore di unità e della normale corrente.](images/tex05.png)

Infine, Let

![Equazione che Mostra m come funzione del vettore di Reflection.](images/tex07.png)

Quindi i valori assegnati alle coordinate di trama i e t sono

![Equazione che mostra i valori assegnati alle coordinate di trama i e t.](images/tex06.png)

È possibile abilitare o disabilitare una funzione di generazione della coordinata di trama usando [**glEnable**](glenable.md) o [**glDisable**](gldisable.md) con uno dei nomi di coordinati di trama simbolici (GL texture gen \_ \_ \_ S, GL \_ texture \_ gen \_ T, GL \_ texture \_ gen \_ R o GL \_ texture \_ gen \_ Q) come argomento. Quando questa funzione è abilitata, la coordinata di trama specificata viene calcolata in base alla funzione di generazione associata a tale coordinata. Quando questa funzione è disabilitata, i vertici successivi accettano la coordinata di trama specificata dal set corrente di coordinate di trama. Inizialmente, tutte le funzioni di generazione di trama sono impostate su GL \_ Eye \_ Linear e sono disabilitate. Entrambe le equazioni del piano s sono (1, 0, 0, 0); entrambe le equazioni del piano t sono (0, 1, 0, 0); e tutte le equazioni del piano r e q sono (0, 0, 0, 0).

Le funzioni seguenti consentono di recuperare informazioni correlate a glTexGen:

<dl>

[**glGetTexGen**](glgettexgen.md)  
[**glIsEnabled**](glisenabled.md) con argomento GL \_ texture \_ gen \_ S  
[**glIsEnabled**](glisenabled.md) con argomento GL \_ texture \_ gen \_ T  
[**glIsEnabled**](glisenabled.md) con argomento GL \_ texture \_ gen \_ R  
[**glIsEnabled**](glisenabled.md) con argomento GL \_ texture \_ gen \_ Q  
</dl>

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

 

 





