---
description: Un manifesto dell'assembly è un file XML che descrive un assembly side-by-side.
ms.assetid: f7973019-0a80-498e-adf1-c66267c813f4
title: Manifesti di assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94310ce3fdbb05706f889ea9755f7a47320ada56
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884891"
---
# <a name="assembly-manifests"></a>Manifesti di assembly

Un manifesto dell'assembly è un file XML che descrive un assembly side-by-side. I manifesti dell'assembly descrivono i nomi e le versioni di assembly, file e risorse side-by-side dell'assembly, nonché la dipendenza dell'assembly da altri assembly side-by-side. L'installazione, l'attivazione e l'esecuzione corrette di assembly side-by-side richiedono che il manifesto dell'assembly accompagna sempre un assembly nel sistema.

Per un elenco completo dello schema XML, vedere [Schema del file manifesto](manifest-file-schema.md).

I manifesti dell'assembly hanno gli elementi e gli attributi seguenti.



| Elemento                           | Attributi                | Necessario |
|-----------------------------------|---------------------------|----------|
| **Assemblea**                      |                           | Sì      |
|                                   | **manifestVersion**       | Sì      |
| **noInheritable**                 |                           | No       |
| **Assemblyidentity**              |                           | Sì      |
|                                   | **type**                  | Sì      |
|                                   | **nome**                  | Sì      |
|                                   | **language**              | No       |
|                                   | **processorArchitecture** | No       |
|                                   | **version**               | Sì      |
|                                   | **Publickeytoken**        | No       |
| **Dipendenza**                    |                           | No       |
| **dependentAssembly**             |                           | No       |
| **file**                          |                           | No       |
|                                   | **nome**                  | Sì      |
|                                   | **hashalg**               | No       |
|                                   | **hash**                  | No       |
| **comClass**                      |                           | No       |
|                                   | **description**           | No       |
|                                   | **Clsid**                 | Sì      |
|                                   | **Threadingmodel**        | No       |
|                                   | **tlbid**                 | No       |
|                                   | **Progid**                | No       |
|                                   | **miscStatus**            | No       |
|                                   | **miscStatusIcon**        | No       |
|                                   | **miscStatusContent**     | No       |
|                                   | **miscStatusDocPrint**    | No       |
|                                   | **miscStatusDocPrint**    | No       |
| **Typelib**                       |                           | No       |
|                                   | **tlbid**                 | Sì      |
|                                   | **version**               | Sì      |
|                                   | **helpdir**               | Sì      |
|                                   | **Resourceid**            | No       |
|                                   | **flags**                 | No       |
| **comInterfaceExternalProxyStub** |                           | No       |
|                                   | **Iid**                   | Sì      |
|                                   | **baseInterface**         | No       |
|                                   | **numMethods**            | No       |
|                                   | **nome**                  | No       |
|                                   | **tlbid**                 | No       |
|                                   | **proxyStubClsid32**      | No       |
| **comInterfaceProxyStub**         |                           | No       |
|                                   | **Iid**                   | Sì      |
|                                   | **nome**                  | Sì      |
|                                   | **tlbid**                 | No       |
|                                   | **baseInterface**         | No       |
|                                   | **numMethods**            | No       |
|                                   | **proxyStubClsid32**      | No       |
|                                   | **Threadingmodel**        | No       |
| **windowClass**                   |                           | No       |
|                                   | **con controllo delle versioni**             | No       |



 

## <a name="file-location"></a>Percorso file

I manifesti dell'assembly possono essere installati in tre posizioni:

-   Come manifesti che [accompagnano](/windows/desktop/Msi/shared-assemblies)gli assembly condivisi, i manifesti degli assembly devono essere installati come file separato nella Cache assembly side-by-side. Si tratta in genere della cartella WinSxS nella directory Windows.
-   Come manifesti che [accompagnano assembly privati,](/windows/desktop/Msi/private-assemblies)i manifesti degli assembly devono essere installati nella struttura di directory dell'applicazione. Si tratta in genere di un file separato nella stessa cartella del file eseguibile dell'applicazione.
-   Come risorsa in una DLL, l'assembly è disponibile per l'uso privato della DLL. Un manifesto dell'assembly non può essere incluso come risorsa in un file EXE. Un file EXE può includere un [manifesto dell'applicazione](application-manifests.md) come risorsa.

## <a name="file-name-syntax"></a>Sintassi del nome file

