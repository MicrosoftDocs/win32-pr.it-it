---
description: È importante comprendere la struttura DLL richiesta di un gestore di filtro, ovvero un'implementazione dell'interfaccia IFilter.
ms.assetid: a2b5a813-573a-44d3-8780-99603e3246c1
title: Implementazione di gestori di filtro in Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5f326440b31b62ff5697274962f4d4a2cfe7c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306169"
---
# <a name="implementing-filter-handlers-in-windows-search"></a>Implementazione di gestori di filtro in Windows Search

È importante comprendere la struttura DLL richiesta di un gestore di filtro, ovvero un'implementazione dell'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .

Questo argomento è organizzato nel modo seguente:

- [Implementazione ed esportazione dei punti di ingresso della DLL](#implementing-and-exporting-the-dll-entry-points)
- [Implementazione della classe IFilter e della class factory](#implementing-the-ifilter-class-and-class-factory)
- [Eredità delle interfacce COM](#inheriting-the-com-interfaces)
- [Implementazione dei metodi dell'interfaccia COM](#implementing-the-com-interface-methods)
  - [Metodi COM non implementati](#com-methods-that-are-not-implemented)
- [Risorse aggiuntive](#additional-resources)
- [Argomenti correlati](#related-topics)

## <a name="implementing-and-exporting-the-dll-entry-points"></a>Implementazione ed esportazione dei punti di ingresso della DLL

Ogni dll [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) (indicata da Ifilter.dll in questa sezione) deve implementare ed esportare i punti di ingresso seguenti. Questi punti di ingresso vengono in genere esportati utilizzando un file di definizione moduli (con estensione def) per l'interfaccia **IFilter** o utilizzando la parola chiave **\_ \_ declspec (dllexport)** . Il file DLL può essere registrato in qualsiasi cartella, ma in genere si trova nella cartella% SystemRoot% \\ system32.

I punti di ingresso della DLL sono elencati e descritti nella tabella seguente.

| Nome DLL                                                                                     | Descrizione DLL                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DllRegisterServer](/windows/win32/api/olectl/nf-olectl-dllregisterserver)            | Il punto di ingresso [DllRegisterServer](/windows/win32/api/olectl/nf-olectl-dllregisterserver) registra la dll come filtro nel registro di sistema. Per registrare la DLL, è necessario eseguire il programma regsvr32.exe con il nome del file DLL dell'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) come argomento: `regsvr32.exe %SystemRoot%\system32\Ifilter.dll`                                              |
| [DllUnregisterServer (funzione)](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) | Il punto di ingresso della [funzione DllUnregisterServer](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) rimuove la dll come gestore permanente nel registro di sistema. Si annulla la registrazione della DLL eseguendo il programma regsvr32.exe con il `/u` flag: `regsvr32.exe /u %SystemRoot%\system32\Ifilter.dll`                                                                                    |
| [DllGetClassObject (funzione)](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject)   | Il client di indicizzazione del contenuto chiama il punto di ingresso della [funzione DllGetClassObject](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) , tramite Component Object Model (com), per creare un oggetto class factory per l'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) e per ottenere un puntatore all'interfaccia class factory di tale oggetto.                                               |
| [DllCanUnloadNow (funzione)](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow)     | Il client di indicizzazione del contenuto chiama il punto di ingresso della [funzione DllCanUnloadNow](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) , tramite com, per determinare se è possibile scaricare la dll [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)  . L'interfaccia **IFilter** viene scaricata dopo essere stata inutilizzata per un intervallo di tempo, come specificato dal valore del registro di sistema FilterIdleTimeOut. |

## <a name="implementing-the-ifilter-class-and-class-factory"></a>Implementazione della classe IFilter e della class factory

Almeno due classi, ad esempio CFilter e CFilterCF, vengono in genere implementate da ogni dll [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) . La classe CFilter produce l'oggetto interfaccia **IFilter** che implementa la funzionalità di filtro dei contenuti. Le funzioni membro implementano i metodi di interfaccia dell'interfaccia **IFilter** . Ogni classe **IFilter** richiede un identificatore di classe univoco (CLSID), generato dall'implementatore dell'interfaccia **IFilter** .

La classe CFilterCF produce l'oggetto class-factory per l'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) . Il class factory viene chiamato, tramite l'interfaccia dell' [interfaccia IClassFactory](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) , dal punto di ingresso della [funzione DllGetClassObject](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) della dll. La classe CFilterCF crea l'oggetto CFilter e restituisce un puntatore a [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown). In casi più complessi, un **IFilter** può implementare una gerarchia di classi al posto della singola classe cfilter.

## <a name="inheriting-the-com-interfaces"></a>Eredità delle interfacce COM

Windows Search 3,0 e versioni successive richiedono l'uso di [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) per i motivi seguenti:

- Per garantire prestazioni e compatibilità futura.
- Per aumentare la sicurezza. I filtri IFilter implementati con [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) sono più sicuri perché il contesto in cui viene eseguita l'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) non necessita dei diritti per aprire i file sul disco o sulla rete.
- Sebbene Windows Search usi solo [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream), la classe di interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) può anche ereditare l' [interfaccia IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) e/o le implementazioni dell'interfaccia dell' [interfaccia IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) per la compatibilità con le versioni precedenti.

Queste interfacce sono dichiarate nei file inclusi dalla \\ directory di inclusione MSSDK e hanno identificatori di interfaccia predefiniti (IID). Il client di indicizzazione del contenuto esegue una query sull'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) tramite [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) per determinare quali di queste interfacce utilizzare per filtrare il contenuto.

## <a name="implementing-the-com-interface-methods"></a>Implementazione dei metodi dell'interfaccia COM

L'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) implementa i metodi [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) sia per la classe di interfaccia **IFilter** sia per l'interfaccia **IFilter** -class factory. Nella tabella seguente sono elencati, in ordine vtable, le interfacce e i metodi specifici dell'interfaccia **IFilter** che devono essere implementati dall'interfaccia **IFilter** . L'interfaccia **IFilter** deve implementare almeno [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream), ma può implementare altre interfacce derivate da IPersist.

| Interfaccia COM                                                                             | Metodo                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Interfaccia IClassFactory](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)   | CreateInstance, LockServer                                                                                                                                                                                                                                                     |
| [Interfaccia IClassFactory2](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2)  | GetLicInfo, RequestLicKey, CreateInstanceLic                                                                                                                                                                                                                                   |
| [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)                                                        | [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init), [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk), [**IFilter:: GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext), [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue), [**IFilter:: BindRegion**](/windows/win32/api/filter/nf-filter-ifilter-bindregion) |
| [Interfaccia IPersist](/windows/desktop/api/objidl/nn-objidl-ipersist)               | GetClassID                                                                                                                                                                                                                                                                     |
| [Interfaccia IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile)    | IsDirty, Load, Save, SaveCompleted, GetCurFile                                                                                                                                                                                                                                 |
| [Interfaccia IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) | IsDirty, Load, Save, GetSizeMax                                                                                                                                                                                                                                                |
| [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream)            | IsDirty, Load, Save, GetSizeMax                                                                                                                                                                                                                                                |

La pagina di riferimento per ogni metodo specifica i parametri e il comportamento funzionale per il metodo. Ogni pagina di riferimento fornisce inoltre i codici di risultato da implementare per il metodo. Le pagine di riferimento per i metodi [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) forniscono i codici specifici dell'interfaccia nei codici risultato della [funzionalità \_ ITF](../com/codes-in-facility-itf.md) da implementare e il client di indicizzazione del contenuto è in grado di gestire anche i codici di risultato generici, ad esempio la funzionalità \_ null e la funzione \_ Win32. Per ulteriori informazioni, vedere la pagina relativa alla [struttura dei codici di errore com](../com/structure-of-com-error-codes.md).

### <a name="com-methods-that-are-not-implemented"></a>Metodi COM non implementati

L'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) deve implementare almeno [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream), ma non è necessario implementare altre interfacce derivate da IPersist.

Windows Search non deve implementare i metodi COM elencati nella tabella seguente.

| Metodo non obbligatorio                               | Descrizione                       |
|-----------------------------------------------------------|-----------------------------------|
| IPersistStream:: IsDirty                                   | I filtri devono restituire E \_ NOTIMPL. |
| IPersistStream:: Save                                      | I filtri devono restituire E \_ NOTIMPL. |
| IPersistStream:: GetSizeMax                                | I filtri devono restituire E \_ NOTIMPL. |
| [**IFilter:: BindRegion**](/windows/win32/api/filter/nf-filter-ifilter-bindregion) | I filtri devono restituire E \_ NOTIMPL. |

## <a name="additional-resources"></a>Risorse aggiuntive

- Nell'esempio di codice [IFilterSample](-search-sample-ifiltersample.md) , disponibile in [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), viene illustrato come creare una classe di base IFilter per implementare l'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .
- Per una panoramica del processo di indicizzazione, vedere [il processo di indicizzazione](-search-indexing-process-overview.md).
- Per una panoramica dei tipi di file, vedere [tipi di file](../shell/fa-file-types.md).
- Per eseguire query sugli attributi di associazione file per un tipo di file, vedere [PerceivedTypes, SystemFileAssociations e registrazione dell'applicazione](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).

## <a name="related-topics"></a>Argomenti correlati

[Sviluppo di gestori di filtri](-search-ifilter-conceptual.md)

[Informazioni sui gestori di filtro in Windows Search](-search-ifilter-about.md)

[Procedure consigliate per la creazione di gestori di filtro in Windows Search](-search-3x-wds-extidx-filters.md)

[Restituzione di proprietà da un gestore di filtro](-search-ifilter-property-filtering.md)

[Gestori di filtri forniti con Windows](-search-ifilter-implementations.md)

[Registrazione di gestori di filtro](-search-ifilter-registering-filters.md)

[Test di gestori filtro](-search-ifilter-testing-filters.md)
