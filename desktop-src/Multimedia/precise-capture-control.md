---
title: Controllo di acquisizione preciso
description: Controllo di acquisizione preciso
ms.assetid: 497c9d77-f392-4cbb-88f3-8418e1e9fc6b
keywords:
- Funzioni di callback AVICap, controllo di acquisizione preciso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d365482f5f6309f9642aa5c8b497b58a1d9416e398e5c3624191d777e006b23e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118372661"
---
# <a name="precise-capture-control"></a>Controllo di acquisizione preciso

Una finestra di acquisizione può fornire alla funzione di callback di controllo di acquisizione un controllo preciso sui momenti di inizio e fine dell'acquisizione di streaming. Il primo messaggio inviato dal driver di acquisizione alla procedura di callback imposta il parametro *nState* su CONTROLCALLBACK PREROLL dopo il completamento dell'allocazione di tutti i buffer e di tutte le altre operazioni di preparazione \_ dell'acquisizione. Questo messaggio offre all'applicazione la possibilità di eseguire la pre-registrazione delle origini video. La funzione di callback specifica *nState* come secondo parametro. La funzione di callback restituisce quindi nel momento esatto in cui la registrazione deve iniziare. Il valore restituito **TRUE dalla** funzione di callback continua l'acquisizione. Il valore restituito **FALSE interrompe** l'acquisizione. Una volta avviata l'acquisizione, la funzione di callback viene chiamata di frequente con *nState* impostato su CONTROLCALLBACK CAPTURING per consentire all'applicazione di terminare l'acquisizione \_ restituisce **FALSE.**

 

 




