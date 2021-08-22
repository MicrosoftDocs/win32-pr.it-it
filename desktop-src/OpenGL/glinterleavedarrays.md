---
title: Funzione glInterleavedArrays (Gl.h)
description: La funzione glInterleavedArrays specifica e abilita simultaneamente diverse matrici interleaved in una matrice di aggregazione più grande.
ms.assetid: f1133949-d755-43e3-bf29-8e4c7fb17980
keywords:
- Funzione glInterleavedArrays OpenGL
topic_type:
- apiref
api_name:
- glInterleavedArrays
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce3b37186614fa431585c1e5a932edab946afd6d881ba1cf8eb5c5690220f603
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118938562"
---
# <a name="glinterleavedarrays-function"></a>Funzione glInterleavedArrays

La **funzione glInterleavedArrays** specifica e abilita simultaneamente diverse matrici interleaved in una matrice di aggregazione più grande.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glInterleavedArrays(
         GLenum  format,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*format* 
</dt> <dd>

Tipo di matrice da abilitare. Il parametro può presupporre uno dei valori simbolici seguenti: GL \_ V2F, GL \_ V3F, GL \_ C4UB \_ V2F, GL \_ C4UB \_ V3F, GL \_ C3F \_ V3F, \_ GL \_ N3F V3F, GL \_ C4F \_ \_ N3F V3F, GL \_ T2F \_ V3F, GL \_ T4F \_ V4F, GL \_ T2F \_ C4UB \_ V3F, GL \_ T2F \_ \_ C3F V3F, GL \_ T2F \_ N3F \_ V3F, GL \_ T2F \_ C4F \_ \_ N3F V3F o GL \_ T4F \_ C4F \_ \_ N3F V4F.

</dd> <dt>

*Passo* 
</dt> <dd>

Offset in byte tra ogni elemento della matrice di aggregazione.

</dd> <dt>

*indicatore di misura* 
</dt> <dd>

Puntatore al primo elemento di una matrice di aggregazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl>      | *format* non è un valore accettato.<br/>                                                                                        |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | *stride* è un valore negativo.<br/>                                                                                             |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

Con la funzione **glInterleavedArrays** è possibile specificare e abilitare contemporaneamente diverse matrici di colori interleaved, normali, trame e vertici i cui elementi fanno parte di un elemento di matrice di aggregazione più grande. Per alcune architetture di memoria, questa operazione è più efficiente rispetto alla specifica delle matrici separatamente.

Se il *parametro stride* è zero, gli elementi della matrice di aggregazione vengono archiviati consecutivamente; in caso *contrario, i byte* stride si verificano tra gli elementi della matrice aggregata.

Il *parametro format* funge da chiave che descrive come estrarre singole matrici dalla matrice di aggregazione:

-   Se *format* contiene una T, le coordinate della trama vengono estratte dalla matrice interleaved.
-   Se C è presente, vengono estratti i valori dei colori.
-   Se N è presente, vengono estratte le coordinate normali.
-   Le coordinate dei vertici vengono sempre estratte.
-   Le cifre 2, 3 e 4 indicano il numero di valori estratti.
-   F indica che i valori vengono estratti come valori a virgola mobile.
-   Se 4UB segue C, i colori possono essere estratti anche come 4 byte senza segno. Se un colore viene estratto come 4 byte senza segno, l'elemento della matrice di vertici che segue si trova in corrispondenza del primo possibile indirizzo allineato a virgola mobile.

Se si chiama **glInterleavedArrays** durante la compilazione di un elenco di visualizzazione, non viene compilato nell'elenco, ma viene eseguito immediatamente.

Non è possibile includere chiamate **a glInterleavedArrays** in **glDisableClientState** tra le chiamate a [**glBegin**](glbegin.md) e la chiamata corrispondente a **glEnd**.

> [!Note]  
> La **funzione glInterleavedArrays** è disponibile solo in OpenGL versione 1.1 o successiva.

 

La **funzione glInterleavedArrays** viene implementata sul lato client senza protocollo. Poiché i parametri della matrice dei vertici sono sullo stato lato client, non vengono salvati o ripristinati da [**glPushAttrib**](glpushattrib.md) e **glPopAttrib**. Usare [**invece glPushClientAttrib**](glpushclientattrib.md) **e glPopClientAttrib.**

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

[**glArrayElement**](glarrayelement.md)
</dt> <dt>

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glDrawElements**](gldrawelements.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnableClientState**](glenableclientstate.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**glPushClientAttrib**](glpushclientattrib.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





