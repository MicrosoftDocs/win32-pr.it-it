---
description: Usare il codice seguente per impostare la frequenza di callback.
ms.assetid: fdcad3c2-7e36-4194-83c7-dccbd50762d5
title: Impostazione della frequenza di callback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e03c260b6d289e473f27bb3ae6b84a3f42d0878
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343866"
---
# <a name="setting-the-callback-frequency"></a>Impostazione della frequenza di callback

Usare il codice seguente per impostare la frequenza di callback:

**DWORD** Valore = 1;


```C++
rc = SetDwordInBlob(hNPPBlob, OWNER_NPP, CATEGORY_CONFIG,
                    TAG_UPDATE_FREQUENCY, Value);
```



Questo frammento di codice imposta la frequenza di callback su 1 secondo (valore minimo). Il valore massimo deve essere molto maggiore di 1. Se il buffer del provider di pacchetti di rete (NPP) è pieno, l'oggetto NPP chiama prima il monitoraggio.

 

 



