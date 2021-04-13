---
title: Problemi di implementazione per i provider ADSI
description: Problemi di implementazione per i provider ADSI
ms.assetid: 0be772aa-e7d8-4d34-b55a-162abfb0bfd4
ms.tgt_platform: multiple
keywords:
- Problemi di implementazione per i provider ADSI ADSI
- provider ADSI, implementazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c362b04244580e448e7bb7bd78889e66db12fe
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399731"
---
# <a name="implementation-issues-for-adsi-providers"></a>Problemi di implementazione per i provider ADSI

Per implementare le interfacce ADSI, implementare prima l'interfaccia COM [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject). Fornendo questa interfaccia come livello di overhead minimo, è necessario fornire alle applicazioni client il controllo necessario per accedere agli oggetti directory direttamente dalla directory anziché tramite la cache ADSI, che consente di ottimizzare le prestazioni di rete. L'uso di questa interfaccia fornirà anche un'implementazione personalizzata con la massima flessibilità.

In secondo luogo, implementare le interfacce ADSI di base, [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsCollection**](/windows/desktop/api/Iads/nn-iads-iadscollection)e le interfacce della cache delle proprietà [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue), [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry), [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) . [**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup) e [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) sono inoltre interfacce in richiesta frequente da software di amministrazione del sistema.

Terzo, implementare le interfacce di gestione dello schema se il servizio directory presenta uno schema sottostante: [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass), [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty), [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax). Se non è presente alcuno schema sottostante, usare queste interfacce per astrarre le classi e le proprietà usate dal servizio directory. Gli schemi possono essere utilizzati per pubblicare le funzionalità del servizio directory nei client ADSI.

## <a name="collections"></a>Raccolte

I componenti del provider ADSI possono seguire uno dei tre modelli per la memorizzazione nella cache delle raccolte durante l'enumerazione. La scelta di un modello di memorizzazione nella cache determina il comportamento di ADSI quando un oggetto in una raccolta viene eliminato dal servizio directory sottostante esterno a ADSI.

I modelli di Caching includono:

-   Raccolte memorizzate nella cache in anticipo. La raccolta di istanze di oggetti viene recuperata interamente dal servizio directory sottostante quando viene chiamato [**IADsCollection:: Get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscollection-get__newenum) per creare un nuovo oggetto enumeratore. Se l'oggetto di origine per un'istanza dell'oggetto Active Directory nella raccolta recuperata viene eliminato dal servizio directory sottostante, il client non riconosce l'eliminazione fino a quando un oggetto [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) o [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) tenta di accedere alla raccolta.
-   Raccolte memorizzate in modo incrementale nella cache. La raccolta viene recuperata dal servizio directory sottostante un oggetto alla volta quando viene chiamato [**IEnumVARIANT:: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) . [**IEnumVARIANT:: Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset) tornerà all'inizio della raccolta nella cache e **IEnumVARIANT:: Next** restituirà oggetti memorizzati nella cache fino a quando non viene raggiunta la fine della cache, a cui verranno aggiunti nuovi oggetti dall'archivio sottostante. Quando un'istanza dell'oggetto Active Directory si trova nella cache, il client non viene a conoscenza dell'eliminazione dal servizio directory sottostante fino a quando [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) o [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) tenta di accedere all'oggetto.
-   Raccolte non memorizzate nella cache. La raccolta viene recuperata dal servizio directory sottostante un oggetto alla volta quando viene chiamato [**IEnumVARIANT:: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) . [**IEnumVARIANT:: Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset) tornerà all'inizio della raccolta nell'archivio sottostante. Le operazioni **IEnumVARIANT:: Next** e **IEnumVARIANT:: Reset** non possono recuperare gli oggetti eliminati perché gli oggetti vengono recuperati su richiesta dal servizio directory sottostante. Solo l'oggetto corrente viene memorizzato nella cache. Se l'oggetto corrente viene eliminato, il client non sarà in grado di rilevare l'eliminazione dal servizio directory sottostante fino a quando [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) o [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) tenta di accedere all'oggetto.

Indipendentemente dal modello di memorizzazione nella cache, tenere presente che l'enumerazione ADSI restituisce Active Directory interfacce del servizio al chiamante. Per evitare il sovraccarico dovuto all'ottenimento di un nuovo puntatore di interfaccia, le applicazioni ADSI devono memorizzare nella cache i puntatori dell'interfaccia restituiti per gli oggetti che desiderano modificare. Ad esempio, un'applicazione Visual Basic che enumera un contenitore e popola una casella di riepilogo con i nomi può memorizzare nella cache i puntatori di interfaccia associati ai nomi per un uso successivo. Questo approccio offre prestazioni maggiori rispetto al popolamento della casella di riepilogo durante l'enumerazione e al recupero di un nuovo puntatore di interfaccia quando l'utente effettua una selezione.

## <a name="about-dispatch-ids"></a>Informazioni sugli ID di invio

