---
description: Un manifesto di applicazione è un file XML nel quale vengono descritti e identificati gli assembly side-by-side condivisi e privati con i quali un'applicazione deve stabilire un'associazione in fase di esecuzione.
ms.assetid: c5016251-db7a-4edc-9be9-3acb03d495f8
title: Manifesti dell'applicazione
ms.topic: article
ms.date: 10/08/2020
ms.custom: 19H1
ms.openlocfilehash: a1ced7ffb4052f418e989e907f26abb85c2c63db
ms.sourcegitcommit: 25211012b002a7d1303e438277373d7faf958a68
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122436709"
---
# <a name="application-manifests"></a>Manifesti dell'applicazione

Un manifesto di applicazione è un file XML nel quale vengono descritti e identificati gli assembly side-by-side condivisi e privati con i quali un'applicazione deve stabilire un'associazione in fase di esecuzione. Le versioni di questi assembly devono corrispondere a quelle utilizzate per testare l'applicazione. I manifesti di applicazione possono inoltre contenere una descrizione dei metadati di file privati dell'applicazione.

Per un elenco completo dello schema XML, vedere [Schema del file manifesto](manifest-file-schema.md).

I manifesti dell'applicazione hanno gli elementi e gli attributi seguenti.

| Elemento                               | Attributi                | Necessario |
|---------------------------------------|---------------------------|----------|
| **Assemblea**                          |                           | Sì      |
|                                       | **manifestVersion**       | Sì      |
| **noInherit**                         |                           | No       |
| **Assemblyidentity**                  |                           | Sì      |
|                                       | **type**                  | Sì      |
|                                       | **nome**                  | Sì      |
|                                       | **language**              | No       |
|                                       | **processorArchitecture** | No       |
|                                       | **version**               | Sì      |
|                                       | **Publickeytoken**        | No       |
| **Compatibilità**                     |                           | No       |
| **applicazione**                       |                           | No       |
| **supportedOS**                       | **Id**                    | No       |
| **maxversiontested**                  | **Id**                    | No       |
| **Dipendenza**                        |                           | No       |
| **dependentAssembly**                 |                           | No       |
| **file**                              |                           | No       |
|                                       | **nome**                  | No       |
|                                       | **hashalg**               | No       |
|                                       | **hash**                  | No       |
| **activeCodePage**                    |                           | No       |
| **autoElevate**                       |                           | No       |
| **disableTheming**                    |                           | No       |
| **disableWindowFiltering**            |                           | No       |
| **dpiAware**                          |                           | No       |
| **dpiAwareness**                      |                           | No       |
| **gdiScaling**                        |                           | No       |
| **highResolutionScrollingAware**      |                           | No       |
| **longPathAware**                     |                           | No       |
| **printerDriverIsolation**            |                           | No       |
| **ultraHighResolutionScrollingAware** |                           | No       |
| **msix**                              |                           | No       |
| **heapType**                          |                           | No       |

## <a name="file-location"></a>Percorso file

I manifesti dell'applicazione devono essere inclusi come risorsa nel file EXE o nella DLL dell'applicazione.

Per altre informazioni, vedere [Installazione di assembly side-by-side](installing-side-by-side-assemblies.md).

## <a name="file-name-syntax"></a>Sintassi del nome file

Il nome di un file manifesto dell'applicazione è il nome del file eseguibile dell'applicazione seguito da .manifest.

Ad esempio, un manifesto dell'applicazione che fa riferimento example.exe o example.dll usare la sintassi del nome file seguente. È possibile omettere il campo *<'ID* risorsa> se l'ID risorsa è 1.

**example.exe.<*id risorsa*>.manifest**

**example.dll.<*id risorsa*>.manifest**

## <a name="elements"></a>Elementi

Per i nomi di elementi e attributi viene fatto distinzione tra maiuscole e minuscole. Per i valori di elementi e attributi non viene fatta distinzione tra maiuscole e minuscole, ad eccezione del valore dell'attributo di tipo.

<span id="assembly"></span><span id="ASSEMBLY"></span>

### <a name="assembly"></a>assembly

Elemento contenitore. Il primo sottoelemento deve essere **un elemento noInherit** o **assemblyIdentity.** Obbligatorio.

