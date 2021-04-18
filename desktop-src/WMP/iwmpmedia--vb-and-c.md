---
title: Interfaccia IWMPMedia (VB e C) (WMP. h)
description: Consente di impostare e recuperare le proprietà di un elemento multimediale. L'interfaccia IWMPMedia espone le proprietà seguenti.
ms.assetid: 4f67336e-d1d3-4f18-b063-086edf9d9094
keywords:
- Interfaccia IWMPMedia (VB e C) Windows Media Player
- Interfaccia IWMPMedia (VB e C) Windows Media Player, descritta
topic_type:
- apiref
api_name:
- IWMPMedia (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c60a3396710ea4c426bd41c96db34e1e59cc690
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331391"
---
# <a name="iwmpmedia-vb-and-c-interface"></a>Interfaccia IWMPMedia (VB e C#)

Consente di impostare e recuperare le proprietà di un elemento multimediale.

L'interfaccia **IWMPMedia** espone le proprietà seguenti.

## <a name="members"></a>Membri

L'interfaccia **IWMPMedia (VB e C#)** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia **IWMPMedia (VB e C#)** presenta questi metodi.



| Metodo                                                                             | Descrizione                                                                                                   |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [**getAttributeName**](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)   | Restituisce il nome dell'attributo corrispondente all'indice specificato.<br/>                            |
| [**getItemInfo**](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)             | Restituisce il valore dell'attributo specificato per l'elemento multimediale.<br/>                                   |
| [**getItemInfoByAtom**](wmplibiwmpmedia-iwmpmedia-getiteminfobyatom--vb-and-c.md) | Restituisce il valore dell'attributo con il numero di indice specificato.<br/>                                |
| [**getmarcatore**](wmplibiwmpmedia-iwmpmedia-getmarkername--vb-and-c.md)         | Restituisce il nome del marcatore in corrispondenza dell'indice specificato.<br/>                                             |
| [**getMarkerTime**](wmplibiwmpmedia-iwmpmedia-getmarkertime--vb-and-c.md)         | Restituisce l'ora del marcatore in corrispondenza dell'indice specificato.<br/>                                             |
| [**isMemberOf**](wmplibiwmpmedia-iwmpmedia-ismemberof--vb-and-c.md)               | Restituisce un valore che indica se l'elemento multimediale specificato è un membro della playlist specificata.<br/> |
| [**isReadOnlyItem**](wmplibiwmpmedia-iwmpmedia-isreadonlyitem--vb-and-c.md)       | Restituisce un valore che indica se è possibile modificare gli attributi dell'elemento multimediale specificato.<br/>       |
| [**setItemInfo**](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)             | Imposta il valore dell'attributo specificato per l'elemento multimediale.<br/>                                      |



 

### <a name="properties"></a>Proprietà

L'interfaccia **IWMPMedia (VB e C#)** presenta queste proprietà.



| Proprietà                                                                                      | Tipo di accesso          | Descrizione                                                                                                                                          |
|:----------------------------------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**attributeCount**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)<br/>       | Sola lettura<br/> | Ottiene il numero di attributi su cui è possibile eseguire query e/o impostare per l'elemento multimediale.<br/>                                                          |
| [**durata**](wmplibiwmpmedia-iwmpmedia-duration--vb-and-c.md)<br/>                   | Sola lettura<br/> | Ottiene la durata in secondi dell'elemento multimediale corrente.<br/>                                                                                   |
| [**durationString**](wmplibiwmpmedia-iwmpmedia-durationstring--vb-and-c.md)<br/>       | Sola lettura<br/> | Ottiene un valore che indica la durata dell'elemento multimediale corrente nel formato HH: MM: SS.<br/>                                                        |
| [**imageSourceHeight**](wmplibiwmpmedia-iwmpmedia-imagesourceheight--vb-and-c.md)<br/> | Sola lettura<br/> | Ottiene l'altezza in pixel dell'elemento multimediale corrente.<br/>                                                                                      |
| [**imageSourceWidth**](wmplibiwmpmedia-iwmpmedia-imagesourcewidth--vb-and-c.md)<br/>   | Sola lettura<br/> | Ottiene la larghezza in pixel dell'elemento multimediale corrente.<br/>                                                                                       |
| [**Identico**](iwmpmedia-isidentical--vb-and-c.md)<br/>                             | Sola lettura<br/> | Ottiene un valore che indica se l'elemento multimediale specificato è uguale a quello corrente. In C# il metodo Get è **\_ identico** .<br/> |
| [**markerCount**](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)<br/>             | Sola lettura<br/> | Ottiene il numero di marcatori nell'elemento multimediale.<br/>                                                                                             |
| [**nome**](wmplibiwmpmedia-iwmpmedia-name--vb-and-c.md)<br/>                           | Sola lettura<br/> | Ottiene o imposta il nome dell'elemento multimediale.<br/>                                                                                                  |
| [**sourceURL**](wmplibiwmpmedia-iwmpmedia-sourceurl--vb-and-c.md)<br/>                 | Sola lettura<br/> | Ottiene l'URL dell'elemento multimediale.<br/>                                                                                                           |



 

Ottenere un'interfaccia **IWMPMedia** usando le proprietà o i metodi seguenti a cui si accede tramite l'oggetto o l'interfaccia seguente.



| Oggetto o interfaccia                                               | Proprietà o metodo                                                                                                                       |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMPControls**](iwmpcontrols--vb-and-c.md)                    | [**CurrentItem**](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)                                                             |
| [AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**currentMedia**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md), [ **newMedia**](axwmplib-axwindowsmediaplayer-newmedia.md) |
| [**IWMPPlaylist**](iwmpplaylist--vb-and-c.md)                    | [**Item**](iwmpplaylist-item--vb-and-c.md) (Get \_ Item in C#)                                                                           |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce per Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interfaccia IWMPMedia2 (VB e C#)**](iwmpmedia2--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPMedia3 (VB e C#)**](iwmpmedia3--vb-and-c.md)
</dt> </dl>

 

 





