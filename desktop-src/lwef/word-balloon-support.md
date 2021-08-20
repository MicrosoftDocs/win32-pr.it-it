---
title: Supporto per il balloon delle parole
description: Supporto per il balloon delle parole
ms.assetid: deac032f-0480-4a0d-bc69-e26f12666bbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9aea0fbd2f73aefb1cedb7c57fc6359849c050761448fc45a9b4c90ea477f53f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118066722"
---
# <a name="word-balloon-support"></a>Supporto per il balloon delle parole

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

L'output parlato può anche essere visualizzato come output testuale sotto forma di fumetto. Può essere usato per integrare l'output parlato di un carattere o come alternativa all'output audio quando si usa il [**metodo Speak.**](speak-method.md)

![yes master word balloon](images/f3ballon.gif)

È anche possibile usare un fumetto di parole per comunicare ciò che un carattere sta "pensando" usando il [**metodo Think.**](think-method.md) Verrà visualizzato il testo fornito in un fumetto ancora "pensato". Il **metodo Think** differisce anche dal metodo [**Speak**](speak-method.md) perché non produce alcun output audio.

I balloon di parola supportano solo la comunicazione con sottotitoli in testo dal carattere, non l'input dell'utente. Pertanto, il fumetto non supporta i controlli di input. Tuttavia, è possibile fornire facilmente l'input dell'utente per un carattere, usando le interfacce del linguaggio di programmazione o gli altri servizi di input forniti da Microsoft Agent, ad esempio il menu a comparsa.

Quando si definisce un carattere, è possibile specificare se includere il supporto per il fumetto. Tuttavia, se si usa un carattere che include il supporto per il fumetto, non è possibile disabilitare il supporto.

 

 




