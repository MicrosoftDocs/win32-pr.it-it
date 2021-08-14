---
description: Il sistema carica un provider di servizi ora in base alle informazioni di configurazione archiviate nel Registro di sistema.
ms.assetid: 67f79c31-9dd7-4e3f-bfe1-701b10611f91
title: Registrazione di un provider di servizi ora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eeb7bce1370e443eaf3eb42d78cdfd058cf2c38147da038de1e921d85e957f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763926"
---
# <a name="registering-a-time-provider"></a>Registrazione di un provider di servizi ora

Il sistema carica un provider di servizi ora in base alle informazioni di configurazione archiviate nel Registro di sistema. Ogni provider di tempo deve creare la chiave del Registro di sistema seguente:

**HKEY \_ Local \_ MACHINE \\ System** \\ **CurrentControlSet** \\ **Services** \\ **W32Time** \\ **TimeProviders** \\ *ProviderName*

Nella tabella seguente vengono descritti i valori che devono esistere nella chiave di ogni provider.



| Valore             | Descrizione                                                                                                                                                                                                              |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **DllName**       | Nome della DLL che contiene il provider. Questo valore è di tipo **REG \_ SZ**.                                                                                                                                     |
| **Enabled**       | Indica se il provider deve essere avviato. Se questo valore è 1, il provider viene avviato. In caso contrario, il provider non viene avviato. Questo valore è di tipo **REG \_ DWORD**.                                           |
| **InputProvider** | Indica se il provider è un provider di input o un provider di output. Se questo valore è 1, il provider è un provider di input. In caso contrario, il provider è un provider di output. Questo valore è di tipo **REG \_ DWORD**. |



 

Il gestore del provider di servizi ora enumera le chiavi nella **chiave TimeProviders** e avvia ogni provider abilitato. I provider vengono avviati all'avvio del sistema e ogni volta che vengono apportate modifiche ai parametri.

Ogni provider di servizi di tempo può anche archiviare le informazioni di configurazione specifiche dell'applicazione nel Registro di sistema.

 

 