[**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) è un'interfaccia di automazione definita da com per i controller che non utilizzano direttamente le interfacce com. L'accesso a un oggetto tramite **IDispatch** è denominato accesso con associazione a nome o ad associazione tardiva, perché si verifica in fase di esecuzione ("tardivo") e usa nomi di stringa di proprietà e metodi per risolvere i riferimenti ("Name"). In fase di esecuzione, i client passano il nome stringa della proprietà o del metodo che desiderano chiamare nel metodo [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames)(). Se la proprietà o il metodo esiste nell'oggetto, viene recuperato l'identificatore di invio (dispID) della funzione corrispondente. Il dispID viene quindi usato per eseguire la funzione tramite [**IDispatch:: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke)(). Con **IDispatch**, le proprietà e i metodi sulle interfacce esposte da un singolo oggetto vengono visualizzati come un elenco semplice. Poiché l'accesso con associazione al nome richiede due chiamate di funzione, è meno efficiente rispetto all'uso diretto di un'interfaccia COM. È consigliabile che i client usino le interfacce ADSI COM sugli oggetti quando le prestazioni sono una considerazione. I controller di automazione avanzati, come Visual Basic 4,0, possono chiamare altre interfacce COM e **IDispatch** se le interfacce sono conformi ai vincoli di automazione per i tipi di dati e il passaggio di parametri.

I provider ADSI generano i DISPID in modo dinamico per ogni oggetto Active Directory. I DISPID recuperati tramite [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) per un determinato oggetto sono i valori generati, ma non i valori presenti nell'IDL per l'oggetto. Gli utenti [**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) devono chiamare **GetIDsOfNames** per ottenere i DISPID validi in fase di esecuzione.

## <a name="type-information-and-type-libraries"></a>Informazioni sul tipo e librerie di tipi

ADSI SDK fornisce una libreria dei tipi, activeds. tlb, che documenta tutte le interfacce standard supportate da ADSI. Un provider deve fornire una libreria dei tipi simile per tutte le interfacce presenti in activeds. tlb, più tutti i dati di tipo aggiuntivi per le interfacce implementate all'interno del componente provider.

Di seguito è riportato un esempio di codice IDL.

``` syntax
[ object, uuid(IID_IADsXYZ), oleautomation, dual ]
interface IADsXYZ: IDispatch
{
// Read-only properties.
[propget]
HRESULT AReadOnlyProp ([out, retval]BSTR *pbstrAReadOnlyProp);
 
// Read/write properties.
[propget]
HRESULT AReadWriteProp ([out, retval]long *plAReadWriteProp);
[propput]
HRESULT AReadWriteProp ([in]long lAReadWriteProp);
 
// Methods.
HRESULT AMethod ([in]DATE dateInParameter,
[out, retval]BSTR *pbstrReturnValue);
};
```

## <a name="thread-safety"></a>Thread safety

Il Component Object Model (COM) descrive i seguenti tre modelli di Threading. Le applicazioni COM indicano quale modello è in uso quando si inizializza la libreria COM usando le funzioni [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) e [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) :

-   Thread singolo. Il modello a thread singolo presuppone un singolo thread di esecuzione in un processo, presupponendo che le strutture di dati COM in un processo non richiedano la serializzazione dell'accesso.
-   Threading dell'Apartment. Un oggetto COM è associato al thread che lo ha creato. Le chiamate a un oggetto in un altro thread devono essere eseguite dal thread che ha creato l'oggetto. A tale scopo, il thread di origine richiama un proxy client che dispone la chiamata al metodo e la recapita a una funzione stub del server nel thread di destinazione tramite la coda di messaggi Win32 associata al thread di destinazione.
-   Threading gratuito. Si presuppone che gli oggetti COM siano thread-safe. A più thread è consentito l'accesso a qualsiasi oggetto nel processo senza alcuna serializzazione imposta.

ADSI non presuppone un modello di threading particolare. I writer dei componenti del provider dovrebbero presupporre il modello di threading libero e garantire la coerenza delle strutture di dati interne proteggendo gli aggiornamenti da thread-unsafe, ovvero non coordinati, tramite l'uso di oggetti di sincronizzazione, ad esempio sezioni critiche o semafori.

## <a name="object-locking"></a>Blocco di oggetti

ADSI non impone o definisce uno schema di blocco degli oggetti. I provider per gli spazi dei nomi che supportano la serializzazione di accesso mediante blocco possono esporre lo schema di blocco sottostante tramite estensioni specifiche del provider a ADSI.

## <a name="property-names-within-a-schema"></a>Nomi delle proprietà all'interno di uno schema

ADSI rappresenta le proprietà come oggetti proprietà all'interno del contenitore dello schema ADSI. Questa operazione richiede che i nomi delle proprietà siano univoci all'interno di ogni contenitore dello schema. Il provider deve assicurarsi che non siano presenti conflitti di nome.

## <a name="primary-interface"></a>Interfaccia primaria

Quando un provider non è in grado di identificare l'interfaccia che deve essere restituita come interfaccia primaria, deve essere restituito **IID \_ IADs** . In questo modo viene fornito l'accesso associato al nome a tutte le proprietà di un oggetto tramite [**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) e i metodi [**IADs:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**IADs:: GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex), [**IADs::P UT**](/windows/desktop/api/Iads/nf-iads-iads-put)e [**IADs::P UTEX**](/windows/desktop/api/Iads/nf-iads-iads-putex) .

 

 