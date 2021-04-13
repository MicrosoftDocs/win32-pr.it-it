---
title: Metodo IDCompositionMatrixTransform sematrixelement (int, int, IDCompositionAnimation)
description: Aggiunge un'animazione al valore di un elemento della matrice di questa trasformazione 2D.
ms.assetid: 16A9E136-5F0C-4F34-A127-BF06C4530499
keywords:
- Metodo sematrixelement DirectComposition
- Metodo sematrixelement DirectComposition, interfaccia IDCompositionMatrixTransform
- Interfaccia IDCompositionMatrixTransform DirectComposition, metodo sematrixelement
topic_type:
- apiref
api_name:
- IDCompositionMatrixTransform.SetMatrixElement
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5b4bf2a43e762b85b8b8cfd0c15468b3dc438221
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399458"
---
# <a name="idcompositionmatrixtransformsetmatrixelementint-int-idcompositionanimation-method"></a>Metodo IDCompositionMatrixTransform:: sematrixelement (int, int, IDCompositionAnimation \* )

Aggiunge un'animazione al valore di un elemento della matrice di questa trasformazione 2D.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetMatrixElement(
  [in] int                    row,
  [in] int                    column,
  [in] IDCompositionAnimation *animation
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*riga* \[ di in\]
</dt> <dd>

Indice di riga dell'elemento da modificare. Questo valore deve essere compreso tra 0 e 2 inclusi.

</dd> <dt>

*colonna* \[ di in\]
</dt> <dd>

Indice di colonna dell'elemento da modificare. Questo valore deve essere compreso tra 0 e 1, inclusi.

</dd> <dt>

*animazione* \[ di in\]
</dt> <dd>

Animazione che rappresenta il modo in cui il valore dell'elemento specificato viene modificato nel tempo. Questo parametro non può essere NULL.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce S \_ OK. In caso contrario, restituisce un codice di errore **HRESULT** . Per un elenco di codici di errore, vedere [codici di errore DirectComposition](directcomposition-error-codes.md) .

## <a name="remarks"></a>Commenti

Questo metodo crea una copia dell'animazione specificata. Se l'oggetto a cui fa riferimento il parametro *Animation* viene modificato dopo la chiamata a questo metodo, la modifica non influisce sull'elemento a meno che questo metodo non venga chiamato nuovamente. Se l'elemento è stato precedentemente animato, la chiamata a questo metodo sostituisce l'animazione precedente con la nuova animazione.

Questo metodo ha esito negativo se l' *animazione* è un puntatore non valido o se non è stato creato dalla stessa interfaccia [**IDCompositionDevice**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) della trasformazione interessata. L'interfaccia non può essere un'implementazione personalizzata. con questo metodo è possibile usare solo le interfacce create da Microsoft DirectComposition.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDCompositionMatrixTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform)
</dt> </dl>

 

 