Il nome di un manifesto dell'assembly è qualsiasi nome di file valido seguito da manifest.

Ad esempio, un manifesto dell'assembly che fa riferimento a myassembly userebbe la sintassi del nome file seguente. È possibile omettere il campo *<'ID* risorsa> se il manifesto dell'assembly viene installato come file separato o se l'ID risorsa è 1.

<dl> myassembly. <resource ID> . Manifesto
</dl>

> [!Note]  
> A causa della modalità di ricerca side-by-side degli assembly privati, durante la creazione del pacchetto di una DLL come assembly privato si applicano le restrizioni di denominazione seguenti. Un modo consigliato per eseguire questa operazione è inserire il manifesto dell'assembly nella DLL come risorsa. In questo caso, l'ID risorsa deve essere uguale a 1 e il nome dell'assembly privato può corrispondere al nome della DLL. Ad esempio, se il nome della DLL è Microsoft.Windows.mysample.dll, anche il valore dell'attributo name usato nell'elemento **assemblyIdentity** del manifesto può essere Microsoft. Windows.mysample. Un modo alternativo è inserire il manifesto dell'assembly in un file separato. In questo caso, il nome dell'assembly e il relativo manifesto devono essere diversi dal nome della DLL. Ad esempio, Microsoft. Windows.mysampleAsm, Microsoft. Windows.mysampleAsm.manifest e Microsoft.Windows.Mysample.dll. Per altre informazioni sulla modalità di ricerca side-by-side di assembly privati, vedere [Sequenza di ricerca di assembly.](assembly-searching-sequence.md)

 

## <a name="elements"></a>Elementi

Per i nomi degli elementi e degli attributi viene fatto distinzione tra maiuscole e minuscole. Per i valori di elementi e attributi non viene fatta distinzione tra maiuscole e minuscole, ad eccezione del valore dell'attributo type.

<dl> <dt>

<span id="assembly"></span><span id="ASSEMBLY"></span>**Assemblea**
</dt> <dd>

Elemento contenitore. Il primo sottoelemento deve essere **un elemento assemblyIdentity** **o noInheritable.** Il manifesto dell'assembly descrive in modo univoco l'assembly side-by-side identificato da **assemblyIdentity.** Obbligatorio.

L'elemento assembly deve essere nello spazio dei nomi "urn:schemas-microsoft-com:asm.v1". Anche gli elementi figlio dell'assembly devono essere in questo spazio dei nomi, per ereditarietà o tramite l'assegnazione di tag.

**L'elemento assembly** ha l'attributo seguente.



| Attributo           | Descrizione                                           |
|---------------------|-------------------------------------------------------|
| **manifestVersion** | **L'attributo manifestVersion** deve essere impostato su 1.0. |



 

</dd> <dt>

<span id="noInheritable"></span><span id="noinheritable"></span><span id="NOINHERITABLE"></span>**noInheritable**
</dt> <dd>

Includere questo elemento in un manifesto dell'assembly per indicare che l'assembly gestisce i [contesti di attivazione](activation-contexts.md) e i relativi oggetti. **L'elemento noInheritable** deve essere un sottoelemento di un **elemento assembly.** **L'elemento assemblyIdentity** deve essere successivo a qualsiasi **elemento noInheritable.** **L'elemento noInheritable** è obbligatorio nel manifesto dell'assembly se l'assembly viene usato da qualsiasi manifesto dell'applicazione che include l'elemento **noInherit.** [](application-manifests.md) Un **elemento noInheritable** in un manifesto dell'applicazione non ha alcun effetto. Un **elemento noInheritable** non ha elementi figlio.

</dd> <dt>

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>**Assemblyidentity**
</dt> <dd>

Descrive e identifica in modo univoco un assembly side-by-side.

Come primo sottoelemento di un elemento **assembly,** **assemblyIdentity** descrive e identifica in modo univoco l'assembly side-by-side proprietario del manifesto dell'assembly. Questa operazione è denominata **assemblyIdentity** del contesto DEF del manifesto dell'assembly.

Come primo sottoelemento di un elemento **dependentAssembly,** **assemblyIdentity** descrive e identifica in modo univoco un assembly side-by-side usato da **def-context assemblyIdentity**. Questa operazione viene definita **assemblyIdentità** del contesto REF del manifesto dell'assembly. L'assembly def-context richiede che l'assembly ref-context funzioni correttamente. Si noti che ogni **assemblyIdentity** del contesto REF deve corrispondere esattamente a un **assemblyIdentity** del contesto DEF corrispondente nel manifesto dell'assembly di riferimento.

