---
title: Oggetto PlayerApplication
description: L'oggetto PlayerApplication consente di coordinare il passaggio tra un controllo Windows Media Player remoto e la modalità completa Windows Media Player.
ms.assetid: 904bb30c-939d-4aeb-ba4b-c27afee471ea
keywords:
- Oggetto PlayerApplication Windows Media Player
topic_type:
- apiref
api_name:
- PlayerApplication Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 46ac009ead54fc4d32b1a302f9228f84484ba6911b353ebb5443653378d9ce61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118571832"
---
# <a name="playerapplication-object"></a>Oggetto PlayerApplication

**L'oggetto PlayerApplication** consente di coordinare il passaggio tra un controllo Windows Media Player remoto e la modalità completa Windows Media Player. Questo oggetto viene usato solo con i programmi C++ che implementano **l'interfaccia IWMPRemoteMediaServices** e incorporano il controllo Player in modalità remota. I file dell'interfaccia utente usati come interfacce personalizzate per l'Windows Media Player controllo remoto accedono a questo oggetto nel codice script tramite **l'attributo globale playerApplication.**

**L'oggetto PlayerApplication** supporta le proprietà seguenti.



| Proprietà                                           | Descrizione                                                                                              |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [hasDisplay](playerapplication-hasdisplay.md)     | Recupera un valore che indica se il video può essere visualizzato tramite il controllo Windows Media Player remoto. |
| [playerDocked](playerapplication-playerdocked.md) | Recupera un valore che indica se Windows Media Player è in uno stato ancorato.                          |



 

**L'oggetto PlayerApplication** supporta i metodi seguenti.



| Metodo                                                                       | Descrizione                                                                     |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [switchToControl](playerapplication-switchtocontrol.md)                     | Passa un controllo Windows Media Player remoto allo stato ancorato.            |
| [switchToPlayerApplication](playerapplication-switchtoplayerapplication.md) | Passa un controllo Windows Media Player remoto alla modalità completa del lettore. |



 

**L'oggetto PlayerApplication** è accessibile tramite la proprietà seguente.



| Oggetto                      | Proprietà                                          |
|-----------------------------|---------------------------------------------------|
| [Player](player-object.md) | [playerApplication](player-playerapplication.md) |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Informazioni di riferimento sul modello a oggetti per lo scripting**](object-model-reference-for-scripting.md)
</dt> <dt>

[**Gestione remota del controllo di Windows Media Player**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




