---
description: Viene illustrato come convalidare manualmente le credenziali di Schannel.
ms.assetid: 0229486a-5812-4a7e-98ad-446292997ee3
title: Convalida manuale di credenziali Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ec87b662cf9d3711c1ae729d2dd3b14ac5f79e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315868"
---
# <a name="manually-validating-schannel-credentials"></a>Convalida manuale di credenziali Schannel

Per impostazione predefinita, Schannel convalida il [*certificato del server*](../secgloss/s-gly.md) chiamando la funzione [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) . Tuttavia, se questa funzionalità è stata disabilitata usando il \_ \_ \_ \_ flag di convalida di ISC req Manual, è necessario convalidare il certificato fornito dal server che sta provando a stabilirne l'identità.

Per convalidare manualmente il certificato del server, è necessario prima ottenerlo. Usare la funzione [**QueryContextAttributes (generale)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) e specificare il \_ valore dell' \_ attributo di contesto del certificato remoto SECPKG attr \_ \_ . Questo attributo restituisce una struttura del [**\_ contesto**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) del certificato contenente il certificato fornito dal server. Questo certificato viene chiamato certificato foglia perché è l'ultimo certificato nella catena di certificati ed è più lontano dal [*certificato radice*](../secgloss/r-gly.md).

Utilizzando il certificato foglia è necessario verificare quanto segue:

-   La catena di certificati è completa e la radice è un certificato di un' [*autorità di certificazione*](../secgloss/c-gly.md) (CA) attendibile.
-   L'ora corrente non è oltre le date di inizio e di fine per ogni certificato nella catena di certificati.
-   Nessuno dei certificati nella catena di certificati è stato revocato.
-   La profondità del certificato foglia non è maggiore della profondità massima consentita specificata nell'estensione del certificato. Questo controllo è necessario solo se è stata specificata una profondità.
-   L'utilizzo del certificato è corretto. ad esempio, un [*certificato client*](../secgloss/c-gly.md) non deve essere utilizzato per autenticare un server.
-   Per l'autenticazione server, l'identità del server contenuta nel certificato foglia del server corrisponde al server che il client sta tentando di contattare. In genere, il client corrisponderà a un elemento nel campo del nome del soggetto del certificato all'indirizzo IP o al nome DNS del server.

 

 
