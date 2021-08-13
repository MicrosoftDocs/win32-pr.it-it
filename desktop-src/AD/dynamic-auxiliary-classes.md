---
title: Classi ausiliarie dinamiche
description: Analogamente alle classi di oggetti strutturali e astratte, le classi ausiliarie sono definite da un oggetto classSchema nello schema di Active Directory.
ms.assetid: bd5f6aed-c79a-4c03-ad03-a4ae00f0b888
ms.tgt_platform: multiple
keywords:
- Classi ausiliarie dinamiche AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45ce88f525b5d72a271aab1746a0ce0d0b308cb7022c4702433b82038c101435
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118429901"
---
# <a name="dynamic-auxiliary-classes"></a>Classi ausiliarie dinamiche

Analogamente alle classi di oggetti strutturali e astratte, le classi ausiliarie sono definite da un [**oggetto classSchema**](/windows/desktop/ADSchema/c-classschema) nello schema di Active Directory. Per altre informazioni, vedere [Classi strutturali, astratte e ausiliarie.](structural-abstract-and-auxiliary-classes.md) Questa definizione dello schema specifica varie caratteristiche della classe, inclusi gli attributi associati alla classe.

A differenza delle classi strutturali, non è possibile creare un'istanza di una classe ausiliaria come con una classe strutturale. Si usa invece una classe ausiliaria per estendere l'elenco di attributi associati a un'altra classe di oggetti strutturale, astratta o ausiliaria.

Nella versione iniziale di Windows 2000, Active Directory Domain Services fornito il supporto per il collegamento statico di classi ausiliarie alla definizione [**classSchema**](/windows/desktop/ADSchema/c-classschema) di un'altra classe di oggetti. Quando una classe ausiliaria viene usata in questo modo, ogni istanza della classe di oggetti supporta gli attributi della classe ausiliaria.

**Windows 2000 Server e versioni precedenti:** Active Directory Domain Services non fornisce il supporto per il collegamento dinamico di classi ausiliarie a singoli oggetti e non solo a intere classi di oggetti. Inoltre, le classi ausiliarie associate a un'istanza dell'oggetto non possono essere successivamente rimosse dall'istanza.

**Windows Server 2003:** Le classi ausiliarie dinamiche sono supportate quando tutti i controller di dominio nella foresta eseguono Windows Server 2003 e la modalità funzionale foresta è Windows Server 2003.

Per altre informazioni sulle classi ausiliarie, vedere:

-   [Classi ausiliarie collegate dinamicamente](dynamically-linked-auxiliary-classes.md)
-   [Classi ausiliarie collegate in modo statico](statically-linked-auxiliary-classes.md)
-   [Determinazione delle classi associate a un'istanza di oggetto](determining-the-classes-associated-with-an-object-instance.md)
-   [Aggiunta di una classe ausiliaria a un'istanza di oggetto](adding-an-auxiliary-class-to-an-object-instance.md)

Per altre informazioni sui livelli di funzionalità della foresta, vedere "How to raise Active Directory domain and forest functional levels" (Come aumentare i livelli di funzionalità del dominio e della foresta di Active Directory) nella guida e supporto Knowledge Base all'indirizzo [https://support/microsoft.com/kb/322692\#4](https://support.microsoft.com/kb/322692) .

 

 