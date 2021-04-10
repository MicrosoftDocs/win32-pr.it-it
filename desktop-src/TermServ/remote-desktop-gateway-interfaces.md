---
title: Interfacce del Gateway Desktop remoto
description: L'API Gateway Desktop remoto (Gateway Desktop remoto) supporta le interfacce seguenti. È possibile usare queste interfacce per implementare plug-in che forniscono l'autenticazione e l'autorizzazione personalizzate.
ms.assetid: a457574a-d856-4490-b20d-48343a82acff
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d2b0a17c19431ea69419443459639d199219a61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955199"
---
# <a name="remote-desktop-gateway-interfaces"></a>Interfacce del Gateway Desktop remoto

L'API Gateway Desktop remoto (Gateway Desktop remoto) supporta le interfacce seguenti. È possibile usare queste interfacce per implementare plug-in che forniscono l'autenticazione e l'autorizzazione personalizzate. Non esiste alcuna dipendenza tra il plug-in di autenticazione e il plug-in di autorizzazione ed è possibile implementare un solo plug-in, se si sceglie.

I plug-in di autenticazione sono [**ITSGAuthenticateUserSink**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticateusersink) e [**ITSGAuthenticationEngine**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticationengine).

I plug-in di autorizzazione sono [**ITSGAccountingEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgaccountingengine), [**ITSGAuthorizeConnectionSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeconnectionsink), [**ITSGAuthorizeResourceSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeresourcesink)e [**ITSGPolicyEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgpolicyengine).

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[**ITSGAccountingEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgaccountingengine)
</dt> <dd>

Espone metodi che forniscono informazioni sulla creazione o la chiusura di sessioni per una connessione.

</dd> <dt>

[**ITSGAuthenticateUserSink**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticateusersink)
</dt> <dd>

Espone metodi che inviano notifiche a Gateway Desktop remoto sugli eventi di autenticazione.

</dd> <dt>

[**ITSGAuthenticationEngine**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticationengine)
</dt> <dd>

Espone metodi che autenticano gli utenti per Gateway Desktop remoto.

</dd> <dt>

[**ITSGAuthorizeConnectionSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeconnectionsink)
</dt> <dd>

Espone metodi che notificano a Gateway Desktop remoto il risultato di un tentativo di autorizzare una connessione.

</dd> <dt>

[**ITSGAuthorizeResourceSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeresourcesink)
</dt> <dd>

Espone metodi che notificano a Gateway Desktop remoto il risultato di un tentativo di autorizzare una risorsa.

</dd> <dt>

[**ITSGPolicyEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgpolicyengine)
</dt> <dd>

Espone metodi che autorizzano connessioni e risorse.

</dd> </dl>

 

 




