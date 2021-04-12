---
title: Server dei criteri di rete
description: Server dei criteri di rete è l'implementazione Microsoft di un server e un proxy RADIUS (Remote Authentication Dial-in User Service).
ms.assetid: d0eb41cb-e9c0-4a60-aeac-77d1dd90a75b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d1dfc680c8a23ca1e80f52230736b3ab586cc8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337886"
---
# <a name="network-policy-server"></a>Server dei criteri di rete

## <a name="purpose"></a>Scopo

Server dei criteri di rete è l'implementazione Microsoft di un server e un proxy RADIUS (Remote Authentication Dial-in User Service). È il successore del servizio di autenticazione Internet (IAS).

Come server RADIUS, NPS esegue l'autenticazione, l'autorizzazione e l'accounting per le connessioni wireless, di autenticazione e di accesso remoto e VPN (Virtual Private Network).

Server dei criteri di rete è anche un server di valutazione dell'integrità per protezione accesso alla rete (NAP). NPS esegue l'autenticazione e l'autorizzazione dei tentativi di connessione di rete e, in base ai criteri di integrità del sistema configurati, valuta la conformità dell'integrità del computer e determina come limitare l'accesso alla rete o la comunicazione di un computer non conforme. Si tratta di una nuova funzionalità specifica solo per NPS. Il servizio IAS non lo supporta. Per un elenco completo delle nuove funzionalità di server dei criteri di [rete, vedere servizio di autenticazione Internet e server dei criteri di rete](internet-authentication-service-vs-network-policy-server.md) .

Server dei criteri di server include due set di API: API per le estensioni NPS e API per oggetti dati server (SDO). Sia l'API di NPS che l'API SDO sono supportate anche dal precursore di NPS, il servizio di autenticazione Internet.

L'API delle estensioni NPS può essere usata per estendere i metodi di autenticazione, autorizzazione e contabilità offerti da server dei criteri di servizio e precedenti da IAS.

L'API oggetti dati server può essere utilizzata per modificare la configurazione dei criteri di rete in un computer che esegue NPS o IAS.

> [!Note]  
> I criteri di rete nel server dei criteri di rete sono equivalenti ai criteri di accesso remoto in IAS.

 

## <a name="developer-audience"></a>Sviluppatori

L'API delle estensioni NPS è progettata per l'uso da parte dei programmatori che usano il software di sviluppo C/C++. I programmatori devono acquisire familiarità con i concetti di rete e il protocollo RADIUS. RADIUS è documentato in [rfc 2865](https://www.ietf.org/rfc/rfc2865.txt) e [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).

L'API oggetti dati server è progettata per l'uso da parte dei programmatori che usano C/C++ o software di sviluppo Visual Basic. I programmatori devono avere familiarità con il [servizio di accesso remoto](/windows/desktop/RRAS/remote-access-request-for-comments) (RAS) e il protocollo RADIUS.

## <a name="run-time-requirements"></a>Requisiti di runtime

L'API delle estensioni NPS è supportata in Windows Server 2008 con l'installazione di Microsoft Commercial Internet Service (MCIS).

L'API oggetti dati server è supportata in Windows Server 2008.

Server dei criteri di rete è disponibile in Windows Server 2008 con l'installazione di Microsoft Commercial Internet Service (MCIS).

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[Overview](about-network-policy-server.md)
</dt> <dd>

Informazioni generali su RADIUS, IAS e NPS.

</dd> <dt>

[API delle estensioni del server dei criteri di rete](ias-extensions.md)
</dt> <dd>

API per l'implementazione delle DLL di estensione usate per l'autenticazione, l'autorizzazione e l'accounting.

</dd> <dt>

[API oggetti dati server](server-data-objects.md)
</dt> <dd>

API per la gestione della configurazione dei criteri di rete.

</dd> <dt>

[Programmabilità SQL](sql-programmability.md)
</dt> <dd>

Esempi di stored procedure utilizzate per la gestione della registrazione di NPS (IAS).

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[TechNet: Server dei criteri di rete](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))
</dt> <dt>

[TechNet: servizio di autenticazione Internet](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))
</dt> <dt>

[Protezione accesso alla rete](/windows/desktop/NAP/network-access-protection-start-page)
</dt> </dl>

 

 