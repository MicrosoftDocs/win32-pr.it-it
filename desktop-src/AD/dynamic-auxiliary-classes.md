---
title: Classi ausiliarie dinamiche
description: Analogamente alle classi di oggetti strutturali e astratte, le classi ausiliarie sono definite da un oggetto classSchema nello schema Active Directory.
ms.assetid: bd5f6aed-c79a-4c03-ad03-a4ae00f0b888
ms.tgt_platform: multiple
keywords:
- Active Directory (classi ausiliarie dinamiche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c13fc8231b5232b82a61b9409f1736e5bd9249
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472579"
---
# <a name="dynamic-auxiliary-classes"></a>Classi ausiliarie dinamiche

Analogamente alle classi di oggetti strutturali e astratte, le classi ausiliarie sono definite da un oggetto [**classSchema**](/windows/desktop/ADSchema/c-classschema) nello schema Active Directory. Per altre informazioni, vedere [classi strutturali, astratte e ausiliarie](structural-abstract-and-auxiliary-classes.md). Questa definizione dello schema specifica varie caratteristiche della classe, inclusi gli attributi associati alla classe.

Diversamente dalle classi strutturali, non è possibile creare un'istanza di una classe ausiliaria come si può con una classe strutturale. Usare invece una classe ausiliaria per estendere l'elenco di attributi associato a un'altra classe di oggetti strutturale, astratta o ausiliaria.

Nella versione iniziale di Windows 2000 Active Directory Domain Services fornito supporto per collegare staticamente le classi ausiliarie alla definizione [**classSchema**](/windows/desktop/ADSchema/c-classschema) di un'altra classe di oggetti. Quando una classe ausiliaria viene utilizzata in questo modo, ogni istanza della classe di oggetti supporta gli attributi della classe ausiliaria.

**Windows 2000 Server e versioni precedenti:** Active Directory Domain Services non fornisce supporto per collegare in modo dinamico le classi ausiliarie a singoli oggetti e non solo a intere classi di oggetti. Inoltre, le classi ausiliarie associate a un'istanza di oggetto non possono essere successivamente rimosse dall'istanza di.

**Windows Server 2003:** Le classi ausiliarie dinamiche sono supportate quando tutti i controller di dominio della foresta eseguono Windows Server 2003 e la modalità funzionale della foresta è Windows Server 2003.

Per ulteriori informazioni sulle classi ausiliarie, vedere:

-   [Classi ausiliarie collegate in modo dinamico](dynamically-linked-auxiliary-classes.md)
-   [Classi ausiliarie collegate in modo statico](statically-linked-auxiliary-classes.md)
-   [Determinazione delle classi associate a un'istanza dell'oggetto](determining-the-classes-associated-with-an-object-instance.md)
-   [Aggiunta di una classe ausiliaria a un'istanza di oggetto](adding-an-auxiliary-class-to-an-object-instance.md)

Per ulteriori informazioni sui livelli di funzionalità della foresta, vedere "come generare Active Directory livelli di funzionalità del dominio e della foresta" nella Knowledge base della guida e del supporto tecnico all'indirizzo [https://support/microsoft.com/kb/322692\#4](https://support.microsoft.com/kb/322692) .

 

 