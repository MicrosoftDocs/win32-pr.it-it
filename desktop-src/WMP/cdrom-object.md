---
title: Oggetto Cdrom
description: L'oggetto Cdrom consente di accedere a un CD o DVD nell'unità.
ms.assetid: 9045b130-3e08-4880-a4e7-79b704c4c1f9
keywords:
- Oggetto Cdrom Windows Media Player
topic_type:
- apiref
api_name:
- Cdrom Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 60c4e1081dec3e44107778e45fd911e0c4bb673d27b5e19874508ddbacb270ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342644"
---
# <a name="cdrom-object"></a>Oggetto Cdrom

**L'oggetto Cdrom** consente di accedere a un CD o DVD nell'unità.

**L'oggetto Cdrom** supporta le proprietà seguenti.



| Proprietà                                   | Descrizione                                                                                                                                             |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [driveSpecifier](cdrom-drivespecifier.md) | Recupera la lettera di unità CD o DVD.                                                                                                                   |
| [Playlist](cdrom-playlist.md)             | Recupera un oggetto [Playlist](playlist-object.md) che rappresenta le tracce sul CD attualmente nell'unità CD o le voci del titolo di livello radice per il DVD. |



 

**L'oggetto Cdrom** supporta il metodo seguente.



| Metodo                   | Descrizione                          |
|--------------------------|--------------------------------------|
| [Espellere](cdrom-eject.md) | Espulse il CD o DVD dall'unità. |



 

È possibile accedere all'oggetto **Cdrom** tramite il metodo seguente.



| Oggetto                                        | Metodo                           |
|-----------------------------------------------|----------------------------------|
| [Raccolta CdromCollection](cdromcollection-object.md) | [item](cdromcollection-item.md) |



 

A scopo illustrativo, player.cdromCollection.item(*index*) viene usato nelle sezioni della sintassi di riferimento.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Informazioni di riferimento sul modello a oggetti per lo scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




