---
title: Token helper per i processi di trasferimento BITS
description: Token helper per i processi di trasferimento BITS
ms.assetid: f29f9870-e406-472b-9342-203def7453ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52925a6e0d5a9601e21848d514214bfb843f6246
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474195"
---
# <a name="helper-tokens-for-bits-transfer-jobs"></a>Token helper per i processi di trasferimento BITS

In Windows Vista, il servizio Servizio trasferimento intelligente in background (BITS) consente a un'applicazione di associare un singolo token di sicurezza a un processo di trasferimento BITS. Il processo di trasferimento BITS usa quindi questo token per l'autenticazione e per l'accesso alle risorse locali e remote.

In Windows 7, il servizio BITS associa un token aggiuntivo a un processo di trasferimento BITS. Il processo di trasferimento BITS può essere configurato con un token di sicurezza aggiuntivo, ovvero un token di rappresentazione creato da un'applicazione che chiama l'API COM BITS. Questo modello di token Helper consente alle applicazioni di usare contemporaneamente due token di sicurezza diversi per accedere ai file locali, ai certificati sul lato client, ai file remoti e ai proxy. Viene ad esempio creato un processo di trasferimento BITS che scrive i dati scaricati in una directory locale con privilegi, quindi presenta un'identità di dominio con diritti limitati al server HTTP e al server proxy.

Un'applicazione, in genere un servizio di Windows, specifica un token Helper usando la nuova interfaccia [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions). Questa interfaccia viene implementata dall'oggetto processo BITS. L'applicazione chiama [**Metodo ibackgroundcopyjob:: QueryInterface**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) per ottenere il puntatore di interfaccia. L'applicazione rappresenta l'identità helper e chiama [**IBitsTokenOptions:: SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) per passare il token al servizio BITS. Quindi, l'applicazione specifica le risorse a cui si applica il token passando un set di flag di bit usando [**IBitsTokenOptions:: SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags). L'applicazione cancella tutti i flag (usando nuovamente **SetHelperTokenFlags** ) per ripristinare il comportamento. Il servizio BITS archivia i flag di bit e il token nel processo di trasferimento BITS.

Quando il proprietario dei processi di trasferimento BITS si disconnette, il servizio BITS Elimina tutti i token Helper associati al processo di trasferimento. Se il trasferimento non è completo, il servizio BITS inserisce il processo in uno stato di errore con il token BG e il codice di errore **\_ \_ \_ richiesto** ed Elimina il token helper. L'applicazione client può aggiornare il token chiamando [**IBitsTokenOptions:: SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) e può riprendere il processo di trasferimento BITS. In alternativa, l'applicazione client può cancellare i flag del token helper utilizzando [**IBitsTokenOptions:: SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) e quindi riprendere il processo di trasferimento senza un token helper.

Analogamente, quando il proprietario di una sessione di servizi Terminal si disconnette, il servizio BITS deve rimuovere tutti i token Helper da tale sessione e collocare i processi di trasferimento interessati in uno stato di errore con il codice di errore del **\_ \_ token \_ BG e** .

Il modello di token Helper richiede una modifica ai criteri di controllo di accesso BITS. Le versioni precedenti di BITS implementavano i controlli di accesso in ogni chiamata al metodo. A partire da Windows 7, il controllo dell'accesso deve essere eseguito all'interno della chiamata [**Metodo ibackgroundcopyjob:: QueryInterface**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) ; in caso contrario, il token Helper potrebbe non avere accesso al processo di trasferimento.

> [!Note]  
> Nelle implementazioni precedenti è necessario che gli utenti BITS dispongano dei privilegi di amministratore per impostare i token helper. A partire da Windows 10, versione 1607, gli utenti BITS non amministratori possono usare [**IBitsTokenOptions:: SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) per impostare i token Helper non amministratori nei processi BITS di cui sono proprietari. Questa modifica consente agli utenti BITS non amministratori, ad esempio i servizi Downloader in background in esecuzione con l' [account NetworkService](/windows/desktop/Services/networkservice-account), di impostare i token helper.
>
> In particolare, l'implementazione è stata modificata per consentire agli utenti senza privilegi di amministratore di impostare i token helper, purché vengano soddisfatte le condizioni seguenti:
>
> -   durante la chiamata a [**Metodo ibackgroundcopyjob:: QueryInterface**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) , il SID del token thread's del chiamante corrisponde al SID dell'account utente del proprietario del processo e
> -   Quando viene chiamato [**IBitsTokenOptions:: SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) , il token Helper non dispone del SID amministratore (**Domain \_ alias \_ RID \_ Admins**) abilitato.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions)
</dt> </dl>

 

 