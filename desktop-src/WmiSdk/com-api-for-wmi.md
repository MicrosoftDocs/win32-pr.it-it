---
description: È possibile utilizzare l'API WMI Component Object Model (COM) per scrivere applicazioni client di gestione o creare un nuovo provider WMI.
ms.assetid: 5fa8f1b5-fd19-4d45-9b53-bc7089eecdb1
ms.tgt_platform: multiple
title: API COM per WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfb585badeeeaae947906bbfc783baf355863e05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315240"
---
# <a name="com-api-for-wmi"></a>API COM per WMI

È possibile utilizzare l'API WMI Component Object Model (COM) per scrivere applicazioni client di gestione o creare un nuovo [*provider*](gloss-p.md)WMI. Le informazioni di riferimento sulle API COM forniscono informazioni per gli amministratori di sistema avanzati, nonché per gli sviluppatori che scrivono applicazioni client e provider.

Per ulteriori informazioni sulla scrittura di applicazioni di gestione aziendale WMI, vedere [creazione di un'applicazione WMI con C++](creating-a-wmi-application-using-c-.md). Per ulteriori informazioni su come scrivere un provider WMI, vedere la pagina relativa [alla fornitura di dati a WMI](providing-data-to-wmi.md).

> [!Note]  
> WMI supporta solo lo sviluppo C++ con Microsoft Visual C++ versione 6,0 e sistemi di sviluppo successivi. Tuttavia, è anche possibile usare altri compilatori, ad esempio quelli di Borland e Watcom.

 

Ognuno dei diversi oggetti WMI eredita da un'interfaccia infine ereditata dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . COM determina il modo in cui gli implementatori di oggetti, o interfacce, gestiscono attività quali la gestione della memoria, la gestione dei parametri e il multithreading. Conformemente a COM, l'API COM per WMI garantisce che supporti la funzionalità fornita dalle interfacce di ogni oggetto WMI.

È possibile accedere a WMI tramite le seguenti interfacce COM specifiche di WMI.



| Interfaccia                                                                    | Descrizione                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)                         | Enumeratore che funziona con gli oggetti di tipo [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject). È simile a enumeratori COM standard, ad esempio [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant).                                                                                                      |
| [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler)                                         | Implementato da Mofd.dll, questa interfaccia fornisce un'interfaccia COM utilizzata dal compilatore MOF e da qualsiasi altra applicazione che compila i file MOF.                                                                                                                                                       |
| [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment)                           | Utilizzato per semplificare il processo di esecuzione di chiamate asincrone da un processo client.                                                                                                                                                                                                                           |
| [**IWbemBackupRestore**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbembackuprestore)                             | Esegue il backup e il ripristino del contenuto del repository WMI.                                                                                                                                                                                                                                                  |
| [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult)                                   | Usato per le chiamate [semisincrono](making-a-semisynchronous-call-with-c--.md) dell'interfaccia [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) . Quando si effettuano chiamate di questo tipo, il metodo **IWbemServices** chiamato viene restituito immediatamente, insieme a un oggetto [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) .                    |
| [**IWbemCausalityAnalysis**](iwbemcausalityaccess.md)                       | Tiene traccia delle richieste figlio generate da una richiesta padre.                                                                                                                                                                                                                                            |
| [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject)                                 | Contiene e modifica sia le definizioni di classe sia le istanze dell'oggetto classe. Gli sviluppatori non devono implementare questa interfaccia; WMI fornisce la relativa implementazione.                                                                                                                                                 |
| [**IWbemConfigureRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemconfigurerefresher)                   | Utilizzato dal codice client per aggiungere o rimuovere enumeratori, oggetti e aggiornamenti annidati in un aggiornamento.                                                                                                                                                                                                         |
| [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext)                                         | Utilizzato facoltativamente per comunicare informazioni di contesto aggiuntive ai provider quando si inviano chiamate [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) alla gestione di Windows.                                                                                                                                             |
| [**IWbemDecoupledBasicEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledbasiceventprovider) | Registra i provider disaccoppiati con WMI.                                                                                                                                                                                                                                                                    |
| [**IWbemDecoupledRegistrar**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledregistrar)                   | Associa i provider disaccoppiati con WMI. Questa interfaccia consente a un provider ospitato dal processo di definire la durata di interoperabilità dell'interfaccia e di coesistere con altri provider.                                                                                                                        |
| [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider)             | Fornisce l'interfaccia principale per un provider di consumer di eventi. Tramite questa interfaccia e il metodo [**FindConsumer**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventconsumerprovider-findconsumer) , un provider di consumer di eventi può indicare quali consumer di eventi devono ricevere un determinato evento.                                          |
| [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider)                             | Utilizzato per avviare la comunicazione con un provider di eventi.                                                                                                                                                                                                                                                     |
| [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink)           | Implementata facoltativamente dai provider di eventi che vogliono conoscere i tipi di filtri di query eventi attualmente attivi per ottimizzare le prestazioni.                                                                                                                                                                 |
| [**IWbemEventProviderSecurity**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovidersecurity)             | Implementata facoltativamente dai provider di eventi che vogliono limitare l'accesso del consumer al proprio evento.                                                                                                                                                                                                             |
| [**IWbemEventSink**](iwbemeventsink.md)                                     | Avvia la comunicazione con un provider di eventi utilizzando un set limitato di query. Questa interfaccia estende [**IWbemObjectSink**](iwbemobjectsink.md), fornendo nuovi metodi di gestione della sicurezza e delle prestazioni.                                                                                          |
| [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider)                           | Consente ai provider di fornire oggetti ed enumeratori aggiornabili.                                                                                                                                                                                                                                           |
| [**IWbemHiPerfEnum**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemhiperfenum)                                   | Utilizzato nelle operazioni di aggiornamento per fornire accesso rapido a enumerazioni di oggetti istanza.                                                                                                                                                                                                                  |
| [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator)                                         | Ottiene il puntatore iniziale dello spazio dei nomi all'interfaccia [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) per WMI in un computer host specifico.                                                                                                                                                                         |
| [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess)                               | Fornisce l'accesso ai metodi e alle proprietà di un oggetto. Un oggetto [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) è un contenitore per un'istanza aggiornata da un [*aggiornamento.*](gloss-r.md)                                                                                           |
| [**IWbemObjectSink**](iwbemobjectsink.md)                                   | Utilizzato per ricevere i risultati di [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) e alcuni tipi di notifiche degli eventi.                                                                                                                                                                                       |
| [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc)                             | Usato per convertire le istanze di [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) da e verso formati di testo diversi.                                                                                                                                                                                               |
| [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider)                       | Supporta il recupero e l'aggiornamento di singole proprietà in un'istanza di una classe WMI.                                                                                                                                                                                                                      |
| [**IWbemProviderIdentity**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemprovideridentity)                       | Implementata da un provider di eventi se il provider si registra usando più di un **nome** (più istanze di [**\_ \_ Win32Provider**](--win32provider.md)) con lo stesso valore [CLSID](../com/clsid.md) . La classe fornisce un meccanismo per distinguere il provider denominato da usare. |
| [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit)                               | Utilizzato per inizializzare i provider.                                                                                                                                                                                                                                                                              |
| [**IWbemProviderInitSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinitsink)                       | Implementato da WMI e chiamato dai provider per segnalare lo stato di inizializzazione.                                                                                                                                                                                                                                |
| [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset)                               | Funge da contenitore per l'intero set di qualificatori denominati per una singola proprietà o intero oggetto (una classe o un'istanza).                                                                                                                                                                                   |
| [**IWbemQuery**](/windows/desktop/api/Wmiutils/nn-wmiutils-iwbemquery)                                             | Fornisce un punto di ingresso tramite il quale è possibile analizzare una query di [*WMI Query Language*](gloss-w.md) (WQL).                                                                                                                                                                        |
| [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher)                                     | Fornisce un punto di ingresso attraverso il quale è possibile aggiornare oggetti aggiornabili, ad esempio enumeratori o oggetti di aggiornamento.                                                                                                                                                                                      |
| [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)                                       | Utilizzato da client e provider per accedere ai servizi WMI. L'interfaccia viene implementata solo da WMI ed è l'interfaccia WMI primaria.                                                                                                                                                                           |
| [**IWbemStatusCodeText**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemstatuscodetext)                           | Estrae le descrizioni di stringhe di testo dei codici di errore o il nome del sottosistema in cui si è verificato l'errore.                                                                                                                                                                                                    |
| [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink)                     | Implementato da tutti i consumer di eventi logici. Si tratta di un'interfaccia di sink semplice che accetta il recapito di oggetti evento.                                                                                                                                                                                          |



 

> [!Note]  
> Molte delle funzioni COM WMI restituiscono codici di errore numerici documentati come costanti denominate. Queste costanti sono definite in Wbemcli. h nella \\ cartella di inclusione WMI PSDK. Per ulteriori informazioni, vedere [codici restituiti WMI](wmi-return-codes.md).

 

Per ulteriori informazioni sugli argomenti seguenti per la programmazione COM, vedere [sviluppo di componenti]( /previous-versions//ee663263(v=vs.85)):

-   Interfacce e progettazione di oggetti.
-   Implementazione di [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).
-   Gestione della memoria
-   Gestione del conteggio dei riferimenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su WMI](wmi-reference.md)
</dt> </dl>

 

 
