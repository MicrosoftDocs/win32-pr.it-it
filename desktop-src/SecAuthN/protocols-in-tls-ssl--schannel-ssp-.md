---
description: SSP Schannel implementa le versioni dei protocolli TLS, DTLS e SSL. Diverse versioni di Windows supportano diverse versioni del protocollo.
ms.assetid: FF716A4E-ABF2-4773-9588-9D200945A866
title: Protocolli in TLS/SSL (SSP Schannel)
ms.topic: article
ms.date: 01/20/2021
ms.custom: contperf-fy21q3
ms.openlocfilehash: 844d75230119b747f77697f67ddecec5f64ce7cf
ms.sourcegitcommit: 07b756a2f350efa5cfd5024a723ef392274ac3d9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/17/2021
ms.locfileid: "103968842"
---
# <a name="protocols-in-tlsssl-schannel-ssp"></a>Protocolli in TLS/SSL (SSP Schannel)

SSP Schannel implementa le versioni dei protocolli TLS, DTLS e SSL. Diverse versioni di Windows supportano diverse versioni del protocollo.

## <a name="tls-protocol-version-support"></a>Supporto della versione del protocollo TLS

La tabella seguente mostra il supporto del provider Microsoft Schannel per le versioni del protocollo TLS.

*Suggerimento: potrebbe essere necessario scorrere orizzontalmente per visualizzare tutte le colonne della tabella:*

| Sistema operativo Windows | Client TLS 1,0 | Server TLS 1,0 | Client TLS 1,1 | Server TLS 1,1 | Client TLS 1,2 | Server TLS 1,2 | Client TLS 1,3 | Server TLS 1,3 |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| Windows Vista/Windows Server 2008                     | Attivato        | Attivato        | Non supportato  | Non supportato  | Non supportato  | Non supportato  | Non supportato  | Non supportato  |
| Windows Server 2008 con Service Pack 2 (SP2)         | Attivato        | Attivato        | Disabled       | Disabled       | Disabled       | Disabled       | Non supportato  | Non supportato  |
| Windows 7/Windows Server 2008 R2                      | Attivato        | Attivato        | Disabled       | Disabled       | Disabled       | Disabled       | Non supportato  | Non supportato  |
| Windows 8/Windows Server 2012                         | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Non supportato  | Non supportato  |
| Windows 8.1/Windows Server 2012 R2                    | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Non supportato  | Non supportato  |
| Windows 10 versione 1507                              | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Non supportato  | Non supportato  |
| Windows 10 versione 1511                              | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Non supportato  | Non supportato  |
| Windows 10, versione 1607/Windows Server 2016 standard | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Non supportato  | Non supportato  |
| Windows 10 versione 1703                              | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Non supportato  | Non supportato  |
| Windows 10, versione 1709                              | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Non supportato  | Non supportato  |
| Windows 10, versione 1803                              | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Non supportato  | Non supportato  |
| Windows 10, versione 1809                              | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Non supportato  | Non supportato  |
| Windows 10, versione 1903                              | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Non supportato  | Non supportato  |
| Windows 10, versione 1909                              | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Non supportato  | Non supportato  | 
| Windows 10, versione 2004                              | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Non supportato  | Non supportato  |
| Windows 10, versione 20H2                              | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Non supportato  | Non supportato  |
| Windows Server 2022                              | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        | Attivato        |


## <a name="dtls-protocol-version-support"></a>Supporto della versione del protocollo DTLS

Di seguito è elencato il supporto del provider Microsoft Schannel per le versioni del protocollo DTLS.

*Suggerimento: potrebbe essere necessario scorrere orizzontalmente per visualizzare tutte le colonne della tabella:*

