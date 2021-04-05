---
description: Verifica se l'oggetto InkDivider può usare la classe InkRecognizerContext per analizzare le parole.
ms.assetid: fd848fcc-5258-401f-8b51-b9d57da173da
title: RecognizerContextSet (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecognizerContextSet
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 51e75b810c2103afed2e8ac8a28706b9c9af5da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882457"
---
# <a name="recognizercontextset-function"></a>RecognizerContextSet (funzione)

Verifica se l'oggetto [**InkDivider**](inkdivider-class.md) può usare la classe [**InkRecognizerContext**](inkrecognizercontext-class.md) per analizzare le parole.

Questa funzione non deve essere usata dal codice dell'applicazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI RecognizerContextSet(
  _In_ INT_PTR hDivider
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDivider* \[ in\]
</dt> <dd>

Handle per l'oggetto [**InkDivider**](inkdivider-class.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione può restituire uno di questi valori.



| Codice restituito                                                                                  | Descrizione                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Funzione completata.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Il parametro *pDivider* non è valido.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                         |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                             |
| Libreria<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




