---
description: Windows Installer possibile configurare l'installazione del software utilizzando i valori delle variabili definite in un pacchetto di installazione o dall'utente.
ms.assetid: b7b715e7-e92c-4b84-b60d-a0ff8412749b
title: Informazioni sulle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dc5d8154533cfebf4163983a149a547372ef4a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227228"
---
# <a name="about-properties"></a>Informazioni sulle proprietà

Windows Installer possibile configurare l'installazione del software utilizzando i valori delle variabili definite in un pacchetto di installazione o dall'utente.

Windows Installer usa tre categorie di variabili globali durante un'installazione:

-   Proprietà private: il programma di installazione utilizza internamente le proprietà private e i relativi valori devono essere creati nel database di installazione o impostati su valori determinati dall'ambiente operativo.
-   Proprietà pubbliche: le proprietà pubbliche possono essere create nel database e modificate da un utente o da un amministratore di sistema nella riga di comando, applicando una trasformazione o interagendo con un'interfaccia utente creata.
-   Proprietà pubbliche limitate: per motivi di sicurezza, l'autore di un pacchetto di installazione può limitare le proprietà pubbliche che un utente può modificare.

Non è necessario definire tutte le proprietà in ogni pacchetto. è necessario definire un piccolo set di proprietà obbligatorie in ogni pacchetto. Il programma di installazione imposta i valori delle proprietà in un ordine di precedenza particolare.

[Proprietà private](private-properties.md)

[Proprietà pubbliche](public-properties.md)

[Proprietà pubbliche limitate](restricted-public-properties.md)

[Proprietà obbligatorie](required-properties.md)

[Ordine di precedenza delle proprietà](order-of-property-precedence.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo delle proprietà](using-properties.md)
</dt> <dt>

[Riferimento alla proprietà](property-reference.md)
</dt> </dl>

 

 



