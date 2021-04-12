---
description: Client-Side requisiti per la rappresentazione
ms.assetid: c2d20233-93c6-4d2d-946d-8abccbeb3c5e
title: Client-Side requisiti per la rappresentazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c3c188f3c03e46a0e6e414efc66c5fdd2366d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342411"
---
# <a name="client-side-requirements-for-impersonation"></a>Client-Side requisiti per la rappresentazione

È possibile specificare le due impostazioni seguenti rispetto alla rappresentazione sul lato client:

-   Livello di rappresentazione, che indica la volontà del client di usare la propria identità del server.
-   Impostazione nel servizio Active Directory tramite la quale l'account client può essere contrassegnato come "account è sensibile e non può essere delegato", che disabilita la delega.

Il livello di rappresentazione può essere impostato in diversi modi. Se il client non indica un livello di rappresentazione, il valore predefinito a livello di computer verrà utilizzato da COM. Il valore predefinito a livello di computer può essere impostato utilizzando lo strumento di amministrazione Servizi componenti o Dcomcnfg.exe. Il client può anche indicare un livello di rappresentazione preferito in maniera amministrativa con Dcomcnfg.exe.

Il client può indicare il livello di rappresentazione a livello di codice, utilizzando [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), equivalente a [**IClientSecurity:: seblankt**](/windows/desktop/api/objidl/nf-objidl-iclientsecurity-setblanket), che può essere chiamato ogni volta che è necessario, o [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), che può essere chiamato una volta per processo.

Se il client indica una rappresentazione a livello di delegato, ovvero l'autorità più ampia che può concedere al server, il client deve essere in esecuzione con un'identità configurata correttamente nel servizio Active Directory per consentire la delega dell'identità.

Per informazioni più dettagliate sui livelli di rappresentazione e sui requisiti per il funzionamento della delega, vedere [delega e rappresentazione](/windows/desktop/com/delegation-and-impersonation).

Naturalmente, le applicazioni COM+ possono fungere sempre da client. Quando l'applicazione COM+ effettua una chiamata a un'altra applicazione o risorsa, esprime un livello di rappresentazione. Per le applicazioni server COM+, è possibile impostare un livello di rappresentazione in modo amministrativo. Le applicazioni della libreria COM+ non possono impostare il proprio livello di rappresentazione; usano invece quello del processo host. Per informazioni su come impostare la rappresentazione per un'applicazione COM+, vedere [impostazione di un livello di rappresentazione](setting-an-impersonation-level.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rappresentazione e delega client](client-impersonation-and-delegation.md)
</dt> <dt>

[Cloaking](cloaking.md)
</dt> <dt>

[Requisiti lato server per la rappresentazione](server-side-requirements-for-impersonation.md)
</dt> </dl>

 

 
