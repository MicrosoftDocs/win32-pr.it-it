---
title: Interfaccia IWMPMetadataPicture (VB e C) (WMP. h)
description: Fornisce le proprietà per ottenere informazioni sull'immagine contenuta in un file multimediale digitale rappresentato da un attributo WM/Picturemetadata.
ms.assetid: f8260882-dfb8-4ff0-954c-5060cb7a6995
keywords:
- Interfaccia IWMPMetadataPicture (VB e C) Windows Media Player
- Interfaccia IWMPMetadataPicture (VB e C) Windows Media Player, descritta
topic_type:
- apiref
api_name:
- IWMPMetadataPicture (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3b462c431a136745974dcde5716c3bd81226f15
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331388"
---
# <a name="iwmpmetadatapicture-vb-and-c-interface"></a>Interfaccia IWMPMetadataPicture (VB e C#)

Fornisce le proprietà per ottenere informazioni sull'immagine contenuta in un file multimediale digitale rappresentato da un attributo di metadati [**WM/Picture**](/windows/desktop/wmformat/wmpicture). Questo attributo corrisponde alle immagini dell'album Art contenute in un file multimediale digitale, non all'Art album scaricato tramite Internet.

L'interfaccia **IWMPMetadataPicture** espone le proprietà seguenti.



| Proprietà                                                                                   | Descrizione                                                               |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [**Descrizione**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-description--vb-and-c.md) | Ottiene la descrizione dell'immagine rappresentata dall'attributo dei metadati.  |
| [**mimeType**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-mimetype--vb-and-c.md)       | Ottiene il tipo MIME dell'immagine rappresentata dall'attributo dei metadati.    |
| [**pictureType**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-picturetype--vb-and-c.md) | Ottiene il tipo di immagine dell'immagine rappresentata dall'attributo dei metadati. |
| [**URL**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-url--vb-and-c.md)                 | Solo per uso interno.                                                        |



 

Ottenere un'interfaccia **IWMPMetadataPicture** passando il nome dell'attributo [**WM/Picture**](/windows/desktop/wmformat/wmpicture) al metodo seguente ed eseguendo il cast dell'oggetto restituito.



| Interfaccia                                  | Proprietà                                                                             |
|--------------------------------------------|--------------------------------------------------------------------------------------|
| [**IWMPMedia3**](iwmpmedia3--vb-and-c.md) | [**getItemInfoByType**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md) |



 

## <a name="members"></a>Membri

L'interfaccia **IWMPMetadataPicture (VB e C#)** non definisce membri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce per Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

