---
title: Classi e server
description: Classi e server
ms.assetid: cc88be56-0d96-47d2-b23b-6a6ad376bdae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30b87ce6b52e73f8ac4e465202b787a2c65dc563f3d7c0678ef82b91601351d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993801"
---
# <a name="classes-and-servers"></a>Classi e server

COM usa **HKEY \_ CLASSES \_ ROOT** per le impostazioni a livello di computer, ma consente anche la configurazione per utente di CLSIDS per una maggiore sicurezza e flessibilità. COM consulta innanzitutto le **classi software HKEY \_ CURRENT USER \_ \\ \\ prima** di cercare **in HKEY CLASSES \_ \_ ROOT**. COM mantiene le informazioni a livello di computer relative ai **CLSID in HKEY \_ CLASSES ROOT \_ \\ CLSID** e mantiene le informazioni sulle classi per utente in **HKEY CURRENT USER Software \_ \_ Classes \\ \\ \\ CLSID**.

I server COM supportano la registrazione automatica. Per un server in-process, ciò significa che la DLL deve esportare le funzioni seguenti:

-   [**Dllregisterserver**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)
-   [**Dllunregisterserver**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver)

È necessario esportare in modo esplicito queste funzioni usando un file di definizione del modulo, opzioni del linker o direttive del compilatore. L'archivio classi usa queste funzioni per configurare il Registro di sistema locale dopo il download del file nel computer client. Oltre all'archivio classi, queste funzioni vengono usate anche da altri ambienti per installare server nei computer host.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione di applicazioni COM](registering-com-applications.md)
</dt> </dl>

 

 