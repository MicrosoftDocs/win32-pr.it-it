---
title: Stati degli oggetti
description: Stati degli oggetti
ms.assetid: 8ebef6d6-7a2f-4b95-91ca-999646cde82d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 268b9bc9c69009850a5172259ab7a13c760d2c72
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297874"
---
# <a name="object-states"></a>Stati degli oggetti

Un oggetto composto esiste in uno dei tre stati seguenti: passivo, caricato o in esecuzione. Lo stato di un oggetto documento composto descrive la relazione tra l'oggetto nel contenitore e l'applicazione responsabile della sua creazione. Nella tabella seguente vengono riepilogati questi Stati.



| Stato oggetto       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Passivo<br/> | L'oggetto documento composto esiste solo nello spazio di archiviazione, su disco o in un database. In questo stato, l'oggetto non è disponibile per la visualizzazione o la modifica.<br/>                                                                                                                                                                                                                                   |
| Loaded<br/>  | Le strutture di dati dell'oggetto create dal gestore dell'oggetto si trovano nella memoria del contenitore. Il contenitore ha stabilito la comunicazione con il gestore oggetti e sono disponibili dati di presentazione memorizzati nella cache per il rendering dell'oggetto. Le chiamate vengono elaborate dal gestore dell'oggetto. Questo stato, a causa del sovraccarico ridotto, viene usato quando un utente sta semplicemente visualizzando o stampando un oggetto.<br/> |
| In esecuzione<br/> | Gli oggetti che controllano la comunicazione remota sono stati creati e l'applicazione server OLE è in esecuzione. Le interfacce dell'oggetto sono accessibili e il contenitore può ricevere una notifica delle modifiche. In questo stato, un utente finale può modificare o modificare l'oggetto in altro modo.<br/>                                                                                                                    |



 

Per altre informazioni, vedere i seguenti argomenti:

-   [Immissione dello stato caricato](entering-the-loaded-state.md)
-   [Immissione dello stato in esecuzione](entering-the-running-state.md)
-   [Immissione dello stato passivo](entering-the-passive-state.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Documenti composti](compound-documents.md)
</dt> </dl>

 

 





