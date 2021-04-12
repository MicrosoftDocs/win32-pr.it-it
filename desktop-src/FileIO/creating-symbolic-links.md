---
description: Creare collegamenti simbolici che usano un percorso assoluto o relativo tramite la funzione CreateSymbolicLink.
ms.assetid: 3821478d-87bb-4e47-8263-d977cf665503
title: Creazione di collegamenti simbolici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c978532ffc11e44615d4de0ea902152438ecc7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347831"
---
# <a name="creating-symbolic-links"></a>Creazione di collegamenti simbolici

La funzione [**CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) consente di creare collegamenti simbolici usando un percorso assoluto o relativo.

I collegamenti simbolici possono essere collegamenti assoluti o relativi. I collegamenti assoluti sono collegamenti che specificano ogni parte del nome del percorso; i collegamenti relativi vengono determinati in relazione alla posizione in cui gli identificatori di collegamento relativi si trovano in un percorso specificato. I collegamenti relativi vengono specificati usando le convenzioni seguenti:

-   Punto (. e..) convenzioni, ad esempio ".. \\ " risolve il percorso relativo alla directory padre.
-   Nomi senza barre ( \) ad esempio, "tmp" risolve il percorso relativo alla directory corrente.
-   Relativa radice, ad esempio " \\ Windows \\ system32" viene risolto nell'*unità "Current Drive*: \\ Windows \\ system32". directory
-   Relativa alla directory di lavoro corrente, ad esempio se la directory di lavoro corrente è "C: \\ Windows \\ system32", "C:File.txt" viene risolto in "c: \\ Windows \\ system32 \\File.txt".

    **Nota**  Se si specifica un collegamento relativo alla directory di lavoro corrente, viene creato come collegamento assoluto, a causa del modo in cui la directory di lavoro corrente viene elaborata in base all'utente e al thread.

Un collegamento simbolico può anche contenere entrambi i punti di giunzione e le cartelle montate come parte del nome del percorso.

I collegamenti simbolici possono puntare direttamente a un file o a una directory remota utilizzando il percorso UNC.

I collegamenti simbolici relativi sono limitati a un singolo volume.

## <a name="example-of-an-absolute-symbolic-link"></a>Esempio di collegamento simbolico assoluto

In questo esempio, il percorso originale contiene un componente,'*x*', che è un collegamento simbolico assoluto. Quando viene rilevato '*x*', il frammento del percorso originale fino *a' x*' viene sostituito completamente dal percorso a cui punta '*x*'. Il resto del percorso dopo '*x*' viene aggiunto al nuovo percorso. Ora diventa il percorso modificato.

X: "C: \\ Alpha \\ beta \\ absLink \\ gamma \\ file"

Link: "absLink" viene mappato a " \\ \\ machineB \\ share"

Percorso modificato: " \\ \\ machineB \\ condivisione \\ \\ file gamma"

## <a name="example-of-a-relative-symbolic-links"></a>Esempio di collegamenti simbolici relativi

In questo esempio, il percorso originale contiene un componente "*x*", che è un collegamento simbolico relativo. Quando viene rilevato '*x*','*x*' viene sostituito completamente dal nuovo frammento a cui punta '*x*'. Il resto del percorso dopo '*x*' viene aggiunto al nuovo percorso. Tutti i punti (..) in questo nuovo percorso sostituiscono i componenti visualizzati prima dei punti (..). Ogni set di punti sostituisce il componente precedente. Se il numero di punti (..) supera il numero di componenti, viene restituito un errore. In caso contrario, al termine della sostituzione di tutti i componenti, rimane il percorso finale modificato.

X: C: \\ \\ \\ file gamma di collegamento alfa beta \\ \\

Collegamento: "link" esegue il mapping a ".. \\ .. \\ Theta

Percorso modificato: "C: \\ Alpha \\ beta \\ .. \\ .. \\ \\file gamma Theta \\ "

Percorso finale: "C: \\ theta \\ gamma \\ file"

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Collegamenti simbolici](symbolic-links.md)
</dt> <dt>

[Collegamenti reali e giunzioni](hard-links-and-junctions.md)
</dt> <dt>

[Denominazione di file, percorsi e spazi dei nomi](naming-a-file.md)
</dt> </dl>

 

 