Questo elemento non ha sottoelementi. **L'elemento assemblyIdentity** dispone degli attributi seguenti.



| Attributo                 | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **type**                  | Specifica il tipo di assembly. Il valore deve essere win32 e in lettere minuscole. Obbligatorio.                                                                                                                                                                                                                                                                                                                                                         |
| **nome**                  | Nome univoco dell'assembly. Usare il formato seguente per il nome dell'assembly: Organization.Division.Name. Ad esempio, Microsoft. Windows.mysampleAsm. Obbligatorio. Si noti che nel caso di una DLL in pacchetto come assembly privato con un file manifesto separato, il nome dell'assembly deve essere diverso dal nome della DLL e del manifesto.<br/>                                                                              |
| **language**              | Identifica la lingua dell'assembly. facoltativo. Se l'assembly è specifico del linguaggio, specificare il codice del linguaggio DHTML. Nell'assembly **DEF-contextIdentity di** un manifesto dell'assembly destinato all'uso in tutto il mondo (indipendente dalla lingua) omettere l'attributo language.<br/> In un assembly di contesto **REFIdentità** di un manifesto dell'assembly destinato all'uso in tutto il mondo (indipendente dalla lingua) impostare il valore di language su " \* ".<br/> |
| **processorArchitecture** | Specifica il processore. I valori validi sono x86 per i Windows a 32 bit e ia64 per le versioni a 64 bit Windows. facoltativo.                                                                                                                                                                                                                                                                                                                               |
| **version**               | Specifica la versione dell'assembly. Usare il formato di versione in quattro parti: mmmmm.nnnnn.ooooo.ppppp. Ognuna delle parti separate da punti può essere compresa tra 0 e 65535 inclusi. Per altre informazioni, vedere [Versioni degli assembly.](assembly-versions.md) Obbligatorio.                                                                                                                                                                                               |
| **Publickeytoken**        | Stringa esadecimale di 16 caratteri che rappresenta gli ultimi 8 byte dell'hash SHA-1 della chiave pubblica con cui viene firmato l'assembly. La chiave pubblica usata per firmare il catalogo deve essere di 2048 bit o superiore. Obbligatorio per gli assembly side-by-side condivisi.                                                                                                                                                                                |



 

</dd> <dt>

<span id="dependency"></span><span id="DEPENDENCY"></span>**Dipendenza**
</dt> <dd>

Elemento contenitore che include almeno un **dependentAssembly.** Il primo sottoelemento deve essere un **elemento dependentAssembly.** Una **dipendenza non** ha attributi. facoltativo.

</dd> <dt>

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>**dependentAssembly**
</dt> <dd>

Il primo sottoelemento deve essere un elemento **assemblyIdentity** che descrive e identifica in modo univoco un assembly side-by-side usato dall'assembly side-by-side proprietario del manifesto dell'assembly. Ogni **dependentAssembly deve** essere all'interno di una **sola dipendenza.** facoltativo.

</dd> <dt>

<span id="file"></span><span id="FILE"></span>**File**
</dt> <dd>

Contiene i file utilizzati da un assembly side-by-side. Contiene **sottoelementi comClass**, **typelib**, **windowClass**, **comInterfaceProxyStub.** facoltativo.

**L'elemento file** ha gli attributi seguenti.



| Attributo   | Descrizione                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| **nome**    | Nome del file, ad esempio Conctl32.dll.                                                            |
| **hashalg** | Algoritmo utilizzato per creare un hash del file. Questo valore deve essere SHA1.                                 |
| **hash**    | Hash del file a cui si fa riferimento in base al nome. Stringa esadecimale di lunghezza a seconda dell'algoritmo hash. |



 

</dd> <dt>

<span id="comClass"></span><span id="comclass"></span><span id="COMCLASS"></span>**Classe comClass**
</dt> <dd>

Sottoelemento di un **elemento file.** facoltativo.

**L'elemento comClass** ha gli attributi seguenti.



