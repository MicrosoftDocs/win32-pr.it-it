---
title: Strutture (messaggi di input del puntatore e notifiche)
description: Negli argomenti di questa sezione vengono fornite le specifiche di riferimento per le strutture di notifiche e messaggi di input del puntatore.
ms.assetid: 2224DCD0-DAE1-4AC2-AB36-23D114801138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: bc796c3924df9a1a349ea2180123f88f56d6a96c
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/26/2021
ms.locfileid: "106334017"
---
# <a name="pointer-input-messages-and-notifications-structures"></a>Strutture di notifiche e messaggi di input del puntatore

Negli argomenti di questa sezione vengono fornite le specifiche di riferimento per le strutture di [notifiche e messaggi di input del puntatore](messages-and-notifications-portal.md) .

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                            | Descrizione                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INPUT_TRANSFORM**](/previous-versions/windows/desktop/api)<br/>                           | Definisce la matrice che rappresenta una trasformazione in un consumer di messaggi. Questa matrice può essere utilizzata per trasformare i dati di input del puntatore da coordinate client a coordinate dello schermo, mentre l'inverso può essere utilizzato per trasformare i dati di input del puntatore dalle coordinate dello schermo alle coordinate del client. <br/>                                                                 |
| [**POINTER_INFO**](/previous-versions/windows/desktop/api)<br/>                          | Contiene informazioni di base sul puntatore comuni a tutti i tipi di puntatore. Le applicazioni possono recuperare queste informazioni usando le funzioni [**GetPointerInfo**](/previous-versions/windows/desktop/api), [**GetPointerFrameInfo**](/previous-versions/windows/desktop/api), [**GetPointerInfoHistory**](/previous-versions/windows/desktop/api) e [**GetPointerFrameInfoHistory**](/previous-versions/windows/desktop/api) . <br/> |
| [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api)<br/>                 | Definisce informazioni di base sulla penna comuni a tutti i tipi di puntatore. <br/>                                                                                                                                                                                                                                                                                                |
| [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api)<br/>             | Definisce le informazioni di base sul tocco comuni a tutti i tipi di puntatore.<br/>                                                                                                                                                                                                                                                                                               |
| [**TOUCHPREDICTIONPARAMETERS**](/previous-versions/windows/desktop/api)<br/> | Contiene i dettagli di input dell'hardware che possono essere usati per stimare le destinazioni tocco e per compensare la latenza hardware durante l'elaborazione dell'input tocco e movimento che contiene i dati relativi alla distanza e alla velocità.<br/>                                                                                                                                                       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento al messaggio di input del puntatore](wmpointer-reference.md)
</dt> </dl>

 

 





