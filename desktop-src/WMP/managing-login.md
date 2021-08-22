---
title: Gestione dell'account di accesso
description: Gestione dell'account di accesso
ms.assetid: 5cafcd3a-e819-4524-b7a9-580ff36fc4f8
keywords:
- Windows Media Player online, gestione degli accessi
- negozi online, gestione degli account di accesso
- tipo 1 punti vendita online, gestione degli account di accesso
- Windows Media Player online, account di accesso
- negozi online, account di accesso
- tipo 1 negozi online, account di accesso
- Windows Media Player store online, processo di accesso standard
- negozi online, processo di accesso standard
- tipo 1 negozi online, processo di accesso standard
- Windows Media Player store online, processo di disconnessione
- negozi online, processo di disconnessione
- tipo 1 negozi online, processo di disconnessione
- processo di accesso standard
- processo di disconnessione
- account di accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 698385f2d5a618899bd4fe440db5a552859c7647ceb2ae11e02b773c96479d52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135174"
---
# <a name="managing-login"></a>Gestione dell'account di accesso

Windows Media Player supporta diversi metodi per l'accesso dell'utente a un negozio online di tipo 1. Il lettore fornisce una finestra di dialogo di accesso standard, ma lo store online può fornire una pagina Web che funge da alternativa alla finestra di dialogo standard.

L'utente può avviare un tentativo di accesso interagendo con l'interfaccia utente di Windows Media Player o interagendo con una pagina di individuazione fornita dallo store online. Se l'utente avvia un tentativo di accesso interagendo con una pagina di individuazione, lo script nella pagina di individuazione chiama il [metodo External.attemptLogin.](external-attemptlogin.md)

