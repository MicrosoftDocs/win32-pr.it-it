---
title: Interfaccia IWMPPlaylistCollection (VB e C) (Wmp.h)
description: Fornisce metodi per la modifica delle interfacce IWMPPlaylist e IWMPPlaylistArray in una raccolta.
ms.assetid: 19a4e0d7-cb3f-42ec-9acb-7ac0c5837662
keywords:
- Interfaccia IWMPPlaylistCollection (VB e C) Windows Media Player
- Interfaccia IWMPPlaylistCollection (VB e C) Windows Media Player , descritta
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection (VB and C )
- IWMPPlaylistCollection (VB and C ).setDeleted
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ae130b9134d9ad6e19fa062946a591cdf7749b428201750fda8ff55252c3212
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118575217"
---
# <a name="iwmpplaylistcollection-vb-and-c-interface"></a>Interfaccia IWMPPlaylistCollection (VB e C#)

Fornisce metodi per la modifica **delle interfacce IWMPPlaylist** e **IWMPPlaylistArray** in una raccolta.

## <a name="members"></a>Membri

**L'interfaccia IWMPPlaylistCollection (VB e C#)** ha questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IWMPPlaylistCollection (VB e C#)** ha questi metodi.



| Metodo                                                                                                 | Descrizione                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**getAll**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getall--vb-and-c.md)                 | Restituisce **un'interfaccia IWMPPlaylistArray** che fornisce l'accesso a tutte le playlist nella libreria.<br/>             |
| [**getByName**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)           | Restituisce **un'interfaccia IWMPPlaylistArray** che fornisce l'accesso alle playlist con il nome specificato, se presente.<br/> |
| [**importPlaylist**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md) | Aggiunge una playlist statica alla libreria.<br/>                                                                              |
| [**isDeleted**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-isdeleted--vb-and-c.md)           | Restituisce un valore che indica se la playlist specificata si trova nella cartella degli elementi eliminati.<br/>                           |
| [**newPlaylist**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)       | Restituisce **un'interfaccia IWMPPlaylist** per una nuova playlist vuota nella libreria.<br/>                                     |
| [**Rimuovere**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-remove--vb-and-c.md)                 | Rimuove una playlist dalla libreria.<br/>                                                                                |
| **setDeleted**                                                                                         | Non più supportata.<br/>                                                                                                |



 

Ottenere **un'interfaccia IWMPPlaylistCollection** usando la proprietà seguente.



| Oggetto                                                                   | Proprietà                                                                                 |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Oggetto AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**playlistCollection**](axwmplib-axwindowsmediaplayer-playlistcollection--vb-and-c.md) |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce per Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interfaccia IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPPlaylistArray (VB e C#)**](iwmpplaylistarray--vb-and-c.md)
</dt> </dl>

 

 