**L'elemento assembly** deve essere nello spazio dei nomi "urn:schemas-microsoft-com:asm.v1". Anche gli elementi figlio dell'assembly devono essere in questo spazio dei nomi, tramite ereditarietà o assegnazione di tag.

**L'elemento assembly** ha gli attributi seguenti.



| Attributo           | Descrizione                                           |
|---------------------|-------------------------------------------------------|
| **manifestVersion** | **L'attributo manifestVersion** deve essere impostato su 1.0. |


<span id="noInherit"></span><span id="noinherit"></span><span id="NOINHERIT"></span>

### <a name="noinherit"></a>noInherit

Includere questo elemento in un manifesto dell'applicazione per impostare i [contesti di](activation-contexts.md) attivazione generati dal manifesto con il flag "no inherit". Quando questo flag non è impostato in un contesto di attivazione e il contesto di attivazione è attivo, viene ereditato dai nuovi thread nello stesso processo, finestra, routine finestra e chiamate di [procedura asincrone](/windows/desktop/Sync/asynchronous-procedure-calls). L'impostazione di questo flag impedisce al nuovo oggetto di ereditare il contesto attivo.

**L'elemento noInherit** è facoltativo e in genere viene omesso. La maggior parte degli assembly non funziona correttamente usando un contesto di attivazione no-inherit perché l'assembly deve essere progettato in modo esplicito per gestire la propagazione del proprio contesto di attivazione. L'uso **dell'elemento noInherit** richiede che tutti gli assembly dipendenti a cui fa riferimento il manifesto dell'applicazione presentino un elemento **noInherit** nel manifesto [dell'assembly.](assembly-manifests.md)

Se **noInherit** viene usato in un manifesto, deve essere il primo sottoelemento **dell'elemento assembly.** **L'elemento assemblyIdentity** deve essere immediatamente successivo all'elemento **noInherit.** Se **non si usa noInherit,** **assemblyIdentity** deve essere il primo sottoelemento dell'elemento **assembly.** **L'elemento noInherit** non ha elementi figlio. Non è un elemento valido nei [manifesti dell'assembly.](assembly-manifests.md)

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>

### <a name="assemblyidentity"></a>assemblyIdentity

Come primo sottoelemento di un **elemento assembly,** **assemblyIdentity** descrive e identifica in modo univoco l'applicazione proprietaria del manifesto dell'applicazione. Come primo sottoelemento di un elemento **dependentAssembly,** **assemblyIdentity** descrive un assembly side-by-side richiesto dall'applicazione. Si noti che ogni assembly a cui viene fatto riferimento nel manifesto dell'applicazione richiede un **elemento assemblyIdentity** che corrisponda esattamente all'elemento **assemblyIdentity** nel manifesto dell'assembly a cui si fa riferimento.

**L'elemento assemblyIdentity** ha gli attributi seguenti. Non ha sottoelementi.

| Attributo                 | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **type**                  | Specifica il tipo di applicazione o assembly. Il valore deve essere Win32 e tutti in lettere minuscole. Obbligatorio.                                                                                                                                                                                                                                                                                                                              |
| **nome**                  | Nome univoco dell'applicazione o dell'assembly. Usare il formato seguente per il nome: Organization.Division.Name. Ad esempio, Microsoft. Windows.mysampleApp. Obbligatorio.                                                                                                                                                                                                                                                               |
| **language**              | Identifica la lingua dell'applicazione o dell'assembly. facoltativo. Se l'applicazione o l'assembly è specifico del linguaggio, specificare il codice del linguaggio DHTML. **Nell'assemblyIdentity di** un'applicazione destinata all'uso globale (indipendente dalla lingua) omettere l'attributo language.<br/> In un **assemblyIdentity di** un assembly destinato all'uso globale (indipendente dalla lingua) impostare il valore della lingua su " \* ".<br/> |
| **processorArchitecture** | Specifica il processore. I valori validi includono `x86`, `amd64`, `arm` e `arm64`. facoltativo.                                                                                                                                                                                                                                                                                                                       |
| **version**               | Specifica la versione dell'applicazione o dell'assembly. Usare il formato di versione in quattro parti: mmmmm.nnnnn.oooooo.ppppp. Ognuna delle parti separate da punti può essere compresa tra 0 e 65535 inclusi. Per altre informazioni, vedere [Versioni degli assembly](assembly-versions.md). Obbligatorio.                                                                                                                                                                        |
| **Publickeytoken**        | Stringa esadecimale di 16 caratteri che rappresenta gli ultimi 8 byte dell'hash SHA-1 della chiave pubblica con cui viene firmata l'applicazione o l'assembly. La chiave pubblica usata per firmare il catalogo deve essere di 2048 bit o superiore. Obbligatorio per tutti gli assembly side-by-side condivisi.                                                                                                                                                     |

