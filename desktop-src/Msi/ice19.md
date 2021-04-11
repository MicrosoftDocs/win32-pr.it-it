---
description: ICE19 verifica che i componenti annunciati facciano riferimento a un file nella colonna percorso tasto della tabella dei componenti e che un collegamento annunciato faccia riferimento a una directory in questa colonna.
ms.assetid: 438153c1-bc4b-4ecf-ab85-d66ad69c987c
title: ICE19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a53aa3268a1c77f674d4a130c9de02c44b56243
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232249"
---
# <a name="ice19"></a>ICE19

ICE19 verifica che i componenti annunciati facciano riferimento a un file nella colonna percorso tasto della [tabella dei componenti](component-table.md) e che un collegamento annunciato faccia riferimento a una directory in questa colonna.

ICE19 verifica che i collegamenti o i componenti annunciati dispongano di un ComponentId. I componenti della [tabella PublishComponent](publishcomponent-table.md), che non vengono annunciati in un'altra tabella, vengono controllati solo per verificare se hanno un ComponentID.

## <a name="result"></a>Risultato

ICE19 Invia un messaggio di errore se la colonna di percorso della tabella dei componenti non fa riferimento a un file nel caso di un componente annunciato o di una directory nel caso di un collegamento annunciato. ICE19 Invia un messaggio di errore se i collegamenti o i componenti annunciati non dispongono di un ComponentId.

## <a name="example"></a>Esempio

ICE19 invia i messaggi di errore seguenti per l'esempio illustrato:

-   L'estensione FLP fa riferimento al componente comp1 che non contiene un ComponentId specificato nella [tabella dei componenti](component-table.md).
-   Estensione exe fa riferimento al componente Comp4 che fa riferimento a una directory come percorso di proprietà. Il percorso della tabella dei componenti è null.
-   Il collegamento Shortcut2 fa riferimento al componente COMP3 che fa riferimento a una voce del registro di sistema come percorso della chiave. Il valore della colonna attributi nella tabella dei componenti è 4.

[Tabella componenti](component-table.md) (parziale)



| Componente | ComponentId                            | Attributi | KeyPath |
|-----------|----------------------------------------|------------|---------|
| Comp1     | Null                                   | 0          | File1   |
| Comp2     | {00000002-0003-0000-0000-624474736554} | 0          | File2   |
| COMP3     | {00000003-0003-0000-0000-624474736554} | 4          | Reg3    |
| Comp4     | {00000004-0003-0000-0000-624474736554} | 0          | Null    |



 

[Tabella di estensione](extension-table.md) (parziale)



| Estensione | Componente\_ |
|-----------|-------------|
| FLP       | Comp1       |
| TST       | Comp2       |
| exe       | Comp4       |



 

[Tabella collegamenti](shortcut-table.md) (parziale)



| Tasto di scelta rapida  | Componente\_ | Funzionalità\_      |
|-----------|-------------|----------------|
| Shortcut1 | Comp4       | ProductFeature |
| Shortcut2 | COMP3       | ProductFeature |



 

[Tabella delle funzionalità](feature-table.md) (parziale)



| Funzionalità        |
|----------------|
| ProductFeature |



 

> [!Note]  
> Se l'estensione FLP e exe fanno riferimento allo stesso componente, il file EXE o il server COM che li apre deve essere lo stesso. Questo file EXE corrisponde in genere al percorso di un componente. Per OFFICE, le estensioni doc e xls non possono fare riferimento allo stesso componente perché lo stesso file EXE non apre entrambe le estensioni. È necessario winword.exe per aprire le estensioni del documento ed è necessario excel.exe per aprire le estensioni xls.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



