---
description: Il tipo di dati filename è una stringa di testo contenente un nome file o una cartella.
ms.assetid: af59e1b8-0699-4031-895f-415752611e21
title: Nome file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fc049fa0808efc180afbd715e311a124bfdada9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528189"
---
# <a name="filename"></a>Nome file

Il tipo di dati filename è una stringa di testo contenente un nome file o una cartella. Per impostazione predefinita, si presuppone che il nome file usi la sintassi del nome file breve. ovvero un nome di otto caratteri, un punto (.) e un'estensione di 3 caratteri. È necessario specificare sempre un nome di file breve perché è possibile impostare la proprietà [**SHORTFILENAMES**](shortfilenames.md) o il volume di destinazione per l'installazione può supportare solo nomi di file brevi.

Per includere un nome di file lungo con il nome del file breve, separarlo dal nome del file breve con una barra verticale ( \| ).

Ad esempio, le due stringhe seguenti sono valide:

-   status.txt
-   Project ~1.txt\| progetto Status.txt

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

Non è consentito alcuno spazio prima del separatore della barra verticale ( \| ) per il nome file breve o la sintassi del nome file lungo. I nomi di file brevi non possono includere uno spazio, sebbene sia possibile un nome di file lungo. Uno spazio può esistere dopo il separatore solo se il nome di file lungo del nome del file inizia con lo spazio. Non è consentita alcuna sintassi per percorsi completi.

> [!Note]  
> Il formato della colonna FileName della tabella [MsiEmbeddedUI](msiembeddedui-table.md) è simile al tipo di dati Format filename, tranne per il fatto che il separatore della barra verticale ( \| ) per il nome file breve o il nome di file lungo non è disponibile.

 

 

 



