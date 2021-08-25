---
title: Chiavi e voci del Registro di sistema per un negozio online di tipo 1
description: Chiavi e voci del Registro di sistema per un negozio online di tipo 1
ms.assetid: cf25a004-e0c3-407c-8704-54be3601528b
keywords:
- Windows Media Player negozi online, registro
- negozi online, registro
- tipo 1 negozi online, registro
- registro, tipo 1 di negozi online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e42b1b75b64a8736c1491ccc058fe5548d78808ba51e142b3272d17d3c0eba9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861531"
---
# <a name="registry-keys-and-entries-for-a-type-1-online-store"></a>Chiavi e voci del Registro di sistema per un negozio online di tipo 1

Per rendere disponibile un negozio online di tipo 1 in Windows Media Player, il provider del negozio online deve creare le sottochiavi e le voci del Registro di sistema seguenti nel computer dell'utente.


```C++
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\Subscriptions\keyName]
"Capabilities"=dword:flags
"SubscriptionObjectGUID"=clsid
"FriendlyName"=friendlyName

[HKEY_CLASSES_ROOT\AppID\appid]
@=pluginName
"DllSurrogate"=""

[HKEY_CLASSES_ROOT\CLSID\clsid]
@=className
"AppID"="appid"

[HKEY_CLASSES_ROOT\CLSID\clsid\InprocServer32]
@=moduleName
"ThreadingModel"="threading"
```



> [!Note]  
> L'impostazione del valore di DllSurrogate sulla stringa vuota indica che il runtime COM carica il plug-in del negozio online nel surrogato DLL predefinito, dllhost.exe.

 

Nella sintassi del Registro di sistema precedente i simboli in corsivo sono segnaposto per i nomi e gli identificatori univoci globali specifici del negozio online. Nella tabella seguente vengono descritti questi segnaposto.



| Segnaposto    | Descrizione                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Keyname*      | Stringa concordata tra Microsoft e il negozio online. Questa stringa identifica in modo univoco il negozio online. Esempio: "Proseware"<br/>                                                                                                                                                                                   |
| *flags*        | OR bit **per** bit di uno o più flag di funzionalità plug-in Questi flag specificano se Windows Media Player chiamare metodi specifici di [IWMPContentPartner.](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) Per informazioni sui flag supportati, vedere la tabella dei flag di funzionalità plug-in che segue questa tabella. Esempio: 00000058<br/> |
| *Clsid*        | GUID che rappresenta l'identificatore di classe (CLSID) per la classe che implementa **IWMPContentPartner** nel plug-in del negozio online. Questo GUID deve essere in formato registro, completo di parentesi graffe. Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/>                                                                  |
| *Friendlyname* | Nome descrittivo per il negozio online. Esempio: "Proseware Musica Service"<br/>                                                                                                                                                                                                                                              |
| *appid*        | GUID che rappresenta l'identificatore dell'applicazione (AppID) per il plug-in del negozio online. Questo GUID deve essere in formato registro, completo di parentesi graffe. Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/>                                                                                                                |
| *pluginName*   | Nome per il plug-in del negozio online. Esempio: "Plug-in partner di contenuti Proseware"<br/>                                                                                                                                                                                                                                   |
| *className*    | Nome della classe che implementa **IWMPContentpartner** nel plug-in del negozio online. Esempio: "CProsewarePartner"<br/>                                                                                                                                                                                              |
| *Modulename*   | Percorso completo della DLL che implementa il plug-in dello store online. Esempio: "C: \\ Programmi \\ Proseware \\ProsewarePartner.dll"<br/>                                                                                                                                                                         |
| *Threading*    | Tipo di apartment in cui viene eseguito il plug-in. "ThreadingModel"="Apartment" indica che il plug-in viene eseguito in un apartment a thread singolo (STA). "ThreadingModel"="Free" indica che il plug-in viene eseguito nell'apartment multithreading (MTA).                                                                                     |



 

Nella tabella seguente vengono descritti i flag di funzionalità del plug-in.



| Flag                                    | valore | Descrizione                                                                                                                                                                                                                                                                 |
|-----------------------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BACKGROUND \_ DEL LIMITE DI \_ SOTTOSCRIZIONEPROCESSING | 0x8   | Windows Media Player chiamare [IWMPContentPartner::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify) per informare il plug-in quando deve avviare e arrestare l'elaborazione in background.                                                                                                     |
| LIMITE \_ DI \_ SOTTOSCRIZIONE DEVICEAVAILABLE      | 0x10  | Windows Media Player chiamare [IWMPContentPartner::UpdateDevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice).                                                                                                                                                                   |
| IL \_ LIMITE DI SOTTOSCRIZIONE È \_ \_ CONTENTPARTNER   | 0x40  | Informa Windows Media Player che il plug-in implementa **l'interfaccia IWMPContentPartner.** Tutti i plug-in del negozio online di tipo 1 devono impostare questo flag.                                                                                                                         |
| LIMITE \_ DI SOTTOSCRIZIONE \_ ALTLOGIN             | 0x80  | Informa Windows Media Player che il plug-in supporta un account di accesso alternativo. Se il plug-in supporta un account di accesso alternativo, Windows Media Player recupera l'URL e la didascalia di accesso alternativi chiamando [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo). |



 

**Voci del Registro di sistema per sviluppo e test**

Quando si inizia a sviluppare il negozio online, Microsoft fornisce due chiavi: una chiave di test e una chiave di produzione. Durante la fase di sviluppo e test, il negozio online verrà visualizzato nel Windows Media Player solo se la chiave di test o la chiave di produzione si trova nel Registro di sistema nel computer dell'utente. Per altre informazioni sulle chiavi di test e di produzione, vedere Chiavi di test e produzione [per un Negozio online di tipo 1.](test-and-production-keys-for-a-type-1-online-store.md)

Inserire la chiave di test o di produzione nel percorso seguente nel Registro di sistema.


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "key1;key2;...;keyN"
```



Si noti che il valore della voce del Registro di sistema TestParameter può specificare più chiavi di test o di produzione. Si supponga, ad esempio, che Proseware abbia una chiave di test "1234" e che Contoso abbia una chiave di test "2345". La voce del Registro di sistema seguente specifica che gli archivi di test per Proseware e Contoso verranno visualizzati in Windows Media Player.


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "1234;2345"
```



**Voce del Registro di sistema ActiveService**

Quando l'utente attiva un negozio online, Windows Media Player le informazioni nel Registro di sistema che identificano il negozio online attivo. Windows Media Player le informazioni nel percorso seguente nel Registro di sistema nel computer dell'utente.


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Subscriptions]
"ActiveService"=serviceInfo
```



Nella sintassi del Registro di sistema precedente *serviceInfo* è un segnaposto per una stringa che contiene informazioni descrittive sul negozio online attivo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Riferimento per negozi online di tipo 1**](reference-for-type-1-online-stores.md)
</dt> </dl>

 

 





