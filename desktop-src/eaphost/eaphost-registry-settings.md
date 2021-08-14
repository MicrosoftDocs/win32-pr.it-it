---
title: Registro EAPHost Impostazioni
description: I valori del Registro di sistema nelle chiavi del Registro di sistema seguenti controllano gli aspetti delle funzionalità di EAPHost.
ms.assetid: 2b954911-7c2e-4c86-b031-24632235a669
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec08a7428dac4c68044b0491e084574c6ff3d006fcf06f59912754c5a9f93833
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482981"
---
# <a name="eaphost-registry-settings"></a>Registro EAPHost Impostazioni

I valori del Registro di sistema nelle chiavi del Registro di sistema seguenti controllano gli aspetti delle funzionalità di EAPHost.



| Sottochiave                                                                 | Descrizione                                                                                                                                                              |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [BypassNegotiation](bypassnegotiation.md)                             | Determina se viene eseguita la negoziazione delle funzionalità tra il server RAS e il client.<br/>                                                                              |
| [AssumePhase2Fragmentation](assumephase2fragmentation.md)             | Determina se il server RAS e il client presuppongono la frammentazione della fase 2.<br/>                                                                                         |
| [OverrideEAPCertificateSelection](overrideeapcertificateselection.md) | Determina se il client eseguirà l'override del comportamento smart card di selezione del certificato predefinito e fornirà all'utente più certificati tra cui scegliere.<br/> |
| [PeapServerUseAllPurposeCert](peapserveruseallpurposecert.md)         | Determina se per l'autenticazione PEAP vengono utilizzati certificati per tutti gli scopi.<br/>                                                                                      |
| [PeapServerAcceptAllPurposeCert](peapserveracceptallpurposecert.md)   | Determina se i certificati per tutti gli scopi vengono accettati per l'autenticazione PEAP.<br/>                                                                                  |
| [TlsServerUseAllPurposeCert](tlsserveruseallpurposecert.md)           | Determina se vengono usati certificati per tutti gli scopi per l'autenticazione EAP-TLS.<br/>                                                                                   |
| [TlsServerAcceptAllPurposeCert](tlsserveracceptallpurposecert.md)     | Determina se i certificati per tutti gli scopi vengono accettati per l'autenticazione EAP-TLS.<br/>                                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sulle API EAPHost](eaphost-api-reference.md)
</dt> </dl>

 

 





