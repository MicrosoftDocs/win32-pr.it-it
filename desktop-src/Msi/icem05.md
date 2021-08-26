---
description: ICEM05 verifica che il modulo unione sia associato correttamente ai componenti nel modulo. L'associazione non corretta di un componente a un modulo causa un'errata associazione del componente al database di destinazione.
ms.assetid: 1bf4041e-b198-4897-8719-8505fd8180ec
title: ICEM05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee34dbc16b9cf3aeaa16aec9b5d62671cd51036c563bfb8561815ad3c21d0ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996781"
---
# <a name="icem05"></a>ICEM05

ICEM05 verifica che il modulo unione sia associato correttamente ai componenti nel modulo. L'associazione non corretta di un componente a un modulo causa un'errata associazione del componente al database di destinazione.

Le ICE del modulo unione vengono archiviate in un file con estensione cub del modulo unione denominato Mergemod.cub e non nel file con estensione cub contenente le ICE usate per la convalida dei pacchetti.

## <a name="result"></a>Risultato

ICEM05 invia un errore se il database del modulo associa erroneamente i componenti e il modulo.

## <a name="example"></a>Esempio

ICEM05 invia i messaggi di errore seguenti per un modulo contenente le voci di database illustrate di seguito.

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
| MyModule. *GUID1* | 1033     | 1.0     |



 

[**Tabella ModuleComponents**](modulecomponents-table.md)



| Componente  | ModuleID            | Linguaggio |
|------------|---------------------|----------|
| Componente1 | MyModule. *GUID1*    | 1033     |
| Componente2 | OtherModule. *GUID2* | 1033     |



 

[Tabella dei componenti](component-table.md) (parziale)



| Componente  | ComponentID |
|------------|-------------|
| Componente3 | *GUID4*     |
| Componente2 | *GUID5*     |



 

Il modulo di merge ICE segnala il primo errore perché la tabella ModuleComponents tenta di associare un componente a un altro modulo che non è il modulo corrente specificato nella tabella ModuleSignature. Per risolvere questo problema, modificare le colonne ModuleID e Language del record ModuleComponents per Component2 in quella per il modulo corrente, MyModule. *GUID1*.

Il modulo di merge ICE segnala il secondo errore perché il primo record nella tabella ModuleComponents tenta di associare Component1 al modulo. Questo componente non esiste nella tabella dei componenti del modulo unione. Un modulo può essere associato solo a un componente presente nel modulo. Per risolvere il problema, rimuovere il record per il componente inesistente.

Il modulo di merge ICE segnala il terzo errore perché il modulo tenta di aggiungere Component3 al database di destinazione. Questo componente non è stato associato al modulo nella tabella ModuleComponents. Per correggere l'errore, aggiungere un record per Component3 alla tabella ModuleComponents.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sul modulo di unione ICE](merge-module-ice-reference.md)
</dt> </dl>

 

 



