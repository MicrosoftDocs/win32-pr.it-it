---
description: Un qualificatore è un flag che descrive ulteriori informazioni su un qualificatore.
ms.assetid: a7d9d1c0-9386-4c90-9788-993b35ed12db
ms.tgt_platform: multiple
title: Descrizione di un qualificatore con una versione di qualificatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525cfc2c590ec8916e2e9538b3e8224e97b3b5dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226949"
---
# <a name="describing-a-qualifier-with-a-qualifier-flavor"></a>Descrizione di un qualificatore con una versione di qualificatore

Un [*qualificatore*](gloss-q.md) è un flag che descrive ulteriori informazioni su un qualificatore. Ad esempio, la versione del qualificatore con restrizioni indica che WMI non deve propagare il qualificatore associato a tutte le classi o istanze derivate. È possibile impostare le versioni utilizzando il codice MOF o a livello di codice. Sebbene sia possibile descrivere diversi effetti con le varianti, lo scopo principale dei flag di sapore è quello di definire la modalità di propagazione dei qualificatori tramite l'ereditarietà da parte di WMI.

WMI definisce diverse versioni del qualificatore che è possibile alleghi a qualsiasi qualificatore, indipendentemente dall'origine del qualificatore. Tuttavia, alcune versioni non sono appropriate per tutti i tipi di qualificatore. La caratteristica **ToClass** , ad esempio, è appropriata solo per i qualificatori definiti per una classe. Non è possibile aggiungere **ToClass** a un qualificatore usato per descrivere un'istanza di.

È possibile utilizzare le varianti per descrivere diversi effetti per i qualificatori. Il flavor può, ad esempio, indicare se un qualificatore può essere localizzato. Uno degli scopi principali di una versione del qualificatore consiste tuttavia nel descrivere se una classe padre può passare i qualificatori a una sottoclasse o a un'istanza della classe. È anche possibile usare i tipi per determinare se una proprietà della classe passa un qualificatore a una proprietà dell'istanza. Usare infine le versioni per indicare se una sottoclasse può eseguire l'override del valore originale di un qualificatore ereditato. Tuttavia, i qualificatori dichiarati per una classe o un'istanza non vengono propagati alle proprietà di tale classe o istanza. Inoltre **, le versioni** che stabiliscono le autorizzazioni di sostituzione sono valide solo se si impostano anche le versioni **ToClass o ToClass** .

Una versione può essere assegnata a livello globale a un qualificatore per un intero file MOF usando la sintassi seguente, in cui lo spazio vuoto funge da delimitatore quando vengono specificate più versioni.

``` syntax
Qualifier QualifierName : flavor1 <flavor2...>;
```

Le versioni globali si applicano a tutti gli utilizzi successivi del qualificatore nel file MOF. Le istruzioni di sapore globale possono essere presenti in qualsiasi punto del file all'esterno di un blocco di dichiarazione dell'oggetto. Le versioni ridefinite a livello di classe, istanza o proprietà sostituiscono le dichiarazioni di sapore globale per l'ambito di tale oggetto.

Non è possibile definire una nuova versione. Sebbene sia possibile creare un nuovo qualificatore, utilizzare solo le [versioni dei qualificatori](qualifier-flavors.md) esistenti per descrivere il nuovo qualificatore.

**Per definire le versioni del qualificatore in MOF**

-   Dichiarare le versioni che descrivono un qualificatore specificato dopo il nome del qualificatore tra le parentesi quadre del qualificatore. Usare uno spazio vuoto come delimitatore tra più varianti.

    Nell'esempio seguente viene illustrato il modello per il fissaggio dei qualificatori predefiniti.

    ``` syntax
    [qualifier1 : flavor1 flavor2 flavor3, qualifier2 : flavor1]
    ```

È possibile aggiungere le versioni del qualificatore a livello di codice solo in C++. Questa operazione non è disponibile nell' [API di scripting per WMI](scripting-api-for-wmi.md), sebbene sia possibile aggiungere un nuovo qualificatore chiamando [**dell'SWbemQualifierSet. Add**](swbemqualifierset-add.md).

**Per assegnare una versione con C++**

-   Chiamare il metodo [**IWbemQualifierSet::P UT**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) con il parametro *lFlavor* impostato su una delle costanti definite per il metodo.

 

 



