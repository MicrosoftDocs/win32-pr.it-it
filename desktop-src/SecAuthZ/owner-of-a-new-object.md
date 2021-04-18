---
description: Un proprietario di oggetti dispone in modo implicito \_ dell'accesso alla DAC di scrittura all'oggetto. Questo significa che il proprietario può modificare l'elenco di controllo di accesso discrezionale (DACL) degli oggetti e, di conseguenza, può controllare l'accesso all'oggetto.
ms.assetid: 16144f38-3416-4594-b5e4-ca84fcbdddc9
title: Proprietario di un nuovo oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32f16124d84e17a075c78c676465ad753fcc12db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314727"
---
# <a name="owner-of-a-new-object"></a>Proprietario di un nuovo oggetto

Il proprietario di un oggetto ha in modo implicito l' \_ accesso all'applicazione livello dati di scrittura all'oggetto. Questo significa che il proprietario può modificare l'elenco di [*controllo di accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) dell'oggetto e, di conseguenza, può controllare l'accesso all'oggetto.

Il proprietario di un nuovo oggetto [*è l'*](/windows/desktop/SecGloss/p-gly) ID di [*sicurezza*](/windows/desktop/SecGloss/s-gly) (SID) [*predefinito del proprietario*](/windows/desktop/SecGloss/i-gly) del [*processo*](/windows/desktop/SecGloss/p-gly)di creazione. Per ottenere o impostare il proprietario predefinito in un [*token di accesso*](/windows/desktop/SecGloss/a-gly), chiamare la funzione [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) o [**SetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-settokeninformation) con la struttura del [**\_ proprietario del token**](/windows/desktop/api/Winnt/ns-winnt-token_owner) . Il sistema non consente di impostare il proprietario predefinito di un token su un SID non valido, ad esempio il SID dell'account di un altro utente.

Un processo con il \_ privilegio se Take \_ ownership abilitato può impostare se stesso come proprietario di un oggetto. Un processo con il \_ privilegio se Restore \_ Name abilitato o con il proprietario di scrittura \_ accede all'oggetto può impostare qualsiasi SID utente o gruppo valido come proprietario di un oggetto.

 

 
