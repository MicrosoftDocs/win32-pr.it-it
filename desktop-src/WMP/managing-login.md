---
title: Gestione dell'accesso
description: Gestione dell'accesso
ms.assetid: 5cafcd3a-e819-4524-b7a9-580ff36fc4f8
keywords:
- Windows Media Player Online Stores, gestione degli account di accesso
- archivi online, gestione di account di accesso
- digitare 1 archivi online, gestione degli account di accesso
- Windows Media Player Online Stores, account di accesso
- archivi online, account di accesso
- digitare 1 archivi online, account di accesso
- Windows Media Player Online Stores, processo di accesso standard
- negozi online, processo di accesso standard
- digitare 1 negozi online, processo di accesso standard
- Windows Media Player Online Stores, processo di disconnessione
- negozi online, processo di disconnessione
- digitare 1 negozi online, processo di disconnessione
- processo di accesso standard
- processo di disconnessione
- account di accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633042692ab9193f46ab83415df13237d3a279e8
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398590"
---
# <a name="managing-login"></a>Gestione dell'accesso

Windows Media Player supporta diversi metodi che consentono all'utente di accedere a un archivio online di tipo 1. Il lettore fornisce una finestra di dialogo di accesso standard, ma l'archivio online può fornire una pagina Web che funge da alternativa alla finestra di dialogo standard.

L'utente può avviare un tentativo di accesso interagendo con l'interfaccia utente di Windows Media Player o interagendo con una pagina di individuazione fornita dallo Store online. Se l'utente avvia un tentativo di accesso interagendo con una pagina di individuazione, lo script nella pagina di individuazione chiama il metodo [External. attemptLogin](external-attemptlogin.md) .

Lo stato di accesso dell'utente è gestito dallo Store online. Quando viene modificato lo stato di accesso dell'utente o se un tentativo di accesso ha esito negativo, il plug-in del negozio online Invia una notifica a Windows Media Player chiamando [IWMPContentPartnerCallback:: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), passando wmpcnLoginStateChange nel parametro di *tipo* . Il giocatore passa la notifica insieme alla pagina di individuazione generando l'evento [External. OnLoginChange](external-onloginchange-event.md) .

Una chiamata a **OnLoginChange** non significa necessariamente che lo stato di accesso dell'utente è cambiato; potrebbe significare che un tentativo di accesso non è riuscito. Per determinare lo stato di accesso dell'utente, il gestore dell'evento **OnLoginChange** può ispezionare la proprietà [External. userLoggedIn](external-userloggedin.md) .

Le sezioni seguenti descrivono il processo di accesso standard, il processo di accesso alternativo e il processo di disconnessione.

## <a name="standard-log-in"></a>Accesso standard

Il processo di accesso standard prevede i passaggi seguenti:

1.  L'utente avvia un tentativo di accesso interagendo con l'interfaccia utente di Windows Media Player o interagendo con una pagina di individuazione.
2.  Windows Media Player visualizza una finestra di dialogo in cui viene richiesto all'utente un nome utente e una password.
3.  Quando l'utente fa clic sul pulsante **Accedi** nella finestra di dialogo, Windows Media Player chiama [IWMPContentPartner:: login](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login), che viene implementato dal plug-in Online Store.
4.  Il plug-in comunica con l'archivio online e riesce o non riesce ad accedere all'utente.
5.  Se il tentativo di accesso ha esito positivo, il plug-in notifica a Windows Media Player chiamando **IWMPContentPartnerCallback:: Notify**, passando la variante \_ true nel membro **boolVal** del parametro *pContext* . Se il tentativo di accesso ha esito negativo, il plug-in notifica a Windows Media Player chiamando **IWMPContentPartnerCallback:: Notify**, passando un valore a 32 bit nel membro **UlVal** del parametro *pContext* . Il lettore passa quindi il valore di 32 bit a [IWMPContentPartner:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) per ottenere l'URL di una pagina Web in grado di gestire l'errore.

## <a name="alternative-login"></a>Accesso alternativo

Se il \_ flag ALTLOGIN Cap della sottoscrizione \_ è impostato nella voce del registro di sistema **funzionalità** per il plug-in del negozio online, Windows Media Player non utilizza la finestra di dialogo di accesso standard. Windows Media Player chiama invece **IWMPContentPartner:: GetItemInfo** per recuperare l'URL di una pagina Web che esegue il processo di accesso. Per ulteriori informazioni sulla voce del registro di sistema **capabilities** , vedere [chiavi e voci del registro di sistema per un archivio online di tipo 1](registry-keys-and-entries-for-a-type-1-online-store.md).

