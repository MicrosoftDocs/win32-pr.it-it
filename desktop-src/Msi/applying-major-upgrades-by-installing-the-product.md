---
description: È possibile applicare un aggiornamento importante installando il nuovo pacchetto di installazione per il prodotto aggiornato.
ms.assetid: f4fb28be-5ec0-4eac-9d4d-eccf5bd61ac4
title: Applicazione degli aggiornamenti principali tramite l'installazione del prodotto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7619b2ae2b8e1f10cac2fcfae61dde0c6dbba5d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311056"
---
# <a name="applying-major-upgrades-by-installing-the-product"></a>Applicazione degli aggiornamenti principali tramite l'installazione del prodotto

È possibile applicare un aggiornamento importante installando il nuovo pacchetto di installazione per il prodotto aggiornato. Poiché gli aggiornamenti principali ottengono un codice prodotto diverso dal prodotto originale, l'installazione dell'aggiornamento deve essere considerata un'installazione di un nuovo prodotto. L'aggiornamento può essere semplicemente installato come un altro prodotto. È possibile fare in modo che il nuovo pacchetto di installazione gestisca la rimozione del prodotto precedente includendo la [tabella di aggiornamento](upgrade-table.md) e l'azione [FindRelatedProducts](findrelatedproducts-action.md) e [RemoveExistingProducts](removeexistingproducts-action.md).

**Per propagare un aggiornamento principale agli utenti correnti dalla riga di comando**

-   Dalla riga di comando, usare: **msiexec/i \[** _percorso del file MSI aggiornato_*_\]_*

**Per propagare un aggiornamento principale agli utenti correnti da un programma**

-   Da un programma, chiamare [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) e specificare il percorso del file MSI aggiornato.

 

 



