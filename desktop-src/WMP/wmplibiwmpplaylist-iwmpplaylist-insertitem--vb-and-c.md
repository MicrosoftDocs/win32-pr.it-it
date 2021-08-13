---
title: Metodo insertItem IWMPPlaylist
description: Il metodo insertItem inserisce un elemento multimediale in una posizione specificata in una playlist.
ms.assetid: 6e472f0a-13df-41d9-8e6f-8430d87fe978
keywords:
- Metodo insertItem Windows Media Player
- Metodo insertItem Windows Media Player, interfaccia IWMPPlaylist
- Interfaccia IWMPPlaylist Windows Media Player , metodo insertItem
topic_type:
- apiref
api_name:
- IWMPPlaylist.insertItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10717c0891443aaa663b748be6a0cb57e04e58b96beb91db6b02b2f6a4b5b621
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119464931"
---
# <a name="iwmpplaylistinsertitem-method"></a>Metodo IWMPPlaylist::insertItem

Il **metodo insertItem** inserisce un elemento multimediale in una posizione specificata in una playlist.

## <a name="syntax"></a>Sintassi


```CSharp
public void insertItem(
  System.Int32 lIndex,
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub insertItem( _
  ByVal lIndex As System.Int32, _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPPlaylist.insertItem
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*lIndex* \[ Pollici\]
</dt> <dd>

Oggetto **System.Int32** che rappresenta l'indice in base zero in corrispondenza del quale l'elemento multimediale verrà inserito nella playlist.

</dd> <dt>

*pIWMPMedia* \[ Pollici\]
</dt> <dd>

Interfaccia **WMPLib.IWMPMedia** che rappresenta l'elemento multimediale da inserire.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Tutti gli elementi multimediali dopo l'elemento inserito avranno gli indici aumentati di uno.

Prima di chiamare questo metodo, è necessario avere accesso completo alla libreria. Per altre informazioni, vedere [Accesso alla libreria](library-access.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist.removeItem (VB e C#)**](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)
</dt> </dl>

 

 





