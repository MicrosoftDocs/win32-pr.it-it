---
description: Ottiene l'elemento padre nell'albero che rappresenta un dispositivo hardware Windows Image Acquisition (WIA) 2,0.
ms.assetid: c6fdaf1d-9875-4852-893c-813894d89f6c
title: 'Metodo IWiaItem2:: GetParentItem (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetParentItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 055625b98807103c3b79109216f6081d00564b15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343666"
---
# <a name="iwiaitem2getparentitem-method"></a>Metodo IWiaItem2:: GetParentItem

Ottiene l'elemento padre nell'albero che rappresenta un dispositivo hardware Windows Image Acquisition (WIA) 2,0.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetParentItem(
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppIWiaItem2* \[ out\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Riceve l'indirizzo di un puntatore all'interfaccia [**IWiaItem2**](-wia-iwiaitem2.md) del padre dell'elemento nell'albero degli oggetti elemento. Se questo metodo viene chiamato sulla radice della struttura ad albero, l'indirizzo restituito è **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Dato qualsiasi oggetto [**IWiaItem2**](-wia-iwiaitem2.md) nell'albero degli oggetti di un dispositivo hardware WIA 2,0, l'applicazione recupera un puntatore all'elemento padre chiamando questa funzione.

Le applicazioni devono chiamare il metodo [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori di interfaccia ricevuti tramite il parametro *ppIWiaItem2* se questi puntatori non sono **null**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
