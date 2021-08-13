---
description: Cerca nell'albero di elementi secondari di un elemento usando il nome come chiave di ricerca.
ms.assetid: e4ce0bfb-9793-4928-b454-66ae1455b7b5
title: Metodo IWiaItem2::FindItemByName (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.FindItemByName
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 5ef0ffdf710d36d2d6c515352bf441e9c66ae169400528db5d5943e2114fefd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118440409"
---
# <a name="iwiaitem2finditembyname-method"></a>Metodo IWiaItem2::FindItemByName

Cerca nell'albero di elementi secondari di un elemento usando il nome come chiave di ricerca.

## <a name="syntax"></a>Sintassi


```C++
HRESULT FindItemByName(
  [in]  LONG      lFlags,
  [in]  BSTR      bstrFullItemName,
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lFlags* \[ Pollici\]
</dt> <dd>

Tipo: **LONG**

Attualmente inutilizzato. Deve essere impostato su zero.

</dd> <dt>

*bstrFullItemName* \[ Pollici\]
</dt> <dd>

Tipo: **BSTR**

Specifica il nome dell'elemento da cercare.

</dd> <dt>

*ppIWiaItem2* \[ Cambio\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Riceve l'indirizzo di un puntatore [**all'interfaccia IWiaItem2**](-wia-iwiaitem2.md) dell'elemento trovato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Questo metodo esegue la ricerca nell'albero degli elementi secondari dell'elemento corrente usando il nome come chiave di ricerca. Se **IWiaItem2::FindItemByName** trova l'elemento specificato da *bstrFullItemName*, archivia l'indirizzo di un puntatore all'interfaccia [**IWiaItem2**](-wia-iwiaitem2.md) dell'elemento nel parametro *ppIWiaItem2.*

Le applicazioni devono chiamare [il metodo IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori a interfaccia ricevuti tramite il *parametro ppIWiaItem2.*

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