| Attributo               | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **description**         | Nome della classe.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Clsid**               | GUID che identifica in modo univoco la classe . Obbligatorio. Il valore deve essere nel formato di un GUID valido.                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **Threadingmodel**      | Modello di threading utilizzato dalle classi COM in-process. Se questa proprietà è Null, non viene usato alcun modello di threading. Il componente viene creato nel thread principale del client e viene effettuato il marshalling delle chiamate da altri thread a questo thread. facoltativo. I valori validi sono: "Apartment", "Free", "Both" e "Neutral".                                                                                                                                                                                                                         |
| **tlbid**               | GUID per la libreria dei tipi per questo componente COM. Il valore deve essere nel formato di un GUID. facoltativo.                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Progid**              | Identificatore a livello di codice dipendente dalla versione associato al componente COM. Il formato di un ProgID è <*del* fornitore>.<componente *>.<* *versione*>.                                                                                                                                                                                                                                                                                                                                                                      |
| **miscStatus**          | Duplica nel manifesto dell'assembly le informazioni fornite dalla chiave del Registro di sistema MiscStatus. Se i valori per gli attributi **miscStatusIcon**, **miscStatusContent**, **miscStatusDocprint** o **miscStatusThumbnail** non vengono trovati, per gli attributi mancanti viene usato il valore predefinito corrispondente elencato in **miscStatus.** Il valore può essere un elenco delimitato da virgole dei valori degli attributi della tabella seguente. È possibile usare questo attributo se la classe COM è una classe OCX che richiede valori della chiave del Registro di sistema Miscstatus. |
| **miscStatusIcon**      | Duplica nel manifesto dell'assembly le informazioni fornite da DVASPECT \_ ICON. Può fornire un'icona di un oggetto. Il valore può essere un elenco delimitato da virgole dei valori degli attributi della tabella seguente. È possibile usare questo attributo se la classe COM è una classe OCX che richiede valori della chiave del Registro di sistema Miscstatus.                                                                                                                                                                                                                |
| **miscStatusContent**   | Duplica nel manifesto dell'assembly le informazioni fornite da DVASPECT \_ CONTENT. Può fornire un documento composto visualizzabile per uno schermo o una stampante. Il valore può essere un elenco delimitato da virgole dei valori degli attributi della tabella seguente. È possibile usare questo attributo se la classe COM è una classe OCX che richiede valori della chiave del Registro di sistema Miscstatus.                                                                                                                                                                          |
| **miscStatusDocprint**  | Duplica nel manifesto dell'assembly le informazioni fornite da DVASPECT \_ DOCPRINT. Può fornire una rappresentazione dell'oggetto visualizzabile sullo schermo come se fosse stampata su una stampante. Il valore può essere un elenco delimitato da virgole dei valori degli attributi della tabella seguente. È possibile usare questo attributo se la classe COM è una classe OCX che richiede valori della chiave del Registro di sistema Miscstatus.                                                                                                                                               |
| **miscStatusThumbnail** | Duplica in un manifesto dell'assembly le informazioni fornite da DVASPECT \_ THUMBNAIL. Può fornire un'anteprima di un oggetto visualizzabile in uno strumento di esplorazione. Il valore può essere un elenco delimitato da virgole dei valori degli attributi della tabella seguente. È possibile usare questo attributo se la classe COM è una classe OCX che richiede valori della chiave del Registro di sistema Miscstatus.                                                                                                                                                                         |



 

**L'elemento comClass** può avere &lt; elementi progid ... come elementi &gt; </progid> figlio, che elencano i progid dipendenti dalla versione.

L'esempio seguente mostra un **elemento comClass** incluso in un **elemento file.**

``` syntax
<file name="sampleu.dll">
        <comClass description="Font Property Page"
    clsid="{0BE35200-8F91-11CE-9DE3-00AA004BB851}"
          threadingModel = "Both"
             tlbid = "{44EC0535-400F-11D0-9DCD-00A0C90391D3}"/>
        <comClass description="Color Property Page"
    clsid="{0BE35201-8F91-11CE-9DE3-00AA004BB851}" 
    progid="ABC.Registrar"/>
    </file>
```

