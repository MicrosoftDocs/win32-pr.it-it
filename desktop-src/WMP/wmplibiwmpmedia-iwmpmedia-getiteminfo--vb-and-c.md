---
title: Metodo IWMPMedia getItemInfo
description: Il metodo getItemInfo restituisce il valore dell'attributo specificato per l'elemento multimediale.
ms.assetid: b95fa61d-a600-4f31-a930-d80516204034
keywords:
- metodo getItemInfo Windows Media Player
- metodo getItemInfo Windows Media Player, interfaccia IWMPMedia
- Interfaccia IWMPMedia Windows Media Player, metodo getItemInfo
topic_type:
- apiref
api_name:
- IWMPMedia.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 523e57e68d13df55395cd4deca6e09904723bbaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332406"
---
# <a name="iwmpmediagetiteminfo-method"></a>Metodo IWMPMedia:: getItemInfo

Il metodo **GetItemInfo** restituisce il valore dell'attributo specificato per l'elemento multimediale.

## <a name="syntax"></a>Sintassi


```CSharp
public System.String getItemInfo(
  System.String bstrItemName
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrItemName As System.String _
) As System.String
Implements IWMPMedia.getItemInfo
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrItemName* \[ in\]
</dt> <dd>

**System. String** che rappresenta il nome dell'attributo. Per informazioni sugli attributi supportati da Windows Media Player, vedere il [riferimento all'attributo](attribute-reference.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**System. String** che corrisponde al valore dell'attributo specificato.

## <a name="remarks"></a>Commenti

Questo metodo restituisce i metadati per un singolo elemento multimediale o un elemento multimediale che fa parte di una playlist.

La proprietà **attributeCount** ottiene il numero di nomi di attributi disponibili per un determinato elemento multimediale. I numeri di indice possono quindi essere usati con il metodo **GetAttribute** per determinare il nome di ogni attributo disponibile. I singoli nomi di attributo possono essere passati a **GetItemInfo**.

Per recuperare gli attributi con più valori e attributi con valori complessi, usare il metodo **getItemInfoByType** .

Se l'elemento multimediale proviene da una libreria recuperata chiamando [IWMPLibrary. mediacollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), il set di attributi disponibili sarà diverso da quelli su cui è possibile eseguire una query dalla libreria locale recuperata chiamando [AxWindowsMediaPlayer. mediacollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md). Ad esempio, gli attributi disponibili dalla libreria locale recuperata tramite **IWMPLibrary** saranno un subset degli attributi disponibili dalla libreria locale recuperata mediante **IWMPCore**. Il set di attributi disponibili da altre origini (librerie remote, dispositivi portatili o CDs) viene definito dalle altre origini.

Prima di chiamare questo metodo, è necessario disporre dell'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> <dt>

[**Interfaccia IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. attributeCount (VB e C#)**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. GetAttribute (VB e C#)**](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. setItemInfo (VB e C#)**](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3. getItemInfoByType (VB e C#)**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





