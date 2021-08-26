---
title: Estensioni del server di Criteri di rete
description: L'API NPS Extensions consente agli sviluppatori software di scrivere DLL di estensione che possono essere usate per l'autenticazione, l'autorizzazione e l'accounting. L'API NPS Extensions supporta il protocollo Remote Authentication Dial-In User Service (RADIUS).
ms.assetid: f459025f-fe5e-4ffa-a651-c70a4f8234ae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8db32889f266861809a0637dd380eb9f5d2ba7265bdf16d6a9404ed96a5420a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128771"
---
# <a name="network-policy-server-extensions"></a>Estensioni del server di Criteri di rete

> [!Note]  
> Il servizio Autenticazione Internet (IAS) è stato rinominato Server dei criteri di rete a partire da Windows Server 2008. Il contenuto di questo argomento si applica sia a IAS che a Server dei criteri di rete. In tutto il testo, Server dei criteri di rete viene usato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente denominate IAS.

 

L'API NPS Extensions consente agli sviluppatori software di scrivere DLL di estensione che possono essere usate per l'autenticazione, l'autorizzazione e l'accounting. L'API NPS Extensions supporta il protocollo Remote Authentication Dial-In User Service (RADIUS).

Le DLL di estensione implementate tramite l'API NPS Extensions possono fornire un controllo e un accounting di sessione migliorati. Queste DLL possono essere usate per scenari come il controllo del numero di sessioni di rete degli utenti finali, l'uso di un server di stato e la connessione ai database di autenticazione del dominio e ai servizi Active Directory. Le DLL di estensione possono espandere le autorizzazioni di accesso remoto fornite da Server dei criteri di rete aggiungendo le proprie autorizzazioni quando si invia una risposta Accept a un client di autenticazione.

L'API NPS Extensions è applicabile in qualsiasi ambiente informatico in cui migliorerebbe l'efficienza per autenticare gli utenti con accesso remoto tramite un server remoto. Questa tecnologia è particolarmente utile per i provider di servizi Internet (ISP).

## <a name="in-this-section"></a>Contenuto della sezione

[Overview](/windows/desktop/Nps/ias-about-internet-authentication-service)

Informazioni generali su RADIUS e sull'API NPS Extensions.

[Utilizzando](/windows/desktop/Nps/ias-using-internet-authentication-service)

Codice di esempio che illustra come usare l'API NPS Extensions.

[Riferimento](/windows/desktop/Nps/ias-internet-authentication-service-reference)

Documentazione di tipi, funzioni e strutture enumerati che costituiscono l'API NPS Extensions.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Server dei criteri di rete (servizio di autenticazione Internet)](portal.md)
</dt> <dt>

[EAP (Extensible Authentication Protocol)](../eap/eap-start-page.md)
</dt> </dl>

 

 