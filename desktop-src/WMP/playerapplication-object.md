---
title: Oggetto PlayerApplication
description: L'oggetto PlayerApplication fornisce un modo per coordinare il passaggio tra un controllo Media Player Windows remoto e la modalità completa di Windows Media Player.
ms.assetid: 904bb30c-939d-4aeb-ba4b-c27afee471ea
keywords:
- Media Player di Windows oggetto PlayerApplication
topic_type:
- apiref
api_name:
- PlayerApplication Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 950efeb0a84f43dec904b3ffd21f715061e50d4d
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2019
ms.locfileid: "104334951"
---
# <a name="playerapplication-object"></a>Oggetto PlayerApplication

L'oggetto **PlayerApplication** fornisce un modo per coordinare il passaggio tra un controllo Media Player Windows remoto e la modalità completa di Windows Media Player. Questo oggetto viene usato solo con i programmi C++ che implementano l'interfaccia **IWMPRemoteMediaServices** e incorporano il controllo Player in modalità remota. I file di interfaccia usati come interfacce personalizzate per il controllo Windows Media Player remoto accedono a questo oggetto nel codice di script tramite l'attributo globale **playerApplication** .

L'oggetto **PlayerApplication** supporta le proprietà seguenti.



| Proprietà                                           | Descrizione                                                                                              |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [hasDisplay](playerapplication-hasdisplay.md)     | Recupera un valore che indica se il video può essere visualizzato tramite il controllo Media Player remoto di Windows. |
| [playerDocked](playerapplication-playerdocked.md) | Recupera un valore che indica se Windows Media Player si trova in uno stato ancorato.                          |



 

L'oggetto **PlayerApplication** supporta i metodi seguenti.



| Metodo                                                                       | Descrizione                                                                     |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [switchToControl](playerapplication-switchtocontrol.md)                     | Passa un controllo Media Player Windows remoto allo stato ancorato.            |
| [switchToPlayerApplication](playerapplication-switchtoplayerapplication.md) | Passa un controllo Media Player Windows remoto alla modalità completa del lettore. |



 

È possibile accedere all'oggetto **PlayerApplication** tramite la proprietà seguente.



| Oggetto                      | Proprietà                                          |
|-----------------------------|---------------------------------------------------|
| [Player](player-object.md) | [playerApplication](player-playerapplication.md) |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento del modello a oggetti per lo scripting**](object-model-reference-for-scripting.md)
</dt> <dt>

[**Gestione remota del controllo di Windows Media Player**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