<span id="compatibility"></span><span id="COMPATIBILITY"></span>

### <a name="compatibility"></a>compatibilità

Contiene almeno **un'applicazione**. Non ha attributi. facoltativo. I manifesti dell'applicazione senza un elemento di compatibilità Windows compatibilità con Vista Windows 7.

<span id="application"></span><span id="APPLICATION"></span>

### <a name="application"></a>application

Contiene almeno un **elemento supportedOS.** A partire Windows 10 versione 1903, può contenere anche un elemento **maxversiontested** facoltativo. Non ha attributi. facoltativo.

<span id="supportedOS"></span><span id="supportedos"></span><span id="SUPPORTEDOS"></span>

### <a name="supportedos"></a>supportedOS

**L'elemento supportedOS** ha l'attributo seguente. Non ha sottoelementi.

| Attributo | Descrizione   |
|-----------|-----------------------|
| **Id**    | Impostare l'attributo Id su **{e2011457-1546-43c5-a5fe-008dee3d3f0}** per eseguire l'applicazione usando la funzionalità Vista. In questo modo un'applicazione progettata per Windows Vista può essere eseguita in un sistema operativo successivo. <br/> Impostare l'attributo Id su **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** per eseguire l'applicazione usando la funzionalità Windows 7.<br/> Le applicazioni che supportano Windows Vista, Windows 7 e Windows 8 funzionalità non richiedono manifesti separati. In questo caso, aggiungere i GUID per tutti i Windows operativi.<br/> Per informazioni sul comportamento **dell'attributo Id** in Windows, vedere il Windows 8 e Windows Server 2012 [compatibility cookbook](https://www.microsoft.com/download/details.aspx?id=27416).<br/> I GUID seguenti corrispondono ai sistemi operativi indicati:<br/> **{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}** -> Windows 10, Windows Server 2016 e Windows Server 2019<br/> **{1f676c76-80e1-4239-95bb-83d0f6d0da78}** -> Windows 8.1 e Windows Server 2012 R2<br/> **{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}** -> Windows 8 e Windows Server 2012<br/> **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** -> Windows 7 e Windows Server 2008 R2<br/> **{e2011457-1546-43c5-a5fe-008dee3d3f0}** -> Windows Vista e Windows Server 2008<br/> È possibile testare questa operazione in Windows 7 o Windows 8.x eseguendo Monitoraggio risorse (resmon), andare alla scheda CPU, fare clic con il pulsante destro del mouse sulle etichette di colonna, selezionare "Seleziona colonna..." e selezionare "Contesto del sistema operativo". In Windows 8.x è anche possibile trovare questa colonna disponibile nel Gestione attività (taskmgr). Il contenuto della colonna mostra il valore più alto trovato o "Windows Vista" come valore predefinito. <br/> |

<span id="maxVersionTested"></span><span id="maxversiontested"></span><span id="MAXVERSIONTESTED"></span>

### <a name="maxversiontested"></a>maxversiontested

**L'elemento maxversiontested** specifica le versioni di Windows in cui l'applicazione è stata testata a partire dalla versione minima del sistema operativo supportata dall'applicazione fino alla versione massima. Il set completo di versioni è disponibile [qui.](https://developer.microsoft.com/windows/downloads/sdk-archive/) Deve essere usato dalle applicazioni desktop che usano isole [XAML](/windows/apps/desktop/modernize/xaml-islands) e che non sono distribuite in un pacchetto MSIX. Questo elemento è supportato in Windows 10, versione 1903 e versioni successive.

**L'elemento maxversiontested** ha l'attributo seguente. Non ha sottoelementi.

| Attributo | Descrizione    |
|-----------|----------------|
| **Id**    | Impostare l'attributo Id su una stringa di versione in 4 parti che specifica la versione massima Windows cui è stata testata l'applicazione. Ad esempio, "10.0.18226.0". |

<span id="dependency"></span><span id="DEPENDENCY"></span>

### <a name="dependency"></a>dependency

Contiene almeno un **dependentAssembly**. Non ha attributi. facoltativo.

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>

### <a name="dependentassembly"></a>dependentAssembly

Il primo sottoelemento **di dependentAssembly** deve essere un **elemento assemblyIdentity** che descrive un assembly side-by-side richiesto dall'applicazione. Ogni **dependentAssembly deve** essere all'interno esattamente di **una dipendenza**. Non ha attributi.

<span id="file"></span><span id="FILE"></span>

### <a name="file"></a>file

Specifica i file privati per l'applicazione. facoltativo.

**L'elemento file** ha gli attributi illustrati nella tabella seguente.



| Attributo   | Descrizione                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| **nome**    | Nome del file. Ad esempio, Comctl32.dll.                                                            |
| **hashalg** | Algoritmo usato per creare un hash del file. Questo valore deve essere SHA1.                                 |
| **hash**    | Hash del file a cui si fa riferimento in base al nome. Stringa esadecimale di lunghezza a seconda dell'algoritmo hash. |

<span id="activeCodePage"></span><span id="activecodepage"></span><span id="ACTIVECODEPAGE"></span>

### <a name="activecodepage"></a>activeCodePage

In Windows 10, questo elemento forza un processo a usare UTF-8 come tabella codici del processo. Per altre informazioni, vedere [Usare la tabella codici UTF-8.](/windows/uwp/design/globalizing/use-utf8-code-page) In Windows 10, l'unico valore valido per **activeCodePage** è **UTF-8.**

A partire Windows 11, questo elemento consente anche di selezionare la tabella codici legacy non UTF-8 o le code pages per impostazioni locali specifiche per la compatibilità delle applicazioni legacy. Le applicazioni moderne sono fortemente incoraggiate a usare Unicode. Nella Windows 11 **activeCodePage** può anche essere impostato sul valore **Legacy** o su un nome di impostazioni locali, ad esempio **en-US** o **ja-JP.**

- Nei computer configurati per una tabella codici attiva del sistema UTF-8, **Legacy** ripristina le code page delle impostazioni locali del sistema. Se le impostazioni locali del sistema non dispongono di code pages definite, Windows-1252/437. **L'impostazione** Della tabella codici legacy è supportata solo nei manifesti Fusion e inizia solo con Windows 11.
- Quando viene specificato un nome di impostazioni locali, ad esempio **en-US,** la tabella codici del processo verrà impostata in modo appropriato per la tabella codici delle impostazioni locali. Ad esempio, Windows-1252 e 437 per en-US o 932 per ja-JP.

Questo elemento è stato aggiunto per la Windows 10 versione 1903 (aggiornamento di maggio 2019). È possibile dichiarare questa proprietà ed eseguirla nelle build Windows precedenti, ma è necessario gestire il rilevamento e la conversione delle code page legacy come di consueto. Questo elemento non ha attributi. 

L'esempio seguente illustra come usare questo elemento per forzare il processo corrente a usare UTF-8 come tabella codici del processo.

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2019/WindowsSettings"> 
      <activeCodePage>UTF-8</activeCodePage> 
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="autoElevate"></span><span id="autoelevate"></span><span id="AUTOELEVATE"></span>

### <a name="autoelevate"></a>autoElevate

Specifica se l'elevazione automatica è abilitata. **TRUE** indica che è abilitato. Non ha attributi.

<span id="disableTheming"></span><span id="disabletheming"></span><span id="DISABLETHEMING"></span>

### <a name="disabletheming"></a>disableTheming

Specifica se fornire elementi dell'interfaccia utente a un tema è disabilitato. **TRUE** indica disabilitato. Non ha attributi.

<span id="disableWindowFiltering"></span><span id="disablewindowfiltering"></span><span id="DISABLEWINDOWFILTERING"></span>

### <a name="disablewindowfiltering"></a>disableWindowFiltering

Specifica se disabilitare il filtro delle finestre. **TRUE** disabilita il filtro delle finestre in modo da poter enumerare le finestre immersive dal desktop. **disableWindowFiltering** è stato aggiunto in Windows 8 e non ha attributi.

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">
      <disableWindowFiltering>true</disableWindowFiltering>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="dpiAware"></span><span id="dpiaware"></span><span id="DPIAWARE"></span>

### <a name="dpiaware"></a>dpiAware

Specifica se il processo corrente è in grado di riconoscere punti per pollice (dpi).

**Windows 10 versione 1607:** **L'elemento dpiAware** viene ignorato se è presente l'elemento **dpiAwareness.** È possibile includere entrambi gli elementi in un manifesto se si vuole specificare un comportamento diverso per Windows 10 versione 1607 rispetto a una versione precedente del sistema operativo.

Nella tabella seguente viene descritto il comportamento che risulta in base alla presenza dell'elemento **dpiAware** e al testo in esso contenuto. Il testo all'interno dell'elemento non fa distinzione tra maiuscole e minuscole.

| Stato **dell'elemento dpiAware** | Descrizione     |
|-----------------------------------|---------|
| Assente                            | Il processo corrente non è a conoscenza di dpi per impostazione predefinita. È possibile modificare questa impostazione a livello di codice chiamando la [**funzione SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) [**o SetProcessDPIAware.**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware)                                                                                                                                                            |
| Contiene "true"                   | Il processo corrente è in grado di riconoscere dpi di sistema.                                                                                                                                                                                                                                                                                                                                                          |
| Contiene "false"                  | **Windows Vista, Windows 7 e Windows 8:** Il comportamento è lo stesso di quando **dpiAware** è assente.<br/> **Windows 8.1 e Windows 10:** Il processo corrente non è a conoscenza di dpi e non è possibile modificare questa impostazione a livello di codice chiamando la [**funzione SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) o [**SetProcessDPIAware.**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware)<br/> |
| Contiene "true/pm"                | **Windows Vista, Windows 7 e Windows 8:** Il processo corrente è in grado di riconoscere dpi di sistema.<br/> **Windows 8.1 e Windows 10:** Il processo corrente è in grado di riconoscere dpi per ogni monitoraggio.<br/>                                                                                                                                                                                                          |
| Contiene "per monitoraggio"            | **Windows Vista, Windows 7 e Windows 8:** Il comportamento è lo stesso di quando **dpiAware** è assente.<br/> **Windows 8.1 e Windows 10:** Il processo corrente è in grado di riconoscere dpi per ogni monitoraggio.<br/>                                                                                                                                                                                      |
| Contiene qualsiasi altra stringa         | **Windows Vista, Windows 7 e Windows 8:** Il comportamento è lo stesso di quando **dpiAware** è assente.<br/> **Windows 8.1 e Windows 10:** Il processo corrente non è a conoscenza di dpi e non è possibile modificare questa impostazione a livello di codice chiamando la [**funzione SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) o [**SetProcessDPIAware.**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware)<br/> |

Per altre informazioni sulle impostazioni di riconoscimento dpi, vedere [Confronto dei livelli di consapevolezza DPI.](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot))

