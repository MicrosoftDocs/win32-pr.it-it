---
description: Tutti i protocolli Schannel richiedono che il server fornisca un certificato da un'autorità di certificazione attendibile (CA) come prova della propria identità.
ms.assetid: 060981e0-b52a-4cc2-bfd2-4cf24f921f16
title: Esecuzione dell'autenticazione con Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a37b8dedf07680286288234c7ca4422f44c2c3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312822"
---
# <a name="performing-authentication-using-schannel"></a>Esecuzione dell'autenticazione con Schannel

Tutti i protocolli Schannel richiedono che il server fornisca un [*certificato*](../secgloss/c-gly.md) da un' [*autorità di certificazione*](../secgloss/c-gly.md) attendibile (CA) come prova della propria identità. Questo processo è denominato autenticazione server. L'autenticazione client, in cui il client fornisce la prova dell'identità, è facoltativa e può essere richiesta dal server in qualsiasi momento.

## <a name="authenticating-the-server"></a>Autenticazione del server

Il comportamento predefinito di Schannel consiste nell'utilizzare la funzione [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) per verificare l' [*integrità*](../secgloss/i-gly.md) e la proprietà del [*certificato del server*](../secgloss/s-gly.md). Per disabilitare questa funzionalità, specificare \_ \_ \_ la convalida del cred manuale di ISC req quando si \_ chiama la funzione [**InitializeSecurityContext (Schannel)**](./initializesecuritycontext--schannel.md) . Per altre informazioni, vedere [convalidare manualmente le credenziali Schannel](manually-validating-schannel-credentials.md).

## <a name="authenticating-the-client"></a>Autenticazione del client

Schannel non convalida i certificati del client. il server deve eseguire questa autenticazione manualmente. In genere, il server verificherà l'identità del client in un database contenente le informazioni sull'account utente. Per i server che devono ottenere un account client usando un certificato, vedere [mapping dei certificati](mapping-certificates.md).

Quando il server richiede l'autenticazione client, il client deve inviare al server uno dei certificati. Per impostazione predefinita, Schannel non invierà alcuna notifica al client, tenta di individuare un [*certificato client*](../secgloss/c-gly.md) e di inviarlo al server. Per disabilitare questa funzionalità, i client specificano \_ \_ l'uso di \_ \_ credenziali di ISC quando chiamano la funzione [**InitializeSecurityContext (Schannel)**](./initializesecuritycontext--schannel.md) . Quando si specifica questo flag, Schannel restituirà \_ \_ \_ al client le credenziali incomplete al secondo quando il server richiede l'autenticazione e il client non ha fornito in precedenza un certificato.

 

 
