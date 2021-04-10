---
title: Estensioni del server dei criteri di rete
description: L'API delle estensioni NPS consente agli sviluppatori di software di scrivere dll di estensione che possono essere usate per l'autenticazione, l'autorizzazione e l'accounting. L'API delle estensioni NPS supporta il protocollo RADIUS (Remote Authentication Dial-In User Service).
ms.assetid: f459025f-fe5e-4ffa-a651-c70a4f8234ae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd6f9bd0be7479726110b41d6060a7e5c836bb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963310"
---
# <a name="network-policy-server-extensions"></a>Estensioni del server dei criteri di rete

> [!Note]  
> Il servizio di autenticazione Internet (IAS) è stato rinominato server dei criteri di rete (NPS) a partire da Windows Server 2008. Il contenuto di questo argomento si applica sia a IAS che a NPS. In tutto il testo, NPS viene utilizzato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente indicate come IAS.

 

L'API delle estensioni NPS consente agli sviluppatori di software di scrivere dll di estensione che possono essere usate per l'autenticazione, l'autorizzazione e l'accounting. L'API delle estensioni NPS supporta il protocollo RADIUS (Remote Authentication Dial-In User Service).

Le DLL di estensione implementate tramite l'API delle estensioni NPS possono fornire un controllo e una contabilità di sessione avanzati. Queste dll possono essere utilizzate per scenari quali il controllo del numero di sessioni di rete degli utenti finali, l'utilizzo di un server di stato e la connessione ai database di autenticazione del dominio e ai servizi Active Directory. Le DLL di estensione possono espandere le autorizzazioni di accesso remoto fornite da NPS aggiungendo le proprie autorizzazioni quando si invia una risposta di accettazione a un client di autenticazione.

L'API delle estensioni NPS è applicabile in qualsiasi ambiente informatico in cui potrebbe migliorare l'efficienza per autenticare gli utenti di connessione remota tramite un server remoto. Questa tecnologia è particolarmente utile per i provider di servizi Internet (ISP).

## <a name="in-this-section"></a>Contenuto della sezione

[Overview](/windows/desktop/Nps/ias-about-internet-authentication-service)

Informazioni generali su RADIUS e sull'API delle estensioni NPS.

[Usando](/windows/desktop/Nps/ias-using-internet-authentication-service)

Codice di esempio che illustra come usare l'API delle estensioni NPS.

[Riferimento](/windows/desktop/Nps/ias-internet-authentication-service-reference)

Documentazione di tipi, funzioni e strutture enumerate che compongono l'API delle estensioni NPS.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Server dei criteri di rete (servizio di autenticazione Internet)](portal.md)
</dt> <dt>

[EAP (Extensible Authentication Protocol)](../eap/eap-start-page.md)
</dt> </dl>

 

 