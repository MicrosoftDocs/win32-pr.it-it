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
# <a name="managing-login"></a><span data-ttu-id="66aad-118">Gestione dell'accesso</span><span class="sxs-lookup"><span data-stu-id="66aad-118">Managing Login</span></span>

<span data-ttu-id="66aad-119">Windows Media Player supporta diversi metodi che consentono all'utente di accedere a un archivio online di tipo 1.</span><span class="sxs-lookup"><span data-stu-id="66aad-119">Windows Media Player supports a variety of methods for the user to log in to a type 1 online store.</span></span> <span data-ttu-id="66aad-120">Il lettore fornisce una finestra di dialogo di accesso standard, ma l'archivio online può fornire una pagina Web che funge da alternativa alla finestra di dialogo standard.</span><span class="sxs-lookup"><span data-stu-id="66aad-120">The Player provides a standard log-in dialog box, but the online store can provide a webpage that serves as an alternative to the standard dialog box.</span></span>

<span data-ttu-id="66aad-121">L'utente può avviare un tentativo di accesso interagendo con l'interfaccia utente di Windows Media Player o interagendo con una pagina di individuazione fornita dallo Store online.</span><span class="sxs-lookup"><span data-stu-id="66aad-121">The user can initiate a log-in attempt by interacting with the Windows Media Player user interface or by interacting with a discovery page provided by the online store.</span></span> <span data-ttu-id="66aad-122">Se l'utente avvia un tentativo di accesso interagendo con una pagina di individuazione, lo script nella pagina di individuazione chiama il metodo [External. attemptLogin](external-attemptlogin.md) .</span><span class="sxs-lookup"><span data-stu-id="66aad-122">If the user initiates a log-in attempt by interacting with a discovery page, script on the discovery page calls the [External.attemptLogin](external-attemptlogin.md) method.</span></span>

<span data-ttu-id="66aad-123">Lo stato di accesso dell'utente è gestito dallo Store online.</span><span class="sxs-lookup"><span data-stu-id="66aad-123">The user's log-in state is maintained by the online store.</span></span> <span data-ttu-id="66aad-124">Quando viene modificato lo stato di accesso dell'utente o se un tentativo di accesso ha esito negativo, il plug-in del negozio online Invia una notifica a Windows Media Player chiamando [IWMPContentPartnerCallback:: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), passando wmpcnLoginStateChange nel parametro di *tipo* .</span><span class="sxs-lookup"><span data-stu-id="66aad-124">When the user's log-in state changes, or if a log-in attempt fails, the online store's plug-in notifies Windows Media Player by calling [IWMPContentPartnerCallback::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), passing wmpcnLoginStateChange in the *type* parameter.</span></span> <span data-ttu-id="66aad-125">Il giocatore passa la notifica insieme alla pagina di individuazione generando l'evento [External. OnLoginChange](external-onloginchange-event.md) .</span><span class="sxs-lookup"><span data-stu-id="66aad-125">The Player passes the notification along to the discovery page by raising the [External.OnLoginChange](external-onloginchange-event.md) event.</span></span>

<span data-ttu-id="66aad-126">Una chiamata a **OnLoginChange** non significa necessariamente che lo stato di accesso dell'utente è cambiato; potrebbe significare che un tentativo di accesso non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="66aad-126">A call to **OnLoginChange** does not necessarily mean that the user's log-in state changed; it could mean that an attempt to log in failed.</span></span> <span data-ttu-id="66aad-127">Per determinare lo stato di accesso dell'utente, il gestore dell'evento **OnLoginChange** può ispezionare la proprietà [External. userLoggedIn](external-userloggedin.md) .</span><span class="sxs-lookup"><span data-stu-id="66aad-127">To determine the user's log-in state, the **OnLoginChange** event handler can inspect the [External.userLoggedIn](external-userloggedin.md) property.</span></span>

