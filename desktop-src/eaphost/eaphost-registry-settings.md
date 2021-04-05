---
title: Impostazioni del registro di sistema EAPHost
description: I valori del registro di sistema nelle chiavi del registro di sistema seguenti controllano gli aspetti della funzionalità di EAPHost.
ms.assetid: 2b954911-7c2e-4c86-b031-24632235a669
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67e4d258062ee2ae365924ecda22c2660ed5b742
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "103857842"
---
# <a name="eaphost-registry-settings"></a>Impostazioni del registro di sistema EAPHost

I valori del registro di sistema nelle chiavi del registro di sistema seguenti controllano gli aspetti della funzionalità di EAPHost.



| Sottochiave                                                                 | Descrizione                                                                                                                                                              |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [BypassNegotiation](bypassnegotiation.md)                             | Determina se viene eseguita la negoziazione delle funzionalità tra il server RAS e il client.<br/>                                                                              |
| [AssumePhase2Fragmentation](assumephase2fragmentation.md)             | Determina se il server RAS e il client presuppongono la frammentazione della fase 2.<br/>                                                                                         |
| [OverrideEAPCertificateSelection](overrideeapcertificateselection.md) | Determina se il client eseguirà l'override del comportamento predefinito per la selezione del certificato della smart card e fornirà all'utente più certificati tra cui scegliere.<br/> |
| [PeapServerUseAllPurposeCert](peapserveruseallpurposecert.md)         | Determina se per l'autenticazione PEAP vengono utilizzati certificati tutti gli scopi.<br/>                                                                                      |
| [PeapServerAcceptAllPurposeCert](peapserveracceptallpurposecert.md)   | Determina se per l'autenticazione PEAP sono accettati certificati tutti gli scopi.<br/>                                                                                  |
| [TlsServerUseAllPurposeCert](tlsserveruseallpurposecert.md)           | Determina se per l'autenticazione EAP-TLS vengono utilizzati certificati tutti gli scopi.<br/>                                                                                   |
| [TlsServerAcceptAllPurposeCert](tlsserveracceptallpurposecert.md)     | Determina se per l'autenticazione EAP-TLS sono accettati certificati tutti gli scopi.<br/>                                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sulle API EAPHost](eaphost-api-reference.md)
</dt> </dl>

 

 





