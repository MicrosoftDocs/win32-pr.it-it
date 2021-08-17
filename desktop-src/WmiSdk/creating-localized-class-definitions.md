---
description: La creazione di definizioni di classi localizzate è un processo in tre passaggi.
ms.assetid: e303b894-07c4-44e3-9c57-58b1db16ae9a
ms.tgt_platform: multiple
title: Creazione di definizioni di classi localizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2d7cb5f2970c3696de7cdd1bdb9d61d6eed5e86dc60c8941eec475d15145dd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119374771"
---
# <a name="creating-localized-class-definitions"></a>Creazione di definizioni di classi localizzate

La creazione di definizioni di classi localizzate è un processo in tre passaggi. Si inizia scrivendo codice MOF che definisce le classi, inclusi tutti i qualificatori che devono essere localizzati. Questo file originale è denominato "file MOF master" perché contiene tutti i qualificatori e le proprietà che definiscono la classe.

Usare quindi il [compilatore MOF](mofcomp.md) per creare le versioni indipendenti dal linguaggio e specifiche del linguaggio del file MOF. Il compilatore MOF inserisce la descrizione della classe di base in un nuovo file MOF e crea una versione localizzata del file MOF che contiene solo le proprietà e i qualificatori che devono essere localizzati. Anche se le versioni specifiche della lingua e indipendenti dalla lingua del file MOF possono avere lo stesso nome file, è consigliabile usare un'estensione mfl per indicare che il file contiene informazioni localizzate. Se necessario, è possibile localizzare il file con estensione mfl in altre impostazioni locali. L'archiviazione delle definizioni di classe nel repository CIM richiede un passaggio aggiuntivo dell'uso del compilatore MOF per compilare sia i file MOF indipendenti dal linguaggio che i file MOF specifici del linguaggio.

La procedura seguente descrive come creare e archiviare una definizione di classe localizzata.

**Per creare e archiviare una definizione di classe localizzata**

1.  Creare il file MOF master che definisce le classi da localizzare.

    Salvare il codice MOF in un file denominato Mastermof.mof.

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

2.  Creare versioni indipendenti dalla lingua e specifiche della lingua del file MOF compilando il file MasterMOF.mof.

    Digitare il comando seguente al prompt dei comandi per compilare il file MasterMOF.mof.

    **mofcomp -MOF:Lnmof.mof -MFL:Lsmof.mfl -Amendment:MS \_ 409 Mastermof.mof**

3.  Compilare i file indipendenti dal linguaggio (Lnmof.mof) e specifici del linguaggio (Lsmof.mfl) e archiviare le informazioni sulla classe nel repository CIM.

    Digitare i comandi seguenti al prompt dei comandi per archiviare le informazioni sulla classe nel repository CIM.

    **Mofcomp Lnmof.mof**

    **Mofcomp Lsmof.mfl**

    Dopo aver compilato questi file, si avrà una definizione di classe indipendente dalla lingua nello spazio dei nomi del test radice e una definizione di classe localizzata nello spazio dei nomi \\ \\ ms \\ 409 del test \_ radice. Per altre informazioni sulla compilazione di file MOF localizzati, vedere [Compilazione di file MOF localizzati](compiling-localized-mof-files.md).

 

 