<span data-ttu-id="66aad-128">Le sezioni seguenti descrivono il processo di accesso standard, il processo di accesso alternativo e il processo di disconnessione.</span><span class="sxs-lookup"><span data-stu-id="66aad-128">The following sections describe the standard log-in process, the alternative log-in process, and the log-out process.</span></span>

## <a name="standard-log-in"></a><span data-ttu-id="66aad-129">Accesso standard</span><span class="sxs-lookup"><span data-stu-id="66aad-129">Standard Log-in</span></span>

<span data-ttu-id="66aad-130">Il processo di accesso standard prevede i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="66aad-130">The standard log-in process involves the following steps:</span></span>

1.  <span data-ttu-id="66aad-131">L'utente avvia un tentativo di accesso interagendo con l'interfaccia utente di Windows Media Player o interagendo con una pagina di individuazione.</span><span class="sxs-lookup"><span data-stu-id="66aad-131">The user initiates a log-in attempt by interacting with the Windows Media Player user interface or by interacting with a discovery page.</span></span>
2.  <span data-ttu-id="66aad-132">Windows Media Player visualizza una finestra di dialogo in cui viene richiesto all'utente un nome utente e una password.</span><span class="sxs-lookup"><span data-stu-id="66aad-132">Windows Media Player displays a dialog box that prompts the user for a user-name and password.</span></span>
3.  <span data-ttu-id="66aad-133">Quando l'utente fa clic sul pulsante **Accedi** nella finestra di dialogo, Windows Media Player chiama [IWMPContentPartner:: login](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login), che viene implementato dal plug-in Online Store.</span><span class="sxs-lookup"><span data-stu-id="66aad-133">When the user clicks the **Sign In** button in the dialog box, Windows Media Player calls [IWMPContentPartner::Login](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login), which is implemented by the online store's plug-in.</span></span>
4.  <span data-ttu-id="66aad-134">Il plug-in comunica con l'archivio online e riesce o non riesce ad accedere all'utente.</span><span class="sxs-lookup"><span data-stu-id="66aad-134">The plug-in communicates with the online store and either succeeds or fails to log in the user.</span></span>
5.  <span data-ttu-id="66aad-135">Se il tentativo di accesso ha esito positivo, il plug-in notifica a Windows Media Player chiamando **IWMPContentPartnerCallback:: Notify**, passando la variante \_ true nel membro **boolVal** del parametro *pContext* .</span><span class="sxs-lookup"><span data-stu-id="66aad-135">If the log-in attempt succeeds, the plug-in notifies Windows Media Player by calling **IWMPContentPartnerCallback::Notify**, passing VARIANT\_TRUE in the **boolVal** member of the *pContext* parameter.</span></span> <span data-ttu-id="66aad-136">Se il tentativo di accesso ha esito negativo, il plug-in notifica a Windows Media Player chiamando **IWMPContentPartnerCallback:: Notify**, passando un valore a 32 bit nel membro **UlVal** del parametro *pContext* .</span><span class="sxs-lookup"><span data-stu-id="66aad-136">If the log-in attempt fails, the plug-in notifies Windows Media Player by calling **IWMPContentPartnerCallback::Notify**, passing a 32-bit value in the **ulVal** member of the *pContext* parameter.</span></span> <span data-ttu-id="66aad-137">Il lettore passa quindi il valore di 32 bit a [IWMPContentPartner:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) per ottenere l'URL di una pagina Web in grado di gestire l'errore.</span><span class="sxs-lookup"><span data-stu-id="66aad-137">The Player then passes that 32-bit value to [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) to get the URL of a webpage that can handle the failure.</span></span>

## <a name="alternative-login"></a><span data-ttu-id="66aad-138">Accesso alternativo</span><span class="sxs-lookup"><span data-stu-id="66aad-138">Alternative Login</span></span>

