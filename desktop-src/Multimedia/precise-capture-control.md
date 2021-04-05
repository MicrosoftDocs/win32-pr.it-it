---
title: Controllo di acquisizione preciso
description: Controllo di acquisizione preciso
ms.assetid: 497c9d77-f392-4cbb-88f3-8418e1e9fc6b
keywords:
- Funzioni di callback AVICap, controllo di acquisizione preciso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0749d420d7a1999d074546a0cf577fdaceb72483
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515700"
---
# <a name="precise-capture-control"></a>Controllo di acquisizione preciso

Una finestra di acquisizione può fornire la funzione di callback Capture-Control con un controllo preciso sui momenti in cui l'acquisizione di flussi inizia e termina. Il primo messaggio inviato dal driver di acquisizione alla procedura di callback imposta il parametro *nState* su CONTROLCALLBACK \_ preroll dopo l'allocazione di tutti i buffer e tutte le altre preparazioni di acquisizione sono completate. Questo messaggio fornisce all'applicazione la possibilità di preregistrare le origini video. (La funzione di callback specifica *nState* come secondo parametro). La funzione di callback viene quindi restituita al momento esatto in cui viene avviata la registrazione. Un valore restituito **true** dalla funzione di callback continua l'acquisizione. Viene restituito un valore di **false** Aborts Capture. Una volta avviata l'acquisizione, la funzione di callback viene chiamata spesso con *nState* impostato sull'acquisizione di CONTROLCALLBACK \_ per consentire all'applicazione di terminare l'acquisizione restituendo **false**.

 

 