| Sistema operativo Windows                                            | Client DTLS 1,0 | Server DTLS 1,0 | Client DTLS 1,2 | Server DTLS 1,2 |
|-------------------------------------------------------|-----------------|-----------------|-----------------|-----------------|
| Windows Vista/Windows Server 2008                     | Non supportato   | Non supportato   | Non supportato   | Non supportato   |
| Windows Server 2008 con SP2                          | Non supportato   | Non supportato   | Non supportato   | Non supportato   |
| Windows 7/Windows Server 2008 R2                      | Attivato         | Attivato         | Non supportato   | Non supportato   |
| Windows 8/Windows Server 2012                         | Attivato         | Attivato         | Non supportato   | Non supportato   |
| Windows 8.1/Windows Server 2012 R2                    | Attivato         | Attivato         | Non supportato   | Non supportato   |
| Windows 10 versione 1507                              | Attivato         | Attivato         | Non supportato   | Non supportato   |
| Windows 10 versione 1511                              | Attivato         | Attivato         | Non supportato   | Non supportato   |
| Windows 10, versione 1607/Windows Server 2016 standard | Attivato         | Attivato         | Attivato         | Attivato         |
| Windows 10 versione 1703                              | Attivato         | Attivato         | Attivato         | Attivato         |
| Windows 10, versione 1803                              | Attivato         | Attivato         | Attivato         | Attivato         |
| Windows 10, versione 1809                              | Attivato         | Attivato         | Attivato         | Attivato         |
| Windows 10, versione 1903                              | Attivato         | Attivato         | Attivato         | Attivato         |
| Windows 10, versione 1909                              | Attivato         | Attivato         | Attivato         | Attivato         |
| Windows 10, versione 2004                              | Attivato         | Attivato         | Attivato         | Attivato         |
| Windows 10, versione 20H2                              | Attivato         | Attivato         | Attivato         | Attivato         |
| Windows 10, versione 21H1                              | Attivato         | Attivato         | Attivato         | Attivato         |

## <a name="pre-tls-standard-protocols-support"></a>Supporto per protocolli standard pre-TLS

Di seguito è elencato il supporto del provider Microsoft Schannel per i protocolli standard pre-TLS:

*Suggerimento: potrebbe essere necessario scorrere orizzontalmente per visualizzare tutte le colonne della tabella:*

| Sistema operativo Windows                                            | PCT 1.0       | Client SSL2   | Server SSL2   | Client SSL3 | Server SSL3 |
|-------------------------------------------------------|---------------|---------------|---------------|-------------|-------------|
| Windows Vista/Windows Server 2008                     | Non supportato | Disabled      | Attivato       | Attivato     | Attivato     |
| Windows Server 2008 con SP2                          | Non supportato | Disabled      | Attivato       | Attivato     | Attivato     |
| Windows 7/Windows Server 2008 R2                      | Non supportato | Disabled      | Attivato       | Attivato     | Attivato     |
| Windows 8/Windows Server 2012                         | Non supportato | Disabled      | Disabled      | Attivato     | Attivato     |
| Windows 8.1/Windows Server 2012 R2                    | Non supportato | Disabled      | Disabled      | Attivato     | Attivato     |
| Windows 10 versione 1507                              | Non supportato | Disabled      | Disabled      | Attivato     | Attivato     |
| Windows 10 versione 1511                              | Non supportato | Disabled      | Disabled      | Attivato     | Attivato     |
| Windows 10, versione 1607/Windows Server 2016 standard | Non supportato | Non supportato | Non supportato | Disabled    | Disabled    |
| Windows 10 versione 1703                              | Non supportato | Non supportato | Non supportato | Disabled    | Disabled    |
| Windows 10, versione 1803                              | Non supportato | Non supportato | Non supportato | Disabled    | Disabled    |
| Windows 10, versione 1809                              | Non supportato | Non supportato | Non supportato | Disabled    | Disabled    |
| Windows 10, versione 1903                              | Non supportato | Non supportato | Non supportato | Disabled    | Disabled    |
| Windows 10, versione 1909                              | Non supportato | Non supportato | Non supportato | Disabled    | Disabled    |
| Windows 10, versione 2004                              | Non supportato | Non supportato | Non supportato | Disabled    | Disabled    |
| Windows 10, versione 20H2                              | Non supportato | Non supportato | Non supportato | Disabled    | Disabled    |
| Windows 10, versione 20H1                              | Non supportato | Non supportato | Non supportato | Disabled    | Disabled    |


> [!IMPORTANT]
> A partire da Windows 10, versione 1607 e Windows Server 2016, SSL 2,0 è stato rimosso e non è più supportato.

> [!TIP]  
> Tutte le versioni di Windows accetteranno un messaggio "ClientHello" in formato unificato anche quando SSL versione 2 è disabilitato o non è più supportato.
