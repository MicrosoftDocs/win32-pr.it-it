---
description: ICE19 verifica che i componenti annunciati facciano riferimento a un file nella colonna KeyPath della tabella Component e che un collegamento annunciato faccia riferimento a una directory in questa colonna.
ms.assetid: 438153c1-bc4b-4ecf-ab85-d66ad69c987c
title: ICE19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1a706999744762a930a800326cb8d38487f19c1c4ea3e01b6b1f8aeae4ca2dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529111"
---
# <a name="ice19"></a>ICE19

ICE19 verifica che i componenti annunciati facciano riferimento a un file nella colonna KeyPath della tabella [Component](component-table.md) e che un collegamento annunciato faccia riferimento a una directory in questa colonna.

ICE19 convalida che i componenti o i collegamenti annunciati hanno un ComponentId. I componenti nella [tabella PublishComponent](publishcomponent-table.md), che non sono annunciati in un'altra tabella, vengono controllati solo per verificare se hanno un ComponentId.

## <a name="result"></a>Risultato

ICE19 invia un messaggio di errore se la colonna KeyPath della tabella Component non fa riferimento a un file nel caso di un componente annunciato o di una directory nel caso di un collegamento annunciato. ICE19 invia un messaggio di errore se i componenti o i collegamenti annunciati non hanno un ComponentId.

## <a name="example"></a>Esempio

ICE19 pubblica i messaggi di errore seguenti per l'esempio illustrato:

-   L'estensione flp fa riferimento al componente Comp1 che non ha un ComponentId specificato nella [tabella Component](component-table.md).
-   Extension exe fa riferimento al componente Comp4 che fa riferimento a una directory come KeyPath. KeyPath è Null nella tabella Component.
-   Il collegamento Shortcut2 fa riferimento al componente Comp3 che fa riferimento a una voce del Registro di sistema come percorso della chiave. Il valore della colonna Attributi nella tabella Componente è 4.

[Tabella dei componenti](component-table.md) (parziale)



| Componente | Componentid                            | Attributi | KeyPath |
|-----------|----------------------------------------|------------|---------|
| Comp1     | Null                                   | 0          | File1   |
| Comp2     | {00000002-0003-0000-0000-624474736554} | 0          | File2   |
| Comp3     | {00000003-0003-0000-0000-624474736554} | 4          | Reg3    |
| Comp4     | {00000004-0003-0000-0000-624474736554} | 0          | Null    |



 

[Tabella di estensione](extension-table.md) (parziale)



| Estensione | Componente\_ |
|-----------|-------------|
| Flp       | Comp1       |
| Tst       | Comp2       |
| exe       | Comp4       |



 

[Tabella dei collegamenti](shortcut-table.md) (parziale)



| Tasto di scelta rapida  | Componente\_ | Funzionalità\_      |
|-----------|-------------|----------------|
| Collegamento1 | Comp4       | ProductFeature |
| Collegamento2 | Comp3       | ProductFeature |



 

[Tabella delle funzionalità](feature-table.md) (parziale)



| Funzionalità        |
|----------------|
| ProductFeature |



 

> [!Note]  
> Se l'estensione flp ed exe fanno entrambi riferimento allo stesso componente, il server EXE o COM che li apre deve essere lo stesso. Questo FILE EXE è in genere il KeyPath per il componente. Per OFFICE, le estensioni doc e xls non possono fare riferimento allo stesso componente perché lo stesso FILE EXE non apre entrambe le estensioni. È necessario winword.exe aprire le estensioni dei documenti ed è necessario excel.exe aprire le estensioni xls.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



