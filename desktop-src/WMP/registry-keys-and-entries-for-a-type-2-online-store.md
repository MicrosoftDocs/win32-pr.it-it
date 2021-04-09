---
title: Chiavi del registro di sistema e voci per un archivio di tipo 2 online
description: Chiavi del registro di sistema e voci per un archivio di tipo 2 online
ms.assetid: 17dff940-3884-488a-9016-29bb47c51caf
keywords:
- Windows Media Player Online Stores, registro di sistema
- archivi online, registro di sistema
- digitare 2 archivi online, registro di sistema
- Registro di sistema, digitare 2 archivi online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 685a26514730e7c370c698cbc9c64c29366c35ee
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104117443"
---
# <a name="registry-keys-and-entries-for-a-type-2-online-store"></a>Chiavi del registro di sistema e voci per un archivio di tipo 2 online

> [!Note]  
> In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

Per rendere disponibile un archivio online di tipo 2 in Windows Media Player, il provider di archivio online deve creare le sottochiavi e le voci del registro di sistema seguenti nel computer dell'utente.


```C++
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\Subscriptions\keyName]
"Capabilities"=dword:flags
"SubscriptionObjectGUID"=clsid
"FriendlyName"=friendlyName

[HKEY_CLASSES_ROOT\CLSID\clsid]
@=className

[HKEY_CLASSES_ROOT\CLSID\clsid\InprocServer32]
@=moduleName
"ThreadingModel"="Apartment"
```



Nella sintassi del registro di sistema precedente, i simboli in corsivo sono segnaposto per i nomi e identificatori univoci globali (GUID) specifici per l'archivio online. Nella tabella seguente vengono descritti i segnaposto.



| Segnaposto    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *keyName*      | Stringa concordata tra Microsoft e il negozio online. Questa stringa identifica in modo univoco l'archivio online. Esempio: "Proseware"<br/>                                                                                                                                                                                                                                                          |
| *flags*        | Un operatore OR bit per bit di **uno o più** plug-in flag di funzionalità questi flag specificano se Windows Media Player deve chiamare metodi specifici di [IWMPSubscriptionService](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice) e [IWMPSubscriptionService2](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2). Per informazioni sui flag supportati, vedere la tabella dei flag di funzionalità plug-in che seguono questa tabella. Esempio: 00000037<br/> |
| *CLSID*        | GUID che rappresenta l'identificatore di classe (CLSID) per la classe che implementa **IWMPSubscriptionService** nel plug-in del negozio online. Il GUID deve essere nel formato del registro di sistema, completo di parentesi graffe. Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/>                                                                                                                                    |
| *FriendlyName* | Nome descrittivo per il negozio online. Esempio: "Proseware Music Service"<br/>                                                                                                                                                                                                                                                                                                                     |
| *pluginName*   | Nome del plug-in del negozio online. Esempio: "plug-in del servizio Proseware"<br/>                                                                                                                                                                                                                                                                                                                  |
| *className*    | Nome della classe che implementa **IWMPSubscriptionService** nel plug-in del negozio online. Esempio: "CProsewareService"<br/>                                                                                                                                                                                                                                                                |
| *moduleName*   | Percorso completo della DLL che implementa il plug-in del negozio online. Esempio: "C: \\ Program Files \\ Proseware \\ProsewareService.dll"<br/>                                                                                                                                                                                                                                                |



 

Nella tabella seguente vengono descritti i flag di funzionalità plug-in.



| Flag                                    | valore | Descrizione                                                                                                                                                                                                                        |
|-----------------------------------------|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ALLOWPLAY Cap \_ sottoscrizione            | 0X1   | Windows Media Player deve chiamare [IWMPSubscriptionService:: allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay).                                                                                                                      |
| \_ALLOWCDBURN Cap \_ sottoscrizione          | 0X2   | Windows Media Player deve chiamare [IWMPSubscriptionService:: allowCDBurn](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowcdburn).                                                                                                                  |
| \_ALLOWPDATRANSFER Cap \_ sottoscrizione     | 0X4   | Windows Media Player deve chiamare [IWMPSubscriptionService:: allowPDATransfer](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowpdatransfer).                                                                                                        |
| \_BACKGROUNDPROCESSING Cap \_ sottoscrizione | 0X8   | Windows Media Player deve chiamare [IWMPSubscriptionService:: startBackgroundProcessing](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-startbackgroundprocessing).                                                                                      |
| \_DEVICEAVAILABLE Cap \_ sottoscrizione      | 0X10  | Windows Media Player deve chiamare [IWMPSubscriptionService2::D eviceavailable](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-deviceavailable).                                                                                                        |
| \_PREPAREFORSYNC Cap \_ sottoscrizione       | 0X20  | Windows Media Player deve chiamare [IWMPSubscriptionService2::P repareforsync](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-prepareforsync).                                                                                                          |
| Caps della sottoscrizione \_ V1 \_                  | 0XF   | Valore predefinito. Questo valore viene utilizzato se non ne viene registrato nessuno. Equivale a combinare \_ Cap \_ ALLOWPLAY, Subscription \_ Cap \_ ALLOWCDBURN, SUBSCRIPTION \_ Cap \_ ALLOWPDATRANSFER e Subscription \_ Cap \_ BACKGROUNDPROCESSING. |



 

**Voci del registro di sistema per sviluppo e test**

Quando si inizia a sviluppare lo Store online, Microsoft fornisce due chiavi: una chiave di test e una chiave di produzione. Durante la fase di sviluppo e test, il negozio online verrà visualizzato in Windows Media Player solo se la chiave di test o la chiave di produzione si trova nel registro di sistema nel computer dell'utente. Per altre informazioni sulle chiavi di test e di produzione, vedere [chiavi di test e di produzione per un negozio online di tipo 2](test-and-production-keys-for-a-type-2-online-store.md).

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

[**Riferimento per negozi online di tipo 2**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 





