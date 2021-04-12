---
description: Il modello di localizzazione dello schema CIM fornisce un meccanismo per localizzare i qualificatori. Non supporta la localizzazione diretta dei valori delle proprietà.
ms.assetid: a88bd873-7132-45b6-831e-64f9bb254c6e
ms.tgt_platform: multiple
title: Localizzazione dei valori delle proprietà
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5ccec714557934ca32a878e21fb2a75d24a211a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344896"
---
# <a name="localizing-property-values"></a>Localizzazione dei valori delle proprietà

Il modello di localizzazione dello schema CIM fornisce un meccanismo per localizzare i qualificatori. Non supporta la localizzazione diretta dei valori delle proprietà.

In alcuni casi, tuttavia, i valori delle proprietà di stringa nelle istanze statiche possono essere sostituiti da un tipo Integer enumerato ed è possibile definire una mappa di valori per la proprietà nella definizione della classe. In questi casi, il qualificatore **values** deve essere localizzato. L'uso di qualificatori di enumerazione è il meccanismo principale per localizzare i valori delle proprietà. Qualsiasi altra forma di localizzazione del valore della proprietà non è supportata.

Nell'esempio seguente viene illustrato il modo in cui le proprietà statiche possono essere localizzate utilizzando le mappe di valori parziali con espressioni regolari. In questo esempio, il subset di valori predefinito viene inizializzato nello schema usando istanze statiche. Il resto dei valori viene fornito dinamicamente.

``` syntax
[abstract]
class DataGroup
{
   [key] string GUID;
   [Description("data group display name"): Amended,
                     ValueMap{"Logical Disk",
                     "CPU Utilization", ".+"}]
                     string GroupDisplayName;
   [ValueMap{"Monitors percentage of disk free space",
                  "Monitors percentage CPU utilization", ".+"}] 
                   string GroupDescription;
};

[static, Description ("pre-configured parameters") :amended]
class InitialGroup : DataGroup {
};

[dynamic, provider("HMProvider"),
    Description ("user-defined parameters") :amended]
class UserDefionedGroup : DataGroup {
};

instance of InitialGroup {
   GUID = "abc";
   GroupDisplayName = "Logical Disk";
   GroupDescription = "Monitors percentage of disk free space";
};

instance of InitialGroup {
   GUID = "def";
   GroupDisplayName = "CPU Utilization";
   GroupDescription = "Monitors percentage CPU utilization";
};
```

Per altre informazioni, vedere [localizzazione di proprietà statiche](localizing-static-properties.md).

 

 



