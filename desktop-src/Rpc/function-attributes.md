---
title: Attributi di funzioni
description: Gli attributi \ callback \ e \ Local \ possono essere applicati come attributi di funzione.
ms.assetid: 05e19164-072c-4a5a-878d-845273975854
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75ef199b937d5a3e9a8444be9ed65749da007ced
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729642"
---
# <a name="function-attributes"></a>Attributi di funzioni

Gli **\[** [](/windows/desktop/Midl/callback) **\]** attributi locali e di callback **\[** [](/windows/desktop/Midl/local) **\]** possono essere applicati come attributi di funzione.

Un callback è una chiamata remota da server a client eseguita come parte di un thread di esecuzione singola concettuale. Un callback viene sempre emesso nel contesto di una chiamata remota (o callback) e viene eseguito dal thread che ha emesso la chiamata remota originale (o callback).

Spesso è consigliabile inserire una dichiarazione di routine locale nel file IDL, perché si tratta della posizione logica per descrivere le interfacce a un pacchetto. L' **\[** [](/windows/desktop/Midl/local) **\]** attributo local indica che una dichiarazione di routine non è in realtà una funzione remota, ma una procedura locale. Il compilatore MIDL non genera stub per le funzioni con l'attributo **\[ Local \]** .

È importante notare che l'uso del **\[** [**callback**](/windows/desktop/Midl/callback) **\]** non è consigliato nella programmazione multithread. Come funzione di programmazione a thread singolo, non è disponibile per supportare le richieste di sicurezza offerte da un ambiente multithread.

 

 