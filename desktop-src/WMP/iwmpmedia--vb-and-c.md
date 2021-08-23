---
title: Interfaccia IWMPMedia (VB e C) (Wmp.h)
description: Consente di impostare e recuperare le proprietà di un elemento multimediale. L'interfaccia IWMPMedia espone le proprietà seguenti.
ms.assetid: 4f67336e-d1d3-4f18-b063-086edf9d9094
keywords:
- Interfaccia IWMPMedia (VB e C) Windows Media Player
- Interfaccia IWMPMedia (VB e C) Windows Media Player , descritta
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
ms.openlocfilehash: 8d36fc2a7c4f65856b68c00147e32f9b3af4cc3e649a9717e7734583d4516b44
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119572461"
---
# <a name="iwmpmedia-vb-and-c-interface"></a>Interfaccia IWMPMedia (VB e C#)

Consente di impostare e recuperare le proprietà di un elemento multimediale.

**L'interfaccia IWMPMedia** espone le proprietà seguenti.

## <a name="members"></a>Membri

**L'interfaccia IWMPMedia (VB e C#)** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'interfaccia IWMPMedia (VB e C#)** include questi metodi.



| Metodo                                                                             | Descrizione                                                                                                   |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [**getAttributeName**](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)   | Restituisce il nome dell'attributo corrispondente all'indice specificato.<br/>                            |
| [**getItemInfo**](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)             | Restituisce il valore dell'attributo specificato per l'elemento multimediale.<br/>                                   |
| [**getItemInfoByAtom**](wmplibiwmpmedia-iwmpmedia-getiteminfobyatom--vb-and-c.md) | Restituisce il valore dell'attributo con il numero di indice specificato.<br/>                                |
| [**getMarkerName**](wmplibiwmpmedia-iwmpmedia-getmarkername--vb-and-c.md)         | Restituisce il nome del marcatore in corrispondenza dell'indice specificato.<br/>                                             |
| [**getMarkerTime**](wmplibiwmpmedia-iwmpmedia-getmarkertime--vb-and-c.md)         | Restituisce l'ora del marcatore in corrispondenza dell'indice specificato.<br/>                                             |
| [**isMemberOf**](wmplibiwmpmedia-iwmpmedia-ismemberof--vb-and-c.md)               | Restituisce un valore che indica se l'elemento multimediale specificato è un membro della playlist specificata.<br/> |
| [**isReadOnlyItem**](wmplibiwmpmedia-iwmpmedia-isreadonlyitem--vb-and-c.md)       | Restituisce un valore che indica se è possibile modificare gli attributi dell'elemento multimediale specificato.<br/>       |
| [**setItemInfo**](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)             | Imposta il valore dell'attributo specificato per l'elemento multimediale.<br/>                                      |



 

### <a name="properties"></a>Proprietà

**L'interfaccia IWMPMedia (VB e C#)** ha queste proprietà.



| Proprietà                                                                                      | Tipo di accesso          | Descrizione                                                                                                                                          |
|:----------------------------------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**attributeCount**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)<br/>       | Sola lettura<br/> | Ottiene il numero di attributi che possono essere sottoposti a query e/o impostati per l'elemento multimediale.<br/>                                                          |
| [**Durata**](wmplibiwmpmedia-iwmpmedia-duration--vb-and-c.md)<br/>                   | Sola lettura<br/> | Ottiene la durata in secondi dell'elemento multimediale corrente.<br/>                                                                                   |
| [**durationString**](wmplibiwmpmedia-iwmpmedia-durationstring--vb-and-c.md)<br/>       | Sola lettura<br/> | Ottiene un valore che indica la durata dell'elemento multimediale corrente in formato HH:MM:SS.<br/>                                                        |
| [**imageSourceHeight**](wmplibiwmpmedia-iwmpmedia-imagesourceheight--vb-and-c.md)<br/> | Sola lettura<br/> | Ottiene l'altezza dell'elemento multimediale corrente in pixel.<br/>                                                                                      |
| [**imageSourceWidth**](wmplibiwmpmedia-iwmpmedia-imagesourcewidth--vb-and-c.md)<br/>   | Sola lettura<br/> | Ottiene la larghezza dell'elemento multimediale corrente in pixel.<br/>                                                                                       |
| [**isIdentical**](iwmpmedia-isidentical--vb-and-c.md)<br/>                             | Sola lettura<br/> | Ottiene un valore che indica se l'elemento multimediale specificato corrisponde a quello corrente. In C# questo è il **metodo \_ get isIdentical.**<br/> |
| [**markerCount**](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)<br/>             | Sola lettura<br/> | Ottiene il numero di marcatori nell'elemento multimediale.<br/>                                                                                             |
| [**Nome**](wmplibiwmpmedia-iwmpmedia-name--vb-and-c.md)<br/>                           | Sola lettura<br/> | Ottiene o imposta il nome dell'elemento multimediale.<br/>                                                                                                  |
| [**sourceURL**](wmplibiwmpmedia-iwmpmedia-sourceurl--vb-and-c.md)<br/>                 | Sola lettura<br/> | Ottiene l'URL dell'elemento multimediale.<br/>                                                                                                           |



 

Ottenere **un'interfaccia IWMPMedia** usando le proprietà o i metodi seguenti accessibili tramite l'oggetto o l'interfaccia seguente.



| Oggetto o interfaccia                                               | Proprietà o metodo                                                                                                                       |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMPControls**](iwmpcontrols--vb-and-c.md)                    | [**Currentitem**](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)                                                             |
| [AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**currentMedia**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md), [ **newMedia**](axwmplib-axwindowsmediaplayer-newmedia.md) |
| [**IWMPPlaylist**](iwmpplaylist--vb-and-c.md)                    | [**Item**](iwmpplaylist-item--vb-and-c.md) (get \_ Item in C#)                                                                           |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce per Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interfaccia IWMPMedia2 (VB e C#)**](iwmpmedia2--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPMedia3 (VB e C#)**](iwmpmedia3--vb-and-c.md)
</dt> </dl>

 

 





