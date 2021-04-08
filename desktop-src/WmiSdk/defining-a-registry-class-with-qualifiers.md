---
description: Le classi utilizzate per conservare i dati del registro di sistema sono definite con diversi qualificatori standard.
ms.assetid: d4786880-6c50-4e36-9a16-47de430e77a9
ms.tgt_platform: multiple
title: Definizione di una classe Registry con qualificatori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f45fdff611814eadbf57eabedf7444d098666918
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880670"
---
# <a name="defining-a-registry-class-with-qualifiers"></a>Definizione di una classe Registry con qualificatori

Le classi utilizzate per conservare i dati del registro di sistema sono definite con diversi qualificatori standard.

Di seguito è riportato un elenco dei qualificatori standard:

-   [Dynamic](standard-wmi-qualifiers.md) e [ **provider**](/windows/desktop/api/Provider/nl-provider-provider)

    Il qualificatore **dinamico** può essere collegato a una classe o a un'istanza. Il qualificatore **dinamico** contrassegna la classe o l'istanza come gestita in modo dinamico da un provider. Quando viene visualizzato **Dynamic** in una classe o in un'istanza, è necessario che venga visualizzato anche il qualificatore del [**provider**](/windows/desktop/api/Provider/nl-provider-provider) . Il qualificatore del **provider** identifica il provider specifico che deve gestire la classe o l'istanza dinamica.

-   [ClassContext](standard-wmi-qualifiers.md)

    Il qualificatore **ClassContext** è associato a una classe. Specifica il percorso della chiave del registro di sistema che contiene le informazioni rappresentate dalla classe.

    Il qualificatore **ClassContext** ha il formato seguente.

    ``` syntax
    MACHINE_NAME|Subtree\\KeyPath
    ```

    Il valore per il percorso della chiave può essere Long se include chiavi con sottochiavi.

    Nell'esempio seguente viene illustrato il qualificatore **ClassContext** che contiene il percorso di un dispositivo di trasporto del computer specifico.

    ``` syntax
    Machine_Name|HKEY_LOCAL_MACHINE\\SOFTWARE\\MICROSOFT\\WBEM\\TRANSPORTS
    ```

Il modello seguente per una definizione di classe illustra l'uso dei qualificatori **dinamici**, [**provider**](/windows/desktop/api/Provider/nl-provider-provider)e **ClassContext** . Il provider denominato dal qualificatore del **provider** è il provider del registro di sistema dell'istanza. Tenere presente che i percorsi del registro di sistema non fanno distinzione tra maiuscole e minuscole.

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

Le applicazioni di gestione possono inoltre utilizzare il provider del registro di sistema per recuperare e modificare i dati del registro di sistema per una chiave specifica.

 

 



