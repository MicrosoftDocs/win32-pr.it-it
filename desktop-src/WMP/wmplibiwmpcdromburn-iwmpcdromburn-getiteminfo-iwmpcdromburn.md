---
title: Metodo getItemInfo IWMPCdromMethod
description: Il metodo getItemInfo recupera il valore dell'attributo specificato per il CD.
ms.assetid: 9ca54ec4-42be-40c1-931e-c3bfcbc2b370
keywords:
- Metodo getItemInfo Windows Media Player
- Metodo getItemInfo Windows Media Player, interfaccia IWMPCdromLim
- Interfaccia IWMPCdromMethod Windows Media Player , metodo getItemInfo
topic_type:
- apiref
api_name:
- IWMPCdromBurn.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2cf1a91ad60826e19051a59617157110fbcd8d75eff325f94f9b3f84d759aa4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118116229"
---
# <a name="iwmpcdromburngetiteminfo-method"></a>Metodo IWMPCdromMethod::getItemInfo

Il **metodo getItemInfo** recupera il valore dell'attributo specificato per il CD.

## <a name="syntax"></a>Sintassi


```CSharp
public System.String getItemInfo(
  System.String bstrItem
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrItem As System.String _
) As System.String
Implements IWMPCdromBurn.getItemInfo
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrItem* \[ Pollici\]
</dt> <dd>

**System.String** che contiene uno dei valori seguenti.



| Valore         | Descrizione                                                                                  |
|---------------|----------------------------------------------------------------------------------------------|
| AvailableTime | Recupera il tempo disponibile sul CD, in secondi.                                          |
| Vuoto         | Recupera un **oggetto System.Boolean** (rappresentato come stringa) che indica se il CD è vuoto. |
| FreeSpace     | Recupera lo spazio disponibile sul CD, in byte.                                                |
| TotalSpace    | Recupera lo spazio totale sul CD, in byte.                                               |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**System.String che** rappresenta il valore dell'attributo specificato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 11<br/>                                                                                     |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPCdrom Sistema (VB e C#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





