---
description: La creazione di definizioni di classe localizzate è un processo in tre passaggi.
ms.assetid: e303b894-07c4-44e3-9c57-58b1db16ae9a
ms.tgt_platform: multiple
title: Creazione di definizioni di classi localizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d41a183c1478c259b0428cd827088a769e680425
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320844"
---
# <a name="creating-localized-class-definitions"></a>Creazione di definizioni di classi localizzate

La creazione di definizioni di classe localizzate è un processo in tre passaggi. Si inizia scrivendo codice MOF che definisce le classi, inclusi tutti i qualificatori che devono essere localizzati. Questo file originale è denominato file "Master MOF" perché contiene tutti i qualificatori e le proprietà che definiscono la classe.

Usare quindi il [compilatore MOF](mofcomp.md) per creare le versioni del file MOF indipendenti dalla lingua e dal linguaggio. Il compilatore MOF inserisce la descrizione della classe di base in un nuovo file MOF e crea una versione localizzata del file MOF che contiene solo le proprietà e i qualificatori che devono essere localizzati. Sebbene le versioni specifiche del linguaggio e indipendenti dalla lingua del file MOF possano avere lo stesso nome file, è necessario utilizzare un'estensione di file. mfl per indicare che il file contiene informazioni localizzate. Se necessario, è possibile localizzare il file con estensione mfl in altre impostazioni locali. L'archiviazione delle definizioni di classe nel repository CIM richiede un passaggio aggiuntivo di utilizzo del compilatore MOF per compilare sia i file MOF indipendenti dalla lingua che quelli specifici della lingua.

Nei passaggi seguenti viene descritto come creare e archiviare una definizione di classe localizzata.

**Per creare e archiviare una definizione di classe localizzata**

1.  Creare il file MOF master che definisce le classi che si desidera localizzare.

    Salvare questo codice MOF in un file denominato Mastermof. mof.

    ```syntax
    #pragma namespace("\\\\.\\root")

    instance of __Namespace
    {
        Name = "TEST" ;
    } ;

    #pragma namespace("\\\\.\\root\\TEST")

    [Description("Localized version of MyClass for American English") 
        : Amended, LOCALE(0x409)] 

    class myclass
    {
        [DisplayName("User Name") : Amended,
        Description("The Name property contains the name of the user") : 
        Amended, key]
         string Name;

        uint64 Value; // non-localized value field

          [DisplayName("Time Stamp") : Amended,
        Description("This property shows when the object was created") : 
        Amended] 
         uint64 Timestamp;
    };
    ```

2.  Creare versioni indipendenti dalla lingua e dalla lingua del file MOF compilando il file MasterMOF. mof.

    Digitare il comando seguente al prompt dei comandi per compilare il file MasterMOF. mof.

    **mofcomp-MOF: Lnmof. mof-MFL: Lsmof. mfl-emendamento: MS \_ 409 Mastermof. mof**

3.  Compilare i file indipendenti dalla lingua (Lnmof. MOF) e specifici della lingua (Lsmof. mfl) e archiviare le informazioni sulla classe nel repository CIM.

    Digitare i comandi seguenti al prompt dei comandi per archiviare le informazioni sulla classe nel repository CIM.

    **Mofcomp Lnmof. mof**

    **Mofcomp Lsmof. mfl**

    Dopo la compilazione di questi file, sarà presente una definizione di classe indipendente dal linguaggio nello \\ spazio dei nomi del test radice e una definizione di classe localizzata nello \\ \\ \_ spazio dei nomi MS 409 del test radice. Per ulteriori informazioni sulla compilazione di file MOF localizzati, vedere [compilazione di file MOF localizzati](compiling-localized-mof-files.md).

 

 



