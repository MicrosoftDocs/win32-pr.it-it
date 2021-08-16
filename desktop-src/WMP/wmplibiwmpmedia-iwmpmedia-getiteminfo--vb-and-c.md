---
title: Metodo IWMPMedia getItemInfo
description: Il metodo getItemInfo restituisce il valore dell'attributo specificato per l'elemento multimediale.
ms.assetid: b95fa61d-a600-4f31-a930-d80516204034
keywords:
- Metodo getItemInfo Windows Media Player
- Metodo getItemInfo Windows Media Player, interfaccia IWMPMedia
- Interfaccia IWMPMedia Windows Media Player metodo , getItemInfo
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
ms.openlocfilehash: ce8fa8b55074781dd835e116b0403391fe9343af30d5236610219dca8aba810b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118331991"
---
# <a name="iwmpmediagetiteminfo-method"></a>Metodo IWMPMedia::getItemInfo

Il **metodo getItemInfo** restituisce il valore dell'attributo specificato per l'elemento multimediale.

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

*bstrItemName* \[ Pollici\]
</dt> <dd>

**System.String** che rappresenta il nome dell'attributo. Per informazioni sugli attributi supportati da Windows Media Player, vedere Riferimento [agli attributi.](attribute-reference.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**System.String che** rappresenta il valore dell'attributo specificato.

## <a name="remarks"></a>Commenti

Questo metodo restituisce i metadati per un singolo elemento multimediale o un elemento multimediale che fa parte di una playlist.

La **proprietà attributeCount** ottiene il numero di nomi di attributi disponibili per un determinato elemento multimediale. I numeri di indice possono quindi essere usati con **il metodo getAttributeName** per determinare il nome di ogni attributo disponibile. I nomi dei singoli attributi possono essere passati **a getItemInfo.**

Per recuperare attributi con più valori e attributi con valori complessi, usare il **metodo getItemInfoByType.**

Se l'elemento multimediale deriva da una libreria recuperata chiamando [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), il set di attributi disponibili sarà diverso da quelli su cui è possibile eseguire query dalla libreria locale recuperata chiamando [AxWindowsMediaPlayer.mediaCollection.](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md) Ad esempio, gli attributi disponibili dalla libreria locale recuperata tramite **IWMPLibrary** saranno un subset degli attributi disponibili dalla libreria locale recuperata tramite **IWMPCore.** Il set di attributi disponibili da altre origini (librerie remote, dispositivi portatili o CD) è definito dalle altre origini.

Prima di chiamare questo metodo, è necessario avere accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria.](library-access.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento all'attributo**](attribute-reference.md)
</dt> <dt>

[**Interfaccia IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia.attributeCount (VB e C#)**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[**IWMPMedia.getAttributeName (VB e C#)**](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[**IWMPMedia.setItemInfo (VB e C#)**](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3.getItemInfoByType (VB e C#)**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





