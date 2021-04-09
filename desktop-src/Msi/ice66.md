---
description: ICE66 utilizza le tabelle nel database per determinare lo schema che deve essere utilizzato dal database.
ms.assetid: 7cf929a0-2c4c-40ca-a902-dfd9dcd203b8
title: ICE66
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea1436ad791941c96c0484a02f40a60fc9939e73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753015"
---
# <a name="ice66"></a>ICE66

ICE66 utilizza le tabelle nel database per determinare lo schema che deve essere utilizzato dal database.

Alcune funzionalità possono essere disponibili solo se il pacchetto viene installato in un sistema con una versione di Windows Installer corrente.

## <a name="result"></a>Risultato

ICE66 pubblica un avviso se il database utilizza uno schema errato.

## <a name="example"></a>Esempio

ICE66 segnala l'avviso seguente per l'esempio illustrato.

``` syntax
WARNING: Complete functionality of the IsolatedComponents table is only available with Windows Installer versions 1.1 or greater. Your schema is 100.
```

Questo avviso può essere ignorato se si desidera che il pacchetto venga installato utilizzando una versione di Windows Installer corrente. Se ad esempio si desidera che il pacchetto sia installabile solo nella versione 2,0 o successive, modificare lo schema del pacchetto (PID \_ PageCount) in 200.

[Tabella IsolatedComponent](isolatedcomponent-table.md)



| Componente \_ condiviso | \_Applicazione componente |
|-------------------|------------------------|
| Component1        | Component2             |



 

[Flusso di informazioni di riepilogo](summary-information-stream.md)



| PIDt           | Valore |
|----------------|-------|
| \_PageCount PID | 100   |



 

## <a name="table-used-during-execution"></a>Tabella utilizzata durante l'esecuzione:

[\_Tabella colonne](-columns-table.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



