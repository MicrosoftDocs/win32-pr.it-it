---
description: Crea un'istanza aggiuntiva dell'interfaccia IEnumWiaItem2 e invia un puntatore a essa.
ms.assetid: 0d36d555-d0d9-4a1c-ac54-de611850449c
title: Metodo IEnumWiaItem2::Clone (Wia.h)
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
ms.openlocfilehash: 21c94c634a6930f28f48cdc35a4d3cf199b8fa33e9fb5f08444797fd76f50c45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965850"
---
# <a name="ienumwiaitem2clone-method"></a>Metodo IEnumWiaItem2::Clone

Crea un'istanza aggiuntiva [**dell'interfaccia IEnumWiaItem2**](-wia-ienumwiaitem2.md) e invia un puntatore a essa.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Clone(
  [out] IEnumWiaItem2 **ppIEnum
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppIEnum* \[ Cambio\]
</dt> <dd>

Tipo: **[ **IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***

Riceve l'indirizzo [**dell'istanza dell'interfaccia IEnumWiaItem2**](-wia-ienumwiaitem2.md) creata **da IEnumWiaItem2::Clone.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Le applicazioni devono chiamare [il metodo IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori a interfaccia ricevuti tramite il *parametro ppIEnum.*

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
