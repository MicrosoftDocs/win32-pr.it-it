---
title: Stati degli oggetti
description: Stati degli oggetti
ms.assetid: 8ebef6d6-7a2f-4b95-91ca-999646cde82d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66cbae9ca9d350c4d8436f99cf2934aa8ab653dc30f4d9196f9d007c61b490a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118105139"
---
# <a name="object-states"></a>Stati degli oggetti

Un oggetto composto esiste in uno dei tre stati seguenti: passivo, caricato o in esecuzione. Lo stato di un oggetto documento composto descrive la relazione tra l'oggetto nel contenitore e l'applicazione responsabile della relativa creazione. Nella tabella seguente vengono riepilogati questi stati.



| Stato oggetto       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Passivo<br/> | L'oggetto documento composto esiste solo nell'archiviazione, su disco o in un database. In questo stato, l'oggetto non è disponibile per la visualizzazione o la modifica.<br/>                                                                                                                                                                                                                                   |
| Loaded<br/>  | Le strutture di dati dell'oggetto create dal gestore dell'oggetto sono nella memoria del contenitore. Il contenitore ha stabilito la comunicazione con il gestore dell'oggetto e sono disponibili dati di presentazione memorizzati nella cache per il rendering dell'oggetto. Le chiamate vengono elaborate dal gestore dell'oggetto. Questo stato, a causa del basso sovraccarico, viene usato quando un utente sta semplicemente visualizzando o stampando un oggetto.<br/> |
| In esecuzione<br/> | Gli oggetti che controllano la comunicazione remota sono stati creati e l'applicazione server OLE è in esecuzione. Le interfacce dell'oggetto sono accessibili e il contenitore può ricevere una notifica delle modifiche. In questo stato, un utente finale può modificare o modificare in altro modo l'oggetto.<br/>                                                                                                                    |



 

Per altre informazioni, vedere i seguenti argomenti:

-   [Immissione dello stato caricato](entering-the-loaded-state.md)
-   [Immissione dello stato di esecuzione](entering-the-running-state.md)
-   [Immissione dello stato passivo](entering-the-passive-state.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Documenti composti](compound-documents.md)
</dt> </dl>

 

 





