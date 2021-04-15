---
description: Recupera le informazioni di analisi dall'oggetto InkDivider.
ms.assetid: 1b073da4-80f4-48f4-8ff6-b21793c173a8
title: CallDivide (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CallDivide
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 0084811ee471bee8fe67653dace49fa83642a7fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524402"
---
# <a name="calldivide-function"></a>CallDivide (funzione)

Recupera le informazioni di analisi dall'oggetto [**InkDivider**](inkdivider-class.md) .

Questa funzione non deve essere usata dal codice dell'applicazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI CallDivide(
  _In_  INT_PTR hDivider,
  _In_  int     *pWordSize,
  _In_  int     *pLineSize,
  _In_  int     *pParagraphSize,
  _In_  int     *pDrawingSize,
  _Out_ int     *pWordCount,
  _Out_ int     *pLineCount,
  _Out_ int     *pParagraphCount
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDivider* \[ in\]
</dt> <dd>

Handle per l'oggetto [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*pWordSize* \[ in\]
</dt> <dd>

Dimensione della parola restituita dall'oggetto [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*pLineSize* \[ in\]
</dt> <dd>

Dimensione della riga restituita dall'oggetto [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*pParagraphSize* \[ in\]
</dt> <dd>

Dimensioni del paragrafo restituito dall'oggetto [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*pDrawingSize* \[ in\]
</dt> <dd>

Dimensioni del disegno restituito dall'oggetto [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*pWordCount* \[ out\]
</dt> <dd>

Numero di parole restituite dall'analisi dell'input penna.

</dd> <dt>

*pLineCount* \[ out\]
</dt> <dd>

Numero di righe restituite dall'analisi dell'input penna.

</dd> <dt>

*pParagraphCount* \[ out\]
</dt> <dd>

Numero di paragrafi restituiti dall'analisi dell'input penna.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione può restituire uno di questi valori.



| Codice restituito                                                                                  | Descrizione                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Funzione riuscito.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Uno o più parametri non sono validi.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                         |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                             |
| Libreria<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




