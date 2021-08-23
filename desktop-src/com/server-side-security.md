---
title: Server-Side sicurezza
description: Server-Side sicurezza
ms.assetid: 6c1d210e-daf0-490a-a6b9-65d99b9e1d7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc7349b318361cfd27969817ec6be9d16accacd29dce625f572a51a7b3bc8082
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611011"
---
# <a name="server-side-security"></a>Server-Side sicurezza

Il server può recuperare le informazioni di sicurezza relative a un chiamante o rappresentare il chiamante usando i metodi di [**IServerSecurity.**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) Un'implementazione **di IServerSecurity** viene fornita da COM nell'oggetto contesto per la chiamata corrente quando viene utilizzato il marshalling standard. Tuttavia, questa interfaccia può essere assente per alcune interfacce con marshalling personalizzato.

Quando arriva una chiamata al server, il server può chiamare [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) per ottenere un puntatore [**all'interfaccia IServerSecurity.**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) Con questo puntatore, i metodi **IServerSecurity** possono essere chiamati dal server per individuare le impostazioni di autenticazione del client e rappresentare il client, se necessario. **L'oggetto IServerSecurity** è valido in qualsiasi thread nell'apartment fino al completamento della chiamata rappresentata da **IServerSecurity.** Per altre informazioni sulla rappresentazione, vedere [Rappresentazione](impersonation.md) e [clonazione.](cloaking.md)

Sono disponibili anche le funzioni helper seguenti che si basano sull'implementazione dell'interfaccia [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) dell'oggetto contesto di chiamata:

-   [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket)
-   [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)
-   [**CoRevertToSelf**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sicurezza in COM](security-in-com.md)
</dt> </dl>

 

 