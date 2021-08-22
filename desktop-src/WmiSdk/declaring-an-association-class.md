---
description: Una classe di associazione è un tipo speciale di classe che definisce una relazione tra altre due classi.
ms.assetid: 21fd6e39-5dd3-41b8-a2f5-0135a6637ce8
ms.tgt_platform: multiple
title: Dichiarazione di una classe di associazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd569d1dc20ba40be6d19f3009ab4311f69e04ca3e8a01031e74a9c84b461552
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244421"
---
# <a name="declaring-an-association-class"></a>Dichiarazione di una classe di associazione

Una classe di associazione è un tipo speciale di classe che definisce una relazione tra altre due classi.

La procedura seguente descrive come creare una classe di associazione usando il codice MOF.

**Per creare una classe di associazione usando il codice MOF**

1.  Assegnare **il qualificatore** Association alla classe.

    Sebbene sia possibile creare una classe con riferimenti a  oggetti o classi, l'uso del qualificatore association non solo rende chiaro che la classe è una classe di associazione, ma, come procedura consigliata, garantisce che la classe funzioni completamente come classe di associazione.

2.  Creare due riferimenti all'interno della classe che descrivono le due istanze dell'oggetto da associare usando il **tipo ref.**

    I riferimenti associano i due oggetti nell'associazione mediante l'associazione di percorsi agli oggetti. Sebbene non sia obbligatorio, usare anche le proprietà di riferimento come proprietà chiave.

    Sebbene sia possibile creare riferimenti completi o relativi allo spazio dei nomi, WMI ha solo un supporto limitato per i riferimenti tra spazi dei nomi. In particolare, solo gli oggetti definiti in modo statico possono fare riferimento tra loro attraverso i limiti dello spazio dei nomi. Gli oggetti supportati dinamicamente non possono fare riferimento tra loro.

    Se necessario, usare i **qualificatori HasClassRef** e **Classref** insieme al tipo **di** riferimento dell'oggetto per fare riferimento a una classe.

    WMI supporta la presenza di un **punto di** riferimento di riferimento a un'istanza e dell'altro punto di riferimento a un oggetto a una classe.  In questo caso, la classe di associazione descrive un'associazione che associa istanze alle classi.

    L'esempio di codice seguente descrive la sintassi per l'uso **di HasClassRef** **e Classref** con un **tipo di** oggetto.

    ``` syntax
    [HasClassRefs, Association]
    class SomeAssocClass
    {
         [key, classref{ "MyEndpoint", "OtherContainer" }]
         object ref ep1;
         [key] object ref ep2;
    }; 
    ```

    Nell'esempio precedente il riferimento **ep1** può puntare alle definizioni di classe per la **classe MyEndpoint** o **otherContainer.** Si noti che anche se è necessario digitare in modo debole la classe di riferimento, non è possibile digitare in modo debole il **qualificatore Classref** stesso; in modo da ridurre notevolmente l'efficienza del motore di query WMI. La tipizzazione debole crea un riferimento che può contenere qualsiasi tipo di dati usando la parola **chiave object** e il tipo di dati **ref.** Per usare correttamente **HasClassRef,** è necessario impostare i tipi di qualificatori pertinenti per la propagazione a tutte le istanze e sottoclassi.

3.  Creare eventuali altre proprietà in base alle esigenze.

    Nell'esempio di codice seguente WMI non supporta attualmente classi di associazione con meno o più di due proprietà di riferimento.

    ``` syntax
    [Association : ToInstance] 
    class MyAssocClass
    {
        ClassX ref PathToClassX ;
        ClassY ref PathToClassY ;
    };
    ```

4.  Al termine, compilare il codice MOF con il compilatore MOF.

    Per altre informazioni, vedere [Compilazione di file MOF.](compiling-mof-files.md)

L'esempio di codice nel passaggio 3 definisce la **classe di associazione MyAssocClass.** La **classe MyAssocClass** definisce una relazione tra **ClassX** e **ClassY.** Le **proprietà PathToClassX** **e PathToClassY** contengono i percorsi degli oggetti alle istanze delle classi da associare. La parola **chiave ToInstance** è uno dei diversi flag flavor definiti da WMI per fornire informazioni sull'uso di un qualificatore. La **parola chiave ToInstance** indica che WMI deve propagare il qualificatore **Association** a tutte le istanze della classe di associazione. Controllando questo qualificatore di istanza, il software client può determinare che un'istanza appartiene a una classe di associazione, senza dover recuperare la definizione della classe per cercare il qualificatore **association.** Per altre informazioni, vedere [Descrizione di un qualificatore con una descrizione qualificatore](describing-a-qualifier-with-a-qualifier-flavor.md) e [riferimenti.](references.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Progettazione di Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



