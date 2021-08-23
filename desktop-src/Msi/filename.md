---
description: Il tipo di dati Filename è una stringa di testo contenente un nome file o una cartella.
ms.assetid: af59e1b8-0699-4031-895f-415752611e21
title: Nome file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19d125a1151520fb4d3b885bd815b0a5bf58d2b00ec61581fc7773f1da1bd29e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118636205"
---
# <a name="filename"></a>Nome file

Il tipo di dati Filename è una stringa di testo contenente un nome file o una cartella. Per impostazione predefinita, si presuppone che il nome del file usi la sintassi del nome file breve. ovvero il nome di otto caratteri, il punto (.) e l'estensione di 3 caratteri. È necessario specificare sempre un nome di file breve perché è possibile impostare la proprietà [**SHORTFILENAMES**](shortfilenames.md) oppure il volume di destinazione per l'installazione può supportare solo nomi di file brevi.

Per includere un nome di file lungo con il nome di file breve, separarlo dal nome del file breve con una barra verticale ( \| ).

Ad esempio, le due stringhe seguenti sono valide:

-   status.txt
-   projec~1.txt\| Project Status.txt

I nomi di file brevi e lunghi non devono contenere i caratteri seguenti:

-   barra (/) o ( \\ )
-   punto interrogativo (?)
-   barra verticale ( \| )
-   parentesi uncinata chiusa (>)
-   parentesi uncinata aperta (<)
-   due punti (:)
-   asterisco ( \* )
-   virgolette doppie (")

Inoltre, i nomi di file brevi non devono contenere i caratteri seguenti:

-   segno di addizione (+)
-   virgola (,)
-   punto e virgola (;)
-   segno di uguale (=)
-   parentesi quadra aperta ( \[ )
-   parentesi quadra chiusa ( \] )

Non è consentito alcuno spazio prima del separatore barra verticale ( \| ) per la sintassi nome file breve/nome file lungo. I nomi di file brevi non possono includere uno spazio, anche se può essere un nome di file lungo. Dopo il separatore può esistere uno spazio solo se il nome file lungo del nome file inizia con lo spazio. Non è consentita alcuna sintassi di percorso completo.

> [!Note]  
> Il formato della colonna FileName della tabella [MsiEmbeddedUI](msiembeddedui-table.md) è simile al formato Tipo di dati Nome file ad eccezione del fatto che il separatore barra verticale ( ) per la sintassi nome file breve/nome file lungo non \| è disponibile.

 

 

 



