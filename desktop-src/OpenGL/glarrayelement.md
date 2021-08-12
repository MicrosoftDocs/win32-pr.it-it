---
title: Funzione glArrayElement (Gl.h)
description: La funzione glArrayElement specifica gli elementi della matrice usati per eseguire il rendering di un vertice.
ms.assetid: 2c4d76bb-e4c9-4baa-a190-66298b8a4335
keywords:
- Funzione glArrayElement OpenGL
topic_type:
- apiref
api_name:
- glArrayElement
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb6fdf3b90c5145c46730e530f26ba7d4f7f3875e51cc4d510e9763d03e27207
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118618060"
---
# <a name="glarrayelement-function"></a>Funzione glArrayElement

La **funzione glArrayElement** specifica gli elementi della matrice usati per eseguire il rendering di un vertice.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glArrayElement(
   GLint index
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*index* 
</dt> <dd>

Indice nelle matrici abilitate.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Usare la **funzione glArrayElement** all'interno delle coppie [**glBegin**](glbegin.md) e [**glEnd**](glend.md) per specificare i dati dei vertici e degli attributi per le primitive punto, linea e poligono. La **funzione glArrayElement** specifica i dati per un singolo vertice usando i dati dei vertici e degli attributi che si trovano in corrispondenza dell'indice  delle matrici di vertici abilitate.

È possibile usare **glArrayElement** per costruire primitive indicizzando i dati dei vertici, anziché tramite lo streaming di matrici di dati in ordine primo-ultimo. Poiché **glArrayElement** specifica un solo vertice, è possibile specificare in modo esplicito gli attributi per le singole primitive. Ad esempio, è possibile impostare una singola normale per ogni singolo triangolo.

Quando si includono chiamate a **glArrayElement** negli elenchi di visualizzazione, nell'elenco di visualizzazione vengono immessi anche i dati di matrice necessari, determinati dai puntatori di matrice e dai valori di abilitazione. I valori di puntatore di matrice e abilitazione vengono determinati quando vengono creati elenchi di visualizzazione, non quando vengono eseguiti gli elenchi di visualizzazione.

È possibile leggere e memorizzare nella cache i dati della matrice statica in qualsiasi momento **con glArrayElement**. Quando si modificano gli elementi di una matrice statica senza specificare di nuovo la matrice, i risultati delle chiamate successive a **glArrayElement** non sono definiti.

Quando si chiama **glArrayElement** senza prima chiamare **glEnableClientState**(GL VERTEX ARRAY), non viene eseguito alcun disegno, ma gli attributi corrispondenti alle \_ \_ matrici abilitate vengono modificati. Anche se non viene generato alcun errore quando si specifica una matrice all'interno delle coppie **glBegin** **e glEnd,** i risultati non sono definiti.

> [!Note]  
> La **funzione glArrayElement** è disponibile solo in OpenGL versione 1.1 o successiva.

 

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

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnableClientState**](glenableclientstate.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





