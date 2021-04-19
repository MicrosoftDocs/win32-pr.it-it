---
title: Interfaccia IWMPMedia2 (VB e C) (WMP. h)
description: Consente di accedere a una proprietà di elemento multimediale aggiuntiva.
ms.assetid: 7d9f8304-ae26-4175-b9d4-9f272861ef87
keywords:
- Interfaccia IWMPMedia2 (VB e C) Windows Media Player
- Interfaccia IWMPMedia2 (VB e C) Windows Media Player, descritta
topic_type:
- apiref
api_name:
- IWMPMedia2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb1a77322e0e6649d9a286c920ccd9ddc77890f3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324540"
---
# <a name="iwmpmedia2-vb-and-c-interface"></a>Interfaccia IWMPMedia2 (VB e C#)

Consente di accedere a una proprietà di elemento multimediale aggiuntiva.

Oltre alle proprietà e ai metodi ereditati da **IWMPMedia**, l'interfaccia **IWMPMedia2** espone la proprietà seguente.



| Proprietà                                                 | Descrizione                                                                   |
|----------------------------------------------------------|-------------------------------------------------------------------------------|
| [Error (Errore) (Error (Errore)e)](wmplibiwmpmedia2-iwmpmedia2-error--vb-and-c.md) | Ottiene un'interfaccia **IWMPErrorItem** se l'elemento multimediale presenta una condizione di errore. |



 

Ottenere un'interfaccia **IWMPMedia2** eseguendo il cast del valore restituito da uno dei metodi o delle proprietà seguenti a cui si accede tramite l'oggetto o l'interfaccia seguente.



| Oggetto o interfaccia                                               | Proprietà o metodo                                                                                                                |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [IWMPControls](iwmpcontrols--vb-and-c.md)                        | [currentItem](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)                                                          |
| [AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [currentMedia](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md) , [newMedia](axwmplib-axwindowsmediaplayer-newmedia.md) |
| [IWMPPlaylist](iwmpplaylist--vb-and-c.md)                        | [Item](iwmpplaylist-item--vb-and-c.md) ( **get \_ Item** in C#)                                                                   |



 

## <a name="members"></a>Membri

L'interfaccia **IWMPMedia2 (VB e C#)** non definisce membri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce per Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**IWMPErrorItem (VB e C#)**](iwmperroritem--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPMedia3 (VB e C#)**](iwmpmedia3--vb-and-c.md)
</dt> </dl>

 

 





