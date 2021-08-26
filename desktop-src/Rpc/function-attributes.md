---
title: Attributi di funzioni
description: Gli attributi \ callback\ e \ local\ possono essere applicati come attributi di funzione.
ms.assetid: 05e19164-072c-4a5a-878d-845273975854
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be36cac561a10ae2e1177c29dfc0e1219f650daf26af8154c47cdbd7e3d2bd57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021021"
---
# <a name="function-attributes"></a>Attributi di funzioni

Il **\[** [**callback e**](/windows/desktop/Midl/callback) **\]** gli **\[** [**attributi**](/windows/desktop/Midl/local) locali possono essere applicati come attributi di **\]** funzione.

Un callback è una chiamata remota dal server al client che viene eseguita come parte di un thread concettuale a esecuzione singola. Un callback viene sempre eseguito nel contesto di una chiamata remota (o callback) e viene eseguito dal thread che ha emesso la chiamata remota originale (o callback).

È spesso consigliabile inserire una dichiarazione di routine locale nel file IDL, poiché questa è la posizione logica per descrivere le interfacce di un pacchetto. **\[** [**L'attributo**](/windows/desktop/Midl/local) **\]** local indica che una dichiarazione di routine non è effettivamente una funzione remota, ma una routine locale. Il compilatore MIDL non genera stub per le funzioni con **\[ l'attributo \]** locale.

È importante notare che l'uso del **\[** [**callback**](/windows/desktop/Midl/callback) **\]** non è consigliato nella programmazione multi-thread. Come funzione di programmazione a thread singolo, non è in grado di supportare le richieste di sicurezza fornite da un ambiente multi-thread.

 

 