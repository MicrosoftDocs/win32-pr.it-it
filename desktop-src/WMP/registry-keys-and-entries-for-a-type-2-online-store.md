---
title: Chiavi e voci del Registro di sistema per un negozio online di tipo 2
description: Chiavi e voci del Registro di sistema per un negozio online di tipo 2
ms.assetid: 17dff940-3884-488a-9016-29bb47c51caf
keywords:
- Windows Media Player negozi online, registro
- negozi online, registro
- tipo 2 negozi online, registro
- registro,tipo 2 negozi online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c01a5494f56a4c3fa7ea91d9537f6177453a1df54f684aa73c347029574f8dde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746452"
---
# <a name="registry-keys-and-entries-for-a-type-2-online-store"></a>Chiavi e voci del Registro di sistema per un negozio online di tipo 2

> [!Note]  
> Questa sezione descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità all'esterno del contesto di un negozio online non è supportato.

 

Per rendere disponibile un negozio online di tipo 2 in Windows Media Player, il provider del negozio online deve creare le sottochiavi e le voci del Registro di sistema seguenti nel computer dell'utente.


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



Nella sintassi del Registro di sistema precedente i simboli in corsivo sono segnaposto per i nomi e gli identificatori univoci globali specifici del negozio online. Nella tabella seguente vengono descritti questi segnaposto.



| Segnaposto    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Keyname*      | Stringa concordata tra Microsoft e il negozio online. Questa stringa identifica in modo univoco il negozio online. Esempio: "Proseware"<br/>                                                                                                                                                                                                                                                          |
| *flags*        | OR bit **per** bit di uno o più flag di funzionalità plug-in Questi flag specificano se Windows Media Player deve chiamare metodi specifici di [IWMPSubscriptionService](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice) e [IWMPSubscriptionService2.](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2) Per informazioni sui flag supportati, vedere la tabella dei flag di funzionalità plug-in che segue questa tabella. Esempio: 00000037<br/> |
| *Clsid*        | GUID che rappresenta l'identificatore di classe (CLSID) per la classe che implementa **IWMPSubscriptionService** nel plug-in del negozio online. Questo GUID deve essere in formato registro, completo di parentesi graffe. Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/>                                                                                                                                    |
| *Friendlyname* | Nome descrittivo per il negozio online. Esempio: "Proseware Musica Service"<br/>                                                                                                                                                                                                                                                                                                                     |
| *pluginName*   | Nome per il plug-in del negozio online. Esempio: "Plug-in del servizio Proseware"<br/>                                                                                                                                                                                                                                                                                                                  |
| *className*    | Nome della classe che implementa **IWMPSubscriptionService** nel plug-in dello store online. Esempio: "CProsewareService"<br/>                                                                                                                                                                                                                                                                |
| *Modulename*   | Percorso completo della DLL che implementa il plug-in dello store online. Esempio: "C: \\ Programmi \\ Proseware \\ProsewareService.dll"<br/>                                                                                                                                                                                                                                                |



 

Nella tabella seguente vengono descritti i flag di funzionalità del plug-in.



| Flag                                    | valore | Descrizione                                                                                                                                                                                                                        |
|-----------------------------------------|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LIMITE \_ DI SOTTOSCRIZIONE \_ ALLOWPLAY            | 0X1   | Windows Media Player chiamare [IWMPSubscriptionService::allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay).                                                                                                                      |
| LIMITE \_ DI SOTTOSCRIZIONE \_ ALLOWCDBURN          | 0X2   | Windows Media Player chiamare [IWMPSubscriptionService::allowCDBurn](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowcdburn).                                                                                                                  |
| LIMITE \_ DI \_ SOTTOSCRIZIONE ALLOWPDATRANSFER     | 0X4   | Windows Media Player chiamare [IWMPSubscriptionService::allowPDATransfer](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowpdatransfer).                                                                                                        |
| BACKGROUND \_ DEL LIMITE DI \_ SOTTOSCRIZIONEPROCESSING | 0X8   | Windows Media Player chiamare [IWMPSubscriptionService::startBackgroundProcessing](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-startbackgroundprocessing).                                                                                      |
| LIMITE \_ DI \_ SOTTOSCRIZIONE DEVICEAVAILABLE      | 0X10  | Windows Media Player chiamare [IWMPSubscriptionService2::d eviceAvailable](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-deviceavailable).                                                                                                        |
| LIMITE \_ DI \_ SOTTOSCRIZIONE PREPAREFORSYNC       | 0X20  | Windows Media Player chiamare [IWMPSubscriptionService2::p repareForSync](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-prepareforsync).                                                                                                          |
| LIMITI \_ DELLA SOTTOSCRIZIONE V1 \_                  | 0xf   | Valore predefinito. Questo valore viene usato se non ne è registrato nessuno. Equivale a combinare SUBSCRIPTION \_ CAP \_ ALLOWPLAY, SUBSCRIPTION \_ CAP \_ ALLOWCDBURN, SUBSCRIPTION \_ CAP \_ ALLOWPDATRANSFER e SUBSCRIPTION \_ CAP \_ BACKGROUNDPROCESSING. |



 

**Voci del Registro di sistema per sviluppo e test**

Quando si inizia a sviluppare il negozio online, Microsoft fornisce due chiavi: una chiave di test e una chiave di produzione. Durante la fase di sviluppo e test, il negozio online verrà visualizzato nel Windows Media Player solo se la chiave di test o la chiave di produzione si trova nel Registro di sistema nel computer dell'utente. Per altre informazioni sulle chiavi di test e di produzione, vedere Chiavi di test e produzione per un negozio [online di tipo 2.](test-and-production-keys-for-a-type-2-online-store.md)

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

[**Riferimento per negozi online di tipo 2**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 





