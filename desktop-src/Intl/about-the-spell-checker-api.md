---
description: Per gli utenti in tutto il mondo, l'input testuale fa parte di un'esperienza di elaborazione moderna, per blogging, commenti, Tweet, messaggistica istantanea o qualsiasi altro tipo di testo. In Windows 8, il controllo ortografico è incorporato per modificare i controlli.
ms.assetid: ED569D4F-568B-4381-91C3-8EAEDA4DD47C
title: Informazioni sull'API controllo ortografico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0d356823e665781052e2a2d5ea98b358155038
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883018"
---
# <a name="about-the-spell-checking-api"></a>Informazioni sull'API controllo ortografico

Per gli utenti in tutto il mondo, l'input testuale fa parte di un'esperienza di elaborazione moderna, per blogging, commenti, Tweet, messaggistica istantanea o qualsiasi altro tipo di testo. In Windows 8, il controllo ortografico è incorporato per modificare i controlli.

Gli sviluppatori possono usare l'API di controllo ortografico nelle app per utilizzare i servizi di controllo ortografico disponibili. Gli sviluppatori possono inoltre creare i controllo ortografici che diventano provider e sono integrati nel Framework di controllo ortografico di Windows.

L'API di controllo ortografico è progettata per l'uso da parte degli sviluppatori C/C++ professionali delle app Windows Component Object Model (COM). L'API di controllo ortografico non è supportata per l'uso in un servizio Windows o ASP.NET.

## <a name="versioning"></a>Controllo delle versioni

L'API controllo ortografico è disponibile a partire da Windows 8 o Windows Server 2012. Le aggiunte future all'API verranno gestite creando nuove interfacce che possono essere determinate usando [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) su quelle esistenti.

## <a name="interfaces"></a>Interfacce

Tutte le interfacce devono essere rilasciate quando non sono più utilizzate. Tutte le stringhe restituite (parametro out) **LPWSTR** (e gli elementi **LPOLESTR** da [**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring)) devono essere rilasciate con [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) quando non vengono più usate.

## <a name="error-handling"></a>Gestione degli errori

Gli errori vengono restituiti come **HRESULT** s. [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) e [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) non sono supportati in questa API. Gli errori non sono particolarmente praticabili ad eccezione degli argomenti non corretti.

I codici di errore RPC standard possono essere restituiti da qualsiasi chiamata API perché sono out-of-process. Si applicano i timeout standard RPC.

## <a name="security"></a>Sicurezza

L'API di controllo ortografico può caricare codice esterno (provider di controllo ortografico). Questo codice verrà eseguito out-of-process e in un contesto di sicurezza con restrizioni.

## <a name="dictionary-files"></a>File dizionario

I dizionari specifici dell'utente per una lingua che contiene il contenuto per gli elenchi di parole aggiunte, escluse e corrette si trovano in% AppData% \\ Microsoft \\ spelling \\ *<language tag>* . I nomi file sono default. dic (added), default. exc (escluso) e default. ACL (correzione automatica). I file sono di testo non crittografato UTF-16 che deve iniziare con il BOM (Byte Order Mark) appropriato. Ogni riga contiene una parola (negli elenchi di parole aggiunte ed escluse) o una coppia di correzione automatica con le parole separate da una barra verticale (" \| ") (nell'elenco di parole correzione automatica). Altri file. dic,. exc e. ACL presenti nella directory verranno rilevati dal servizio di controllo ortografico e aggiunti agli elenchi di parole utente. Questi file sono considerati di sola lettura e non vengono modificati dall'API di controllo ortografico.

## <a name="installing-a-spell-checking-provider"></a>Installazione di un provider di controllo ortografico

L'installazione di un provider di controllo ortografico deve inserire tutti i file usati in un percorso che consenta l'accesso in lettura dal SID ([ID di sicurezza](../secauthz/security-identifiers.md)) "tutti i pacchetti dell'applicazione". L'installazione in una cartella in "programmi" funziona correttamente. Inoltre, il provider deve impostare alcune chiavi nel registro affinché venga visualizzato nell'API di controllo ortografico. Può trovarsi nell'hive dell' \_ utente corrente di HKEY \_ o nell' \_ hive del computer locale hKey, \_ a seconda che venga installato solo per l'utente corrente o per tutti gli utenti.


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



L' [esempio del provider di controllo ortografico](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerProvider) fornisce un esempio della registrazione necessaria per installare un provider.

Se si creano nuove opzioni di controllo ortografico per un provider di controllo ortografico, vedere [**IOptionDescription:: ID**](/windows/desktop/api/Spellcheck/nf-spellcheck-ioptiondescription-get_id) per informazioni aggiuntive sulla denominazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento all'API controllo ortografico](spell-checker-api-reference.md)
</dt> <dt>

[Esempio di client di controllo ortografico](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerClient)
</dt> <dt>

[Esempio di provider di controllo ortografico](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerProvider)
</dt> <dt>

[**IOptionDescription:: ID**](/windows/desktop/api/Spellcheck/nf-spellcheck-ioptiondescription-get_id)
</dt> <dt>

[**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring)
</dt> <dt>

[**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))
</dt> </dl>

 

 
