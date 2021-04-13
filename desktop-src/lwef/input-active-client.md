---
title: Client di Input-Active
description: Client di Input-Active
ms.assetid: b46e91d3-eca7-4a4a-b1ce-27b5e6ad92a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3223ddc7bb412b333d628f93cc56b27efd0abb7a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331252"
---
# <a name="input-active-client"></a>Client di Input-Active

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Poiché più applicazioni client possono condividere lo stesso carattere e perché più client possono usare contemporaneamente caratteri diversi, il server designa un client come client *attivo di input* e invia l'input del mouse e della voce solo a tale applicazione client. Questo mantiene la gestione ordinata dell'input dell'utente, in modo che un client appropriato risponda all'input.

In genere, l'interazione dell'utente determina quale applicazione client diventa attiva in input. Se, ad esempio, l'utente fa clic su un carattere, l'applicazione client di tale carattere diventa attiva per input. Analogamente, se un utente pronuncia il nome di un carattere, diventa attivo come input. Inoltre, quando il server elabora il metodo [**show**](show-method.md) di un carattere, il client di tale carattere diventa attivo come input.

Quando un carattere è nascosto, il client di tale carattere non sarà più attivo come input per tale carattere. Il server rende automaticamente attivo il client attivo di tutti i caratteri rimanenti. Quando tutti i caratteri sono nascosti, nessun client è attivo per l'input. Tuttavia, in questa situazione, se l'utente preme il tasto di scelta rapida in ascolto, Agent continuerà a restare in ascolto dei comandi (usando il motore di riconoscimento vocale che corrisponde al carattere superiore dell'ultimo client attivo di input).

Se più client condividono lo stesso carattere, il server designerà il *client attivo* come client attivo come input. Il carattere attivo è il primo nell'ordine del client. È possibile impostare il client come client attivo o non attivo usando il metodo [**Activate**](activate-method.md) . È anche possibile usare il metodo **Activate** per rendere esplicitamente attiva l'input del client. Tuttavia, per evitare di compromettere altri client del carattere, è necessario eseguire questa operazione solo quando l'applicazione client è attiva. Ad esempio, se l'utente fa clic sulla finestra dell'applicazione, attivando l'applicazione, è possibile chiamare il metodo **Activate** per ricevere ed elaborare l'input del mouse e della voce indirizzato al carattere.

 

 




