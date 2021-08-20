---
title: Esempio di valori del Registro di sistema
description: L'esempio seguente mostra i dati possibili per alcuni dei valori del Registro di sistema del protocollo di autenticazione.
ms.assetid: 07772af0-db56-4cc6-ad72-cf79d3813883
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8a8bc87ef728d2524f9e7f21ad6ff69f1dd58ccee8d4836d8a2ceef4c676e00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118087012"
---
# <a name="registry-values-example"></a>Esempio di valori del Registro di sistema

L'esempio seguente mostra i dati possibili per alcuni dei valori del Registro di sistema del protocollo di autenticazione.

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
| Percorso                | REG \_ EXPAND \_ SZ | %SystemRoot% \\ system32 \\sample.dll     |
| FriendlyName        | REG \_ SZ         | Protocollo EAP di esempio                    |
| ConfigUIPath        | REG \_ EXPAND \_ SZ | %SystemRoot% \\ system32 \\sample.dll     |
| IdentityPath        | REG \_ EXPAND \_ SZ | %SystemRoot% \\ system32 \\sample.dll     |
| InteractiveUIPath   | REG \_ EXPAND \_ SZ | %SystemRoot% \\ system32 \\sample.dll     |
| RequireConfigUI     | REG \_ DWORD      | 1                                      |
| ConfigCLSID         | REG \_ SZ         | {0000031A-0000-0000-C000-000000000046} |
| StandaloneSupported | REG \_ DWORD      | 1                                      |



 

 

 




