---
title: Esempio di valori del registro di sistema
description: Nell'esempio seguente vengono mostrati i dati possibili per alcuni valori del registro di sistema del protocollo di autenticazione.
ms.assetid: 07772af0-db56-4cc6-ad72-cf79d3813883
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bcbc3d4ca10a3e9298177a5eea240d0d34ade04
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "104046152"
---
# <a name="registry-values-example"></a>Esempio di valori del registro di sistema

Nell'esempio seguente vengono mostrati i dati possibili per alcuni valori del registro di sistema del protocollo di autenticazione.

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rasman
               PPP
                  EAP
                     40
                        Path
                        FriendlyName
                        ConfigUIPath
                        IdentityPath
                        InteractiveUIPath
                        RequireConfigUI
                        ConfigCLSID
                        StandaloneSupported
```



| Nome chiave            | Datatype        | Valore                                  |
|---------------------|-----------------|----------------------------------------|
| Percorso                | REG \_ Espandi \_ SZ | % SystemRoot% \\ system32 \\sample.dll     |
| FriendlyName        | REG \_ SZ         | Protocollo EAP di esempio                    |
| ConfigUIPath        | REG \_ Espandi \_ SZ | % SystemRoot% \\ system32 \\sample.dll     |
| IdentityPath        | REG \_ Espandi \_ SZ | % SystemRoot% \\ system32 \\sample.dll     |
| InteractiveUIPath   | REG \_ Espandi \_ SZ | % SystemRoot% \\ system32 \\sample.dll     |
| RequireConfigUI     | REG \_ DWORD      | 1                                      |
| ConfigCLSID         | REG \_ SZ         | {0000031A-0000-0000-C000-000000000046} |
| StandaloneSupported | REG \_ DWORD      | 1                                      |



 

 

 




