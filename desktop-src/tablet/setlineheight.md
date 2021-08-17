---
description: Imposta la proprietà LineHeight sull'oggetto InkDivider.
ms.assetid: ce5e40c5-faa1-4d66-94f4-d5bd1a11ee4c
title: Funzione SetLineHeight
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetLineHeight
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 2c6a176b5878b7aaee4a0e51a5a366302b13a1a643453ad2c6d57e103362c4fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966820"
---
# <a name="setlineheight-function"></a>Funzione SetLineHeight

Imposta la [**proprietà LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) sull'oggetto [**InkDivider.**](inkdivider-class.md)

Questa funzione helper non deve essere usata dal codice dell'applicazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI SetLineHeight(
  _In_ INT_PTR hDivider,
  _In_ LONG    lLineHeight
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDivider* \[ Pollici\]
</dt> <dd>

Handle per [**l'oggetto InkDivider.**](inkdivider-class.md)

</dd> <dt>

*lLineHeight* \[ Pollici\]
</dt> <dd>

Proprietà [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) [**dell'oggetto InkDivider,**](inkdivider-class.md) in unità HIMETRIC.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione può restituire uno di questi valori.



| Codice restituito                                                                                  | Descrizione                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Funzione completata.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Il *parametro pDivider* non è valido.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                         |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                             |
| Libreria<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 
