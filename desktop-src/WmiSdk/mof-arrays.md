---
description: Una matrice è un elenco indicizzato di valori di dati dello stesso tipo di dati a cui è possibile fare riferimento. Oltre alle matrici di stringhe e numeriche, MOF supporta matrici di oggetti e riferimenti incorporati.
ms.assetid: f63c222f-499d-4776-8901-65cb8b142d2b
ms.tgt_platform: multiple
title: Matrici MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1231b89302e15d5a7467ab7ff99d23b200badd67e6c5c95054c90b84554548d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992801"
---
# <a name="mof-arrays"></a>Matrici MOF

Una matrice è un elenco indicizzato di valori di dati dello stesso tipo di dati a cui è possibile fare riferimento. Oltre alle matrici di stringhe e numeriche, MOF supporta matrici di oggetti e riferimenti incorporati.

Le regole seguenti definiscono una matrice MOF:

-   Le parentesi quadre usate dopo l'identificatore di proprietà specificano una matrice in una definizione di classe.

    ``` syntax
    Class ArrayDataSample1
    {
        string strArray1[];
    };
    ```

-   Tutte le matrici devono essere unidimensionali.
-   Le matrici possono essere senza associazione o avere dimensioni esplicite.

    ``` syntax
    Class MyClass
    {
        sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk DiskArray1[]);
        sint32 MyMethod2 ([in, id(0)] Win32_LogicalDisk DiskArray2[32]);
    };
    ```

    WMI implementa matrici delimitate e non associate come **strutture SAFEARRAY,** che consente a WMI di variare le dimensioni delle matrici in fase di esecuzione. Quando si dichiara una matrice con una dimensione esplicita, WMI archivia le dimensioni come qualificatore e considera le dimensioni come dimensioni massime suggerite. Tuttavia, WMI può espandere le dimensioni, se necessario. La modifica delle dimensioni esplicite non ha alcun effetto sui dati effettivi.

-   Le matrici vengono inizializzate specificando valori del tipo appropriato in un elenco delimitato da virgole.

    ``` syntax
    Class ArrayDataSample2
    {
        [key] string s;
        string strArray2[] = {"hello", "there"};
        sint32 dwArray[] = {1,2,3};
    };
    ```

-   Una matrice di riferimenti viene dichiarata come matrice di stringhe di percorso oggetto.

    Quando si dichiara una stringa di percorso dell'oggetto, non inserire spazi vuoti tra gli elementi del percorso dell'oggetto. Nell'esempio seguente viene descritto come dichiarare un riferimento al percorso di un oggetto.

    ``` syntax
    Class ClassWithRefArray
        { 
        [key] string s; 
        object ref refArray[]; 
        };

    instance of ClassWithRefArray
        {
        s = 23;
        refArray = {"Disk.Name=\"C:\"", "Disk.Name=\"E:\""};
        };
    ```

-   È possibile usare una matrice come parametro per un metodo, ma non come valore restituito per un parametro di input o di output di input.
-   Tutti gli elementi in una matrice vengono creati come valori dello stesso tipo.

    Se gli elementi di una matrice sono di tipo **oggetto,** è possibile inserire qualsiasi tipo di oggetto nella matrice. D'altra parte, se si dichiara un tipo specifico di oggetto, WMI consente solo gli oggetti di tale classe o sottoclasse nella matrice. Negli esempi seguenti vengono mostrate le dichiarazioni di matrice che includono l'uso del **tipo di** oggetto .

    ``` syntax
    Class EmbedClass
    {
        [key] sint32 PropOfClass;
    };

    Class ArrayDataClass
    {
        [key] string s;
        string strArray1[];
        string strArray2[] = {"hello", "there"};
        sint32 dwArray[] = {1,2,3};
        EmbedClass objArray[];
    };

    instance of ArrayDataClass
    { 
        s = "keyStuff";
        strArray1 = { "1.2.3.4", "1.2.3.5", "1.2.3.7"};
        strArray2 = 
            {
                "SELECT * FROM RegistryKeyChangeEvent",
                "SELECT * FROM RegistryValueChangeEvent",
                "SELECT * FROM RegistryTreeChangeEvent"
            };
        dwArray  = { 1,2,3,5,6 };
        objArray = {
                       instance of EmbedClass{PropOfClass=3;},
                       instance of EmbedClass{PropOfClass=4;}
                   };
    };
    ```

 

 



