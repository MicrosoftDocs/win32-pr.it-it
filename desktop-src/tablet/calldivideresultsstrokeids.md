---
description: Recupera le proprietà ID per gli oggetti IInkStrokeDisp della parola, della riga, del paragrafo o del disegno corrispondente determinati dall'analisi dell'input penna.
ms.assetid: f05ffa3b-2a47-46fe-bb8f-e682aa094b69
title: CallDivideResultsStrokeIds (funzione)
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
ms.openlocfilehash: ee690c9564df3b8c75eca6eec8eeb88b7531f4ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305350"
---
# <a name="calldivideresultsstrokeids-function"></a>CallDivideResultsStrokeIds (funzione)

Recupera le proprietà [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) per gli oggetti [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) della parola, della riga, del paragrafo o del disegno corrispondente determinati dall'analisi dell'input penna.

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

*hDivider* \[ in\]
</dt> <dd>

Handle per l'oggetto [divisore](the-divider-object.md) .

</dd> <dt>

*\[ aWordStrokeIds \]* in \[ uscita\]
</dt> <dd>

Matrice degli ID tratto dell'input penna nella parola.

</dd> <dt>

*\[ aLineStrokeIds \]* in \[ uscita\]
</dt> <dd>

Matrice degli ID tratto dell'input penna nella riga.

</dd> <dt>

*\[ aParagraphStrokeIds \]* in \[ uscita\]
</dt> <dd>

Matrice degli ID tratto dell'input penna nel paragrafo.

</dd> <dt>

*\[ aDrawingStrokeIds \]* in \[ uscita\]
</dt> <dd>

Matrice degli ID tratto dell'input penna nel disegno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione può restituire uno di questi valori.



| Codice restituito                                                                                  | Descrizione                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Funzione completata.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Il parametro *hDivider* non è valido.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                         |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                             |
| Libreria<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