**dpiAware** non ha attributi.

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
      <dpiAware>true</dpiAware>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="dpiAwareness"></span><span id="dpiawareness"></span><span id="DPIAWARENESS"></span>

### <a name="dpiawareness"></a>dpiAwareness

Specifica se il processo corrente è in grado di riconoscere punti per pollice (dpi).

La versione minima del sistema operativo che supporta **l'elemento dpiAwareness** è Windows 10 versione 1607. Per le versioni che supportano **l'elemento dpiAwareness,** **dpiAwareness** esegue l'override dell'elemento **dpiAware.** È possibile includere entrambi gli elementi in un manifesto se si vuole specificare un comportamento diverso per Windows 10 versione 1607 rispetto a una versione precedente del sistema operativo.

**L'elemento dpiAwareness** può contenere un singolo elemento o un elenco di elementi delimitati da virgole. Nel secondo caso, viene usato il primo elemento (più a sinistra) nell'elenco riconosciuto dal sistema operativo. In questo modo, è possibile specificare comportamenti diversi supportati in versioni future Windows del sistema operativo.

Nella tabella seguente viene descritto il comportamento che risulta in base alla presenza dell'elemento **dpiAwareness** e al testo contenuto nell'elemento riconosciuto all'estrema sinistra. Il testo all'interno dell'elemento non fa distinzione tra maiuscole e minuscole.

