---
title: Server dei criteri di rete
description: Server dei criteri di rete è l'implementazione Microsoft di un server RADIUS (Remote Authentication Dial-in User Service) e di un proxy.
ms.assetid: d0eb41cb-e9c0-4a60-aeac-77d1dd90a75b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d1f604d7cea69bcc8866176f612c76d2e6820bc4a00aa58d3760761ef59270b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118362307"
---
# <a name="network-policy-server"></a>Server dei criteri di rete

## <a name="purpose"></a>Scopo

Server dei criteri di rete è l'implementazione Microsoft di un server RADIUS (Remote Authentication Dial-in User Service) e di un proxy. È il successore del servizio di autenticazione Internet (IAS).

Come server RADIUS, Server dei criteri di rete esegue l'autenticazione, l'autorizzazione e l'accounting per le connessioni wireless, commutatore di autenticazione e connessione remota di accesso remoto e rete privata virtuale (VPN).

Server dei criteri di rete è anche un server dell'analizzatore dell'integrità per Protezione accesso alla rete. Server dei criteri di rete esegue l'autenticazione e l'autorizzazione dei tentativi di connessione di rete e, in base ai criteri di integrità del sistema configurati, valuta la conformità dell'integrità del computer e determina come limitare l'accesso alla rete o la comunicazione di un computer non conforme. Si tratta di una nuova funzionalità specifica solo di Server dei criteri di rete. IAS non lo supporta. Per un elenco completo delle nuove [funzionalità di Server dei criteri di](internet-authentication-service-vs-network-policy-server.md) rete, vedere Servizio di autenticazione Internet e Server dei criteri di rete.

Server dei criteri di rete include due set di API: API NPS Extensions e API SDO (Server Data Objects). Sia l'API NPS Extensions che l'API SDO sono supportate anche dal gruppo NPS, il servizio di autenticazione Internet.

L'API NPS Extensions può essere usata per estendere i metodi di autenticazione, autorizzazione e accounting offerti da Server dei criteri di rete e in precedenza da IAS.

L'API Server Data Objects può essere usata per modificare la configurazione dei criteri di rete in un computer che esegue Server dei criteri di rete o IAS.

> [!Note]  
> I criteri di rete in Server dei criteri di rete sono equivalenti ai criteri di accesso remoto in IAS.

 

## <a name="developer-audience"></a>Sviluppatori

L'API NPS Extensions è progettata per l'uso da parte dei programmatori che usano software di sviluppo C/C++. I programmatori devono avere familiarità con i concetti di rete e il protocollo RADIUS. RADIUS è documentato in [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt) e [RFC 2866.](https://www.ietf.org/rfc/rfc2866.txt)

L'API Server Data Objects è progettata per l'uso da parte dei programmatori che usano C/C++ o Visual Basic software di sviluppo. I programmatori devono avere familiarità [con il servizio](/windows/desktop/RRAS/remote-access-request-for-comments) di accesso remoto (RAS) e il protocollo RADIUS.

## <a name="run-time-requirements"></a>Requisiti di runtime

L'API NPS Extensions è supportata in Windows Server 2008 con l'installazione del Servizio Internet commerciale Microsoft (MCIS).

L'API Server Data Objects è supportata Windows Server 2008.

Server dei criteri di rete è disponibile Windows Server 2008 con l'installazione del Servizio Internet commerciale Microsoft (MCIS).

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[Overview](about-network-policy-server.md)
</dt> <dd>

Informazioni generali su RADIUS, IAS e Server dei criteri di rete.

</dd> <dt>

[API delle estensioni del server dei criteri di rete](ias-extensions.md)
</dt> <dd>

API per l'implementazione delle DLL di estensione usate per l'autenticazione, l'autorizzazione e l'accounting.

</dd> <dt>

[Server Data Objects API](server-data-objects.md)
</dt> <dd>

API per la gestione della configurazione dei criteri di rete.

</dd> <dt>

[SQL Programmabilità](sql-programmability.md)
</dt> <dd>

Esempi di stored procedure usate per la gestione della registrazione di Server dei criteri di rete (IAS).

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[TechNet: Server dei criteri di rete](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))
</dt> <dt>

[TechNet: Servizio di autenticazione Internet](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))
</dt> <dt>

[Protezione accesso alla rete](/windows/desktop/NAP/network-access-protection-start-page)
</dt> </dl>

 

 