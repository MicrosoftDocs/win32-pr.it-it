---
description: Un manifesto dell'assembly è un file XML che descrive un assembly affiancato.
ms.assetid: f7973019-0a80-498e-adf1-c66267c813f4
title: Manifesti dell'assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 254702d5044331fa5d47def815556dbd8edef2f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232053"
---
# <a name="assembly-manifests"></a>Manifesti dell'assembly

Un manifesto dell'assembly è un file XML che descrive un assembly affiancato. I manifesti dell'assembly descrivono i nomi e le versioni degli assembly affiancati, i file e le risorse dell'assembly, nonché la dipendenza dell'assembly sugli altri assembly affiancati. Per correggere l'installazione, l'attivazione e l'esecuzione di assembly side-by-Side è necessario che il manifesto dell'assembly accompagni sempre un assembly nel sistema.

Per un elenco completo delle XML Schema, vedere [schema del file manifesto](manifest-file-schema.md).

I manifesti dell'assembly hanno gli elementi e gli attributi seguenti.



| Elemento                           | Attributi                | Necessario |
|-----------------------------------|---------------------------|----------|
| **assembly**                      |                           | Sì      |
|                                   | **manifestVersion**       | Sì      |
| **noInheritable**                 |                           | No       |
| **assemblyIdentity**              |                           | Sì      |
|                                   | **type**                  | Sì      |
|                                   | **nome**                  | Sì      |
|                                   | **language**              | No       |
|                                   | **processorArchitecture** | No       |
|                                   | **version**               | Sì      |
|                                   | **publicKeyToken**        | No       |
| **dipendenza**                    |                           | No       |
| **dependentAssembly**             |                           | No       |
| **file**                          |                           | No       |
|                                   | **nome**                  | Sì      |
|                                   | **hashAlg**               | No       |
|                                   | **hash**                  | No       |
| **comClass**                      |                           | No       |
|                                   | **description**           | No       |
|                                   | **CLSID**                 | Sì      |
|                                   | **threadingModel**        | No       |
|                                   | **tlbid**                 | No       |
|                                   | **ProgID**                | No       |
|                                   | **miscStatus**            | No       |
|                                   | **miscStatusIcon**        | No       |
|                                   | **miscStatusContent**     | No       |
|                                   | **miscStatusDocPrint**    | No       |
|                                   | **miscStatusDocPrint**    | No       |
| **TypeLib**                       |                           | No       |
|                                   | **tlbid**                 | Sì      |
|                                   | **version**               | Sì      |
|                                   | **HELPDIR**               | Sì      |
|                                   | **ResourceId**            | No       |
|                                   | **flags**                 | No       |
| **comInterfaceExternalProxyStub** |                           | No       |
|                                   | **IID**                   | Sì      |
|                                   | **baseInterface**         | No       |
|                                   | **numMethods**            | No       |
|                                   | **nome**                  | No       |
|                                   | **tlbid**                 | No       |
|                                   | **proxyStubClsid32**      | No       |
| **comInterfaceProxyStub**         |                           | No       |
|                                   | **IID**                   | Sì      |
|                                   | **nome**                  | Sì      |
|                                   | **tlbid**                 | No       |
|                                   | **baseInterface**         | No       |
|                                   | **numMethods**            | No       |
|                                   | **proxyStubClsid32**      | No       |
|                                   | **threadingModel**        | No       |
| **windowClass**                   |                           | No       |
|                                   | **versione**             | No       |



 

## <a name="file-location"></a>Percorso file

I manifesti dell'assembly possono essere installati in tre posizioni:

-   Come manifesti che accompagnano gli [assembly condivisi](/windows/desktop/Msi/shared-assemblies), i manifesti dell'assembly devono essere installati come file distinti nell'assembly cache affiancato. Si tratta in genere della cartella WinSxS nella directory Windows.
-   Come manifesti che accompagnano [assembly privati](/windows/desktop/Msi/private-assemblies), i manifesti dell'assembly devono essere installati nella struttura di directory dell'applicazione. Si tratta in genere di un file separato nella stessa cartella del file eseguibile dell'applicazione.
-   Come risorsa in una DLL, l'assembly è disponibile per l'utilizzo privato della DLL. Un manifesto dell'assembly non può essere incluso come risorsa in un file EXE. Un file EXE può includere un [manifesto dell'applicazione](application-manifests.md) come risorsa.

