---
description: ICE48 verifica la presenza di directory hardcoded in percorsi locali nella tabella delle proprietà.
ms.assetid: 9dcc2475-23a3-4f77-8828-4d0a036670d4
title: ICE48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c9c9ace086d044109e5f9b91bbc471c37094de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314209"
---
# <a name="ice48"></a>ICE48

ICE48 verifica la presenza di directory hardcoded in percorsi locali nella [tabella delle proprietà](property-table.md).

Non impostare come hardcoded i percorsi della directory nelle unità locali perché i computer differiscono per la configurazione dell'unità locale. Questa pratica può essere accettabile se si distribuisce un'applicazione in un numero elevato di computer in cui le parti rilevanti delle unità sono tutte uguali.

## <a name="result"></a>Risultato

ICE48 Invia un messaggio di errore se è presente una directory hardcoded in un percorso locale nella tabella delle proprietà.

## <a name="example"></a>Esempio

ICE48 segnala l'avviso seguente per l'esempio illustrato.

``` syntax
Directory 'Dir1' appears to be hardcoded in the property 
    table to a local drive.
```

[Tabella directory](directory-table.md) (parziale)



| Directory | \_Padre directory | DefaultDir |
|-----------|-------------------|------------|
| Dir1      |                   | SourceDir  |



 

[Tabella delle proprietà](property-table.md) (parziale)



| Proprietà | Valore      |
|----------|------------|
| Dir1     | d: \\ origine |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



