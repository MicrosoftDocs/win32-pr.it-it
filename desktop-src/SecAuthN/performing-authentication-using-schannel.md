---
description: Tutti i protocolli Schannel richiedono al server di fornire un certificato da un'autorità di certificazione (CA) attendibile come prova della propria identità.
ms.assetid: 060981e0-b52a-4cc2-bfd2-4cf24f921f16
title: Esecuzione dell'autenticazione tramite Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6c2a5099dd29d6b3b342b583e37e2dc98187f5011c7cc75b75432924fba9ea1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921020"
---
# <a name="performing-authentication-using-schannel"></a>Esecuzione dell'autenticazione tramite Schannel

Tutti i protocolli Schannel richiedono al server di fornire [*un*](../secgloss/c-gly.md) certificato da un'autorità di [*certificazione*](../secgloss/c-gly.md) (CA) attendibile come prova della propria identità. Questo processo è denominato autenticazione server. L'autenticazione client, in cui il client fornisce la prova della propria identità, è facoltativa e può essere richiesta dal server in qualsiasi momento.

## <a name="authenticating-the-server"></a>Autenticazione del server

Il comportamento predefinito di Schannel è l'uso della [](../secgloss/i-gly.md) [**funzione WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) per verificare l'integrità e la proprietà del [*certificato server.*](../secgloss/s-gly.md) Per disabilitare questa funzionalità, specificare ISC REQ MANUAL CRED VALIDATION quando si \_ \_ chiama la funzione \_ \_ [**InitializeSecurityContext (Schannel).**](./initializesecuritycontext--schannel.md) Per altre informazioni, vedere [Convalida manuale delle credenziali Schannel.](manually-validating-schannel-credentials.md)

## <a name="authenticating-the-client"></a>Autenticazione del client

Schannel non convalida i certificati del client. il server deve eseguire questa autenticazione manualmente. In genere, il server controlla l'identità del client in un database contenente informazioni sull'account utente. Per i server che devono ottenere l'account di un client usando un certificato, vedere [Mapping dei certificati](mapping-certificates.md).

Quando il server richiede l'autenticazione client, il client deve inviare al server uno dei relativi certificati. Per impostazione predefinita, Schannel, senza alcuna notifica al client, tenterà di individuare un certificato [*client*](../secgloss/c-gly.md) e inviarlo al server. Per disabilitare questa funzionalità, i client specificano ISC \_ REQ \_ USE \_ SUPPLIED CREDS quando chiamano la funzione \_ [**InitializeSecurityContext (Schannel).**](./initializesecuritycontext--schannel.md) Quando si specifica questo flag, Schannel restituirà SEC I INCOMPLETE CREDENTIALS al client quando il server richiede l'autenticazione e il client non ha precedentemente \_ \_ fornito un \_ certificato.

 

 
