---
title: Sicurezza Server-Side
description: Sicurezza Server-Side
ms.assetid: 6c1d210e-daf0-490a-a6b9-65d99b9e1d7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77501c395c3ae1f14c8451d4691e7e776545e756
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963493"
---
# <a name="server-side-security"></a>Sicurezza Server-Side

Il server può recuperare le informazioni di sicurezza relative a un chiamante o rappresentare il chiamante utilizzando i metodi di [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity). Un'implementazione di **IServerSecurity** viene fornita da com nell'oggetto Context per la chiamata corrente quando viene utilizzato il marshalling standard. Questa interfaccia potrebbe tuttavia essere assente per alcune interfacce con marshalling personalizzato.

Quando arriva una chiamata al server, il server può chiamare [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) per ottenere un puntatore all'interfaccia [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) . Con questo puntatore, i metodi **IServerSecurity** possono essere chiamati dal server per individuare le impostazioni di autenticazione del client e per rappresentare il client, se necessario. L'oggetto **IServerSecurity** è valido in qualsiasi thread nell'Apartment finché la chiamata rappresentata da **IServerSecurity** non viene completata. Per ulteriori informazioni sulla rappresentazione, vedere [rappresentazione](impersonation.md) e [mascheramento](cloaking.md).

Sono disponibili anche le funzioni di supporto seguenti che si basano sull'implementazione dell'interfaccia [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) dell'oggetto contesto di chiamata:

-   [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket)
-   [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)
-   [**CoRevertToSelf**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sicurezza in COM](security-in-com.md)
</dt> </dl>

 

 