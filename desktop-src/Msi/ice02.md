---
description: ICE02 verifica che alcuni riferimenti tra le tabelle Component, File e Registry siano reciproci. Questi riferimenti devono essere reciproci perché il programma di installazione determinare correttamente lo stato di installazione dei componenti.
ms.assetid: 864404f1-439d-49a2-973d-4e6e1618863e
title: ICE02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b97696ee4a8f93d49237dbac8661b6bfc72e478922c87b9095620bc5c29dc546
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946655"
---
# <a name="ice02"></a>ICE02

ICE02 verifica che alcuni riferimenti tra le [tabelle Component](component-table.md), [File](file-table.md)e [Registry](registry-table.md) siano reciproci. Questi riferimenti devono essere reciproci perché il programma di installazione determinare correttamente lo stato di installazione dei componenti.

Il programma di installazione usa la colonna KeyPath della tabella Component per rilevare la presenza del componente elencato nella colonna Componente. La colonna KeyPath contiene una chiave nelle tabelle Registro di sistema o File. Entrambe queste tabelle hanno una colonna Component che contiene una chiave nella tabella Component che punta al componente che controlla la voce \_ o il file del Registro di sistema. Questi riferimenti devono essere reciproci.

## <a name="result"></a>Risultato

ICE02 invia un messaggio di errore se trova un riferimento che deve essere reciproco e non lo è.

## <a name="example"></a>Esempio

ICE02 pubblica il messaggio di errore seguente per un file .msi contenente le voci di database visualizzate.

``` syntax
File: 'Red_File' cannot be the key file for Component: 'Blue'. The file belongs to Component: 'Red'
```

[Tabella dei componenti](component-table.md) (parziale)



| Componente | KeyPath   |
|-----------|-----------|
| Red       | File \_ rosso |
| Blu      | File \_ rosso |



 

[Tabella file](file-table.md) (parziale)



| Colonna File | Componente\_ |
|-------------|-------------|
| File \_ rosso   | Red         |
| File \_ blu  | Blu        |



 

Component Blue fa riferimento a Red File, ma Red File non è controllato da \_ Component Blue e pertanto non può essere il file \_ KeyPath. Se il programma di installazione è stato chiamato per ottenere lo stato di installazione di Blu, viene erroneamente verificata \_ l'installazione di File rosso. La modifica del campo KeyPath per Blu nella tabella dei componenti in \_ File blu consente di correggere l'errore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



