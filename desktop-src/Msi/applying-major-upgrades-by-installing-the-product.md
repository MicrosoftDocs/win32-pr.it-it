---
description: È possibile applicare un aggiornamento importante installando il nuovo pacchetto di installazione per il prodotto aggiornato.
ms.assetid: f4fb28be-5ec0-4eac-9d4d-eccf5bd61ac4
title: Applicazione di aggiornamenti principali tramite l'installazione del prodotto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79570051ddbff27b12a11e04e41c37f4babad96ff045bc408e00c2b7164b263a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045681"
---
# <a name="applying-major-upgrades-by-installing-the-product"></a>Applicazione di aggiornamenti principali tramite l'installazione del prodotto

È possibile applicare un aggiornamento importante installando il nuovo pacchetto di installazione per il prodotto aggiornato. Poiché gli aggiornamenti principali ottengono un codice prodotto diverso dal prodotto originale, l'installazione dell'aggiornamento deve essere considerata come un'installazione di un nuovo prodotto. L'aggiornamento può essere semplicemente installato come un altro prodotto. È possibile fare in modo che il nuovo pacchetto di installazione gestirà la rimozione del prodotto precedente includendo la tabella [Upgrade](upgrade-table.md) e l'azione [FindRelatedProducts](findrelatedproducts-action.md) e [l'azione RemoveExistingProducts](removeexistingproducts-action.md).

**Per propagare un aggiornamento principale agli utenti correnti dalla riga di comando**

-   Dalla riga di comando usare: **msiexec /i \[** path to updated msi _file_*_\]_*

**Per propagare un aggiornamento principale agli utenti correnti da un programma**

-   Da un programma chiamare [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) e specificare il percorso del file msi aggiornato.

 

 