## <a name="file-name-syntax"></a>Sintassi del nome file

Il nome di un manifesto dell'assembly è un nome file valido seguito da. manifest.

Ad esempio, un manifesto dell'assembly che fa riferimento a MyAssembly utilizzerebbe la sintassi del nome file seguente. È possibile omettere il campo <*ID risorsa*> se il manifesto dell'assembly viene installato come file separato o se l'ID risorsa è 1.

<dl> MyAssembly. <resource ID> .. manifesto
</dl>

> [!Note]  
> A causa del modo in cui gli assembly privati vengono ricercati side-by-Side, le restrizioni di denominazione seguenti si applicano quando si crea il pacchetto di una DLL come assembly privato. Una procedura consigliata consiste nell'inserire il manifesto dell'assembly nella DLL come risorsa. In questo caso, l'ID risorsa deve essere uguale a 1 e il nome dell'assembly privato può corrispondere al nome della DLL. Se, ad esempio, il nome della DLL è Microsoft.Windows.mysample.dll, anche il valore dell'attributo Name usato nell'elemento **assemblyIdentity** del manifesto potrebbe essere Microsoft. Windows. di esempio. Una modalità alternativa consiste nell'inserire il manifesto dell'assembly in un file separato. In questo caso, il nome dell'assembly e il relativo manifesto devono essere diversi dal nome della DLL. Ad esempio, Microsoft. Windows. mysampleAsm, Microsoft. Windows. mysampleAsm. manifest e Microsoft.Windows.Mysample.dll. Per altre informazioni su come eseguire ricerche affiancate degli assembly privati, vedere sequenza di [ricerca degli assembly](assembly-searching-sequence.md).

 

## <a name="elements"></a>Elementi

I nomi degli elementi e degli attributi distinguono tra maiuscole e minuscole. I valori degli elementi e degli attributi non fanno distinzione tra maiuscole e minuscole, ad eccezione del valore dell'attributo Type.

<dl> <dt>

<span id="assembly"></span><span id="ASSEMBLY"></span>**assembly**
</dt> <dd>

Elemento contenitore. Il primo sottoelemento deve essere un elemento **assemblyIdentity** o **noInheritable** . Il manifesto dell'assembly descrive in modo univoco l'assembly affiancato identificato da **assemblyIdentity**. Obbligatorio.

L'elemento assembly deve trovarsi nello spazio dei nomi "urn: schemas-microsoft-com: ASM. V1". Gli elementi figlio dell'assembly devono trovarsi anche in questo spazio dei nomi, in base all'ereditarietà o all'assegnazione di tag.

L'elemento **assembly** presenta l'attributo seguente.



| Attributo           | Descrizione                                           |
|---------------------|-------------------------------------------------------|
| **manifestVersion** | L'attributo **manifestVersion** deve essere impostato su 1,0. |



 

</dd> <dt>

<span id="noInheritable"></span><span id="noinheritable"></span><span id="NOINHERITABLE"></span>**noInheritable**
</dt> <dd>

Includere questo elemento in un manifesto dell'assembly per indicare che l'assembly gestisce i [contesti di attivazione](activation-contexts.md) e i relativi oggetti. L'elemento **noInheritable** deve essere un sottoelemento di un elemento **assembly** . L'elemento **assemblyIdentity** deve essere seguito da qualsiasi elemento non **ereditabile** . L'elemento **noInheritable** è obbligatorio nel manifesto dell'assembly se l'assembly viene usato da qualsiasi [manifesto dell'applicazione](application-manifests.md) che include l'elemento **NoInherit** . Un elemento non **ereditabile** in un manifesto dell'applicazione non ha alcun effetto. Un elemento non **ereditabile** non ha elementi figlio.

