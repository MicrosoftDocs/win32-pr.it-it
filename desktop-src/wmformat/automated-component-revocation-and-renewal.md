---
title: Revoca e rinnovo automatici dei componenti
description: Revoca e rinnovo automatici dei componenti
ms.assetid: be4899d7-1d87-4450-8c0e-75cf112ca66a
keywords:
- Windows Media Format SDK, revoca e rinnovo automatici
- Windows Media Format SDK, revoca
- Windows Media Format SDK, rinnovo
- Digital Rights Management (DRM), revoca e rinnovo automatici
- DRM (Digital Rights Management), revoca e rinnovo automatici
- Digital Rights Management (DRM), revoca
- DRM (Digital Rights Management), revoca
- Digital Rights Management (DRM), rinnovo
- DRM (Digital Rights Management), rinnovo
- API estese del client DRM, revoca e rinnovo automatici
- API estese client, revoca e rinnovo automatici
- API estese del client DRM, revoca
- API estese client, revoca
- API estese del client DRM, rinnovo
- API estese client, rinnovo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b9046d04d8ca7a138a06cba4d26cd82bc5a12b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338630"
---
# <a name="automated-component-revocation-and-renewal"></a>Revoca e rinnovo automatici dei componenti

Le applicazioni software o i componenti considerati compromessi possono essere revocati da Microsoft. L'API estesa client Windows Media Format fornisce un meccanismo per la revoca e il rinnovo automatici dei componenti.

I componenti revocati sono elencati in un elenco di revoche di certificati, pubblicato da Microsoft. Quando un componente viene revocato, il certificato viene aggiunto all'elenco di revoche di certificati e il BLOB delle informazioni di revoca \_ viene aggiornato sui server Microsoft.

Per eseguire la revoca e il rinnovo automatici quando un utente tenta di elaborare contenuti protetti da DRM di Windows Media, l'applicazione deve eseguire le operazioni seguenti:

1.  Estrarre la \_ versione di Rev info dalla licenza. Il numero di versione di REV \_ info si trova nel percorso seguente in una licenza XMR:
    ```C++
    <LICENSE version="2.0.0.0">
        <LICENSORINFO/>
        <DATA>
            <LID>...</LID>
            <KID>...</KID>
            <RevInfoVersion>42</RevInfoVersion>
            ...
         </DATA>
    ....
    </LICENSE>
    ```

    

2.  Confrontare il \_ numero di versione di Rev info della licenza con il \_ numero di versione di Rev info nell'archivio locale chiamando il metodo [**IWMDRMSecurity:: GetRevocationDataVersion**](iwmdrmsecurity-getrevocationdataversion.md) .
3.  Se la \_ versione di Rev info non è aggiornata, chiamare il metodo [**IWMDRMSecurity::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) , passando il \_ \_ \_ \_ flag di aggiornamento di revoca della sicurezza WMDRM nel parametro *dwFlags* .
4.  Recuperare l'elenco di revoche di certificati dall'archivio locale chiamando il metodo [**IWMDRMSecurity:: GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) .
5.  Analizzare l'elenco di revoche e verificare la presenza di revoche DRM Windows Media. Per ulteriori informazioni, vedere [controllo della revoca del certificato](checking-certificate-revocation.md).
6.  Se sono presenti revoche DRM di Windows Media:
    1.  Creare un Enabler di contenuto per rinnovare i componenti revocati chiamando il metodo [**IWMDRMSecurity:: GetContentEnablersForRevocations**](iwmdrmsecurity-getcontentenablersforrevocations.md) .
    2.  Chiamare **IMFContentEnabler:: AutomaticEnable** che indirizza l'utente a un URL che contiene informazioni di rinnovo dei componenti. Questo metodo è documentato nell' [SDK Media Foundation](../medfound/microsoft-media-foundation-sdk.md) ( https://msdn.microsoft.com/library/ms694197(VS.85).aspx) .
        > [!Note]  
        > È necessario chiarire questo processo all'utente tramite l'utilizzo di un'informativa sulla privacy, perché il processo di aggiornamento Invia le informazioni dal computer client a un sito Web Microsoft.

         

    3.  Se possibile, l'utente rinnova il componente dall'URL, in modo automatico o seguendo istruzioni specifiche. In alcune situazioni il componente non può essere rinnovato.
    4.  Provare ad accedere di nuovo al contenuto fino a quando non sono presenti altre revoche oppure il processo viene interrotto per qualche motivo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida per programmatori**](drm-programming-guide.md)
</dt> </dl>

 

 