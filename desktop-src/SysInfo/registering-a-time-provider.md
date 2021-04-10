---
description: Il sistema carica un provider di tempo in base alle informazioni di configurazione archiviate nel registro di sistema.
ms.assetid: 67f79c31-9dd7-4e3f-bfe1-701b10611f91
title: Registrazione di un provider Time
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a98e5e516db6b2c800c917c5e47da9bd75ba5c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882350"
---
# <a name="registering-a-time-provider"></a>Registrazione di un provider Time

Il sistema carica un provider di tempo in base alle informazioni di configurazione archiviate nel registro di sistema. Ogni provider di servizi temporali deve creare la chiave del registro di sistema seguente:

**HKEY \_ \_Computer locale \\ System** \\ **CurrentControlSet** \\ **Services** \\ **W32Time** \\ **TimeProviders** \\ *providerName*

Nella tabella seguente vengono descritti i valori che devono esistere nella chiave di ogni provider.



| Valore             | Descrizione                                                                                                                                                                                                              |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **DllName**       | Nome della DLL che contiene il provider. Questo valore è di tipo **reg \_ SZ**.                                                                                                                                     |
| **Enabled**       | Indica se il provider deve essere avviato. Se questo valore è 1, il provider viene avviato. In caso contrario, il provider non viene avviato. Questo valore è di tipo **reg \_ DWORD**.                                           |
| **InputProvider** | Indica se il provider è un provider di input o un provider di output. Se questo valore è 1, il provider è un provider di input. In caso contrario, il provider è un provider di output. Questo valore è di tipo **reg \_ DWORD**. |



 

Gestione provider di servizi temporali enumera le chiavi sotto la chiave **TimeProviders** e avvia ogni provider abilitato. I provider vengono avviati all'avvio del sistema e ogni volta che vengono apportate modifiche ai parametri.

Ogni provider di servizi temporali può inoltre archiviare informazioni di configurazione specifiche dell'applicazione nel registro di sistema.

 

 