</dd> <dt>

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>**assemblyIdentity**
</dt> <dd>

Descrive e identifica in modo univoco un assembly side-by-side.

Come primo sottoelemento di un elemento **assembly** , **assemblyIdentity** descrive e identifica in modo univoco l'assembly affiancato proprietario del manifesto dell'assembly. Questo metodo è denominato **assemblyIdentity** del contesto def del manifesto dell'assembly.

Come primo sottoelemento di un elemento **dependentAssembly** , **assemblyIdentity** descrive e identifica in modo univoco un assembly side-by-side usato da **assemblyIdentity** del contesto def. Questo metodo è denominato **assemblyIdentity** del contesto di riferimento del manifesto dell'assembly. Per il corretto funzionamento dell'assembly del contesto di riferimento. Si noti che ogni **assemblyIdentity** del contesto di riferimento deve corrispondere esattamente a un oggetto **ASSEMBLYIDENTITY** del contesto def corrispondente nel manifesto dell'assembly a cui si fa riferimento.

Questo elemento non contiene sottoelementi. L'elemento **assemblyIdentity** ha gli attributi seguenti.



| Attributo                 | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **type**                  | Specifica il tipo di assembly. Il valore deve essere Win32 e in lettere minuscole. Obbligatorio.                                                                                                                                                                                                                                                                                                                                                         |
| **nome**                  | Assegna un nome univoco all'assembly. Usare il formato seguente per il nome dell'assembly: Organization.Division.Name. Ad esempio, Microsoft. Windows. mysampleAsm. Obbligatorio. Si noti che nel caso di una DLL assemblata come assembly privato con un file manifesto separato, il nome dell'assembly deve essere diverso dal nome della DLL e dal manifesto.<br/>                                                                              |
| **language**              | Identifica la lingua dell'assembly. facoltativo. Se l'assembly è specifico della lingua, specificare il codice della lingua DHTML. Nell'oggetto **assemblyIdentity** del contesto def di un manifesto dell'assembly progettato per l'uso in tutto il mondo (indipendente dal linguaggio) omettere l'attributo Language.<br/> In un oggetto **assemblyIdentity** del contesto di riferimento di un manifesto dell'assembly progettato per l'uso in tutto il mondo (indipendente dalla lingua), impostare il valore della lingua su " \* ".<br/> |
| **processorArchitecture** | Specifica il processore. I valori validi sono x86 per Windows a 32 bit e ia64 per Windows a 64 bit. facoltativo.                                                                                                                                                                                                                                                                                                                               |
| **version**               | Specifica la versione dell'assembly. Usare il formato di versione in quattro parti: mmmm. NNNNN. ooooo. ppppp. Ognuna delle parti separate da punti può essere 0-65535 inclusi. Per altre informazioni, vedere [versioni degli assembly](assembly-versions.md). Obbligatorio.                                                                                                                                                                                               |
| **publicKeyToken**        | Stringa esadecimale di 16 caratteri che rappresenta gli ultimi 8 byte dell'hash SHA-1 della chiave pubblica in cui è firmato l'assembly. La chiave pubblica usata per firmare il catalogo deve essere di 2048 bit o superiore. Obbligatorio per gli assembly affiancati condivisi.                                                                                                                                                                                |



 

</dd> <dt>

<span id="dependency"></span><span id="DEPENDENCY"></span>**dipendenza**
</dt> <dd>

Elemento contenitore che include almeno un **dependentAssembly**. Il primo sottoelemento deve essere un elemento **dependentAssembly** . Una **dipendenza** non ha attributi. facoltativo.

</dd> <dt>

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>**dependentAssembly**
</dt> <dd>

Il primo sottoelemento deve essere un elemento **assemblyIdentity** che descrive e identifica in modo univoco un assembly affiancato usato dall'assembly affiancato che possiede questo manifesto dell'assembly. Ogni **dependentAssembly** deve trovarsi all'interno di una sola **dipendenza**. facoltativo.

