---
description: I programmi di esempio nelle sezioni seguenti eseguono operazioni che richiedono la disponibilità di coppie di chiavi pubblica/privata per la crittografia e la decrittografia di file, messaggi e firme.
ms.assetid: b03528ff-0170-4dde-ae35-f5c3951d6b1f
title: Contenitori di chiavi, chiavi e certificati necessari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee5f86f887050d0d7abe440c89cc9c9444dba26854645d5ad6d16279af91e1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992721"
---
# <a name="necessary-key-containers-keys-and-certificates"></a>Contenitori di chiavi, chiavi e certificati necessari

I programmi di esempio nelle sezioni seguenti eseguono operazioni che richiedono la disponibilità di coppie di chiavi [*pubblica/privata*](../secgloss/p-gly.md) per la crittografia e la decrittografia di file, messaggi e firme. Molti di questi programmi verranno compilati, collegati ed eseguiti, ma avranno esito negativo in fase di esecuzione senza l'esistenza di contenitori di [*chiavi,*](../secgloss/k-gly.md) [*chiavi,*](../secgloss/c-gly.md)archivi certificati e certificati in tali archivi.

Inoltre, alcuni certificati nell'archivio MY devono avere alcune delle relative proprietà estese impostate.

Per creare il contenitore di chiavi predefinito necessario, è possibile eseguire il programma in [Example C Program: Creating a Key Container and Generating Keys](example-c-program-creating-a-key-container-and-generating-keys.md). Si noti che la creazione di un contenitore di chiavi non genera automaticamente coppie di chiavi pubblica/privata. Il programma di esempio, tuttavia, crea il contenitore di chiavi e genera le coppie di chiavi pubblica/privata.

Dopo la generazione delle coppie di chiavi pubblica/privata, i certificati di test che usano tali chiavi possono essere ottenuti da un'autorità [*di certificazione*](../secgloss/c-gly.md) (CA).

Molti programmi presuppongono che nell'archivio di sistema MY siano presenti certificati con nomi di soggetto specifici. In particolare, diversi programmi ricercano i certificati con i nomi di soggetto "Full Test Cert" e "Hortense". I nomi dei soggetti per i certificati possono essere modificati nel codice in modo che corrispondano ai nomi dei soggetti dei certificati presenti nell'archivio certificati MY.

Esecuzione del programma di esempio nel programma C di [esempio:](example-c-program-listing-the-certificates-in-a-store.md) l'elenco dei certificati in un archivio consente di visualizzare tutti i certificati in un archivio e tutte le proprietà estese impostate su tali certificati.

 

 
