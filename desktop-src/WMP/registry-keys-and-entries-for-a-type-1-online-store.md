---
title: Chiavi e voci del registro di sistema per un archivio online di tipo 1
description: Chiavi e voci del registro di sistema per un archivio online di tipo 1
ms.assetid: cf25a004-e0c3-407c-8704-54be3601528b
keywords:
- Windows Media Player Online Stores, registro di sistema
- archivi online, registro di sistema
- digitare 1 archivi online, registro di sistema
- Registro di sistema, digitare 1 negozio online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1329ad69e91ebce41b258d1e148403f62caceb96
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299423"
---
# <a name="registry-keys-and-entries-for-a-type-1-online-store"></a>Chiavi e voci del registro di sistema per un archivio online di tipo 1

Per rendere disponibile un archivio online di tipo 1 in Windows Media Player, il provider di archivio online deve creare le sottochiavi e le voci del registro di sistema seguenti nel computer dell'utente.


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
> L'impostazione del valore di DllSurrogate sulla stringa vuota indica che il runtime COM caricherà il plug-in del negozio online nel surrogato predefinito della DLL, dllhost.exe.

 

Nella sintassi del registro di sistema precedente, i simboli in corsivo sono segnaposto per i nomi e identificatori univoci globali (GUID) specifici per l'archivio online. Nella tabella seguente vengono descritti i segnaposto.



| Segnaposto    | Descrizione                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *keyName*      | Stringa concordata tra Microsoft e il negozio online. Questa stringa identifica in modo univoco l'archivio online. Esempio: "Proseware"<br/>                                                                                                                                                                                   |
| *flags*        | Un operatore OR bit per bit di uno o più plug-in **flag di funzionalità** questi flag specificano se Windows Media Player deve chiamare metodi specifici di [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner). Per informazioni sui flag supportati, vedere la tabella dei flag di funzionalità plug-in che seguono questa tabella. Esempio: 00000058<br/> |
| *CLSID*        | GUID che rappresenta l'identificatore di classe (CLSID) per la classe che implementa **IWMPContentPartner** nel plug-in del negozio online. Il GUID deve essere nel formato del registro di sistema, completo di parentesi graffe. Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/>                                                                  |
| *FriendlyName* | Nome descrittivo per il negozio online. Esempio: "Proseware Music Service"<br/>                                                                                                                                                                                                                                              |
| *appid*        | GUID che rappresenta l'ID applicazione (AppID) per il plug-in del negozio online. Il GUID deve essere nel formato del registro di sistema, completo di parentesi graffe. Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/>                                                                                                                |
| *pluginName*   | Nome del plug-in del negozio online. Esempio: "plug-in di Proseware content partner"<br/>                                                                                                                                                                                                                                   |
| *className*    | Nome della classe che implementa **IWMPContentpartner** nel plug-in del negozio online. Esempio: "CProsewarePartner"<br/>                                                                                                                                                                                              |
| *moduleName*   | Percorso completo della DLL che implementa il plug-in del negozio online. Esempio: "C: \\ Program Files \\ Proseware \\ProsewarePartner.dll"<br/>                                                                                                                                                                         |
| *Threading*    | Tipo di Apartment in cui viene eseguito il plug-in. "ThreadingModel" = "Apartment" indica che il plug-in viene eseguito in un Apartment a thread singolo (STA). "ThreadingModel" = "Free" indica che il plug-in viene eseguito nell'Apartment a thread multipli (MTA).                                                                                     |



 

Nella tabella seguente vengono descritti i flag di funzionalità plug-in.



| Flag                                    | valore | Descrizione                                                                                                                                                                                                                                                                 |
|-----------------------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_BACKGROUNDPROCESSING Cap \_ sottoscrizione | 0x8   | Windows Media Player deve chiamare [IWMPContentPartner:: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify) per informare il plug-in quando deve avviare e arrestare l'elaborazione in background.                                                                                                     |
| \_DEVICEAVAILABLE Cap \_ sottoscrizione      | 0x10  | Windows Media Player deve chiamare [IWMPContentPartner:: UpdateDevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice).                                                                                                                                                                   |
| il \_ limite della sottoscrizione \_ è \_ CONTENTPARTNER   | 0x40  | Informa Windows Media Player che il plug-in implementa l'interfaccia **IWMPContentPartner** . Tutti i plug-in di archiviazione di tipo 1 devono impostare questo flag.                                                                                                                         |
| \_ALTLOGIN Cap \_ sottoscrizione             | 0x80  | Informa Windows Media Player che il plug-in supporta un account di accesso alternativo. Se il plug-in supporta un account di accesso alternativo, Windows Media Player recupera l'URL e la didascalia di accesso alternativi chiamando [IWMPContentPartner:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo). |



 

**Voci del registro di sistema per sviluppo e test**

Quando si inizia a sviluppare lo Store online, Microsoft fornisce due chiavi: una chiave di test e una chiave di produzione. Durante la fase di sviluppo e test, il negozio online verrà visualizzato in Windows Media Player solo se la chiave di test o la chiave di produzione si trova nel registro di sistema nel computer dell'utente. Per ulteriori informazioni sulle chiavi di test e di produzione, vedere [chiavi di test e di produzione per un negozio online di tipo 1](test-and-production-keys-for-a-type-1-online-store.md).

Inserire la chiave di test o di produzione nel seguente percorso del registro di sistema.


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "key1;key2;...;keyN"
```



Si noti che il valore della voce del registro di sistema TestParameter può specificare più chiavi di test o di produzione. Si supponga, ad esempio, che Proseware disponga di una chiave di test "1234" e che Contoso disponga di una chiave di test "2345". La voce del registro di sistema seguente specifica che gli archivi di test per Proseware e contoso verranno visualizzati in Windows Media Player.


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "1234;2345"
```



**Voce del registro di sistema ActiveService**

Quando l'utente attiva uno Store online, Windows Media Player scrive le informazioni nel registro di sistema che identifica l'archivio online attivo. Windows Media Player inserisce le informazioni nel seguente percorso del registro di sistema nel computer dell'utente.


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Subscriptions]
"ActiveService"=serviceInfo
```



Nella sintassi del registro di sistema precedente, *serviceInfo* è un segnaposto per una stringa che contiene informazioni descrittive sull'archivio online attivo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Riferimento per negozi online di tipo 1**](reference-for-type-1-online-stores.md)
</dt> </dl>

 

 





