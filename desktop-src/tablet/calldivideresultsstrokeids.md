---
description: Recupera le proprietà Id per gli oggetti IInkStrokeDisp della parola, della riga, del paragrafo o del disegno corrispondenti determinati dall'analisi dell'input penna.
ms.assetid: f05ffa3b-2a47-46fe-bb8f-e682aa094b69
title: Funzione CallDivideResultsStrokeIds
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CallDivideResultsStrokeIds
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 64b3e4180a34c45890408f8ba92cc79465fffa7f1028152e27f8d5c0aa40e3e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009131"
---
# <a name="calldivideresultsstrokeids-function"></a>Funzione CallDivideResultsStrokeIds

Recupera le proprietà [**Id**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) per gli [**oggetti IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) della parola, della riga, del paragrafo o del disegno corrispondenti determinati dall'analisi dell'input penna.

Questa funzione non deve essere usata dal codice dell'applicazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI CallDivideResultsStrokeIds(
  _In_  INT_PTR hDivider,
  _Out_ int     aWordStrokeIds[],
  _Out_ int     aLineStrokeIds[],
  _Out_ int     aParagraphStrokeIds[],
  _Out_ int     aDrawingStrokeIds[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDivider* \[ Pollici\]
</dt> <dd>

Handle per [l'oggetto Divider.](the-divider-object.md)

</dd> <dt>

*aWordStrokeIds \[ \]* \[out\]
</dt> <dd>

Matrice degli ID tratto dell'input penna nella parola.

</dd> <dt>

*aLineStrokeIds \[ \]* \[out\]
</dt> <dd>

Matrice degli ID tratto dell'input penna nella riga.

</dd> <dt>

*aParagraphStrokeIds \[ \]* \[out\]
</dt> <dd>

Matrice degli ID tratto dell'input penna nel paragrafo.

</dd> <dt>

*aDrawingStrokeIds \[ \]* \[out\]
</dt> <dd>

Matrice degli ID tratto dell'input penna nel disegno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione può restituire uno di questi valori.



| Codice restituito                                                                                  | Descrizione                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Funzione completata.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Il *parametro hDivider* non è valido.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                         |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                             |
| Libreria<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




