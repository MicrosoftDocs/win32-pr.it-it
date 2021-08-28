---
description: Per gli utenti di tutto il mondo, l'input testuale fa parte di un'esperienza di elaborazione moderna, per blog, commenti, tweet, messaggistica immediata o qualsiasi altro tipo di digitazione di testo. In Windows 8, il controllo ortografico è incorporato per modificare i controlli.
ms.assetid: ED569D4F-568B-4381-91C3-8EAEDA4DD47C
title: Informazioni sull'API Controllo ortografico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e3c15594be003b67a6e0c9df62e234e8076cd4ea213bc08468f3bb72698f51f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754941"
---
# <a name="about-the-spell-checking-api"></a>Informazioni sull'API Controllo ortografico

Per gli utenti di tutto il mondo, l'input testuale fa parte di un'esperienza di elaborazione moderna, per blog, commenti, tweet, messaggistica immediata o qualsiasi altro tipo di digitazione di testo. In Windows 8, il controllo ortografico è incorporato per modificare i controlli.

Gli sviluppatori possono usare l'API controllo ortografico nelle app per usare i servizi di controllo ortografico disponibili. Gli sviluppatori possono anche creare correttori ortografico che diventano provider e sono integrati nel framework Windows controllo ortografico.

L'API Controllo ortografico è progettata per l'uso da parte di sviluppatori professionisti C/C++ di app Windows Component Object Model (COM). L'API Controllo ortografico non è supportata per l'uso in Windows o ASP.NET servizio.

## <a name="versioning"></a>Controllo delle versioni

L'API Controllo ortografico è disponibile a partire Windows 8 o Windows Server 2012. Le aggiunte future all'API verranno gestite creando nuove interfacce che possono essere determinate usando [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) su quelle esistenti.

## <a name="interfaces"></a>Interfacce

Tutte le interfacce devono essere rilasciate quando non vengono più usate. Tutte le stringhe **LPWSTR** restituite (parametro out) (e gli elementi **LPOLESTR** di [**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring)) devono essere rilasciate con [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) quando non vengono più usate.

## <a name="error-handling"></a>Gestione degli errori

Gli errori vengono restituiti **come HRESULT** s. [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) e [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) non sono supportati in questa API. Gli errori non sono particolarmente gestibili se non per argomenti non corretti.

I codici di errore RPC standard possono essere restituiti da una delle chiamate API perché sono out-of-process. Si applicano timeout RPC standard.

## <a name="security"></a>Sicurezza

L'API Controllo ortografico può caricare codice esterno (provider di controllo ortografico). Questo codice verrà eseguito out-of-process e in un contesto di sicurezza limitato.

## <a name="dictionary-files"></a>File di dizionario

I dizionari specifici dell'utente per una lingua, che contengono il contenuto per gli elenchi di parole Aggiunte, Escluse e Correzione automatica, si trovano in %AppData% \\ Microsoft \\ Spelling \\ *<language tag>* . I nomi dei file sono default.dic (Added), default.exc (Excluded) e default.acl (Correzione automatica). I file sono testo non crittografato UTF-16 LE che deve iniziare con il byte order mark (BOM) appropriato. Ogni riga contiene una parola (negli elenchi Parole aggiunte ed escluse) o una coppia di correzione automatica con le parole separate da una barra verticale (" ") (nell'elenco di parole di Correzione \| automatica). Altri file con estensione dic, exc e acl presenti nella directory verranno rilevati dal servizio di controllo ortografico e aggiunti agli elenchi di parole utente. Questi file sono considerati di sola lettura e non vengono modificati dall'API di controllo ortografico.

## <a name="installing-a-spell-checking-provider"></a>Installazione di un provider di controllo ortografico

L'installazione di un provider di controllo ortografico deve inserire tutti i file utilizzati in un percorso che consenta l'accesso in lettura dal SID[(](../secauthz/security-identifiers.md)identificatore di sicurezza ) "ALL APPLICATION PACKAGES". L'installazione in una cartella in "Programmi" funziona correttamente. Inoltre, il provider deve impostare alcune chiavi nel Registro di sistema perché venga visualizzata nell'API controllo ortografico. Può essere presente nell'hive HKEY CURRENT USER o \_ \_ nell'hive HKEY LOCAL MACHINE a seconda che debba essere installato solo per l'utente corrente \_ o per tutti gli \_ utenti.


```
Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>
     Default (REG_SZ) = <Name of the provider>

Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>\InprocServer32
     ThreadingModel (REG_SZ) = "Both"

Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>\Version
     Version (REG_SZ) = <Version>

Key: <Registry hive>\SOFTWARE\Microsoft\Spelling\Spellers\<Provider id string>
     CLSID (REG_SZ) = <CLSID of the COM Server that implements the provider>
```



[L'esempio di provider di controllo](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerProvider) ortografico fornisce un esempio della registrazione necessaria per installare un provider.

Se si creano nuove opzioni di controllo ortografico per un provider di controllo ortografico, vedere [**IOptionDescription::Id**](/windows/desktop/api/Spellcheck/nf-spellcheck-ioptiondescription-get_id) per indicazioni sulla denominazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sulle API di controllo ortografico](spell-checker-api-reference.md)
</dt> <dt>

[Esempio di client di controllo ortografico](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerClient)
</dt> <dt>

[Esempio di provider di controllo ortografico](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerProvider)
</dt> <dt>

[**IOptionDescription::Id**](/windows/desktop/api/Spellcheck/nf-spellcheck-ioptiondescription-get_id)
</dt> <dt>

[**Ienumstring**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring)
</dt> <dt>

[**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))
</dt> </dl>

 

 