</dd> <dt>

<span id="file"></span><span id="FILE"></span>**file**
</dt> <dd>

Contiene i file utilizzati da un assembly affiancato. Contiene sottoelementi **ComClass**, **typelib**, **WindowClass**, **comInterfaceProxyStub** . facoltativo.

L'elemento **file** ha gli attributi seguenti.



| Attributo   | Descrizione                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| **nome**    | Nome del file, ad esempio Conctl32.dll.                                                            |
| **hashAlg** | Algoritmo utilizzato per creare un hash del file. Questo valore deve essere SHA1.                                 |
| **hash**    | Hash del file a cui si fa riferimento in base al nome. Stringa esadecimale di lunghezza, a seconda dell'algoritmo hash. |



 

</dd> <dt>

<span id="comClass"></span><span id="comclass"></span><span id="COMCLASS"></span>**comClass**
</dt> <dd>

Sottoelemento di un elemento **file** . facoltativo.

L'elemento **ComClass** ha gli attributi seguenti.



| Attributo               | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **description**         | Nome della classe.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **CLSID**               | GUID che identifica in modo univoco la classe. Obbligatorio. Il valore deve essere nel formato di un GUID valido.                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **threadingModel**      | Modello di threading utilizzato dalle classi COM in-process. Se questa proprietà è null, non viene utilizzato alcun modello di Threading. Il componente viene creato nel thread principale del client e viene effettuato il marshalling di chiamate da altri thread a questo thread. facoltativo. I valori validi sono: "Apartment", "Free", "both" e "neutral".                                                                                                                                                                                                                         |
| **tlbid**               | GUID della libreria dei tipi per il componente COM. Il valore deve essere nel formato di un GUID. facoltativo.                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **ProgID**              | Identificatore a livello di codice dipendente dalla versione associato al componente COM. Il formato di un ProgID è <*fornitore*>. <*componente*>. <*versione*>.                                                                                                                                                                                                                                                                                                                                                                      |
| **miscStatus**          | Duplicati nell'assembly manifesto le informazioni fornite dalla chiave del registro di sistema MiscStatus. Se non vengono trovati valori per gli attributi **miscStatusIcon**, **miscStatusContent**, **miscStatusDocprint** o **miscStatusThumbnail** , viene usato il valore predefinito corrispondente elencato in **miscStatus** per gli attributi mancanti. Il valore può essere un elenco delimitato da virgole dei valori di attributo della tabella seguente. È possibile utilizzare questo attributo se la classe COM è una classe OCX che richiede i valori della chiave del registro di sistema MiscStatus. |
| **miscStatusIcon**      | Duplicati nell'assembly manifesto le informazioni fornite dall'icona DVASPECT \_ . Può fornire un'icona di un oggetto. Il valore può essere un elenco delimitato da virgole dei valori di attributo della tabella seguente. È possibile utilizzare questo attributo se la classe COM è una classe OCX che richiede i valori della chiave del registro di sistema MiscStatus.                                                                                                                                                                                                                |
| **miscStatusContent**   | Duplicati nell'assembly manifesti le informazioni fornite dal contenuto di DVASPECT \_ . Può fornire un documento composito visualizzabile per una schermata o una stampante. Il valore può essere un elenco delimitato da virgole dei valori di attributo della tabella seguente. È possibile utilizzare questo attributo se la classe COM è una classe OCX che richiede i valori della chiave del registro di sistema MiscStatus.                                                                                                                                                                          |
| **miscStatusDocprint**  | Duplicati nell'assembly manifesto le informazioni fornite da DVASPECT \_ DOCPRINT. Può fornire una rappresentazione dell'oggetto visualizzabile sullo schermo come se fosse stampata su una stampante. Il valore può essere un elenco delimitato da virgole dei valori di attributo della tabella seguente. È possibile utilizzare questo attributo se la classe COM è una classe OCX che richiede i valori della chiave del registro di sistema MiscStatus.                                                                                                                                               |
| **miscStatusThumbnail** | Duplicati in un assembly manifesto le informazioni fornite dall'anteprima di DVASPECT \_ . Può fornire un'anteprima di un oggetto visualizzabile in uno strumento di esplorazione. Il valore può essere un elenco delimitato da virgole dei valori di attributo della tabella seguente. È possibile utilizzare questo attributo se la classe COM è una classe OCX che richiede i valori della chiave del registro di sistema MiscStatus.                                                                                                                                                                         |



 