<span data-ttu-id="66aad-139">Se il \_ flag ALTLOGIN Cap della sottoscrizione \_ è impostato nella voce del registro di sistema **funzionalità** per il plug-in del negozio online, Windows Media Player non utilizza la finestra di dialogo di accesso standard.</span><span class="sxs-lookup"><span data-stu-id="66aad-139">If the SUBSCRIPTION\_CAP\_ALTLOGIN flag is set in the **Capabilities** registry entry for the online store's plug-in, Windows Media Player does not use the standard log-in dialog box.</span></span> <span data-ttu-id="66aad-140">Windows Media Player chiama invece **IWMPContentPartner:: GetItemInfo** per recuperare l'URL di una pagina Web che esegue il processo di accesso.</span><span class="sxs-lookup"><span data-stu-id="66aad-140">Instead, Windows Media Player calls **IWMPContentPartner::GetItemInfo** to retrieve the URL of a webpage that performs the log-in process.</span></span> <span data-ttu-id="66aad-141">Per ulteriori informazioni sulla voce del registro di sistema **capabilities** , vedere [chiavi e voci del registro di sistema per un archivio online di tipo 1](registry-keys-and-entries-for-a-type-1-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="66aad-141">For more information about the **Capabilities** registry entry, see [Registry Keys and Entries for a Type 1 Online Store](registry-keys-and-entries-for-a-type-1-online-store.md).</span></span>

<span data-ttu-id="66aad-142">Il lettore chiama **GetItemInfo** due volte: una volta passato g \_ szItemInfo \_ ALTLOGINURL per recuperare l'URL della pagina Web di accesso e una volta passato g \_ szItemInfo \_ ALTLoginCaption per recuperare la didascalia per la finestra che ospita la pagina Web.</span><span class="sxs-lookup"><span data-stu-id="66aad-142">The Player calls **GetItemInfo** twice: once passing g\_szItemInfo\_ALTLoginURL to retrieve the URL of the log-in webpage and once passing g\_szItemInfo\_ALTLoginCaption to retrieve the caption for the window that hosts the webpage.</span></span> <span data-ttu-id="66aad-143">Quando **GetItemInfo** restituisce l'URL della pagina Web di accesso, può specificare le dimensioni della finestra di accesso aggiungendo la stringa di parametro seguente all'URL:</span><span class="sxs-lookup"><span data-stu-id="66aad-143">When **GetItemInfo** returns the URL of the log-in webpage, it can specify the size of the log-in window by appending the following parameter string to the URL:</span></span>

<span data-ttu-id="66aad-144">? DlgX =*width*&DlgY =*Height*</span><span class="sxs-lookup"><span data-stu-id="66aad-144">?DlgX=*width*&DlgY=*height*</span></span>

<span data-ttu-id="66aad-145">Nella stringa del parametro, *larghezza* e *altezza* sono la larghezza e l'altezza della finestra in pixel.</span><span class="sxs-lookup"><span data-stu-id="66aad-145">In the parameter string, *width* and *height* are the width and height of the window in pixels.</span></span> <span data-ttu-id="66aad-146">Ad esempio, **GetItemInfo** può restituire la stringa seguente per specificare che AltLogin.htm deve essere visualizzato in una finestra con una larghezza di 800 pixel e un'altezza di 400 pixel</span><span class="sxs-lookup"><span data-stu-id="66aad-146">For example **GetItemInfo** could return the following string to specify that AltLogin.htm should be displayed in a window that has a width of 800 pixels and a height of 400 pixels</span></span>


```C++
https://proseware.com/AltLogin.htm?DlgX=800&DlgY=400
```



<span data-ttu-id="66aad-147">Il processo di accesso alternativo prevede i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="66aad-147">The alternative log-in process involves the following steps:</span></span>

1.  <span data-ttu-id="66aad-148">L'utente avvia un tentativo di accesso interagendo con l'interfaccia utente di Windows Media Player o interagendo con una pagina di individuazione.</span><span class="sxs-lookup"><span data-stu-id="66aad-148">The user initiates a log-in attempt by interacting with the Windows Media Player user interface or by interacting with a discovery page.</span></span>
2.  <span data-ttu-id="66aad-149">Windows Media Player apre una finestra modale che consente di visualizzare la pagina Web di accesso fornita dal negozio online.</span><span class="sxs-lookup"><span data-stu-id="66aad-149">Windows Media Player opens a modal window that displays the log-in webpage provided by the online store.</span></span>
3.  <span data-ttu-id="66aad-150">La pagina Web comunica con il negozio online e ha esito positivo o negativo per l'accesso dell'utente.</span><span class="sxs-lookup"><span data-stu-id="66aad-150">The webpage communicates with the online store and either succeeds or fails to log in the user.</span></span>
4.  <span data-ttu-id="66aad-151">Se il tentativo di accesso ha esito positivo, la pagina Web invia una notifica al plug-in del negozio online chiamando [External. SendMessage](external-sendmessage.md), che comporta una chiamata a [IWMPContentPartner:: SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage).</span><span class="sxs-lookup"><span data-stu-id="66aad-151">If the log-in attempt succeeds, the webpage notifies the online store's plug-in by calling [External.sendMessage](external-sendmessage.md), which results in a call to [IWMPContentPartner::SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage).</span></span> <span data-ttu-id="66aad-152">Il plug-in del negozio online determina che il tentativo di accesso ha avuto esito positivo controllando i parametri passati a **IWMPContentPartner:: SendMessage**.</span><span class="sxs-lookup"><span data-stu-id="66aad-152">The online store's plug-in determines that the log-in attempt succeeded by inspecting the parameters passed to **IWMPContentPartner::SendMessage**.</span></span> <span data-ttu-id="66aad-153">Questi parametri non vengono interpretati da Windows Media Player; hanno un significato solo per il negozio online.</span><span class="sxs-lookup"><span data-stu-id="66aad-153">Those parameters are not interpreted by Windows Media Player; they have meaning only to the online store.</span></span> <span data-ttu-id="66aad-154">Il plug-in chiama **IWMPContentPartnerCallback:: Notify**, passando la variante \_ true nel membro **boolVal** del parametro *pContext* .</span><span class="sxs-lookup"><span data-stu-id="66aad-154">The plug-in calls **IWMPContentPartnerCallback::Notify**, passing VARIANT\_TRUE in the **boolVal** member of the *pContext* parameter.</span></span> <span data-ttu-id="66aad-155">Se l'accesso ha esito negativo, l'archivio online deve determinare come supportare l'utente.</span><span class="sxs-lookup"><span data-stu-id="66aad-155">If the log-in fails, the online store must determine how to assist the user.</span></span> <span data-ttu-id="66aad-156">Una possibilità consiste nel visualizzare una nuova pagina Web nella finestra modale che ospita la pagina Web di accesso alternativo.</span><span class="sxs-lookup"><span data-stu-id="66aad-156">One possibility is to display a new webpage in the modal window that hosts the alternative log-in webpage.</span></span>

## <a name="log-out"></a><span data-ttu-id="66aad-157">Disconnetti</span><span class="sxs-lookup"><span data-stu-id="66aad-157">Log-out</span></span>

<span data-ttu-id="66aad-158">Il processo di disconnessione prevede i passaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="66aad-158">The log-out process involves the following steps.</span></span>

1.  <span data-ttu-id="66aad-159">L'utente avvia un tentativo di disconnessione interagendo con l'interfaccia utente di Windows Media Player o interagendo con una pagina di individuazione.</span><span class="sxs-lookup"><span data-stu-id="66aad-159">The user initiates a log-out attempt by interacting with the Windows Media Player user interface or by interacting with a discovery page.</span></span>
2.  <span data-ttu-id="66aad-160">Windows Media Player chiama [IWMPContentPartner:: logout](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-logout), che viene implementato dal plug-in Online Store.</span><span class="sxs-lookup"><span data-stu-id="66aad-160">Windows Media Player calls [IWMPContentPartner::Logout](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-logout), which is implemented by the online store's plug-in.</span></span>
3.  <span data-ttu-id="66aad-161">Il plug-in comunica con l'archivio online e ha esito positivo o negativo per la disconnessione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="66aad-161">The plug-in communicates with the online store and either succeeds or fails to log out the user.</span></span>
4.  <span data-ttu-id="66aad-162">Se il tentativo di disconnessione ha esito positivo, il plug-in notifica a Windows Media Player chiamando **IWMPContentPartnerCallback:: Notify**, passando Variant \_ false nel membro **boolVal** del parametro *pContext* .</span><span class="sxs-lookup"><span data-stu-id="66aad-162">If the log-out attempt succeeds, the plug-in notifies Windows Media Player by calling **IWMPContentPartnerCallback::Notify**, passing VARIANT\_FALSE in the **boolVal** member of the *pContext* parameter.</span></span>

<span data-ttu-id="66aad-163">Quando un tentativo di accesso o di disconnessione ha esito positivo, il plug-in Online Store chiama **IWMPContentPartnerCallback:: Notify**, passando wmpcnLoginStateChange nel parametro di *tipo* .</span><span class="sxs-lookup"><span data-stu-id="66aad-163">When an attempt to log in or out is successful, the online store's plug-in calls **IWMPContentPartnerCallback::Notify**, passing wmpcnLoginStateChange in the *type* parameter.</span></span> <span data-ttu-id="66aad-164">Il plug-in USA il parametro *pContext* per specificare lo stato di accesso corrente dell'utente.</span><span class="sxs-lookup"><span data-stu-id="66aad-164">The plug-in uses the *pContext* parameter to specify the user's current log-in state.</span></span> <span data-ttu-id="66aad-165">Se il plug-in imposta *pContext* -> **boolVal** su Variant \_ true, l'utente ha eseguito l'accesso.</span><span class="sxs-lookup"><span data-stu-id="66aad-165">If the plug-in sets *pContext*->**boolVal** to VARIANT\_TRUE, the user is logged in.</span></span> <span data-ttu-id="66aad-166">Se il plug-in imposta *pContext* -> **boolVal** su Variant \_ false, l'utente viene disconnesso. Si noti che *pContext* non indica l'esito positivo o negativo del tentativo. indica invece lo stato di accesso corrente dell'utente.</span><span class="sxs-lookup"><span data-stu-id="66aad-166">If the plug-in sets *pContext*->**boolVal** to VARIANT\_FALSE, the user is logged out. Note that *pContext* does not indicate the success or failure of the attempt; rather, it indicates user's current log-in state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="66aad-167">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="66aad-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66aad-168">**External. attemptLogin**</span><span class="sxs-lookup"><span data-stu-id="66aad-168">**External.attemptLogin**</span></span>](external-attemptlogin.md)
</dt> <dt>

[<span data-ttu-id="66aad-169">**Evento External. OnLoginChange**</span><span class="sxs-lookup"><span data-stu-id="66aad-169">**External.OnLoginChange Event**</span></span>](external-onloginchange-event.md)
</dt> <dt>

[<span data-ttu-id="66aad-170">**External. userLoggedIn**</span><span class="sxs-lookup"><span data-stu-id="66aad-170">**External.userLoggedIn**</span></span>](external-userloggedin.md)
</dt> <dt>

[<span data-ttu-id="66aad-171">**IWMPContentPartner:: login**</span><span class="sxs-lookup"><span data-stu-id="66aad-171">**IWMPContentPartner::Login**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login)
</dt> <dt>

[<span data-ttu-id="66aad-172">**IWMPContentPartner:: logout**</span><span class="sxs-lookup"><span data-stu-id="66aad-172">**IWMPContentPartner::Logout**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-logout)
</dt> <dt>

[<span data-ttu-id="66aad-173">**Guida per programmatori per i negozi di tipo 1 online**</span><span class="sxs-lookup"><span data-stu-id="66aad-173">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




