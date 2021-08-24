---
description: Elimina un oggetto InkDivider e rilascia le risorse associate.
ms.assetid: adf772e0-2829-4410-83c4-45a24bf3a848
title: Funzione DeleteInkDivider
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteInkDivider
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 526186dd2a867f8fb3ee9201ca13df6afd43cb02f8361da202a036dde8e9fb56
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709521"
---
# <a name="deleteinkdivider-function"></a>Funzione DeleteInkDivider

Elimina un [**oggetto InkDivider**](inkdivider-class.md) e rilascia le risorse associate.

Questa funzione non deve essere usata dal codice dell'applicazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI DeleteInkDivider(
  _In_ INT_PTR hDivider
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDivider* \[ Pollici\]
</dt> <dd>

Handle per [**l'oggetto InkDivider.**](inkdivider-class.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione può restituire uno di questi valori.



| Codice restituito                                                                                  | Descrizione                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Il metodo è riuscito.<br/>                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Il *parametro hDivider* non è valido.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                         |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                             |
| Libreria<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




