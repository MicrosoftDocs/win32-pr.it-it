---
title: Supporto per fumetti di Word
description: Supporto per fumetti di Word
ms.assetid: deac032f-0480-4a0d-bc69-e26f12666bbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f78316c509ece6fc8f9b0cefd50b1564a50697a3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221193"
---
# <a name="word-balloon-support"></a>Supporto per fumetti di Word

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

L'output parlato può anche apparire come output testuale sotto forma di fumetto di parole. Questo può essere usato per integrare l'output parlato di un carattere o come alternativa all'output audio quando si usa il metodo [**Speak**](speak-method.md) .

![Sì fumetto Word Master](images/f3ballon.gif)

È anche possibile usare un fumetto di Word per comunicare il tipo di carattere "Thinking" usando il metodo [**think**](think-method.md) . Viene visualizzato il testo fornito in un fumetto ancora "pensato". Il metodo **think** differisce anche dal metodo [**Speak**](speak-method.md) in quanto non produce alcun output audio.

I fumetti di Word supportano solo la comunicazione con didascalia dal carattere, non l'input dell'utente. Pertanto, la parola Balloon non supporta i controlli di input. Tuttavia, è possibile fornire facilmente l'input dell'utente per un carattere, usando le interfacce del linguaggio di programmazione o gli altri servizi di input forniti da Microsoft Agent, ad esempio il menu di scelta rapida.

Quando si definisce un carattere, è possibile specificare se includere il supporto per i fumetti di Word. Tuttavia, se si usa un carattere che include il supporto di Word Balloon, non è possibile disabilitare il supporto.

 

 




