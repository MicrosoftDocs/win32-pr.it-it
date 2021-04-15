---
title: Sicurezza in COM
description: La protezione in COM è saldamente basata sulla sicurezza fornita da Windows e dai meccanismi di sicurezza RPC sottostanti.
ms.assetid: c9f6d06c-da24-48ea-908a-2462c33f7ee3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e5e462317d85f7c445d4d8a5ae0aa4d9d3ee724
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399785"
---
# <a name="security-in-com"></a>Sicurezza in COM

La protezione in COM è saldamente basata sulla sicurezza fornita da Windows e dai meccanismi di sicurezza RPC sottostanti. La sicurezza COM si basa sull' *autenticazione* (il processo di verifica dell'identità di un chiamante) e sull' *autorizzazione* (il processo che consente di determinare se un chiamante è autorizzato a eseguire l'operazione che sta richiedendo). Esistono due tipi principali di sicurezza in COM: *sicurezza dell'attivazione* e *sicurezza delle chiamate*. La sicurezza dell'attivazione determina se un client può avviare un server. Dopo che un server è stato avviato, è possibile utilizzare chiama sicurezza per controllare l'accesso agli oggetti di un server.

In questo modello di sicurezza, i server gestiscono e proteggono gli oggetti, i client ottengono l'accesso agli oggetti tramite server e i server possono tentare l'accesso durante la rappresentazione del client.

Il sistema implementa il protocollo di autenticazione Kerberos V5 e il pacchetto di protezione SChannel. Include inoltre funzionalità come la rappresentazione a livello di delegato, l'autenticazione reciproca, la possibilità di impostare i livelli di autenticazione per un AppID nel registro di sistema e il mascheramento. Grazie alla sicurezza COM, è possibile implementare oggetti in grado di eseguire operazioni con privilegi senza compromettere la sicurezza.

Poiché è disponibile un'ampia gamma di funzionalità di sicurezza COM, è utile determinare inizialmente il tipo di sicurezza necessario per l'applicazione. Per la maggior parte delle applicazioni, l'impostazione di un livello accettabile di sicurezza può essere un processo indolore, ma è anche possibile usare la sicurezza COM per supportare scenari di sicurezza molto complessi.

È possibile impostare processwide di sicurezza, usando Dcomcnfg.exe per impostare il registro di sistema o chiamando [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Due interfacce primarie, [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) e [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) (e funzioni helper associate), consentono di impostare la sicurezza a livello di chiamata all'interno del programma.

Per ulteriori informazioni sulla sicurezza COM, vedere gli argomenti seguenti:

-   [Determinazione delle esigenze di sicurezza](determining-your-security-needs.md)
-   [Impostazioni predefinite di sicurezza COM](com-security-defaults.md)
-   [Sicurezza attivazione](activation-security.md)
-   [Valori di sicurezza](security-values.md)
-   [Impostazione della sicurezza per le applicazioni COM](setting-security-for-com-applications.md)
-   [Abilitazione della sicurezza COM tramite DCOMCNFG](enabling-com-security-using-dcomcnfg.md)
-   [Disattivazione della sicurezza](turning-off-security.md)
-   [Sicurezza lato server](server-side-security.md)
-   [Negoziazione della copertura della sicurezza](security-blanket-negotiation.md)
-   [Pacchetti COM e di sicurezza](com-and-security-packages.md)
-   [Miglioramenti della protezione DCOM in Windows XP Service Pack 2 e Windows Server 2003 Service Pack 1](dcom-security-enhancements-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1.md)
-   [Elenchi di controllo di accesso per COM](access-control-lists-for-com.md)
-   [Moniker di elevazione COM](the-com-elevation-moniker.md)

 

 