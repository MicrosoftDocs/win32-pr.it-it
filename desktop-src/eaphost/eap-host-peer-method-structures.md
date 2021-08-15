---
title: Strutture del metodo peer EAPHost
description: Informazioni sulle strutture api del metodo peer EAPHost, ad esempio EapCertificateCredential ed EapSimCredential.
ms.assetid: 546ef715-8f51-4f5a-a569-8bf64d52de85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56582c920536cabd294680df265d16ae51d8b4bd951f8efcdb988de677a2a2ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118498620"
---
# <a name="eaphost-peer-method-structures"></a>Strutture del metodo peer EAPHost

Le strutture dell'API EAPHost Peer Method sono le seguenti.



| Struttura                                                              | Descrizione                                                                                                                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EapCertificateCredential**](/windows/desktop/api/eaptypes/ns-eaptypes-eapcertificatecredential)           | Contiene informazioni sul certificato utilizzato dal metodo EAP per l'autenticazione.                                                                                                            |
| [**EapCredential**](/windows/desktop/api/eaptypes/ns-eaptypes-eapcredential)                                 | Contiene informazioni sul tipo di credenziali e sulle credenziali appropriate. Viene passato come input all'API [**EapPeerGetConfigBlobAndUserBlob.**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetconfigblobanduserblob) |
| [**ROUTINE DEL METODO PEER EAP \_ \_ \_**](/windows/desktop/api/eapmethodpeerapis/ns-eapmethodpeerapis-eap_peer_method_routines)        | Contiene un set di puntatori a funzione alle API del metodo peer EAPHost.                                                                                                                               |
| [**EapPeerMethodOutput**](/windows/win32/api/eapauthenticatoractiondefine/ns-eapauthenticatoractiondefine-eappeermethodoutput)                     | Contiene le informazioni sull'azione restituite da un metodo peer EAP.                                                                                                                                    |
| [**EapPeerMethodResult**](/windows/win32/api/eapmethodpeerapis/ns-eapmethodpeerapis-eappeermethodresult)                     | Contiene i dati dei risultati generati da un metodo EAP durante l'autenticazione.                                                                                                                             |
| [**EapSimCredential**](/windows/desktop/api/eaptypes/ns-eaptypes-eapsimcredential)                           | Contiene informazioni sulla SIM usata dal metodo EAP per l'autenticazione.                                                                                                              |
| [**EapUsernamePasswordCredential**](/windows/desktop/api/eaptypes/ns-eaptypes-eapusernamepasswordcredential) | Contiene il nome utente e la password utilizzati dal metodo EAP per l'autenticazione dell'utente.                                                                                                     |



 

 

 




