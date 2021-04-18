---
description: È possibile utilizzare il provider del registro di sistema come istanza o provider di proprietà.
ms.assetid: 0a8198c0-57c1-4d96-9965-3867c8c0e738
ms.tgt_platform: multiple
title: Usare il provider del registro di sistema come provider di proprietà
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 64fc701843438b4d173b1914ed2ac86214fe685e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315186"
---
# <a name="use-the-system-registry-provider-as-a-property-provider"></a>Usare il provider del registro di sistema come provider di proprietà

È possibile utilizzare il [provider del registro di sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) come istanza o provider di proprietà.

Se si sceglie di accedere alle interfacce del provider di proprietà, è necessario contrassegnare le classi WMI per indicare l'intenzione.

**Per utilizzare il provider del registro di sistema come provider di proprietà**

-   Definire la classe WMI con i qualificatori standard **DynProps**, [**provider**](/windows/desktop/api/Provider/nl-provider-provider)e **PropertyContext** .

    Il qualificatore **DynProps** identifica una classe come avente proprietà gestite dal provider di proprietà identificato dal qualificatore del [**provider**](/windows/desktop/api/Provider/nl-provider-provider) . Il qualificatore **PropertyContext** specifica il nome del valore del registro di sistema da archiviare con la proprietà. Il formato del qualificatore **PropertyContext** è uguale al formato del qualificatore **ClassContext** con valori *valueName* e *Expression* aggiuntivi.

    ``` syntax
    MACHINE_NAME | Subtree\\KeyPath [|valuename [expression]]
    ```

    *ValueName* ed *Expression* sono facoltativi. L'impostazione *valueName* viene usata solo se il valore del registro di sistema ha un nome. L' *espressione* è inoltre facoltativa e viene utilizzata per i dati del descrittore di risorse. Per ulteriori informazioni, vedere [Descrizione di una risorsa per il registro di sistema](describing-a-resource-for-the-registry.md).

    Nell'esempio di codice seguente viene illustrato il modo in cui la classe utilizza il provider del registro di sistema come provider di proprietà per mantenere le proprietà colonne.

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

 

 
