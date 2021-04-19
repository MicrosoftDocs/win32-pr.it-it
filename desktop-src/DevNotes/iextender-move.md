---
description: Sposta un MDIForm, un form o un controllo.
ms.assetid: 963e6533-f571-4043-bdd8-2596df6b5b35
title: 'Metodo IExtender:: Move'
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
ms.openlocfilehash: 2c7ed806629f0e5e1bb0cdee5c76910728fd651d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332089"
---
# <a name="iextendermove-method"></a>Metodo IExtender:: Move

Sposta un MDIForm, un form o un controllo.

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

a *sinistra* \[ in\]
</dt> <dd>

Bordo sinistro del form o del controllo.

</dd> <dt>

in *alto* \[ in\]
</dt> <dd>

Bordo superiore del form o del controllo.

</dd> <dt>

*larghezza* \[ in\]
</dt> <dd>

Larghezza del form o del controllo.

</dd> <dt>

*altezza* \[ in\]
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

 

 




