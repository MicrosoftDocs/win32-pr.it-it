---
title: Strutture del metodo peer EAPHost
description: Informazioni sulle strutture API del metodo peer EAPHost, ad esempio EapCertificateCredential e EapSimCredential.
ms.assetid: 546ef715-8f51-4f5a-a569-8bf64d52de85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73dab0d2bcd5bf1a6dc48ab01fa12c24785cd92a
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300468"
---
# <a name="eaphost-peer-method-structures"></a>Strutture del metodo peer EAPHost

Di seguito sono riportate le strutture API del metodo peer EAPHost.



| Struttura                                                              | Descrizione                                                                                                                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EapCertificateCredential**](/windows/desktop/api/eaptypes/ns-eaptypes-eapcertificatecredential)           | Contiene informazioni sul certificato utilizzato dal metodo EAP per l'autenticazione.                                                                                                            |
| [**EapCredential**](/windows/desktop/api/eaptypes/ns-eaptypes-eapcredential)                                 | Contiene informazioni sul tipo di credenziali e le credenziali appropriate. Viene passato come input per l'API [**EapPeerGetConfigBlobAndUserBlob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetconfigblobanduserblob) . |
| [**\_routine del \_ metodo \_ peer EAP**](/windows/desktop/api/eapmethodpeerapis/ns-eapmethodpeerapis-eap_peer_method_routines)        | Contiene un set di puntatori a funzione per le API del metodo peer EAPHost.                                                                                                                               |
| [**EapPeerMethodOutput**](/windows/win32/api/eapauthenticatoractiondefine/ns-eapauthenticatoractiondefine-eappeermethodoutput)                     | Contiene le informazioni sull'azione restituite da un metodo peer EAP.                                                                                                                                    |
| [**EapPeerMethodResult**](/windows/win32/api/eapmethodpeerapis/ns-eapmethodpeerapis-eappeermethodresult)                     | Contiene i dati dei risultati generati da un metodo EAP durante l'autenticazione.                                                                                                                             |
| [**EapSimCredential**](/windows/desktop/api/eaptypes/ns-eaptypes-eapsimcredential)                           | Contiene informazioni sulla SIM utilizzata dal metodo EAP per l'autenticazione.                                                                                                              |
| [**EapUsernamePasswordCredential**](/windows/desktop/api/eaptypes/ns-eaptypes-eapusernamepasswordcredential) | Contiene il nome utente e la password utilizzati dal metodo EAP per l'autenticazione dell'utente.                                                                                                     |



 

 

 




