---
title: Metodo insertItem IWMPPlaylist
description: Il metodo insertItem inserisce un elemento multimediale in una posizione specificata in una playlist.
ms.assetid: 6e472f0a-13df-41d9-8e6f-8430d87fe978
keywords:
- metodo insertItem Media Player Windows
- metodo insertItem Windows Media Player, interfaccia IWMPPlaylist
- Interfaccia IWMPPlaylist Windows Media Player, metodo insertItem
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
ms.openlocfilehash: b1ef167a5f3931f34d4cd6fb91b3d044affb9484
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330973"
---
# <a name="iwmpplaylistinsertitem-method"></a>Metodo IWMPPlaylist:: insertItem

Il metodo **InsertItem** inserisce un elemento multimediale in una posizione specificata in una playlist.

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

*lIndex* \[ in\]
</dt> <dd>

**System. Int32** che rappresenta l'indice in base zero in corrispondenza del quale verrà inserito l'elemento multimediale nella playlist.

</dd> <dt>

*pIWMPMedia* \[ in\]
</dt> <dd>

Interfaccia **wmplib. IWMPMedia** che rappresenta l'elemento multimediale da inserire.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Tutti gli elementi multimediali dopo l'elemento inserito avranno indici aumentati di uno.

Prima di chiamare questo metodo, è necessario disporre dell'accesso completo alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. removeItem (VB e C#)**](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)
</dt> </dl>

 

 





