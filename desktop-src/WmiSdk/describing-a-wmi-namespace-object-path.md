---
description: Il percorso di un oggetto spazio dei nomi descrive la posizione di un determinato spazio dei nomi in un server. Il percorso di un oggetto spazio dei nomi contiene elementi server e spazio dei nomi e viene formattato con le barre avanti o indietro.
ms.assetid: 6d8da19e-0914-4267-870e-c203176b895e
ms.tgt_platform: multiple
title: Descrizione del percorso di un oggetto dello spazio dei nomi WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586104a1c193f1c229b0fbb27437d22e3686585b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049814"
---
# <a name="describing-a-wmi-namespace-object-path"></a>Descrizione del percorso di un oggetto dello spazio dei nomi WMI

Il percorso di un oggetto spazio dei nomi descrive la posizione di un determinato spazio dei nomi in un server. Il percorso di un oggetto spazio dei nomi contiene elementi server e spazio dei nomi e viene formattato con le barre avanti o indietro.

L'elemento server specifica il nome di rete del computer che ospita lo spazio dei nomi, come illustrato nell'esempio seguente.

``` syntax
\\Server\Namespace
```

\- - oppure -

``` syntax
//Server/Namespace
```

Se il server è il computer locale, usare un singolo punto anziché il nome del server, come illustrato nell'esempio seguente.

``` syntax
\\.\Namespace
```

L'elemento Namespace specifica qualsiasi spazio dei nomi valido. Uno spazio dei nomi è rappresentato da una stringa gerarchica contenente elementi delimitati da singole barre rovesciate, ad esempio \\ CIMV2 radice. Non è possibile utilizzare le barre nei nomi degli spazi dei nomi.

 

 



