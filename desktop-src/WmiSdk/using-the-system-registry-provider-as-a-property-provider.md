---
description: È possibile usare il provider del Registro di sistema come istanza o provider di proprietà.
ms.assetid: 0a8198c0-57c1-4d96-9965-3867c8c0e738
ms.tgt_platform: multiple
title: Usare il provider del Registro di sistema come provider di proprietà
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1b9b23be76845512df76bc0327543d463fd5eec6a816d57871f959b53229aecf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118107451"
---
# <a name="use-the-system-registry-provider-as-a-property-provider"></a>Usare il provider del Registro di sistema come provider di proprietà

È possibile usare il [provider del Registro di](/previous-versions/windows/desktop/regprov/system-registry-provider) sistema come istanza o provider di proprietà.

Se si sceglie di accedere alle interfacce del provider di proprietà, è necessario contrassegnare le classi WMI per indicare l'intenzione.

**Per usare il provider del Registro di sistema come provider di proprietà**

-   Definire la classe WMI con i qualificatori standard **DynProps,** [**Provider**](/windows/desktop/api/Provider/nl-provider-provider)e **PropertyContext.**

    Il **qualificatore DynProps** identifica una classe come con proprietà gestite dal provider di proprietà identificato dal [**qualificatore Provider.**](/windows/desktop/api/Provider/nl-provider-provider) Il **qualificatore PropertyContext** specifica il nome del valore del Registro di sistema che deve essere archiviato dalla proprietà . Il formato del qualificatore **PropertyContext** è lo stesso del formato del qualificatore **ClassContext** con *valori valuename e* *expression* aggiuntivi.

    ``` syntax
    MACHINE_NAME | Subtree\\KeyPath [|valuename [expression]]
    ```

    Sia *valuename che* *expression* sono facoltativi. *L'impostazione valuename* viene usata solo se il valore del Registro di sistema ha un nome. *L'espressione* è facoltativa e viene usata per i dati del descrittore di risorse. Per altre informazioni, vedere [Descrizione di una risorsa per il Registro di sistema.](describing-a-resource-for-the-registry.md)

    Nell'esempio di codice seguente viene illustrato come la classe usa il provider del Registro di sistema come provider di proprietà per mantenere le proprietà non chiave.

    ``` syntax
    [DYNPROPS]
    class PropReg {

        [KEY]  STRING  MyKey;
        STRING Logging;
        STRING Events;
        uint32 Resource1;
    };

    [DYNPROPS]
    instance of PropReg
    {
      MyKey = "a";

      [PropertyContext("local|hkey_local_Machine\\software\\microsoft\\
       wbem\\cimom|Logging"), Dynamic, Provider("RegPropProv")]  Logging;

      [PropertyContext("local|hkey_local_Machine\\software\\microsoft\\
       wbem\\cimom|EnableEvents"), Dynamic, Provider("RegPropProv")]
       Events;

      [PropertyContext("local|hkey_local_Machine\\hardware\\
       ResourceMap\\Hardware Abstraction Layer\\PC Compatible Eisa/isa 
       hal|.raw(\"Internal\")(0)(0)(\"interrupt.vector\")"), Dynamic, 
       Provider("RegPropProv")]  Resource1;
    };
    ```

 

 