Se la classe COM è una classe OCX che richiede la sottochiave del Registro di sistema MiscStatus per specificare come creare e visualizzare un oggetto, è possibile abilitare l'oggetto duplicando queste informazioni nel manifesto dell'assembly. Specificare le caratteristiche dell'oggetto usando gli attributi **miscStatus**, **miscStatusIcon**, **miscStatusContent**, **miscStatusDocprint** e **miscStatusThumbnail** dell'elemento **comClass.** Impostare questi attributi su un elenco delimitato da virgole di valori di attributo della tabella seguente. Questi attributi duplicano le informazioni che verrebbero fornite da un'enumerazione DVASPECT. Se non viene trovato alcun valore per **miscStatusIcon**, **miscStatusContent**, **miscStatusDocprint** o **miscStatusThumbnail**, vengono usati i valori predefiniti specificati in **miscStatus.** Usare i valori degli attributi della tabella seguente. Corrispondono ai flag di bit di [**un'enumerazione OLEMISC.**](/windows/win32/api/oleidl/ne-oleidl-olemisc)



| Valore dell'attributo              | Costante OLEMISC                      |
|------------------------------|---------------------------------------|
| recomposeonresize            | OLEMISC \_ RECOMPOSEONRESIZE            |
| onlyiconic                   | OLEMISC \_ ONLYICONIC                   |
| insertnotreplace             | OLEMISC \_ INSERTNOTREPLACE             |
| static                       | OLEMISC \_ STATIC                       |
| cantlinkinside               | OLEMISC \_ CANTLINKINSIDE               |
| canlinkbyole1                | OLEMISC \_ CANLINKBYOLE1                |
| islinkobject                 | OLEMISC \_ ISLINKOBJECT                 |
| insideout                    | OLEMISC \_ INSIDEOUT                    |
| activatewhenvisible          | OLEMISC \_ ACTIVATEWHENVISIBLE          |
| renderingisdeviceindependent | RENDERING \_ OLEMISCISDEVICEINDEPENDENT |
| invisibleatruntime           | OLEMISC \_ INVISIBLEATRUNTIME           |
| alwaysrun                    | OLEMISC \_ ALWAYSRUN                    |
| actslikebutton               | OLEMISC \_ ACTSLIKEBUTTON               |
| actslikelabel                | OLEMISC \_ ACTSLIKELABEL                |
| nouiactivate                 | OLEMISC \_ NOUIACTIVATE                 |
| allineabile                    | OLEMISC \_ ALIGNABLE                    |
| simpleframe                  | OLEMISC \_ SIMPLEFRAME                  |
| setclientsitefirst           | OLEMISC \_ SETCLIENTSITEFIRST           |
| Imemode                      | TOLEMISC \_ IMEMODE                     |
| ignoreativatewhenvisible     | OLEMISC \_ IGNOREACTIVATEWHENVISIBLE    |
| wantstomenumerge             | OLEMISC \_ WANTSTOMENUMERGE             |
| supportsmultilevelundo       | OLEMISC \_ SUPPORTAMULTILEVELUNDO       |



 

</dd> <dt>

<span id="typelib"></span><span id="TYPELIB"></span>**Typelib**
</dt> <dd>

Sottoelemento di un **elemento file.** facoltativo.

**L'elemento typelib** ha gli attributi illustrati nella tabella seguente.



