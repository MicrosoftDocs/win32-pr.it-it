---
title: Moniker elemento
description: Un'altra classe del moniker implementata da OLE è il moniker dell'elemento, che può essere usato per identificare un oggetto contenuto in un altro oggetto.
ms.assetid: ddcf3669-4ad0-4a4e-80a6-eb78058cff09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57b692502ba44519a2c51a661ef62a51e133ac04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297625"
---
# <a name="item-monikers"></a>Moniker elemento

Un'altra classe del moniker implementata da OLE è il *moniker dell'elemento*, che può essere usato per identificare un oggetto contenuto in un altro oggetto. Un tipo di oggetto contenuto è un oggetto OLE incorporato in un documento composto. Un documento composto potrebbe identificare gli oggetti incorporati che contiene assegnando ognuno un nome arbitrario, ad esempio "embedobj1", "embedobj2" e così via. Un altro tipo di oggetto contenuto è la selezione di un utente in un documento, ad esempio un intervallo di celle in un foglio di calcolo o un intervallo di caratteri in un documento di testo. Un oggetto costituito da una selezione è denominato *pseudo-oggetto* perché non viene considerato come un oggetto distinto fino a quando un utente non contrassegna la selezione. Un foglio di calcolo può identificare un intervallo di celle usando un nome, ad esempio "1A: 7F", mentre un documento di elaborazione di testo può identificare un intervallo di caratteri usando il nome di un segnalibro.

Un moniker di elemento è utile principalmente quando viene concatenato o *composto* con un altro moniker, ovvero uno che identifica il contenitore. Un moniker di elemento viene in genere creato e quindi composto su (ad esempio) un moniker di file per creare l'equivalente di un percorso completo dell'oggetto. È ad esempio possibile comporre il moniker del file "c: \\ work \\report.doc" (che identifica l'oggetto contenitore) con il moniker dell'elemento "embedobj1" (che identifica un oggetto all'interno del contenitore) per formare il moniker "c: \\ Work \\report.doc\\ embedobj1", che identifica in modo univoco un particolare oggetto all'interno di un determinato file. È anche possibile concatenare ulteriori moniker di elemento per identificare gli oggetti annidati in profondità. Se, ad esempio, "embedobj1" è il nome di un oggetto foglio di calcolo, per identificare un determinato intervallo di celle nell'oggetto foglio di calcolo è possibile aggiungere un altro moniker di elemento per creare un moniker equivalente a "c: \\ work \\report.doc\\ Embedobj1 \\ 1a: 7F".

In combinazione con un moniker di file, un moniker di elemento costituisce un percorso completo. I moniker degli elementi estendono pertanto la nozione di nomi di percorso oltre il file system, definendo i nomi di percorso per identificare singoli oggetti, non solo file.

Esiste una differenza significativa tra un moniker di elemento e un moniker di file. Il percorso contenuto in un moniker di file è significativo per chiunque conosca la file system, mentre il percorso parziale contenuto in un moniker di elemento è significativo solo per un contenitore specifico. Tutti sanno quale "c: \\ work \\report.doc" si riferisce a, ma un solo oggetto contenitore specifico sa quale "1a: 7F" si riferisce a. Un contenitore non può interpretare un moniker di elemento creato da un'altra applicazione. l'unico contenitore che conosce l'oggetto a cui fa riferimento un moniker di elemento è il contenitore che ha assegnato il moniker dell'elemento all'oggetto nella prima posizione. Per questo motivo, l'origine dell'oggetto denominato dalla combinazione del moniker di un file e di un elemento non deve solo implementare [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile), per semplificare l'associazione del moniker del file, ma anche [**IOleItemContainer**](/windows/desktop/api/OleIdl/nn-oleidl-ioleitemcontainer) per semplificare la risoluzione del nome del moniker dell'elemento nell'oggetto appropriato, nel contesto di un file.

Il vantaggio dei moniker è che un utente che usa un moniker per individuare un oggetto non deve comprendere il nome contenuto all'interno del moniker dell'elemento, purché il moniker dell'elemento faccia parte di un oggetto composito. In genere, non è opportuno che un moniker di elemento esista autonomamente. In alternativa, è possibile comporre un moniker di elemento in un moniker di file. Si chiamerà quindi [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) sul composito, che associa i singoli moniker al suo interno, interpretando i nomi.

Per creare un oggetto moniker di elemento e restituire il relativo puntatore al provider del moniker, OLE fornisce la funzione di supporto [**CreateItemMoniker**](/windows/desktop/api/Objbase/nf-objbase-createitemmoniker). Questa funzione crea un oggetto moniker di elemento e restituisce il relativo puntatore al provider.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Anti-moniker](anti-monikers.md)
</dt> <dt>

[Moniker della classe](class-monikers.md)
</dt> <dt>

[Moniker compositi](composite-monikers.md)
</dt> <dt>

[Moniker di file](file-monikers.md)
</dt> <dt>

[Moniker puntatore](pointer-monikers.md)
</dt> </dl>

 

 