| **Stato dell'elemento dpiAwareness:**        | Descrizione                          |
|-----------------------------------------|-------------------------------------------|
| L'elemento è assente                       | **L'elemento dpiAware** specifica se il processo è in grado di riconoscere dpi.                                                                                                                                                                   |
| Non contiene elementi riconosciuti            | Il processo corrente non è a conoscenza di dpi per impostazione predefinita. È possibile modificare questa impostazione a livello di codice chiamando la [**funzione SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) [**o SetProcessDPIAware.**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) |
| Il primo elemento riconosciuto è "system"       | Il processo corrente è in grado di riconoscere dpi di sistema.                                                                                                                                                                                               |
| Il primo elemento riconosciuto è "permonitor"   | Il processo corrente è in grado di riconoscere dpi per ogni monitoraggio.                                                                                                                                                                                          |
| Il primo elemento riconosciuto è "permonitorv2" | Il processo corrente usa il contesto di riconoscimento dpi per monitor-v2. Questo elemento verrà riconosciuto solo in Windows 10 versione 1703 o successiva.                                                                                              |
| Il primo elemento riconosciuto è "inconsapevole"      | Il processo corrente è dpi inconsapevole. Non **è possibile** modificare questa impostazione a livello di codice chiamando la funzione [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) o [**SetProcessDPIAware.**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware)      |

