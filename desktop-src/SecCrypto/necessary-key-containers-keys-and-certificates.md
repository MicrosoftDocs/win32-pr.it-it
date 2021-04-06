---
description: I programmi di esempio nelle sezioni seguenti eseguono operazioni che richiedono la disponibilità di coppie di chiavi pubbliche/private per la crittografia e la decrittografia di file, messaggi e firme.
ms.assetid: b03528ff-0170-4dde-ae35-f5c3951d6b1f
title: Contenitori chiave, chiavi e certificati necessari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2d1f01a59c83ea21437608608e033a2ee0f8fae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759464"
---
# <a name="necessary-key-containers-keys-and-certificates"></a>Contenitori chiave, chiavi e certificati necessari

I programmi di esempio nelle sezioni seguenti eseguono operazioni che richiedono la disponibilità di [*coppie di chiavi pubbliche/private*](../secgloss/p-gly.md) per la crittografia e la decrittografia di file, messaggi e firme. Molti di questi programmi verranno compilati, collegati ed eseguiti, ma non riusciranno in fase di esecuzione senza la presenza di [*contenitori*](../secgloss/k-gly.md)di chiavi, chiavi, [*archivi certificati*](../secgloss/c-gly.md)e certificati appropriati in tali archivi.

Inoltre, alcuni dei certificati nell'archivio MY devono disporre di alcune delle proprietà estese impostate.

La creazione del contenitore di chiavi predefinito necessario può essere eseguita eseguendo il programma nel [programma C di esempio: creazione di un contenitore di chiavi e generazione di chiavi](example-c-program-creating-a-key-container-and-generating-keys.md). Si noti che la creazione di un contenitore di chiavi non genera automaticamente coppie di chiavi pubbliche/private. Il programma di esempio, tuttavia, crea il contenitore di chiavi e genera le coppie di chiavi pubblica/privata.

Dopo la generazione delle coppie di chiavi pubblica/privata, è possibile ottenere i certificati di test con tali chiavi da un' [*autorità di certificazione*](../secgloss/c-gly.md) (CA).

Molti programmi presuppongono che i certificati con nomi di soggetto specifici esistano nell'archivio di sistema MY. In particolare, diversi programmi cercano certificati con i nomi di soggetto "certificato di test completo" e "Hortense". I nomi oggetto per i certificati possono essere modificati nel codice in modo che corrispondano ai nomi soggetto dei certificati presenti nell'archivio certificati personali.

Esecuzione del programma di esempio nel [programma C di esempio: elencare i certificati in un archivio](example-c-program-listing-the-certificates-in-a-store.md) visualizzerà tutti i certificati in un archivio e tutte le proprietà estese impostate per tali certificati.

 

 
