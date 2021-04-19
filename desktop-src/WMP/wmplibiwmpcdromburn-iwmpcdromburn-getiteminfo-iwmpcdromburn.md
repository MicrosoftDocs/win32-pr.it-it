---
title: Metodo IWMPCdromBurn getItemInfo
description: Il metodo getItemInfo Recupera il valore dell'attributo specificato per il CD.
ms.assetid: 9ca54ec4-42be-40c1-931e-c3bfcbc2b370
keywords:
- metodo getItemInfo Windows Media Player
- metodo getItemInfo Windows Media Player, interfaccia IWMPCdromBurn
- Interfaccia IWMPCdromBurn Windows Media Player, metodo getItemInfo
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
ms.openlocfilehash: 9030bd230b2e17bab6ad54dc762a78d2cb343d03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329659"
---
# <a name="iwmpcdromburngetiteminfo-method"></a>Metodo IWMPCdromBurn:: getItemInfo

Il metodo **GetItemInfo** Recupera il valore dell'attributo specificato per il CD.

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

*bstrItem* \[ in\]
</dt> <dd>

**System. String** che contiene uno dei valori seguenti.



| Valore         | Descrizione                                                                                  |
|---------------|----------------------------------------------------------------------------------------------|
| Availabletime disponibile | Recupera l'ora disponibile sul CD, in secondi.                                          |
| Vuoto         | Recupera un oggetto **System. Boolean** (rappresentato come stringa) che indica se il CD è vuoto. |
| FreeSpace     | Recupera lo spazio disponibile sul CD, in byte.                                                |
| TotalSpace    | Recupera lo spazio totale del CD, in byte.                                               |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**System. String** che corrisponde al valore dell'attributo specificato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 11<br/>                                                                                     |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPCdromBurn (VB e C#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





