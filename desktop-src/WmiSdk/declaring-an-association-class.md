---
description: Una classe di associazione è un tipo speciale di classe che definisce una relazione tra due altre classi.
ms.assetid: 21fd6e39-5dd3-41b8-a2f5-0135a6637ce8
ms.tgt_platform: multiple
title: Dichiarazione di una classe di associazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 083ce578ca912290fd026f225799793f89685aab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058020"
---
# <a name="declaring-an-association-class"></a>Dichiarazione di una classe di associazione

Una classe di associazione è un tipo speciale di classe che definisce una relazione tra due altre classi.

Nella procedura seguente viene descritto come creare una classe di associazione utilizzando il codice MOF.

**Per creare una classe di associazione usando il codice MOF**

1.  Assegnare il qualificatore **Association** alla classe.

    Sebbene sia possibile creare una classe con riferimenti a oggetti o classi, l'utilizzo del qualificatore di **associazione** non solo rende chiaro che la classe è una classe di associazione, ma, come procedura consigliata, assicura che la classe funzioni completamente come una classe di associazione.

2.  Creare due riferimenti all'interno della classe che descrivono le due istanze di oggetti che si desidera associare utilizzando il tipo di **riferimento** .

    I riferimenti associano i due oggetti nell'associazione, contenenti i percorsi degli oggetti. Sebbene non sia obbligatorio, utilizzare anche le proprietà di riferimento come proprietà chiave.

    Sebbene sia possibile creare riferimenti completi o relativi agli spazi dei nomi, WMI ha solo un supporto limitato per i riferimenti tra più spazi dei nomi. In particolare, solo gli oggetti definiti in modo statico possono fare riferimento tra loro tra i limiti dello spazio dei nomi. gli oggetti supportati dinamicamente non possono fare riferimento l'uno all'altro.

    Se necessario, usare i qualificatori **HasClassRef** e **Classref** in combinazione con il tipo di riferimento dell' **oggetto** per fare riferimento a una classe.

    WMI supporta la presenza di un punto di riferimento **ref** a un'istanza di e l'altro riferimento all' **oggetto** punta a una classe. In questo caso, la classe Association Descriva un'associazione che associa le istanze alle classi.

    Nell'esempio di codice seguente viene descritta la sintassi per l'utilizzo di **HasClassRef** e **Classref** con un tipo di **oggetto** .

    ``` syntax
    [HasClassRefs, Association]
    class SomeAssocClass
    {
         [key, classref{ "MyEndpoint", "OtherContainer" }]
         object ref ep1;
         [key] object ref ep2;
    }; 
    ```

    Nell'esempio precedente, il riferimento **EP1** può puntare alle definizioni di classe per la classe di **endpoint** o la classe **OtherContainer** . Si noti che, sebbene sia necessario digitare debolmente la classe di riferimento, non è possibile digitare debolmente il qualificatore **Classref** ; Questa operazione ridurrebbe notevolmente l'efficienza del motore di query WMI. La tipizzazione debole sta creando un riferimento che può contenere qualsiasi tipo di dati tramite la parola chiave **Object** e il tipo di dati **ref** . Per usare correttamente **HasClassRef**, è necessario impostare le versioni dei qualificatori rilevanti per la propagazione a tutte le istanze e sottoclassi.

3.  Creare qualsiasi altra proprietà, se necessario.

    Nell'esempio di codice seguente viene illustrato che WMI non supporta attualmente le classi di associazione con meno o più di due proprietà di riferimento.

    ``` syntax
    [Association : ToInstance] 
    class MyAssocClass
    {
        ClassX ref PathToClassX ;
        ClassY ref PathToClassY ;
    };
    ```

4.  Al termine, compilare il codice MOF con il compilatore MOF.

    Per ulteriori informazioni, vedere [compilazione di file MOF](compiling-mof-files.md).

L'esempio di codice nel passaggio 3 definisce la classe di associazione **MyAssocClass** . La classe **MyAssocClass** definisce una relazione tra **classx** e **Classy**. Le proprietà **PathToClassX** e **PathToClassY** contengono percorsi di oggetti per le istanze delle classi da associare. La parola chiave **ToInstance** è uno dei diversi flag di sapore definiti da WMI per fornire informazioni sull'utilizzo di un qualificatore. La parola chiave **ToInstance** indica che WMI deve propagare il qualificatore dell' **associazione** a tutte le istanze della classe Association. Controllando questo qualificatore di istanza, il software client può determinare che un'istanza appartiene a una classe di associazione, senza dover recuperare la definizione della classe per cercare il qualificatore dell' **associazione** . Per ulteriori informazioni, vedere [Descrizione di un qualificatore con una versione del qualificatore](describing-a-qualifier-with-a-qualifier-flavor.md) e [riferimenti](references.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Progettazione di classi Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



