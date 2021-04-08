---
description: Anche i provider WMI possono gestire i log. I file di log visualizzati in un sistema dipendono dai provider installati.
ms.assetid: 04f041e5-4f2c-4c94-9aba-b040d941b46d
ms.tgt_platform: multiple
title: File di log del provider WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0b485c16c44ad5ac26c51db7551baa423ad1a58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880398"
---
# <a name="wmi-provider-log-files"></a>File di log del provider WMI

Anche i provider WMI possono gestire i log. I file di log visualizzati in un sistema dipendono dai provider installati.

Questi log possono trovarsi nella directory% SystemRoot% \\ system32 \\ WBEM \\ logs.

-   [Wmiprov. log](#wmiprovlog)
-   [Ntevt. log](#ntevtlog)
-   [Dsprovider. log](#dsproviderlog)
-   [Argomenti correlati](#related-topics)

## <a name="wmiprovlog"></a>Wmiprov. log

Il file wmiprov. log contiene i dati di gestione e gli eventi dai driver WDM (WMI-Enabled Windows Driver Model) e dal [provider WDM](/windows/desktop/WmiCoreProv/wdm-provider). Fornisce informazioni sugli errori e sugli avvisi principalmente per la risoluzione dei problemi e il debug del provider e delle applicazioni client che lo usano.

Il file wmiprov. log contiene:

-   Errori del [provider WDM](/windows/desktop/WmiCoreProv/wdm-provider) o del driver di dispositivo, ad esempio la compilazione MOF binaria non riuscita o il recupero dei dati.
-   Stato della compilazione MOF per ogni driver che utilizza il formato MOF.
-   Creazione e decostruzione di eventi del provider.
-   Stampa di WNODE.

## <a name="ntevtlog"></a>Ntevt. log

Il file ntevt. log contiene i messaggi di traccia del [provider di log eventi](/previous-versions/windows/desktop/eventlogprov/event-log-provider).

## <a name="dsproviderlog"></a>Dsprovider. log

Il file Dsprovider. log contiene informazioni di traccia e messaggi di errore per il [provider di Active Directory](/previous-versions/windows/desktop/dsprov/active-directory-provider).

La tabella seguente elenca alcuni problemi comuni che possono verificarsi e offre possibili cause e soluzioni.



| Message                                                                                                                                                                                                                                                                                                        | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CLDAPClassProvider:: InitializeLDAPProvider ADsGetObject su RootDSE non riuscito: <hresult>                                                                                                                                                                                                                    | La chiamata ADSI non è riuscita durante il tentativo di ottenere la radice dei servizi directory. Verificare che il computer sia membro di un dominio.                                                                                                                                                                                                                                                                             |
| CDSClassProvider:: GetObjectAsync () GetClassFromCacheOrADSI non riuscito per <class name> con <hresult>                                                                                                                                                                                                  | La classe che si sta tentando di ottenere non è una classe valida nella directory. Verificare che il nome della classe sia corretto.                                                                                                                                                                                                                                                                                                |
| CLDAPInstanceProvider::P utInstanceAsync () ModifyExistingInstance non riuscito per LDAP://CN = foo1, CN = Users, DC = dsprovider, DC = nttest, DC = Microsoft, DC = com con <hresult>                                                                                                                                       | Il provider non è stato in grado di scrivere un'istanza modificata per i servizi directory. Assicurarsi di utilizzare l'interfaccia [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) per specificare il set di proprietà che si desidera modificare. Per altre informazioni su come usare l'interfaccia **IWbemContext** con [**PutInstance**](/windows/desktop/api/Provider/nf-provider-provider-putinstance(constcinstance__long)), vedere [aggiornamento di un'intera istanza](updating-an-entire-instance.md). |
| CLDAPHelper:: GetADSIInstance ADsOpenObject () non riuscito <class name> con <hresult><br/> CLDAPInstanceProvider:: GetObjectAsync: GetADSIInstance () non riuscito con <hresult><br/> CLDAPInstanceProvider:: GetObjectAsync () non riuscito per l' \_ utente DS. ADSIPath = "<class name><br/> | Questi tre messaggi indicano che l'istanza che si sta tentando di ottenere non esiste nel servizio directory. Verificare che il valore di **ADSIPath** e il nome della classe siano corretti.                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[File di log WMI](wmi-log-files.md)
</dt> </dl>

 

