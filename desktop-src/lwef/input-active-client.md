---
title: Input-Active Client
description: Input-Active Client
ms.assetid: b46e91d3-eca7-4a4a-b1ce-27b5e6ad92a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9555b614a30e73df0cc7d1d81cd8192480d49261a32e8be8d164bdb277e4c0f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943961"
---
# <a name="input-active-client"></a>Input-Active Client

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Poiché più applicazioni client possono condividere lo stesso carattere e poiché più client possono usare caratteri diversi contemporaneamente, il server designa un client come client attivo per *l'input* e invia input vocale e mouse solo a tale applicazione client. In questo modo viene mantenuta la gestione ordinata dell'input dell'utente, in modo che un client appropriato risponda all'input.

In genere, l'interazione dell'utente determina quale applicazione client diventa attiva per l'input. Ad esempio, se l'utente fa clic su un carattere, l'applicazione client di tale carattere diventa attiva per l'input. Analogamente, se un utente pronuncia il nome di un carattere, diventa attivo per l'input. Inoltre, quando il server elabora il metodo [**Show**](show-method.md) di un carattere, il client di tale carattere diventa attivo per l'input.

Quando un carattere è nascosto, il client di tale carattere non sarà più attivo per tale carattere. Il server rende automaticamente attivo il client attivo di tutti i caratteri rimanenti. Quando tutti i caratteri sono nascosti, nessun client è attivo per l'input. Tuttavia, in questa situazione, se l'utente preme il tasto di scelta rapida Ascolto, Agent continuerà a restare in ascolto dei relativi comandi (usando il motore di riconoscimento vocale che corrisponde al carattere più in alto dell'ultimo client attivo di input).

Se più client condividono lo stesso carattere, il server designerà il *client attivo* come client attivo di input. Il carattere attivo è il primo nell'ordine del client. È possibile impostare il client come client attivo o non attivo usando il [**metodo Activate.**](activate-method.md) È anche possibile usare il **metodo Activate** per rendere attivo l'input del client in modo esplicito. ma per evitare l'interruzione di altri client del carattere, è consigliabile farlo solo quando l'applicazione client è attiva. Ad esempio, se l'utente fa clic sulla finestra dell'applicazione attivando l'applicazione, è possibile chiamare il **metodo Activate** per ricevere ed elaborare l'input vocale e del mouse indirizzato al carattere.

 

 




