---
description: Crea un'istanza aggiuntiva dell'interfaccia IEnumWiaItem2 e restituisce un puntatore.
ms.assetid: 0d36d555-d0d9-4a1c-ac54-de611850449c
title: 'Metodo IEnumWiaItem2:: Clone (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Clone
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3279e7db3efe66e940adbcb9677204e5df7867f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752871"
---
# <a name="ienumwiaitem2clone-method"></a>Metodo IEnumWiaItem2:: Clone

Crea un'istanza aggiuntiva dell'interfaccia [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) e restituisce un puntatore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Clone(
  [out] IEnumWiaItem2 **ppIEnum
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppIEnum* \[ out\]
</dt> <dd>

Tipo: **[ **IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***

Riceve l'indirizzo dell'istanza dell'interfaccia [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) creata da **IEnumWiaItem2:: Clone** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Le applicazioni devono chiamare il metodo [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori di interfaccia ricevuti tramite il parametro *ppIEnum* .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
