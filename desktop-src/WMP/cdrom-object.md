---
title: Oggetto cdrom
description: L'oggetto cdrom fornisce un modo per accedere a un CD o DVD nell'unità.
ms.assetid: 9045b130-3e08-4880-a4e7-79b704c4c1f9
keywords:
- Media Player di Windows per oggetti cdrom
topic_type:
- apiref
api_name:
- Cdrom Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17c2de88749b4dd4a0ab756b77866c16e8878486
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104333191"
---
# <a name="cdrom-object"></a>Oggetto cdrom

L'oggetto **CDROM** fornisce un modo per accedere a un CD o DVD nell'unità.

L'oggetto **CDROM** supporta le seguenti proprietà.



| Proprietà                                   | Descrizione                                                                                                                                             |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [driveSpecifier](cdrom-drivespecifier.md) | Recupera la lettera dell'unità CD o DVD.                                                                                                                   |
| [playlist](cdrom-playlist.md)             | Recupera un oggetto [playlist](playlist-object.md) che rappresenta le tracce del CD attualmente presenti nell'unità CD o le voci del titolo a livello di radice per DVD. |



 

L'oggetto **CDROM** supporta il seguente metodo.



| Metodo                   | Descrizione                          |
|--------------------------|--------------------------------------|
| [Eject](cdrom-eject.md) | Espelle il CD o il DVD dall'unità. |



 

È possibile accedere all'oggetto **CDROM** tramite il metodo seguente.



| Oggetto                                        | Metodo                           |
|-----------------------------------------------|----------------------------------|
| [Cdromcollection](cdromcollection-object.md) | [item](cdromcollection-item.md) |



 

Ai fini dell'illustrazione, Player. cdromCollection. Item (*index*) viene usato nelle sezioni della sintassi di riferimento.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento del modello a oggetti per lo scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




