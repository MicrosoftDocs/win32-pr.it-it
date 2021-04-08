---
description: ICE02 verifica che determinati riferimenti tra le tabelle del componente, del file e del registro di sistema siano reciproci. Questi riferimenti devono essere reciproci affinché il programma di installazione determini correttamente lo stato di installazione dei componenti.
ms.assetid: 864404f1-439d-49a2-973d-4e6e1618863e
title: ICE02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1975203825d079d5eeb1ec5e4183767dd68625bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750135"
---
# <a name="ice02"></a>ICE02

ICE02 verifica che determinati riferimenti tra le tabelle del [componente](component-table.md), del [file](file-table.md)e [del registro di sistema](registry-table.md) siano reciproci. Questi riferimenti devono essere reciproci affinché il programma di installazione determini correttamente lo stato di installazione dei componenti.

Il programma di installazione utilizza la colonna di percorso della tabella dei componenti per rilevare la presenza del componente elencato nella colonna componente. La colonna di chiave percorso contiene una chiave nel registro di sistema o nelle tabelle di file. In entrambe le tabelle è presente una \_ colonna Component che contiene una chiave nella tabella Component che punta al componente che controlla la voce del registro di sistema o il file. Questi riferimenti devono essere reciproci.

## <a name="result"></a>Risultato

ICE02 Invia un messaggio di errore se trova un riferimento che deve essere reciproco e non lo è.

## <a name="example"></a>Esempio

ICE02 invierà il messaggio di errore seguente per un file con estensione msi contenente le voci di database indicate.

``` syntax
File: 'Red_File' cannot be the key file for Component: 'Blue'. The file belongs to Component: 'Red'
```

[Tabella componenti](component-table.md) (parziale)



| Componente | KeyPath   |
|-----------|-----------|
| Red       | \_File rosso |
| Blu      | \_File rosso |



 

[Tabella file](file-table.md) (parziale)



| Colonna file | Componente\_ |
|-------------|-------------|
| \_File rosso   | Red         |
| \_File blu  | Blu        |



 

Il componente blu fa riferimento \_ al file rosso, ma \_ il file rosso non è controllato dal blu del componente e pertanto non può essere il file del percorso di base. Se è stato chiamato il programma di installazione per ottenere lo stato di installazione di Blue, non verrà verificato correttamente se \_ è stato installato il file rosso. Se si modifica il campo del percorso della tabella per il blu nella tabella dei componenti nel \_ file blu, viene risolto l'errore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