| Attributo      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **tlbid**      | ID univoco della libreria dei tipi. Obbligatorio.                                                                                                                                                                                                                                                                                                                                                                                    |
| **version**    | Numero di versione in due parti della libreria dei tipi. Se aumenta solo il numero di versione secondaria, tutte le funzionalità della libreria dei tipi precedente sono supportate in modo compatibile. Se il numero di versione principale cambia, il codice compilato nella libreria dei tipi deve essere ricompilato. Il numero di versione della libreria dei tipi può essere diverso dal numero di versione dell'applicazione. Obbligatorio.                                      |
| **helpdir**    | Directory in cui si trova il file della Guida per i tipi nella libreria dei tipi. Se l'applicazione supporta librerie dei tipi per più linguaggi, le librerie possono fare riferimento a nomi di file diversi nella directory dei file della Guida. Se non è presente alcun valore, specificare "". Obbligatorio.                                                                                                                                                          |
| **Resourceid** | Rappresentazione di stringa esadecimale dell'identificatore delle impostazioni locali (LCID). È da una a quattro cifre esadecimali senza prefisso 0x e senza zeri iniziali. L'identificatore LCID può avere un identificatore di sottolinguaggio neutro. Per altre informazioni, vedere [Identificatori delle impostazioni locali](/windows/desktop/Intl/locale-identifiers). facoltativo.                                                                                                                                      |
| **flags**      | Rappresentazione di stringa dei flag della libreria dei tipi per questa libreria dei tipi. In particolare, deve essere tra "RESTRICTED", "CONTROL", "HIDDEN" e "HASDISKIMAGE". Questi sono i valori [**dell'enumerazione LIBFLAGS**](/windows/win32/api/oaidl/ne-oaidl-libflags) e sono gli stessi flag specificati nel *parametro uLibFlags* del metodo [**ICreateTypeLib::SetLibFlags.**](/windows/win32/api/oaidl/nf-oaidl-icreatetypelib-setlibflags) facoltativo. |



 

Nell'esempio seguente viene illustrato un **elemento typelib** incluso in un **elemento file.**

``` syntax
<file name="sampleu.dll">
       <typelib tlbid="{44EC0535-400F-11D0-9DCD-00A0C90391D3}"
       version="1.0" helpdir=""/>
</file>
```

</dd> <dt>

<span id="comInterfaceExternalProxyStub"></span><span id="cominterfaceexternalproxystub"></span><span id="COMINTERFACEEXTERNALPROXYSTUB"></span>**comInterfaceExternalProxyStub**
</dt> <dd>

**comInterfaceExternalProxyStub** è un sottoelemento di un elemento **assembly** e viene usato per le interfacce di automazione. Ad esempio, [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) e le relative interfacce derivate. facoltativo.

L'implementazione predefinita di proxy-stub è adeguata per la maggior parte delle interfacce di automazione, ad esempio le interfacce derivate da [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch). Lo stub del proxy di interfaccia e tutte le altre implementazioni dell'interfaccia proxy-stub esterne devono essere elencati in **comInterfaceExternalProxyStub**. **L'elemento comInterfaceExternalProxyStub** ha gli attributi illustrati nella tabella seguente.



| Attributo         | Descrizione                                                                                                                                                                                 |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Iid**           | IID dell'interfaccia per cui viene dichiarato il proxy. Obbligatorio. Il valore deve essere nel formato: "{iid}".                                                                         |
| **baseInterface** | IID dell'interfaccia da cui deriva quello descritto dall'attributo **iid.** Questo attributo è facoltativo. Il valore deve essere nel formato: "{iid}".                            |
| **numMethods**    | Numero di metodi implementati dall'interfaccia . Questo attributo è facoltativo. Il valore deve essere nel formato: "n".                                                                       |
| **nome**          | Nome dell'interfaccia così come verrebbe visualizzata nel codice. Ad esempio, "IViewObject". Non deve essere una stringa descrittiva. Questo attributo è facoltativo. Il valore deve essere nel formato "name". |
| **tlbid**         | Libreria dei tipi che contiene la descrizione dell'interfaccia specificata **dall'attributo iid.** Questo attributo è facoltativo. Il valore deve essere nel formato: "{tlbid}" .                |
| proxyStubClsid32  | Mappe un IID a un CLSID nelle DLL proxy a 32 bit.                                                                                                                                                |



 

L'esempio seguente illustra **un elemento comInterfaceExternalProxyStub.**

``` syntax
<comInterfaceExternalProxyStub 
  name="IAxWinAmbientDispatch" 
    iid="{B6EA2051-048A-11D1-82B9-00C04FB9942E}" 
    numMethods="35" 
  baseInterface="{00000000-0000-0000-C000-000000000046}"/>
```

</dd> <dt>

<span id="comInterfaceProxyStub"></span><span id="cominterfaceproxystub"></span><span id="COMINTERFACEPROXYSTUB"></span>**comInterfaceProxyStub**
</dt> <dd>

Sottoelemento di un **elemento file.** facoltativo.

Se un file nell'assembly implementa uno stub proxy, il tag di file corrispondente deve includere un sottoelemento **comInterfaceProxyStub** con attributi identici a un **elemento comInterfaceProxyStub.** Il marshalling delle interfacce tra processi e thread potrebbe non funzionare come previsto se si omettono alcune delle dipendenze **comInterfaceProxyStub** per il componente.

**L'elemento comInterfaceProxyStub** ha gli attributi seguenti.



| Attributo            | Descrizione                                                                                                                                                                                                                                                                                                 |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Iid**              | Le. IID dell'interfaccia per cui viene dichiarato il proxy. Obbligatorio. Il valore deve essere nel formato: "{iid}".                                                                                                                                                                                        |
| **nome**             | Nome dell'interfaccia così come verrebbe visualizzata nel codice. Ad esempio, "IViewObject". Non deve essere una stringa descrittiva. Questo attributo è facoltativo. Il valore deve essere nel formato "name".                                                                                                                 |
| **tlbid**            | Libreria dei tipi che contiene la descrizione dell'interfaccia specificata **dall'attributo iid.** Questo attributo è facoltativo. Il valore deve essere nel formato: "{tlbid}".                                                                                                                                 |
| **baseInterface**    | IID dell'interfaccia da cui deriva quello descritto dall'attributo **iid.** Questo attributo è facoltativo. Il valore deve essere nel formato: "{iid}".                                                                                                                                            |
| **numMethods**       | Numero di metodi implementati dall'interfaccia . Questo attributo è facoltativo. Il valore deve essere nel formato: "n".                                                                                                                                                                                       |
| **proxyStubClsid32** | Mappe un IID a un CLSID nelle DLL proxy a 32 bit.                                                                                                                                                                                                                                                                |
| **Threadingmodel**   | Modello di threading usato dalle classi COM in-process. Se questa proprietà è Null, non viene usato alcun modello di threading. Il componente viene creato nel thread principale del client e viene effettuato il marshalling delle chiamate da altri thread a questo thread. facoltativo. I valori validi sono: "Apartment", "Free", "Both" e "Neutral". |



 

</dd> <dt>

<span id="windowclass"></span><span id="WINDOWCLASS"></span>**windowclass**
</dt> <dd>

Nome di una classe windows di cui eseguire il controllo delle versioni. **L'elemento windowclass** ha l'attributo seguente.



| Attributo     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **con controllo delle versioni** | Questo attributo controlla se il nome della classe della finestra interna utilizzato nella registrazione contiene o meno la versione dell'assembly contenente la classe della finestra. Il valore di questo attributo può essere "sì" o "no". Il valore predefinito è "sì". Il valore "no" deve essere usato solo se la stessa classe di finestra è definita da un componente side-by-side e da un componente non side-by-side equivalente e si vuole considerarli come la stessa classe finestra. Si noti che le regole consuete sulla registrazione della classe finestra si applicano solo al primo componente che registra la classe della finestra, perché non è con controllo delle versioni. |



 

L'esempio seguente illustra un **elemento windowclass** incluso in un **elemento file.**

``` syntax
<file name="comctl32.dll">
        <windowClass versioned="no">ToolbarWindow32</windowClass>
</file>
```

</dd> </dl>

## <a name="example"></a>Esempio

Di seguito è riportato un esempio di manifesto dell'assembly.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" 
manifestVersion="1.0">
    <assemblyIdentity type="win32" name="Microsoft.Tools.SampleAssembly" version="6.0.0.0" processorArchitecture="x86" publicKeyToken="0000000000000000"/>
    <file name="sampleu.dll" hash="3eab067f82504bf271ed38112a4ccdf46094eb5a" hashalg="SHA1">
        <comClass description="Font Property Page" clsid="{0BE35200-8F91-11CE-9DE3-00AA004BB851}"/>
        <comClass description="Color Property Page" clsid="{0BE35201-8F91-11CE-9DE3-00AA004BB851}"/>
        <comClass description="Picture Property Page" clsid="{0BE35202-8F91-11CE-9DE3-00AA004BB851}"/>
    </file>
    <file name="bar.dll" hash="ac72753e5bb20446d88a48c8f0aaae769a962338" hashalg="SHA1"/>
    <file name="foo.dll" hash="a7312a1f6cfb46433001e0540458de60adcd5ec5" hashalg="SHA1">
        <comClass description="Registrar Class" clsid="{44EC053A-400F-11D0-9DCD-00A0C90391D3}" progid="ATL.Registrar"/>
    <comInterfaceProxyStub iid="{B6EA2051-048A-11D1-82B9-00C04FB9942E}" name=" IAxWinAmbientDispatch " tlbid="{34EC053A-400F-11D0-9DCD-00A0C90391D3}"/>
        <typelib tlbid="{44EC0535-400F-11D0-9DCD-00A0C90391D3}" version="1.0" helpdir=""/>
    </file>
    <file name="sampledll.dll" hash="ba62960ceb15073d2598379307aad84f3a73dfcb" hashalg="SHA1"/>
<windowClass>ToolbarWindow32</windowClass>
        <windowClass>ComboBoxEx32</windowClass>
        <windowClass>sample_trackbar32</windowClass>
        <windowClass>sample_updown32</windowClass>
</assembly>
```

 

