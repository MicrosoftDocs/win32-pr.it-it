---
description: ICEM05 verifica che il modulo unione sia associato correttamente ai componenti del modulo. Associando erroneamente un componente a un modulo, il componente viene associato erroneamente al database di destinazione.
ms.assetid: 1bf4041e-b198-4897-8719-8505fd8180ec
title: ICEM05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e62ca481ef836c2675c381817fe2242e37384818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049904"
---
# <a name="icem05"></a>ICEM05

ICEM05 verifica che il modulo unione sia associato correttamente ai componenti del modulo. Associando erroneamente un componente a un modulo, il componente viene associato erroneamente al database di destinazione.

I moduli CIEM di tipo merge vengono archiviati in un file con estensione cub del modulo merge denominato Mergemod. cub e non nel file con estensione cub contenente i ghiacci utilizzati per la convalida del pacchetto.

## <a name="result"></a>Risultato

ICEM05 Invia un errore se il database del modulo associa erroneamente i componenti e il modulo.

## <a name="example"></a>Esempio

ICEM05 invia i messaggi di errore seguenti per un modulo contenente le voci di database indicate di seguito.

``` syntax
The component Component2.OtherModule.GUID2.1033 in the 
ModuleComponents table does not belong to this Merge Module.
The component Component1.MyModule.GUID1.1033 in the ModuleComponents 
table is not listed in the Component table.
The component 'Component3' in the Component table is not listed in the 
ModuleComponents table.
```

[Tabella ModuleSignature](modulesignature-table.md)



| ModuleID         | Linguaggio | Versione |
|------------------|----------|---------|
| MyModule. *Guid1* | 1033     | 1.0     |



 

[**Tabella ModuleComponents**](modulecomponents-table.md)



| Componente  | ModuleID            | Linguaggio |
|------------|---------------------|----------|
| Component1 | MyModule. *Guid1*    | 1033     |
| Component2 | OtherModule. *Guid2* | 1033     |



 

[Tabella componenti](component-table.md) (parziale)



| Componente  | ComponentID |
|------------|-------------|
| Component3 | *GUID4*     |
| Component2 | *GUID5*     |



 

Il modulo merge ICE segnala il primo errore perché la tabella ModuleComponents tenta di associare un componente a un altro modulo che non è il modulo corrente specificato nella tabella ModuleSignature. Per risolvere questo problema, modificare le colonne ModuleID e Language del record ModuleComponents per Component2 in quello per il modulo corrente, modulo. *Guid1*.

Il modulo merge ICE segnala il secondo errore perché il primo record nella tabella ModuleComponents tenta di associare Component1 al modulo. Questo componente non esiste nella tabella dei componenti del modulo merge. Un modulo può essere associato solo a un componente esistente nel modulo. Per risolvere il problema, rimuovere il record per il componente non esistente.

Il modulo merge ICE segnala il terzo errore perché il modulo tenta di aggiungere Component3 al database di destinazione. Questo componente non è stato associato al modulo nella tabella ModuleComponents. Per correggere l'errore, aggiungere un record per Component3 alla tabella ModuleComponents.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio del modulo merge](merge-module-ice-reference.md)
</dt> </dl>

 

 



