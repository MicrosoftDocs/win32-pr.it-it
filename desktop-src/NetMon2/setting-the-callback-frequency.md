---
description: Usare il codice seguente per impostare la frequenza di callback.
ms.assetid: fdcad3c2-7e36-4194-83c7-dccbd50762d5
title: Impostazione della frequenza di callback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4f235377865583e48d6a4b9c16abce4209e6449f74ed3cf42688dfa417287bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363247"
---
# <a name="setting-the-callback-frequency"></a>Impostazione della frequenza di callback

Usare il codice seguente per impostare la frequenza di callback:

**DWORD** Valore = 1;


```C++
rc = SetDwordInBlob(hNPPBlob, OWNER_NPP, CATEGORY_CONFIG,
                    TAG_UPDATE_FREQUENCY, Value);
```



Questo frammento di codice imposta la frequenza di callback su 1 secondo (valore minimo). Il valore massimo deve essere molto maggiore di 1. Se il buffer del provider di pacchetti di rete (NPP) è pieno, il servizio NPP richiama il monitoraggio prima.

 

 



