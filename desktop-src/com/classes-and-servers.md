---
title: Classi e server
description: Classi e server
ms.assetid: cc88be56-0d96-47d2-b23b-6a6ad376bdae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d319fd985b812692e6d0bfc421c4bb9da2a2605c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399775"
---
# <a name="classes-and-servers"></a>Classi e server

COM utilizza **la \_ \_ radice delle classi HKEY** per le impostazioni a livello di computer, ma consente anche la configurazione per utente dei CLSID per una maggiore sicurezza e flessibilità. COM innanzitutto consulta **\_ \_ \\ \\ le classi del software utente corrente di HKEY** prima di cercare nella **\_ \_ radice delle classi HKEY**. COM mantiene le informazioni a livello di computer correlate ai CLSID **nel \_ \_ \\ CLSID radice delle classi HKEY** e mantiene le informazioni sulle classi per utente in **HKEY \_ \_ \\ classi software utente correnti \\ \\ CLSID**.

I server COM supportano la registrazione automatica. Per un server in-process, significa che la DLL deve esportare le funzioni seguenti:

-   [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)
-   [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver)

È necessario esportare in modo esplicito queste funzioni utilizzando un file di definizione del modulo, commutatori del linker o direttive del compilatore. L'archivio classi utilizza queste funzioni per configurare il registro di sistema locale dopo il download del file nel computer client. Oltre all'archivio classi, queste funzioni vengono usate anche da altri ambienti per installare i server nei computer host.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione di applicazioni COM](registering-com-applications.md)
</dt> </dl>

 

 