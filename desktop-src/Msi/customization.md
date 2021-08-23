---
description: Poiché il Windows Installer mantiene tutte le informazioni sull'installazione in un database relazionale, l'installazione di un'applicazione o di un prodotto può essere personalizzata per determinati gruppi di utenti applicando le operazioni di trasformazione al pacchetto.
ms.assetid: 98c5cda2-a01a-4bdd-840f-76c0ffacd194
title: Personalizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ece84afd2b9ca5ce547d9ea96aed23786f78c89f01f5b5b5eaa78e2791e86b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947855"
---
# <a name="customization"></a>Personalizzazione

Poiché il Windows Installer mantiene tutte le informazioni sull'installazione in un database relazionale, l'installazione di un'applicazione o di un prodotto può essere personalizzata per determinati gruppi di utenti applicando le operazioni di trasformazione al pacchetto. Le trasformazioni possono essere usate per incapsulare le varie personalizzazioni di un pacchetto di base richieste da gruppi di lavoro diversi. Per altre informazioni, vedere [Unioni e trasformazioni](merges-and-transforms.md).

Durante l'installazione è possibile applicare più trasformazioni di un pacchetto di base in tempo reale. In questo modo viene fornito un meccanismo per assegnare in modo efficiente installazioni personalizzate a diversi gruppi di utenti. Ad esempio, ciò sarebbe utile nelle organizzazioni in cui i reparti di supporto finanziario e del personale richiedono installazioni diverse di un determinato prodotto. Il prodotto può essere reso disponibile a tutti gli utenti dell'organizzazione da [un'installazione](administrative-installation.md) amministrativa del pacchetto di base a un singolo punto di installazione amministrativa. Ogni gruppo di lavoro può quindi ricevere automaticamente la personalizzazione appropriata tramite una trasformazione in tempo reale quando installa il prodotto.

 

 