L'elemento **ComClass** può avere elementi <progid>...</progid> come elementi figlio, che elencano i ProgID dipendenti dalla versione.

Nell'esempio seguente viene illustrato un elemento **ComClass** incluso in un elemento **file** .

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

Se la classe COM è una classe OCX che richiede la sottochiave del registro di sistema MiscStatus per specificare come creare e visualizzare un oggetto, è possibile abilitare l'oggetto duplicando queste informazioni nel manifesto dell'assembly. Specificare le caratteristiche dell'oggetto utilizzando gli attributi **miscStatus**, **miscStatusIcon**, **miscStatusContent**, **miscStatusDocprint** e **miscStatusThumbnail** dell'elemento **ComClass** . Impostare questi attributi su un elenco delimitato da virgole di valori di attributo della tabella seguente. Questi attributi duplicano le informazioni che verrebbero fornite da un'enumerazione DVASPECT. Se non viene trovato alcun valore per **miscStatusIcon**, **miscStatusContent**, **miscStatusDocprint** o **miscStatusThumbnail**, vengono usati i valori predefiniti specificati in **miscStatus** . Utilizzare i valori di attributo della tabella seguente. Questi corrispondono ai flag di bit di un'enumerazione [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc) .



| Valore dell'attributo              | Costante OLEMISC                      |
|------------------------------|---------------------------------------|
| recomposeonresize            | \_RECOMPOSEONRESIZE OLEMISC            |
| onlyiconic                   | \_ONLYICONIC OLEMISC                   |
| insertnotreplace             | \_INSERTNOTREPLACE OLEMISC             |
| static                       | OLEMISC \_ statico                       |
| cantlinkinside               | \_CANTLINKINSIDE OLEMISC               |
| canlinkbyole1                | \_CANLINKBYOLE1 OLEMISC                |
| islinkobject                 | \_ISLINKOBJECT OLEMISC                 |
| InsideOut                    | OLEMISC all' \_ interno                    |
| activatewhenvisible          | \_ACTIVATEWHENVISIBLE OLEMISC          |
| renderingisdeviceindependent | \_RENDERINGISDEVICEINDEPENDENT OLEMISC |
| invisibleatruntime           | \_INVISIBLEATRUNTIME OLEMISC           |
| alwaysrun                    | \_ALWAYSRUN OLEMISC                    |
| actslikebutton               | \_ACTSLIKEBUTTON OLEMISC               |
| actslikelabel                | \_ACTSLIKELABEL OLEMISC                |
| nouiactivate                 | \_NOUIACTIVATE OLEMISC                 |
| regolabile                    | OLEMISC \_ allineabile                    |
| simpleframe                  | \_SIMPLEFRAME OLEMISC                  |
| setclientsitefirst           | \_SETCLIENTSITEFIRST OLEMISC           |
| ImeMode                      | TOLEMISC \_ IMEMODE                     |
| ignoreativatewhenvisible     | \_IGNOREACTIVATEWHENVISIBLE OLEMISC    |
| wantstomenumerge             | \_WANTSTOMENUMERGE OLEMISC             |
| supportsmultilevelundo       | \_SUPPORTSMULTILEVELUNDO OLEMISC       |



 

</dd> <dt>

<span id="typelib"></span><span id="TYPELIB"></span>**TypeLib**
</dt> <dd>

Sottoelemento di un elemento **file** . facoltativo.

L'elemento **typelib** dispone degli attributi mostrati nella tabella seguente.



