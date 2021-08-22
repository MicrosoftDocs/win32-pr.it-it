---
title: Token helper per i processi di trasferimento BITS
description: Token helper per i processi di trasferimento BITS
ms.assetid: f29f9870-e406-472b-9342-203def7453ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79a22708b11bd07165166f647454c05663d59f6cfeddde659a9bb5903d5a9606
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528681"
---
# <a name="helper-tokens-for-bits-transfer-jobs"></a>Token helper per i processi di trasferimento BITS

In Windows Vista, il servizio Servizio trasferimento intelligente in background (BITS) consente a un'applicazione di associare un singolo token di sicurezza a un processo di trasferimento BITS. Il processo di trasferimento BITS usa quindi questo token per l'autenticazione e per l'accesso alle risorse locali e remote.

Nella Windows 7, il servizio BITS associa un token aggiuntivo a un processo di trasferimento BITS. Il processo di trasferimento BITS può essere configurato con un token di sicurezza aggiuntivo, ovvero un token di rappresentazione creato da un'applicazione che chiama l'API COM BITS. Questo modello di token helper consente alle applicazioni di usare contemporaneamente due token di sicurezza diversi per accedere a file locali, certificati lato client, file remoti e proxy. Ad esempio, viene creato un processo di trasferimento BITS che scrive i dati scaricati in una directory locale con privilegi e quindi presenta un'identità di dominio con diritti limitati al server HTTP e al server proxy.

Un'applicazione, in Windows servizio, specifica un token helper usando la nuova [**interfaccia IBitsTokenOptions.**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions) Questa interfaccia viene implementata dall'oggetto processo BITS. L'applicazione chiama [**IBackgroundCopyJob::QueryInterface per**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) ottenere il puntatore di interfaccia. L'applicazione rappresenta l'identità helper e chiama [**IBitsTokenOptions::SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) per passare il token al servizio BITS. L'applicazione specifica quindi le risorse a cui si applica il token passando un set di flag di bit [**usando IBitsTokenOptions::SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags). L'applicazione cancella tutti i flag (usando **di nuovo SetHelperTokenFlags)** per ripristinare il comportamento. Il servizio BITS archivia i flag di bit e il token nel processo di trasferimento BITS.

Quando il proprietario dei processi di trasferimento BITS si disconnette, il servizio BITS elimina tutti i token helper associati al processo di trasferimento. Se il trasferimento non è completo, il servizio BITS inserisce il processo in uno stato di errore con il codice di errore **BG \_ E TOKEN \_ \_ REQUIRED** ed elimina il token helper. L'applicazione client può aggiornare il token chiamando [**IBitsTokenOptions::SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) e può quindi riprendere il processo di trasferimento BITS. In alternativa, l'applicazione client può cancellare i flag del token helper usando [**IBitsTokenOptions::SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) e quindi riprendere il processo di trasferimento senza un token helper.

Analogamente, quando il proprietario di una sessione di Servizi terminal si disconnette, il servizio BITS deve rimuovere tutti i token helper da tale sessione e inserire i processi di trasferimento interessati in uno stato di errore con il codice di errore **BG \_ E TOKEN \_ \_ REQUIRED.**

Il modello di token helper richiede una modifica ai criteri di controllo di accesso BITS. Le versioni precedenti di BITS implementano i controlli di accesso a ogni chiamata al metodo. A partire Windows 7, il controllo di accesso deve essere eseguito all'interno della chiamata [**IBackgroundCopyJob::QueryInterface;**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) In caso contrario, il token helper potrebbe non avere accesso al processo di trasferimento.

> [!Note]  
> Le implementazioni precedenti richiedeva in effetti che gli utenti BITS dispone di privilegi di amministratore per impostare i token helper. A partire da Windows 10 versione 1607, gli utenti BITS non amministratori possono usare [**IBitsTokenOptions::SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) per impostare token helper non di amministratore nei processi BITS di cui sono proprietari. Questa modifica consente agli utenti BITS non amministratori ,ad esempio i servizi downloader in background in esecuzione con [l'account NetworkService](/windows/desktop/Services/networkservice-account), di impostare i token helper.
>
> In particolare, l'implementazione è stata modificata per consentire agli utenti senza privilegi di amministratore di impostare i token helper, purché siano soddisfatte le condizioni seguenti:
>
> -   durante la chiamata [**a IBackgroundCopyJob::QueryInterface,**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) il SID del token del thread del chiamante corrisponde al SID dell'account utente del proprietario del processo e
> -   Quando [**viene chiamato IBitsTokenOptions::SetHelperToken,**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) per il token helper non è abilitato il SID dell'amministratore (**DOMAIN ALIAS RID \_ \_ \_ ADMINS).**

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions)
</dt> </dl>

 

 