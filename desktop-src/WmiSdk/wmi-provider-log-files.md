---
description: I provider WMI possono anche gestire i log. I file di log visualizzati in un sistema dipendono dai provider installati.
ms.assetid: 04f041e5-4f2c-4c94-9aba-b040d941b46d
ms.tgt_platform: multiple
title: File di log del provider WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed9cc74b9f1c6be16f1d85eb1e1863e0dc8b7b33
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880007"
---
# <a name="wmi-provider-log-files"></a>File di log del provider WMI

I provider WMI possono anche gestire i log. I file di log visualizzati in un sistema dipendono dai provider installati.

Questi log possono trovarsi nella directory %systemroot% \\ system32 \\ wbem \\ logs.

-   [Wmiprov.log](#wmiprovlog)
-   [Ntevt.log](#ntevtlog)
-   [Dsprovider.log](#dsproviderlog)
-   [Argomenti correlati](#related-topics)

## <a name="wmiprovlog"></a>Wmiprov.log

Il file Wmiprov.log contiene i dati di gestione e gli eventi dei driver WDM (Windows Driver Model) abilitati per WMI e [del provider WDM.](/windows/desktop/WmiCoreProv/wdm-provider) Fornisce informazioni di avviso ed errore principalmente per la risoluzione dei problemi e il debug delle applicazioni client e del provider che lo usano.

Wmiprov.log contiene:

-   Errori del provider [WDM o](/windows/desktop/WmiCoreProv/wdm-provider) del driver di dispositivo, ad esempio la compilazione BINARIA MOF non riesce o non riesce a recuperare i dati.
-   Stato della compilazione MOF per ognuno dei driver che usano il formato MOF.
-   Eventi di costruzione e decostruzione del provider.
-   Stampa di WNODE.

## <a name="ntevtlog"></a>Ntevt.log

Il file Ntevt.log contiene i messaggi di traccia del [provider del registro eventi](/previous-versions/windows/desktop/eventlogprov/event-log-provider).

## <a name="dsproviderlog"></a>Dsprovider.log

Il file Dsprovider.log contiene informazioni di traccia e messaggi di errore per il [provider di Active Directory.](/previous-versions/windows/desktop/dsprov/active-directory-provider)

La tabella seguente elenca alcuni problemi comuni che possono verificarsi e offre possibili cause e soluzioni.



| Message                                                                                                                                                                                                                                                                                                        | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CLDAPClassProvider::InitializeLDAPProvider ADsGetObject in RootDSE FAILED: &lt; hresult&gt;                                                                                                                                                                                                                    | La chiamata ADSI non è riuscita durante il tentativo di ottenere la radice dei servizi directory. Verificare che il computer sia membro di un dominio.                                                                                                                                                                                                                                                                             |
| CDSClassProvider::GetObjectAsync() GetClassFromCacheOrADSI FAILED for <class name> con &lt; hresult&gt;                                                                                                                                                                                                  | La classe che si sta tentando di ottenere non è una classe valida nella directory. Verificare che il nome della classe sia corretto.                                                                                                                                                                                                                                                                                                |
| CLDAPInstanceProvider::P utInstanceAsync() ModifyExistingInstance FAILED per LDAP://CN=foo1, CN=Users, DC=dsprovider,DC=nttest, DC=Microsoft, DC=com con &lt; hresult&gt;                                                                                                                                       | Il provider non è riuscito a scrivere un'istanza modificata nei servizi directory. Assicurarsi di usare [**l'interfaccia IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) per specificare il set di proprietà da modificare. Per altre informazioni su come usare **l'interfaccia IWbemContext** con [**PutInstance,**](/windows/desktop/api/Provider/nf-provider-provider-putinstance(constcinstance__long))vedere [Aggiornamento di un'intera istanza.](updating-an-entire-instance.md) |
| CLDAPHelper::GetADSIInstance ADsOpenObject() FAILED on <class name> with &lt; hresult&gt;<br/> CLDAPInstanceProvider::GetObjectAsync: GetADSIInstance() FAILED con &lt; hresult&gt;<br/> CLDAPInstanceProvider::GetObjectAsync() FAILED per l'utente \_ ds. ADSIPath="<class name><br/> | Questi tre messaggi indicano che l'istanza che si sta tentando di ottenere non esiste nel servizio directory. Verificare che il **valore ADSIPath** e il nome della classe siano corretti.                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[File di log WMI](wmi-log-files.md)
</dt> </dl>

 

