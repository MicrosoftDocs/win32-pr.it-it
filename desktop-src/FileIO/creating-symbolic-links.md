---
description: Creare collegamenti simbolici che usano un percorso assoluto o relativo usando la funzione CreateSymbolicLink.
ms.assetid: 3821478d-87bb-4e47-8263-d977cf665503
title: Creazione di collegamenti simbolici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0340dc362ff550ab2d74e533ac66e74622c965266440103d6f6ec155bfa80f21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150857"
---
# <a name="creating-symbolic-links"></a>Creazione di collegamenti simbolici

La funzione [**CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) consente di creare collegamenti simbolici usando un percorso assoluto o relativo.

I collegamenti simbolici possono essere collegamenti assoluti o relativi. I collegamenti assoluti sono collegamenti che specificano ogni parte del nome del percorso. i collegamenti relativi vengono determinati in relazione alla posizione in cui gli identificatori di collegamento relativo si trova in un percorso specificato. I collegamenti relativi vengono specificati usando le convenzioni seguenti:

-   Punto (. e ..) convenzioni, ad esempio ".. \\ " risolve il percorso relativo alla directory padre.
-   Nomi senza barre ( ) : \\ ad esempio, "tmp" risolve il percorso relativo alla directory corrente.
-   Relativo alla radice, ad esempio " Windows System32" viene risolto \\ nell'unità corrente : Windows \\  \\ \\ System32". directory
-   Relativo alla directory di lavoro corrente, ad esempio se la directory di lavoro corrente è "C: \\ Windows \\ System32", "C:File.txt" viene risolto in "C: \\ Windows \\ System32 \\File.txt".

    **Nota**  Se si specifica un collegamento relativo alla directory di lavoro corrente, viene creato come collegamento assoluto, a causa del modo in cui la directory di lavoro corrente viene elaborata in base all'utente e al thread.

Un collegamento simbolico può contenere anche punti di giunzione e cartelle montate come parte del nome del percorso.

I collegamenti simbolici possono puntare direttamente a un file o a una directory remota usando il percorso UNC.

I collegamenti simbolici relativi sono limitati a un singolo volume.

## <a name="example-of-an-absolute-symbolic-link"></a>Esempio di collegamento simbolico assoluto

In questo esempio il percorso originale contiene un componente, '*x*', che è un collegamento simbolico assoluto. Quando viene rilevato '*x*', il frammento del percorso originale fino a e incluso '*x*' viene completamente sostituito dal percorso a cui punta '*x*'. Il resto del percorso dopo '*x*' viene aggiunto a questo nuovo percorso. Questo diventa ora il percorso modificato.

X: "C: \\ alpha \\ beta \\ absLink \\ gamma \\ file"

Collegamento: "absLink" esegue il mapping a \\ \\ "machineB \\ share"

Percorso modificato: " \\ \\ machineB \\ share \\ gamma \\ file"

## <a name="example-of-a-relative-symbolic-links"></a>Esempio di collegamenti simbolici relativi

In questo esempio il percorso originale contiene un componente '*x*', che è un collegamento simbolico relativo. Quando viene rilevato '*x*', '*x*' viene completamente sostituito dal nuovo frammento a cui punta '*x*'. Il resto del percorso dopo '*x*', viene aggiunto al nuovo percorso. Tutti i punti (..) in questo nuovo percorso sostituiscono i componenti visualizzati prima dei punti (..). Ogni set di punti sostituisce il componente precedente. Se il numero di punti (..) supera il numero di componenti, viene restituito un errore. In caso contrario, al termine della sostituzione di tutti i componenti, rimane il percorso finale modificato.

X: C: \\ alpha beta link gamma \\ \\ \\ \\ file

Collegamento: "link" è mappato a ".. \\ .. \\ theta"

Percorso modificato: "C: \\ alpha \\ beta \\ .. \\ .. \\ theta \\ gamma \\ file"

Percorso finale: "C: \\ theta \\ gamma \\ file"

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Collegamenti simbolici](symbolic-links.md)
</dt> <dt>

[Collegamenti e giunzioni rigidi](hard-links-and-junctions.md)
</dt> <dt>

[Denominazione di file, percorsi e spazi dei nomi](naming-a-file.md)
</dt> </dl>

 

 



