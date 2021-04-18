---
title: funzione glArrayElement (GL. h)
description: La funzione glArrayElement specifica gli elementi della matrice usati per eseguire il rendering di un vertice.
ms.assetid: 2c4d76bb-e4c9-4baa-a190-66298b8a4335
keywords:
- funzione glArrayElement OpenGL
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
ms.openlocfilehash: 6a20aff9fcaa5bf922bc9447f7b7022a8cd1a9c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301804"
---
# <a name="glarrayelement-function"></a>glArrayElement (funzione)

La funzione **glArrayElement** specifica gli elementi della matrice usati per eseguire il rendering di un vertice.

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

Usare la funzione **glArrayElement** all'interno delle coppie [**glBegin**](glbegin.md) e [**glEnd**](glend.md) per specificare i dati dei vertici e degli attributi per le primitive di punti, linee e poligoni. La funzione **glArrayElement** specifica i dati per un singolo vertice usando i dati dei vertici e degli attributi posizionati in corrispondenza dell' *Indice* delle matrici di vertici abilitate.

È possibile utilizzare **glArrayElement** per costruire primitive indicizzando i dati dei vertici, anziché tramite la trasmissione di matrici di dati nell'ordine da primo a ultimo. Poiché **glArrayElement** specifica solo un singolo vertice, è possibile specificare in modo esplicito gli attributi per le singole primitive. Ad esempio, è possibile impostare un singolo normale per ogni singolo triangolo.

Quando si includono chiamate a **glArrayElement** negli elenchi di visualizzazione, i dati di matrice necessari, determinati dai puntatori di matrice e abilitano i valori, vengono immessi anche nell'elenco di visualizzazione. Il puntatore di matrice e i valori di abilitazione vengono determinati quando vengono creati gli elenchi di visualizzazione, non quando vengono eseguiti gli elenchi di visualizzazione.

È possibile leggere e memorizzare nella cache dati di matrici statici in qualsiasi momento con **glArrayElement**. Quando si modificano gli elementi di una matrice statica senza specificare nuovamente la matrice, i risultati di tutte le chiamate successive a **glArrayElement** non sono definiti.

Quando si chiama **glArrayElement** senza prima chiamare **glEnableClientState**( \_ matrice di vertici GL \_ ), non viene eseguito alcun disegno, ma gli attributi corrispondenti alle matrici abilitate vengono modificati. Sebbene non venga generato alcun errore quando si specifica una matrice all'interno di **glBegin** e di coppie **glEnd** , i risultati non sono definiti.

> [!Note]  
> La funzione **glArrayElement** è disponibile solo in OpenGL versione 1,1 o successiva.

 

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

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnableClientState**](glenableclientstate.md)
</dt> <dt>

[**Remo**](glend.md)
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

 

 