| Attributo      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **tlbid**      | ID univoco della libreria dei tipi. Obbligatorio.                                                                                                                                                                                                                                                                                                                                                                                    |
| **version**    | Numero di versione in due parti della libreria dei tipi. Se aumenta solo il numero di versione secondario, tutte le funzionalità della libreria dei tipi precedente sono supportate in modo compatibile. Se viene modificato il numero di versione principale, è necessario ricompilare il codice compilato con la libreria dei tipi. Il numero di versione della libreria dei tipi può essere diverso dal numero di versione dell'applicazione. Obbligatorio.                                      |
| **HELPDIR**    | Directory in cui si trova il file della Guida per i tipi nella libreria dei tipi. Se l'applicazione supporta le librerie dei tipi per più lingue, le librerie possono fare riferimento a nomi file diversi nella directory del file della guida. Se non è presente alcun valore, specificare "". Obbligatorio.                                                                                                                                                          |
| **ResourceId** | Rappresentazione in forma di stringa esadecimale dell'identificatore delle impostazioni locali (LCID). È da uno a quattro cifre esadecimali senza prefisso 0x e senza zeri iniziali. L'identificatore LCID può avere un identificatore di sottolingua neutro. Per ulteriori informazioni, vedere [identificatori delle impostazioni locali](/windows/desktop/Intl/locale-identifiers). facoltativo.                                                                                                                                      |
| **flags**      | Rappresentazione di stringa dei flag della libreria dei tipi per questa libreria dei tipi. In particolare, deve essere uno dei "Restricted", "CONTROL", "HIDDEN" e "HASDISKIMAGE". Questi sono i valori dell'enumerazione [**LIBFLAGS**](/windows/win32/api/oaidl/ne-oaidl-libflags) e sono gli stessi flag specificati nel parametro *ULibFlags* del metodo [**ICreateTypeLib:: SetLibFlags**](/windows/win32/api/oaidl/nf-oaidl-icreatetypelib-setlibflags) . facoltativo. |



 

Nell'esempio seguente viene illustrato un elemento **typelib** incluso in un elemento **file** .

``` syntax
<file name="sampleu.dll">
       <typelib tlbid="{44EC0535-400F-11D0-9DCD-00A0C90391D3}"
       version="1.0" helpdir=""/>
</file>
```

</dd> <dt>

<span id="comInterfaceExternalProxyStub"></span><span id="cominterfaceexternalproxystub"></span><span id="COMINTERFACEEXTERNALPROXYSTUB"></span>**comInterfaceExternalProxyStub**
</dt> <dd>

**ComInterfaceExternalProxyStub** è un sottoelemento di un elemento **assembly** e viene usato per le interfacce di automazione. Ad esempio [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) e le relative interfacce derivate. facoltativo.

L'implementazione predefinita dello stub proxy è adeguata per la maggior parte delle interfacce di automazione, ad esempio le interfacce derivate da [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch). Lo stub del proxy di interfaccia e tutte le altre implementazioni di interfacce dello stub proxy esterno devono essere elencate in **comInterfaceExternalProxyStub**. L'elemento **comInterfaceExternalProxyStub** ha gli attributi illustrati nella tabella seguente.



| Attributo         | Descrizione                                                                                                                                                                                 |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **IID**           | IID dell'interfaccia per cui viene dichiarato il proxy. Obbligatorio. Il valore deve essere nel formato: "{IID}".                                                                         |
| **baseInterface** | IID dell'interfaccia da cui deriva quello descritto dall'attributo **IID** . Questo attributo è facoltativo. Il valore deve essere nel formato: "{IID}".                            |
| **numMethods**    | Numero di metodi implementati dall'interfaccia. Questo attributo è facoltativo. Il valore deve essere nel formato: "n".                                                                       |
| **nome**          | Nome dell'interfaccia come verrebbe visualizzato nel codice. Ad esempio, "IViewObject". Non deve essere una stringa descrittiva. Questo attributo è facoltativo. Il valore deve essere nel formato: "nome". |
| **tlbid**         | Libreria dei tipi che contiene la descrizione dell'interfaccia specificata dall'attributo **IID** . Questo attributo è facoltativo. Il valore deve essere nel formato: "{TLBID}".                |
| proxyStubClsid32  | Esegue il mapping di un IID a un CLSID in DLL proxy a 32 bit.                                                                                                                                                |



 

