---
description: Windows Il programma di installazione può configurare l'installazione del software usando i valori delle variabili definite in un pacchetto di installazione o dall'utente.
ms.assetid: b7b715e7-e92c-4b84-b60d-a0ff8412749b
title: Informazioni sulle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb4a7bdd5a70721520c4d2afb975aabaca312975dc3bf4b7d94215112f69a0a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382078"
---
# <a name="about-properties"></a>Informazioni sulle proprietà

Windows Il programma di installazione può configurare l'installazione del software usando i valori delle variabili definite in un pacchetto di installazione o dall'utente.

Windows Il programma di installazione usa tre categorie di variabili globali durante un'installazione:

-   Proprietà private: il programma di installazione usa proprietà private internamente e i relativi valori devono essere creati nel database di installazione o impostati su valori determinati dall'ambiente operativo.
-   Proprietà pubbliche: le proprietà pubbliche possono essere scritte nel database e modificate da un utente o un amministratore di sistema dalla riga di comando, applicando una trasformazione o interagendo con un'interfaccia utente modificata.
-   Proprietà pubbliche con restrizioni: per motivi di sicurezza, l'autore di un pacchetto di installazione può limitare le proprietà pubbliche che un utente può modificare.

Non tutte le proprietà devono essere definite in ogni pacchetto, ma è necessario definire un piccolo set di proprietà obbligatorie in ogni pacchetto. Il programma di installazione imposta i valori delle proprietà in un particolare ordine di precedenza.

[Proprietà private](private-properties.md)

[Proprietà pubbliche](public-properties.md)

[Proprietà pubbliche con restrizioni](restricted-public-properties.md)

[Proprietà obbligatorie](required-properties.md)

[Ordine di precedenza delle proprietà](order-of-property-precedence.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo delle proprietà](using-properties.md)
</dt> <dt>

[Riferimento alle proprietà](property-reference.md)
</dt> </dl>

 

 



