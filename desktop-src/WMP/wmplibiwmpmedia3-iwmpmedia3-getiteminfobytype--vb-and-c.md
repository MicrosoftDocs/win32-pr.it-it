---
title: Metodo IWMPMedia3 getItemInfoByType
description: Il metodo getItemInfoByType restituisce il valore dell'attributo corrispondente al tipo di attributo e all'indice specificati.
ms.assetid: e4cf14b4-3c59-485f-a573-734a0076647b
keywords:
- Metodo getItemInfoByType Windows Media Player
- Metodo getItemInfoByType Windows Media Player, interfaccia IWMPMedia3
- Interfaccia IWMPMedia3 Windows Media Player, metodo getItemInfoByType
topic_type:
- apiref
api_name:
- IWMPMedia3.getItemInfoByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f37992201d5d19397724071f8c2a4b8e851aac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324366"
---
# <a name="iwmpmedia3getiteminfobytype-method"></a>Metodo IWMPMedia3:: getItemInfoByType

Il metodo **getItemInfoByType** restituisce il valore dell'attributo corrispondente al tipo di attributo e all'indice specificati.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Object getItemInfoByType(
  System.String bstrType,
  System.String bstrLanguage,
  System.Int32 lIndex
);
```


```VB

Public Function getItemInfoByType( _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String, _
  ByVal lIndex As System.Int32 _
) As System.Object
Implements IWMPMedia3.getItemInfoByType
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrType* \[ in\]
</dt> <dd>

**System. String** che rappresenta il tipo di attributo.

</dd> <dt>

*bstrLanguage* \[ in\]
</dt> <dd>

**System. String** che rappresenta il linguaggio. Se il valore è impostato su null o su una stringa di lunghezza zero (""), viene utilizzata la stringa delle impostazioni locali corrente. In caso contrario, il valore deve essere una stringa di linguaggio RFC 1766 valida, ad esempio "en-US".

</dd> <dt>

*lIndex* \[ in\]
</dt> <dd>

**System. Int32** che rappresenta l'indice dell'attributo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**Oggetto System. Object** che rappresenta il valore dell'attributo. Il tipo su cui eseguire il cast di questo oggetto dipende dal tipo dell'attributo.

## <a name="remarks"></a>Commenti

Questo metodo restituisce i metadati per un singolo elemento multimediale digitale o un elemento multimediale che fa parte di una playlist.

Questo metodo supporta attributi con più valori e attributi con valori complessi. Il metodo **GetItemInfo** non supporta attributi con più valori e attributi con valori complessi.

La proprietà **attributeCount** ottiene il numero di nomi di attributi disponibili per un determinato elemento multimediale. I numeri di indice possono quindi essere usati con il metodo **GetAttribute** per determinare il nome di ogni attributo disponibile. I singoli nomi di attributo possono essere passati al parametro *Name* di **getItemInfoByType**.

Il metodo **getAttributeCountByType** restituisce il numero di attributi che corrispondono a un nome di attributo specifico per un determinato elemento multimediale. I numeri di indice possono quindi essere passati al parametro di *Indice* di **getItemInfoByType**. Questa operazione è utile quando un elemento multimediale è stato categorizzato in più generi, ad esempio.

Se l'elemento multimediale proviene da una libreria recuperata chiamando [IWMPLibrary. mediacollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), il set di attributi disponibili sarà diverso da quelli su cui è possibile eseguire una query dalla libreria locale recuperata chiamando [AxWindowsMediaPlayer. mediacollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md). Ad esempio, gli attributi disponibili dalla libreria locale recuperata tramite **IWMPLibrary** saranno un subset degli attributi disponibili dalla libreria locale recuperata mediante **AxWindowsMediaPlayer**. Il set di attributi disponibili da altre origini (librerie remote, dispositivi portatili o CDs è definito da altre origini).

Prima di chiamare questo metodo, è necessario disporre dell'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPMedia3 (VB e C#)**](iwmpmedia3--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. attributeCount (VB e C#)**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. GetAttribute (VB e C#)**](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. getItemInfo (VB e C#)**](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3. getAttributeCountByType (VB e C#)**](wmplibiwmpmedia3-iwmpmedia3-getattributecountbytype--vb-and-c.md)
</dt> </dl>

 

 





