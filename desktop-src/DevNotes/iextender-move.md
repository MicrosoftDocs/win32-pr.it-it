---
description: Sposta un oggetto MDIForm, un form o un controllo.
ms.assetid: 963e6533-f571-4043-bdd8-2596df6b5b35
title: Metodo IExtender::Move
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IExtender.Move
api_type:
- COM
api_location:
- Ole2disp.dll
- Oleaut32.dll
ms.openlocfilehash: 13002457952490588fa9e9ad40e7f66e7d31465b74f9757a3193ccaed1e8bf7e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002101"
---
# <a name="iextendermove-method"></a>Metodo IExtender::Move

Sposta un oggetto MDIForm, un form o un controllo.

## <a name="syntax"></a>Sintassi


```C++
void Move(
  [in] object left,
  [in] object top,
  [in] object width,
  [in] object height
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*left* \[ Pollici\]
</dt> <dd>

Bordo sinistro del form o del controllo.

</dd> <dt>

*top* \[ Pollici\]
</dt> <dd>

Bordo superiore del form o del controllo.

</dd> <dt>

*width* \[ Pollici\]
</dt> <dd>

Larghezza del form o del controllo.

</dd> <dt>

*height* \[ Pollici\]
</dt> <dd>

Altezza del form o del controllo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ole2disp.dll; </dt> <dt>Oleaut32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IExtender**](iextender.md)
</dt> </dl>

 

 




