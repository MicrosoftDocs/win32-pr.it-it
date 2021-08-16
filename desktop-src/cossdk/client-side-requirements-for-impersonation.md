---
description: Client-Side per la rappresentazione
ms.assetid: c2d20233-93c6-4d2d-946d-8abccbeb3c5e
title: Client-Side per la rappresentazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bceb47c2ffb5f3b8e443d2dc50add83a39b5dfc1ee31a6909c34b0170a85db11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118308530"
---
# <a name="client-side-requirements-for-impersonation"></a>Client-Side per la rappresentazione

È possibile specificare le due impostazioni seguenti in relazione alla rappresentazione sul lato client:

-   Livello di rappresentazione, che indica la disponibilità del client a fare in modo che il server usi la propria identità.
-   Impostazione nel servizio Active Directory tramite la quale l'account client può essere contrassegnato come "L'account è sensibile e non può essere delegato", che disabilita la delega.

Il livello di rappresentazione può essere impostato in diversi modi. Se il client non indica un livello di rappresentazione, il valore predefinito a livello di computer verrà utilizzato da COM. L'impostazione predefinita a livello di computer può essere impostata tramite lo strumento amministrativo Servizi componenti o Dcomcnfg.exe. Il client può anche indicare un livello di rappresentazione preferito a livello amministrativo con Dcomcnfg.exe.

Il client può indicare il livello di rappresentazione a livello di codice, usando [**CoSetProxyBlanket,**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)equivalente a [**IClientSecurity::SetBlanket,**](/windows/desktop/api/objidl/nf-objidl-iclientsecurity-setblanket)che può essere chiamato con la frequenza necessaria, oppure [**CoInitializeSecurity,**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)che può essere chiamato una volta per processo.

Se il client indica la rappresentazione a livello di delegato, ovvero l'autorità più ampia che può concedere al server, il client deve essere in esecuzione con un'identità configurata correttamente nel servizio Active Directory per consentire la delega della propria identità.

Per altri dettagli sui livelli di rappresentazione e sui requisiti per il funzionamento della delega, vedere [Delega e rappresentazione.](/windows/desktop/com/delegation-and-impersonation)

Naturalmente, le applicazioni COM+ possono sempre fungere da client. Quando l'applicazione COM+ effettua una chiamata a un'altra applicazione o risorsa, esprime un livello di rappresentazione. Per le applicazioni server COM+, è possibile impostare un livello di rappresentazione a livello amministrativo. Le applicazioni della libreria COM+ non possono impostare il proprio livello di rappresentazione. usano invece quella del processo host. Per informazioni su come impostare la rappresentazione per un'applicazione COM+, vedere [Impostazione di un livello di rappresentazione.](setting-an-impersonation-level.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rappresentazione e delega del client](client-impersonation-and-delegation.md)
</dt> <dt>

[Cloaking](cloaking.md)
</dt> <dt>

[Requisiti lato server per la rappresentazione](server-side-requirements-for-impersonation.md)
</dt> </dl>

 

 
