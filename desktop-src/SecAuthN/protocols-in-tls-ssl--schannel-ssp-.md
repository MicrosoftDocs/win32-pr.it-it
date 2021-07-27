---
description: SSP schannel implementa le versioni dei protocolli TLS, DTLS e SSL. Versioni Windows supportano versioni del protocollo diverse.
ms.assetid: FF716A4E-ABF2-4773-9588-9D200945A866
title: Protocolli in TLS/SSL (SSP Schannel)
ms.topic: article
ms.date: 01/20/2021
ms.custom: contperf-fy21q3
ms.openlocfilehash: 0aa3c3900a422a1460a2163043fb736e590ca2fe
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436266"
---
# <a name="protocols-in-tlsssl-schannel-ssp"></a>Protocolli in TLS/SSL (SSP Schannel)

SSP Schannel implementa le versioni dei protocolli TLS, DTLS e SSL. Versioni Windows supportano versioni del protocollo diverse.

## <a name="tls-protocol-version-support"></a>Supporto della versione del protocollo TLS

La tabella seguente mostra il supporto del provider Microsoft Schannel per le versioni del protocollo TLS.

> [!TIP]
> Potrebbe essere necessario scorrere orizzontalmente per visualizzare tutte le colonne della tabella.

| Sistema operativo Windows | TLS 1.0 Client | TLS 1.0 Server | TLS 1.1 Client | TLS 1.1 Server | TLS 1.2 Client | TLS 1.2 Server | TLS 1.3 Client | TLS 1.3 Server |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| Windows Vista/Windows Server 2008                     | Attivato        | Attivato        | Non supportato  | Non supportato  | Non supportato  | Non supportato  | Non supportato  | Non supportato  |
| Windows Server 2008 con Service Pack 2 (SP2)         | Attivato        | Attivato        | Disabled       | Disabled       | Disabled       | Disabled       | Non supportato  | Non supportato  |
| Windows 7/Windows Server 2008 R2                      | Attivato        | Attivato        | Disabled       | Disabled       | Disabled       | Disabled       | Non supportato  | Non supportato  |
| Windows 8/Windows Server 2012                         | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Non supportato  | Non supportato  |
| Windows 8.1/Windows Server 2012 R2                    | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Non supportato  | Non supportato  |
| Windows 10, versione 1507                              | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Non supportato  | Non supportato  |
| Windows 10 versione 1511                              | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Non supportato  | Non supportato  |
| Windows 10, versione 1607/Windows Server 2016 Standard | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Non supportato  | Non supportato  |
| Windows 10 versione 1703                              | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Non supportato  | Non supportato  |
| Windows 10, versione 1709                              | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Non supportato  | Non supportato  |
| Windows 10, versione 1803                              | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Non supportato  | Non supportato  |
| Windows 10, versione 1809//Windows Server 2019         | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Non supportato  | Non supportato  |
| Windows 10, versione 1903                              | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Non supportato  | Non supportato  |
| Windows 10, versione 1909                              | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Non supportato  | Non supportato  |
| Windows 10, versione 2004                              | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Non supportato  | Non supportato  |
| Windows 10, versione 20H2                              | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Non supportato  | Non supportato  |
| Windows 10, versione 21H1                              | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Non supportato  | Non supportato  |
| Windows Server 2022                                   | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        |


## <a name="dtls-protocol-version-support"></a>Supporto della versione del protocollo DTLS

Di seguito è elencato il supporto del provider Microsoft Schannel per le versioni del protocollo DTLS.

*Suggerimento: potrebbe essere necessario scorrere orizzontalmente per visualizzare tutte le colonne in questa tabella:*