Lo stato di accesso dell'utente viene gestito dallo store online. Quando lo stato di accesso dell'utente cambia o se un tentativo di accesso non riesce, il plug-in dello store online invia una notifica Windows Media Player chiamando [IWMPContentPartnerCallback::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), passando wmpcnLoginStateChange nel parametro *di* tipo. Il lettore passa la notifica alla pagina di individuazione generando [l'evento External.OnLoginChange.](external-onloginchange-event.md)

Una chiamata a **OnLoginChange** non significa necessariamente che lo stato di accesso dell'utente sia cambiato. Potrebbe significare che un tentativo di accesso non è riuscito. Per determinare lo stato di accesso dell'utente, il gestore dell'evento **OnLoginChange** può esaminare la [proprietà External.userLoggedIn.](external-userloggedin.md)

Le sezioni seguenti descrivono il processo di accesso standard, il processo di accesso alternativo e il processo di disconnessione.

## <a name="standard-log-in"></a>Accesso standard

Il processo di accesso standard prevede i passaggi seguenti:

1.  L'utente avvia un tentativo di accesso interagendo con il Windows Media Player utente o interagendo con una pagina di individuazione.
2.  Windows Media Player viene visualizzata una finestra di dialogo che richiede all'utente un nome utente e una password.
3.  Quando l'utente  fa clic sul pulsante Accedi nella finestra di dialogo, Windows Media Player chiama [IWMPContentPartner::Login,](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login)implementato dal plug-in dello store online.
4.  Il plug-in comunica con lo store online e riesce o non riesce ad accedere all'utente.
5.  Se il tentativo di accesso ha esito positivo, il plug-in invia una notifica Windows Media Player chiamando **IWMPContentPartnerCallback::Notify**, passando VARIANT TRUE nel membro \_ **boolVal** del *parametro pContext.* Se il tentativo di accesso non riesce, il plug-in invia una notifica Windows Media Player chiamando **IWMPContentPartnerCallback::Notify,** passando un valore a 32 bit nel membro **ulVal** del *parametro pContext.* Il lettore passa quindi tale valore a 32 bit a [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) per ottenere l'URL di una pagina Web in grado di gestire l'errore.

## <a name="alternative-login"></a>Account di accesso alternativo

Se il flag SUBSCRIPTION CAP ALTLOGIN è impostato nella voce del Registro di sistema Capabilities per il plug-in dello store online, Windows Media Player non usa la finestra di dialogo di \_ \_ accesso standard.  Chiama invece Windows Media Player **IWMPContentPartner::GetItemInfo** per recuperare l'URL di una pagina Web che esegue il processo di accesso. Per altre informazioni sulla voce **del Registro di sistema Capabilities,** vedere Registry Keys and [Entries for a Type 1 Online Store](registry-keys-and-entries-for-a-type-1-online-store.md).

Il lettore chiama **GetItemInfo** due volte: dopo aver passato g szItemInfo ALTLoginURL per recuperare l'URL della pagina Web di accesso e dopo aver passato \_ \_ g \_ szItemInfo ALTLoginCaption per recuperare la didascalia per la finestra che ospita la pagina \_ Web. Quando **GetItemInfo** restituisce l'URL della pagina Web di accesso, può specificare le dimensioni della finestra di accesso aggiungendo la stringa di parametro seguente all'URL:

? DlgX=*width*&DlgY=*height*

Nella stringa del parametro larghezza *e* *altezza* sono la larghezza e l'altezza della finestra in pixel. Ad **esempio, GetItemInfo** può restituire la stringa seguente per specificare che AltLogin.htm deve essere visualizzato in una finestra con una larghezza di 800 pixel e un'altezza di 400 pixel


```C++
https://proseware.com/AltLogin.htm?DlgX=800&DlgY=400
```



Il processo di accesso alternativo prevede i passaggi seguenti:

1.  L'utente avvia un tentativo di accesso interagendo con il Windows Media Player utente o interagendo con una pagina di individuazione.
2.  Windows Media Player apre una finestra modale che visualizza la pagina Web di accesso fornita dallo store online.
3.  La pagina Web comunica con lo store online e ha esito positivo o negativo per l'accesso dell'utente.
4.  Se il tentativo di accesso ha esito positivo, la pagina Web invia una notifica al plug-in dello store online chiamando [External.sendMessage](external-sendmessage.md), che comporta una chiamata a [IWMPContentPartner::SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage). Il plug-in dello store online determina che il tentativo di accesso è riuscito controllando i parametri passati a **IWMPContentPartner::SendMessage**. Questi parametri non vengono interpretati da Windows Media Player; hanno un significato solo per lo store online. Il plug-in chiama **IWMPContentPartnerCallback::Notify,** passando VARIANT TRUE nel membro \_ **boolVal** del *parametro pContext.* Se l'accesso non riesce, lo store online deve determinare come assistere l'utente. Una possibilità consiste nel visualizzare una nuova pagina Web nella finestra modale che ospita la pagina Web di accesso alternativa.

## <a name="log-out"></a>Disconnessione

Il processo di disconnessione prevede i passaggi seguenti.

1.  L'utente avvia un tentativo di disconnessione interagendo con il Windows Media Player utente o interagendo con una pagina di individuazione.
2.  Windows Media Player [chiama IWMPContentPartner::Logout,](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-logout)implementato dal plug-in dello store online.
3.  Il plug-in comunica con lo store online e riesce o non riesce a disconnettere l'utente.
4.  Se il tentativo di disconnessione ha esito positivo, il plug-in invia una notifica Windows Media Player chiamando **IWMPContentPartnerCallback::Notify,** passando VARIANT FALSE nel membro \_ **boolVal** del *parametro pContext.*

Quando un tentativo di accesso o disconnessione ha esito positivo, il plug-in dello store online chiama **IWMPContentPartnerCallback::Notify,** passando wmpcnLoginStateChange nel parametro di tipo.  Il plug-in usa il *parametro pContext* per specificare lo stato di accesso corrente dell'utente. Se il plug-in imposta *pContext* -> **boolVal** su VARIANT \_ TRUE, l'utente è connesso. Se il plug-in imposta *pContext* -> **boolVal** su VARIANT \_ FALSE, l'utente viene disconnesso. Si noti *che pContext* non indica l'esito positivo o negativo del tentativo. indica invece lo stato di accesso corrente dell'utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**External.attemptLogin**](external-attemptlogin.md)
</dt> <dt>

[**Evento External.OnLoginChange**](external-onloginchange-event.md)
</dt> <dt>

[**External.userLoggedIn**](external-userloggedin.md)
</dt> <dt>

[**IWMPContentPartner::Login**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login)
</dt> <dt>

[**IWMPContentPartner::Logout**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-logout)
</dt> <dt>

[**Guida di programmazione per gli store online di tipo 1**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




