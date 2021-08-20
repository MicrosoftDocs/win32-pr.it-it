---
title: Metodo IDCompositionMatrixTransform SetMatrixElement(int, int, IDCompositionAnimation)
description: Aggiunge un'animazione al valore di un elemento della matrice di questa trasformazione 2D.
ms.assetid: 16A9E136-5F0C-4F34-A127-BF06C4530499
keywords:
- Metodo SetMatrixElement DirectComposition
- Metodo SetMatrixElement DirectComposition, interfaccia IDCompositionMatrixTransform
- Interfaccia IDCompositionMatrixTransform DirectComposition, metodo SetMatrixElement
topic_type:
- apiref
api_name:
- IDCompositionMatrixTransform.SetMatrixElement
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6c5a0813243f3d04a729f000c9e42a1eb1ade6406273a1217ca067d8e2f1c3a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043219"
---
# <a name="idcompositionmatrixtransformsetmatrixelementint-int-idcompositionanimation-method"></a>Metodo IDCompositionMatrixTransform::SetMatrixElement(int, int, \* IDCompositionAnimation)

Aggiunge un'animazione al valore di un elemento della matrice di questa trasformazione 2D.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetMatrixElement(
  [in] int                    row,
  [in] int                    column,
  [in] IDCompositionAnimation *animation
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*riga* \[ Pollici\]
</dt> <dd>

Indice di riga dell'elemento da modificare. Questo valore deve essere compreso tra 0 e 2 inclusi.

</dd> <dt>

*column* \[ Pollici\]
</dt> <dd>

Indice di colonna dell'elemento da modificare. Questo valore deve essere compreso tra 0 e 1, inclusi.

</dd> <dt>

*animazione* \[ Pollici\]
</dt> <dd>

Animazione che rappresenta il modo in cui il valore dell'elemento specificato cambia nel tempo. Questo parametro non deve essere NULL.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce S \_ OK. In caso contrario, restituisce un **codice di errore HRESULT.** Per un elenco di codici di errore, vedere Codici di errore [DirectComposition.](directcomposition-error-codes.md)

## <a name="remarks"></a>Commenti

Questo metodo crea una copia dell'animazione specificata. Se l'oggetto a cui fa riferimento il parametro *di* animazione viene modificato dopo la chiamata a questo metodo, la modifica non influisce sull'elemento a meno che questo metodo non venga chiamato nuovamente. Se l'elemento è stato animato in precedenza, la chiamata a questo metodo sostituisce l'animazione precedente con la nuova animazione.

Questo metodo ha esito negativo *se l'animazione* è un puntatore non valido o se non è stata creata dalla stessa interfaccia [**IDCompositionDevice**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) della trasformazione interessata. L'interfaccia non può essere un'implementazione personalizzata. solo le interfacce create da Microsoft DirectComposition possono essere usate con questo metodo.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDCompositionMatrixTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform)
</dt> </dl>

 

 