Il lettore chiama **GetItemInfo** due volte: una volta passato g \_ szItemInfo \_ ALTLOGINURL per recuperare l'URL della pagina Web di accesso e una volta passato g \_ szItemInfo \_ ALTLoginCaption per recuperare la didascalia per la finestra che ospita la pagina Web. Quando **GetItemInfo** restituisce l'URL della pagina Web di accesso, può specificare le dimensioni della finestra di accesso aggiungendo la stringa di parametro seguente all'URL:

? DlgX =*width*&DlgY =*Height*

Nella stringa del parametro, *larghezza* e *altezza* sono la larghezza e l'altezza della finestra in pixel. Ad esempio, **GetItemInfo** può restituire la stringa seguente per specificare che AltLogin.htm deve essere visualizzato in una finestra con una larghezza di 800 pixel e un'altezza di 400 pixel


```C++
https://proseware.com/AltLogin.htm?DlgX=800&DlgY=400
```



Il processo di accesso alternativo prevede i passaggi seguenti:

1.  L'utente avvia un tentativo di accesso interagendo con l'interfaccia utente di Windows Media Player o interagendo con una pagina di individuazione.
2.  Windows Media Player apre una finestra modale che consente di visualizzare la pagina Web di accesso fornita dal negozio online.
3.  La pagina Web comunica con il negozio online e ha esito positivo o negativo per l'accesso dell'utente.
4.  Se il tentativo di accesso ha esito positivo, la pagina Web invia una notifica al plug-in del negozio online chiamando [External. SendMessage](external-sendmessage.md), che comporta una chiamata a [IWMPContentPartner:: SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage). Il plug-in del negozio online determina che il tentativo di accesso ha avuto esito positivo controllando i parametri passati a **IWMPContentPartner:: SendMessage**. Questi parametri non vengono interpretati da Windows Media Player; hanno un significato solo per il negozio online. Il plug-in chiama **IWMPContentPartnerCallback:: Notify**, passando la variante \_ true nel membro **boolVal** del parametro *pContext* . Se l'accesso ha esito negativo, l'archivio online deve determinare come supportare l'utente. Una possibilità consiste nel visualizzare una nuova pagina Web nella finestra modale che ospita la pagina Web di accesso alternativo.

## <a name="log-out"></a>Disconnetti

Il processo di disconnessione prevede i passaggi seguenti.

1.  L'utente avvia un tentativo di disconnessione interagendo con l'interfaccia utente di Windows Media Player o interagendo con una pagina di individuazione.
2.  Windows Media Player chiama [IWMPContentPartner:: logout](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-logout), che viene implementato dal plug-in Online Store.
3.  Il plug-in comunica con l'archivio online e ha esito positivo o negativo per la disconnessione dell'utente.
4.  Se il tentativo di disconnessione ha esito positivo, il plug-in notifica a Windows Media Player chiamando **IWMPContentPartnerCallback:: Notify**, passando Variant \_ false nel membro **boolVal** del parametro *pContext* .

Quando un tentativo di accesso o di disconnessione ha esito positivo, il plug-in Online Store chiama **IWMPContentPartnerCallback:: Notify**, passando wmpcnLoginStateChange nel parametro di *tipo* . Il plug-in USA il parametro *pContext* per specificare lo stato di accesso corrente dell'utente. Se il plug-in imposta *pContext* -> **boolVal** su Variant \_ true, l'utente ha eseguito l'accesso. Se il plug-in imposta *pContext* -> **boolVal** su Variant \_ false, l'utente viene disconnesso. Si noti che *pContext* non indica l'esito positivo o negativo del tentativo. indica invece lo stato di accesso corrente dell'utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**External. attemptLogin**](external-attemptlogin.md)
</dt> <dt>

[**Evento External. OnLoginChange**](external-onloginchange-event.md)
</dt> <dt>

[**External. userLoggedIn**](external-userloggedin.md)
</dt> <dt>

[**IWMPContentPartner:: login**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login)
</dt> <dt>

[**IWMPContentPartner:: logout**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-logout)
</dt> <dt>

[**Guida per programmatori per i negozi di tipo 1 online**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