Nell'esempio seguente viene illustrato un elemento **comInterfaceExternalProxyStub** .

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

Sottoelemento di un elemento **file** . facoltativo.

Se un file nell'assembly implementa uno stub proxy, il tag del file corrispondente deve includere un sottoelemento **comInterfaceProxyStub** con attributi identici a un elemento **comInterfaceProxyStub** . Il marshalling delle interfacce tra processi e thread potrebbe non funzionare come previsto se si ometteno alcune delle dipendenze di **comInterfaceProxyStub** per il componente.

L'elemento **comInterfaceProxyStub** ha gli attributi seguenti.



| Attributo            | Descrizione                                                                                                                                                                                                                                                                                                 |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **IID**              | Il. IID dell'interfaccia per cui viene dichiarato il proxy. Obbligatorio. Il valore deve essere nel formato: "{IID}".                                                                                                                                                                                        |
| **nome**             | Nome dell'interfaccia come verrebbe visualizzato nel codice. Ad esempio, "IViewObject". Non deve essere una stringa descrittiva. Questo attributo è facoltativo. Il valore deve essere nel formato: "nome".                                                                                                                 |
| **tlbid**            | Libreria dei tipi che contiene la descrizione dell'interfaccia specificata dall'attributo **IID** . Questo attributo è facoltativo. Il valore deve essere nel formato: "{TLBID}".                                                                                                                                 |
| **baseInterface**    | IID dell'interfaccia da cui deriva quello descritto dall'attributo **IID** . Questo attributo è facoltativo. Il valore deve essere nel formato: "{IID}".                                                                                                                                            |
| **numMethods**       | Numero di metodi implementati dall'interfaccia. Questo attributo è facoltativo. Il valore deve essere nel formato: "n".                                                                                                                                                                                       |
| **proxyStubClsid32** | Esegue il mapping di un IID a un CLSID in DLL proxy a 32 bit.                                                                                                                                                                                                                                                                |
| **threadingModel**   | Modello di threading utilizzato dalle classi COM in-process. Se questa proprietà è null, non viene utilizzato alcun modello di Threading. Il componente viene creato nel thread principale del client e viene effettuato il marshalling di chiamate da altri thread a questo thread. facoltativo. I valori validi sono: "Apartment", "Free", "both" e "neutral". |



 

</dd> <dt>

<span id="windowclass"></span><span id="WINDOWCLASS"></span>**WindowClass**
</dt> <dd>

Nome di una classe di Windows di cui eseguire il controllo delle versioni. L'elemento **WindowClass** ha l'attributo seguente.



| Attributo     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **versione** | Questo attributo controlla se il nome della classe interna della finestra utilizzato nella registrazione contiene la versione dell'assembly contenente la classe della finestra. Il valore di questo attributo può essere "Yes" o "No". Il valore predefinito è "Yes". Il valore "No" deve essere usato solo se la stessa classe di finestra è definita da un componente affiancato e da un componente non side-by-side equivalente e si vuole gestirli come la stessa classe di finestra. Si noti che le normali regole per la registrazione della classe di finestra applicano solo il primo componente che registra la classe di finestra sarà in grado di registrarlo perché non è con versione. |



 

Nell'esempio seguente viene illustrato un elemento **WindowClass** incluso in un elemento **file** .

``` syntax
<file name="comctl32.dll">
        <windowClass versioned="no">ToolbarWindow32</windowClass>
</file>
```

</dd> </dl>

## <a name="example"></a>Esempio

Di seguito è riportato un esempio di un manifesto dell'assembly.

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

 

