---
description: Le classi utilizzate per contenere i dati del Registro di sistema sono definite con diversi qualificatori standard.
ms.assetid: d4786880-6c50-4e36-9a16-47de430e77a9
ms.tgt_platform: multiple
title: Definizione di una classe del Registro di sistema con qualificatori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f42e3c383a5d71d66c88f388aa1745f8a8324568a7fd85ac0f48e5e2cff30e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117925227"
---
# <a name="defining-a-registry-class-with-qualifiers"></a>Definizione di una classe del Registro di sistema con qualificatori

Le classi utilizzate per contenere i dati del Registro di sistema sono definite con diversi qualificatori standard.

Di seguito è riportato un elenco dei qualificatori standard:

-   [Dinamico](standard-wmi-qualifiers.md) e [ **provider**](/windows/desktop/api/Provider/nl-provider-provider)

    È possibile associare il **qualificatore Dynamic** a una classe o a un'istanza di . Il **qualificatore Dynamic** contrassegna la classe o l'istanza come gestita dinamicamente da un provider. Quando **Dynamic viene** visualizzato in una classe o in un'istanza, deve essere visualizzato anche il [**qualificatore**](/windows/desktop/api/Provider/nl-provider-provider) Provider. Il **qualificatore Provider** identifica il provider specifico che deve gestire la classe o l'istanza dinamica.

-   [ClassContext](standard-wmi-qualifiers.md)

    Il **qualificatore ClassContext** è associato a una classe. Specifica il percorso della chiave del Registro di sistema che contiene le informazioni rappresentate dalla classe .

    Il **formato del qualificatore ClassContext** è il seguente.

    ``` syntax
    MACHINE_NAME|Subtree\\KeyPath
    ```

    Il valore di KeyPath può essere lungo se include chiavi con sottochiavi.

    Nell'esempio seguente viene illustrato il **qualificatore ClassContext** che contiene il percorso di un dispositivo di trasporto computer specifico.

    ``` syntax
    Machine_Name|HKEY_LOCAL_MACHINE\\SOFTWARE\\MICROSOFT\\WBEM\\TRANSPORTS
    ```

Il modello seguente per una definizione di classe illustra l'uso dei qualificatori **Dynamic**, [**Provider**](/windows/desktop/api/Provider/nl-provider-provider)e **ClassContext.** Il provider denominato dal qualificatore Provider è il **provider** del Registro di sistema dell'istanza. Tenere presente che per i percorsi del Registro di sistema non viene fatto distinzione tra maiuscole e minuscole, così come i nomi dei qualificatori.

``` syntax
[dynamic, provider("RegProv"), 
    ClassContext("local|hkey_local_machine\\software\\microsoft
    \\WBEM\\transports\\Network Transport Modules")]

class RegTrans
{
  [key] string  TransportsGUID;
  [PropertyContext("Name")] string Name;
  [PropertyContext("Independent")] uint32 Enabled;
};
```

Le applicazioni di gestione possono anche usare il provider del Registro di sistema per recuperare e modificare i dati del Registro di sistema per una chiave specifica.

 

 