| Sistema operativo Windows                                            | DTLS 1.0 Client | DTLS 1.0 Server | DTLS 1.2 Client | DTLS 1.2 Server |
|-------------------------------------------------------|-----------------|-----------------|-----------------|-----------------|
| Windows Vista/Windows Server 2008                     | Non supportato   | Non supportato   | Non supportato   | Non supportato   |
| Windows Server 2008 con SP2                          | Non supportato   | Non supportato   | Non supportato   | Non supportato   |
| Windows 7/Windows Server 2008 R2                      | Attivato         | Attivato         | Non supportato   | Non supportato   |
| Windows 8/Windows Server 2012                         | Attivato         | Attivato         | Non supportato   | Non supportato   |
| Windows 8.1/Windows Server 2012 R2                    | Attivato         | Attivato         | Non supportato   | Non supportato   |
| Windows 10, versione 1507                              | Attivato         | Attivato         | Non supportato   | Non supportato   |
| Windows 10 versione 1511                              | Attivato         | Attivato         | Non supportato   | Non supportato   |
| Windows 10, versione 1607/Windows Server 2016 Standard | Attivato         | Attivato         | Attivato         | Attivato         |
| Windows 10 versione 1703                              | Attivato         | Attivato         | Attivato         | Attivato         |
| Windows 10, versione 1803                              | Attivato         | Attivato         | Attivato         | Attivato         |
| Windows 10, versione 1809                              | Attivato         | Attivato         | Attivato         | Attivato         |
| Windows 10, versione 1903                              | Attivato         | Attivato         | Attivato         | Attivato         |
| Windows 10, versione 1909                              | Attivato         | Attivato         | Attivato         | Attivato         |
| Windows 10, versione 2004                              | Attivato         | Attivato         | Attivato         | Attivato         |
| Windows 10, versione 20H2                              | Attivato         | Attivato         | Attivato         | Attivato         |
| Windows 10, versione 21H1                              | Attivato         | Attivato         | Attivato         | Attivato         |

## <a name="pre-tls-standard-protocols-support"></a>Supporto dei protocolli standard pre-TLS

Di seguito è elencato il supporto del provider Microsoft Schannel per i protocolli standard pre-TLS:

*Suggerimento: potrebbe essere necessario scorrere orizzontalmente per visualizzare tutte le colonne in questa tabella:*

| Sistema operativo Windows                                            | PCT 1.0       | SSL2 Client   | SSL2 Server   | SSL3 Client | SSL3 Server |
|-------------------------------------------------------|---------------|---------------|---------------|-------------|-------------|
| Windows Vista/Windows Server 2008                     | Non supportato | Disabled      | Attivato       | Attivato     | Attivato     |
| Windows Server 2008 con SP2                          | Non supportato | Disabled      | Attivato       | Attivato     | Attivato     |
| Windows 7/Windows Server 2008 R2                      | Non supportato | Disabled      | Attivato       | Attivato     | Attivato     |
| Windows 8/Windows Server 2012                         | Non supportato | Disabled      | Disabled      | Attivato     | Attivato     |
| Windows 8.1/Windows Server 2012 R2                    | Non supportato | Disabled      | Disabled      | Attivato     | Attivato     |
| Windows 10, versione 1507                              | Non supportato | Disabled      | Disabled      | Attivato     | Attivato     |
| Windows 10 versione 1511                              | Non supportato | Disabled      | Disabled      | Attivato     | Attivato     |
| Windows 10, versione 1607/Windows Server 2016 Standard | Non supportato | Non supportato | Non supportato | Disabled    | Disabled    |
| Windows 10 versione 1703                              | Non supportato | Non supportato | Non supportato | Disabled    | Disabled    |
| Windows 10, versione 1803                              | Non supportato | Non supportato | Non supportato | Disabled    | Disabled    |
| Windows 10, versione 1809                              | Non supportato | Non supportato | Non supportato | Disabled    | Disabled    |
| Windows 10, versione 1903                              | Non supportato | Non supportato | Non supportato | Disabled    | Disabled    |
| Windows 10, versione 1909                              | Non supportato | Non supportato | Non supportato | Disabled    | Disabled    |
| Windows 10, versione 2004                              | Non supportato | Non supportato | Non supportato | Disabled    | Disabled    |
| Windows 10, versione 20H2                              | Non supportato | Non supportato | Non supportato | Disabled    | Disabled    |
| Windows 10, versione 21H1                              | Non supportato | Non supportato | Non supportato | Disabled    | Disabled    |


> [!IMPORTANT]
> A partire da Windows 10 versione 1607 e Windows Server 2016, SSL 2.0 è stato rimosso e non è più supportato.

> [!TIP]  
> Tutte le versioni Windows accettano un messaggio "ClientHello" in formato unificato anche quando SSL versione 2 è disabilitato o non è più supportato.