Per altre informazioni sulle impostazioni di riconoscimento dpi supportate da questo elemento, vedere [DPI \_ AWARENESS](/windows/desktop/api/windef/ne-windef-dpi_awareness) e [DPI \_ AWARENESS \_ CONTEXT](/windows/desktop/hidpi/dpi-awareness-context).

**dpiAwareness** non ha attributi.

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2016/WindowsSettings">
      <dpiAwareness>PerMonitorV2, unaware</dpiAwareness>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="gdiScaling"></span><span id="gdiscaling"></span><span id="GDISCALING"></span>

### <a name="gdiscaling"></a>gdiScaling

Specifica se il ridimensionamento GDI è abilitato. La versione minima del sistema operativo che supporta l'elemento **gdiScaling** è Windows 10 1703.

Il framework GDI (graphics device interface) può applicare il ridimensionamento DPI alle primitive e al testo in base al monitoraggio senza aggiornamenti all'applicazione stessa. Ciò può essere utile per le applicazioni GDI che non vengono più aggiornate attivamente.

La grafica non vettoriale (ad esempio bitmap, icone o barre degli strumenti) non può essere ridimensionata da questo elemento. Inoltre, la grafica e il testo visualizzati all'interno di bitmap costruite dinamicamente dalle applicazioni non possono essere ridimensionati da questo elemento.

**TRUE** indica che questo elemento è abilitato. Non ha attributi.


```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2017/WindowsSettings">
      <gdiScaling>true</gdiScaling>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="highResolutionScrollingAware"></span><span id="highresolutionscrollingaware"></span><span id="HIGHRESOLUTIONSCROLLINGAWARE"></span>

### <a name="highresolutionscrollingaware"></a>highResolutionScrollingAware

Specifica se è abilitata la funzionalità di scorrimento ad alta risoluzione. **TRUE** indica che è abilitato. Non ha attributi.

<span id="longPathAware"></span><span id="longpathaware"></span><span id="LONGPATHAWARE"></span>

### <a name="longpathaware"></a>longPathAware

Abilita percorsi lunghi che **superano MAX_PATH** lunghezza. Questo elemento è supportato in Windows 10, versione 1607 e successive. Per altre informazioni, vedi [questo articolo](../fileio/maximum-file-path-limitation.md).

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns:ws2="http://schemas.microsoft.com/SMI/2016/WindowsSettings">
      <ws2:longPathAware>true</ws2:longPathAware>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="printerDriverIsolation"></span><span id="printerdriverisolation"></span><span id="PRINTERDRIVERISOLATION"></span>

### <a name="printerdriverisolation"></a>printerDriverIsolation

Specifica se l'isolamento del driver della stampante è abilitato. **TRUE** indica che è abilitato. Non ha attributi. L'isolamento del driver della stampante migliora l'affidabilità del servizio di stampa Windows consentendo l'esecuzione dei driver della stampante in processi separati dal processo in cui viene eseguito lo spooler di stampa. Il supporto per l'isolamento del driver della stampante Windows 7 e Windows Server 2008 R2. Un'app può dichiarare l'isolamento del driver della stampante nel manifesto dell'app per isolarsi dal driver della stampante e migliorarne l'affidabilità. Ciò significa che l'app non si arresta in modo anomalo se il driver della stampante presenta un errore.


```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">
      <printerDriverIsolation>true</printerDriverIsolation>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="ultraHighResolutionScrollingAware"></span><span id="ultrahighresolutionscrollingaware"></span><span id="ULTRAHIGHRESOLUTIONSCROLLINGAWARE"></span>

