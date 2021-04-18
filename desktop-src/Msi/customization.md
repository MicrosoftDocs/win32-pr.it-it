---
description: Poiché il Windows Installer conserva tutte le informazioni sull'installazione di in un database relazionale, l'installazione di un'applicazione o di un prodotto può essere personalizzata per gruppi di utenti specifici applicando operazioni di trasformazione al pacchetto.
ms.assetid: 98c5cda2-a01a-4bdd-840f-76c0ffacd194
title: Personalizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5238cc145bc4a47bff459cb6caa30be37e1ca6ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307844"
---
# <a name="customization"></a>Personalizzazione

Poiché il Windows Installer conserva tutte le informazioni sull'installazione di in un database relazionale, l'installazione di un'applicazione o di un prodotto può essere personalizzata per gruppi di utenti specifici applicando operazioni di trasformazione al pacchetto. Le trasformazioni possono essere utilizzate per incapsulare le varie personalizzazioni di un pacchetto di base richiesto da gruppi di lavoro diversi. Per altre informazioni, vedere [unioni e trasformazioni](merges-and-transforms.md).

Durante l'installazione è possibile applicare più trasformazioni di un pacchetto di base in tempo reale. Questo fornisce un meccanismo per assegnare in modo efficiente installazioni personalizzate a diversi gruppi di utenti. Questo, ad esempio, può essere utile nelle organizzazioni in cui i reparti di supporto per Finanza e personale richiedono installazioni diverse di un determinato prodotto. Il prodotto può essere reso disponibile a tutti gli utenti dell'organizzazione mediante un' [installazione amministrativa](administrative-installation.md) del pacchetto di base in un singolo punto di installazione amministrativa. Ogni gruppo di lavoro può quindi ricevere automaticamente la personalizzazione appropriata per mezzo di una trasformazione immediata al momento dell'installazione del prodotto.

 

 