### <a name="ultrahighresolutionscrollingaware"></a>ultraHighResolutionScrollingAware

Specifica se è abilitata la funzionalità di scorrimento ad alta risoluzione. **TRUE** indica che è abilitato. Non ha attributi.

<span id="msix"></span><span id="MSIX"></span>

### <a name="msix"></a>msix

Specifica le informazioni sull'identità di un pacchetto MSIX di [tipo sparse](/windows/apps/desktop/modernize/grant-identity-to-nonpackaged-apps) per l'applicazione corrente. Questo elemento è supportato in Windows 10, versione 2004 e versioni successive.

**L'elemento msix** deve essere nello spazio dei nomi `urn:schemas-microsoft-com:msix.v1` . Ha gli attributi illustrati nella tabella seguente.

| Attributo   | Descrizione                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| **Editore**    | Descrive le informazioni sull'autore. Questo valore deve corrispondere **all'Publisher** nell'elemento [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) nel manifesto del pacchetto di tipo sparse. |
| **Nomepacchetto** | Descrive il contenuto del pacchetto. Questo valore deve corrispondere **all'attributo Name** nell'elemento [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) nel manifesto del pacchetto di tipo sparse.    |
| **applicationId**    | Identificatore univoco dell'applicazione. Questo valore deve corrispondere **all'attributo Id** nell'elemento [Application](/uwp/schemas/appxpackage/uapmanifestschema/element-application) nel manifesto del pacchetto di tipo sparse.  |

```xml
<?xml version="1.0" encoding="utf-8"?>
<assembly manifestVersion="1.0" xmlns="urn:schemas-microsoft-com:asm.v1">
  <assemblyIdentity version="1.0.0.0" name="Contoso.PhotoStoreApp"/>
  <msix xmlns="urn:schemas-microsoft-com:msix.v1"
          publisher="CN=Contoso"
          packageName="ContosoPhotoStore"
          applicationId="ContosoPhotoStore"
        />
</assembly>
```

### <a name="heaptype"></a>heapType

Esegue l'override dell'implementazione dell'heap predefinita per l'uso delle [API dell'heap Win32.](../Memory/heap-functions.md)

* Il valore **SegmentHeap** indica che verrà usato l'heap dei segmenti. L'heap dei segmenti è un'implementazione moderna dell'heap che in genere ridurrà l'utilizzo complessivo della memoria. Questo elemento è supportato in Windows 10 versione 2004 (build 19041) e versioni successive.
* Tutti gli altri valori vengono ignorati.

Questo elemento non ha attributi.

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2020/WindowsSettings">
      <heapType>SegmentHeap</heapType>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

## <a name="example"></a>Esempio

Di seguito è riportato un esempio di manifesto dell'applicazione per un'applicazione denominata MySampleApp.exe. L'applicazione utilizza l'assembly side-by-side SampleAssembly.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">

  <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1"> 
      <application> 
        <!--This Id value indicates the application supports Windows Vista functionality -->
          <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        <!--This Id value indicates the application supports Windows 7 functionality-->
          <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
        <!--This Id value indicates the application supports Windows 8 functionality-->
          <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
        <!--This Id value indicates the application supports Windows 8.1 functionality-->
          <supportedOS Id="{1f676c76-80e1-4239-95bb-83d0f6d0da78}"/>
      </application> 
  </compatibility>

  <assemblyIdentity type="win32" 
                    name="myOrganization.myDivision.mySampleApp" 
                    version="6.0.0.0" 
                    processorArchitecture="x86" 
                    publicKeyToken="0000000000000000"
  />
  <dependency>
    <dependentAssembly>
      <assemblyIdentity type="win32" 
                        name="Proseware.Research.SampleAssembly" 
                        version="6.0.0.0" 
                        processorArchitecture="X86" 
                        publicKeyToken="0000000000000000" 
                        language="*"
      />
    </dependentAssembly>
  </dependency>
</assembly>
```
