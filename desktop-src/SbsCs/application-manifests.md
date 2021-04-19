---
description: Un manifesto di applicazione è un file XML nel quale vengono descritti e identificati gli assembly side-by-side condivisi e privati con i quali un'applicazione deve stabilire un'associazione in fase di esecuzione.
ms.assetid: c5016251-db7a-4edc-9be9-3acb03d495f8
title: Manifesti dell'applicazione
ms.topic: article
ms.date: 10/08/2020
ms.custom: 19H1
ms.openlocfilehash: cb065bc4d6d29f4142c23cdd91c83769e2fb9b87
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "106320229"
---
# <a name="application-manifests"></a>Manifesti dell'applicazione

Un manifesto di applicazione è un file XML nel quale vengono descritti e identificati gli assembly side-by-side condivisi e privati con i quali un'applicazione deve stabilire un'associazione in fase di esecuzione. Le versioni di questi assembly devono corrispondere a quelle utilizzate per testare l'applicazione. I manifesti di applicazione possono inoltre contenere una descrizione dei metadati di file privati dell'applicazione.

Per un elenco completo delle XML Schema, vedere [schema del file manifesto](manifest-file-schema.md).

I manifesti dell'applicazione hanno gli elementi e gli attributi seguenti.

| Elemento                               | Attributi                | Necessario |
|---------------------------------------|---------------------------|----------|
| **assembly**                          |                           | Sì      |
|                                       | **manifestVersion**       | Sì      |
| **noInherit**                         |                           | No       |
| **assemblyIdentity**                  |                           | Sì      |
|                                       | **type**                  | Sì      |
|                                       | **nome**                  | Sì      |
|                                       | **language**              | No       |
|                                       | **processorArchitecture** | No       |
|                                       | **version**               | Sì      |
|                                       | **publicKeyToken**        | No       |
| **compatibilità**                     |                           | No       |
| **applicazione**                       |                           | No       |
| **supportedOS**                       | **Id**                    | No       |
| **maxversiontested**                  | **Id**                    | No       |
| **dipendenza**                        |                           | No       |
| **dependentAssembly**                 |                           | No       |
| **file**                              |                           | No       |
|                                       | **nome**                  | No       |
|                                       | **hashAlg**               | No       |
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

Per ulteriori informazioni, vedere [installazione di assembly affiancati](installing-side-by-side-assemblies.md).

## <a name="file-name-syntax"></a>Sintassi del nome file

Il nome di un file manifesto dell'applicazione è il nome dell'eseguibile dell'applicazione seguito da. manifest.

Ad esempio, un manifesto dell'applicazione che fa riferimento a example.exe o example.dll utilizzerebbe la sintassi del nome file seguente. Se l'ID risorsa è 1, è possibile omettere l' *ID risorsa* <> campo.

**example.exe. <*ID risorsa*>. manifest**

**example.dll. <*ID risorsa*>. manifest**

## <a name="elements"></a>Elementi

I nomi degli elementi e degli attributi distinguono tra maiuscole e minuscole. I valori degli elementi e degli attributi non fanno distinzione tra maiuscole e minuscole, ad eccezione del valore dell'attributo Type.

<span id="assembly"></span><span id="ASSEMBLY"></span>

### <a name="assembly"></a>assembly

Elemento contenitore. Il primo sottoelemento deve essere un elemento **NoInherit** o **assemblyIdentity** . Obbligatorio.

L'elemento **assembly** deve trovarsi nello spazio dei nomi "urn: schemas-microsoft-com: ASM. V1". Gli elementi figlio dell'assembly devono trovarsi anche in questo spazio dei nomi, in base all'ereditarietà o all'assegnazione di tag.

L'elemento **assembly** ha gli attributi seguenti.



| Attributo           | Descrizione                                           |
|---------------------|-------------------------------------------------------|
| **manifestVersion** | L'attributo **manifestVersion** deve essere impostato su 1,0. |


<span id="noInherit"></span><span id="noinherit"></span><span id="NOINHERIT"></span>

### <a name="noinherit"></a>noInherit

Includere questo elemento in un manifesto dell'applicazione per impostare i [contesti di attivazione](activation-contexts.md) generati dal manifesto con il flag "No inherit". Quando questo flag non è impostato in un contesto di attivazione e il contesto di attivazione è attivo, viene ereditato da nuovi thread nello stesso processo, Windows, le routine della finestra e le [chiamate di procedure asincrone](/windows/desktop/Sync/asynchronous-procedure-calls). L'impostazione di questo flag impedisce al nuovo oggetto di ereditare il contesto attivo.

L'elemento **NoInherit** è facoltativo e in genere omesso. La maggior parte degli assembly non funziona correttamente usando un contesto di attivazione senza ereditarietà perché l'assembly deve essere progettato in modo esplicito per gestire la propagazione del proprio contesto di attivazione. Per l'utilizzo dell'elemento **NoInherit** è necessario che tutti gli assembly dipendenti a cui fa riferimento il manifesto dell'applicazione dispongano di un elemento **NoInherit** nel [manifesto dell'assembly](assembly-manifests.md).

Se si utilizza **NoInherit** in un manifesto, deve essere il primo sottoelemento dell'elemento **assembly** . L'elemento **assemblyIdentity** dovrebbe essere immediatamente successivo all'elemento **NoInherit** . Se non si utilizza **NoInherit** , **assemblyIdentity** deve essere il primo sottoelemento dell'elemento **assembly** . L'elemento **NoInherit** non ha elementi figlio. Non è un elemento valido nei [manifesti dell'assembly](assembly-manifests.md).

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>

### <a name="assemblyidentity"></a>assemblyIdentity

Come primo sottoelemento di un elemento **assembly** , **assemblyIdentity** descrive e identifica in modo univoco l'applicazione proprietaria del manifesto dell'applicazione. Come primo sottoelemento di un elemento **dependentAssembly** , **assemblyIdentity** descrive un assembly side-by-side richiesto dall'applicazione. Si noti che per ogni assembly a cui viene fatto riferimento nel manifesto dell'applicazione è necessario un **assemblyIdentity** che corrisponda esattamente a **assemblyIdentity** nel manifesto dell'assembly a cui si fa riferimento.

L'elemento **assemblyIdentity** ha gli attributi seguenti. Non contiene sottoelementi.

| Attributo                 | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **type**                  | Specifica il tipo di applicazione o di assembly. Il valore deve essere Win32 e tutti in lettere minuscole. Obbligatorio.                                                                                                                                                                                                                                                                                                                              |
| **nome**                  | Assegna un nome univoco all'applicazione o all'assembly. Usare il formato seguente per il nome: Organization.Division.Name. Ad esempio Microsoft. Windows. mysampleApp. Obbligatorio.                                                                                                                                                                                                                                                               |
| **language**              | Identifica la lingua dell'applicazione o dell'assembly. facoltativo. Se l'applicazione o l'assembly è specifico della lingua, specificare il codice della lingua DHTML. In **assemblyIdentity** di un'applicazione destinata all'uso in tutto il mondo (indipendente dal linguaggio) omettere l'attributo Language.<br/> In un oggetto **assemblyIdentity** di un assembly progettato per l'uso in tutto il mondo (indipendente dal linguaggio) impostare il valore della lingua su " \* ".<br/> |
| **processorArchitecture** | Specifica il processore. I valori validi includono `x86`, `amd64`, `arm` e `arm64`. facoltativo.                                                                                                                                                                                                                                                                                                                       |
| **version**               | Specifica la versione dell'applicazione o dell'assembly. Usare il formato di versione in quattro parti: mmmm. NNNNN. ooooo. ppppp. Ognuna delle parti separate da punti può essere 0-65535 inclusi. Per altre informazioni, vedere [versioni degli assembly](assembly-versions.md). Obbligatorio.                                                                                                                                                                        |
| **publicKeyToken**        | Stringa esadecimale di 16 caratteri che rappresenta gli ultimi 8 byte dell'hash SHA-1 della chiave pubblica in cui l'applicazione o l'assembly è firmato. La chiave pubblica usata per firmare il catalogo deve essere di 2048 bit o superiore. Obbligatorio per tutti gli assembly affiancati condivisi.                                                                                                                                                     |

<span id="compatibility"></span><span id="COMPATIBILITY"></span>

### <a name="compatibility"></a>compatibilità

Contiene almeno un' **applicazione**. Non ha attributi. facoltativo. I manifesti dell'applicazione senza un elemento di compatibilità vengono predefiniti per la compatibilità con Windows Vista in Windows 7.

<span id="application"></span><span id="APPLICATION"></span>

### <a name="application"></a>application

Contiene almeno un elemento **supported** . A partire da Windows 10, versione 1903, può contenere anche un elemento facoltativo **maxversiontested** . Non ha attributi. facoltativo.

<span id="supportedOS"></span><span id="supportedos"></span><span id="SUPPORTEDOS"></span>

### <a name="supportedos"></a>supportedOS

L'elemento **supportos** presenta l'attributo seguente. Non contiene sottoelementi.

| Attributo | Descrizione   |
|-----------|-----------------------|
| **Id**    | Impostare l'attributo ID su **{e2011457-1546-43C5-a5fe-008deee3d3f0}** per eseguire l'applicazione con la funzionalità vista. Ciò può consentire l'esecuzione di un'applicazione progettata per Windows Vista in un sistema operativo successivo. <br/> Impostare l'attributo ID su **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** per eseguire l'applicazione utilizzando la funzionalità di Windows 7.<br/> Le applicazioni che supportano le funzionalità di Windows Vista, Windows 7 e Windows 8 non richiedono manifesti distinti. In questo caso, aggiungere i GUID per tutti i sistemi operativi Windows.<br/> Per informazioni sul comportamento dell'attributo **ID** in Windows, vedere la Guida di riferimento per la compatibilità con Windows [8 e Windows Server 2012](https://www.microsoft.com/download/details.aspx?id=27416).<br/> I GUID seguenti corrispondono ai sistemi operativi indicati:<br/> **{8e0f7a12-bfb3-4fe8-B9A5-48fd50a15a9a}** -> Windows 10, windows server 2016 e windows server 2019<br/> **{1f676c76-80E1-4239-95bb-83d0f6d0da78}** -> Windows 8.1 e Windows Server 2012 R2<br/> **{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}** -> Windows 8 e windows Server 2012<br/> **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** -> Windows 7 e windows Server 2008 R2<br/> **{e2011457-1546-43C5-a5fe-008deee3d3f0}** -> Windows Vista e windows Server 2008<br/> Per eseguire il test in Windows 7 o Windows 8. x, è possibile eseguire Monitoraggio risorse (resmon), passare alla scheda CPU, fare clic con il pulsante destro del mouse sulle etichette delle colonne, scegliere "Seleziona colonna..." e selezionare "contesto del sistema operativo". In Windows 8. x, è possibile trovare anche questa colonna disponibile in Gestione attività (taskmgr). Il contenuto della colonna Mostra il valore più alto trovato o "Windows Vista" come predefinito. <br/> |

<span id="maxVersionTested"></span><span id="maxversiontested"></span><span id="MAXVERSIONTESTED"></span>

### <a name="maxversiontested"></a>maxversiontested

L'elemento **maxversiontested** specifica la versione massima di Windows in base alla quale l'applicazione è stata testata. Questa operazione deve essere usata da applicazioni desktop che usano le [isole XAML](/windows/apps/desktop/modernize/xaml-islands) e che non sono distribuite in un pacchetto MSIX. Questo elemento è supportato in Windows 10, versione 1903 e versioni successive.

L'elemento **maxversiontested** ha l'attributo seguente. Non contiene sottoelementi.

| Attributo | Descrizione    |
|-----------|----------------|
| **Id**    | Impostare l'attributo ID su una stringa di versione in 4 parti che specifichi la versione massima di Windows su cui è stata testata l'applicazione. Ad esempio, "10.0.18226.0". |

<span id="dependency"></span><span id="DEPENDENCY"></span>

### <a name="dependency"></a>dependency

Contiene almeno un **dependentAssembly**. Non ha attributi. facoltativo.

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>

### <a name="dependentassembly"></a>dependentAssembly

Il primo sottoelemento di **dependentAssembly** deve essere un elemento **assemblyIdentity** che descrive un assembly affiancato richiesto dall'applicazione. Ogni **dependentAssembly** deve trovarsi all'interno di una sola **dipendenza**. Non ha attributi.

<span id="file"></span><span id="FILE"></span>

### <a name="file"></a>file

Specifica i file privati dell'applicazione. facoltativo.

L'elemento **file** ha gli attributi mostrati nella tabella seguente.



| Attributo   | Descrizione                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| **nome**    | Nome del file. Ad esempio, Comctl32.dll.                                                            |
| **hashAlg** | Algoritmo utilizzato per creare un hash del file. Questo valore deve essere SHA1.                                 |
| **hash**    | Hash del file a cui si fa riferimento in base al nome. Stringa esadecimale di lunghezza, a seconda dell'algoritmo hash. |

<span id="activeCodePage"></span><span id="activecodepage"></span><span id="ACTIVECODEPAGE"></span>

### <a name="activecodepage"></a>activeCodePage

Forzare un processo a usare UTF-8 come tabella codici del processo.

**activeCodePage** è stato aggiunto in Windows versione 1903 (aggiornamento di maggio 2019). È possibile dichiarare questa proprietà e la destinazione/esecuzione nelle compilazioni precedenti di Windows, ma è necessario gestire il rilevamento e la conversione della tabella codici legacy come di consueto. Per informazioni dettagliate, vedere [usare la tabella codici UTF-8](/windows/uwp/design/globalizing/use-utf8-code-page) .

Questo elemento non ha attributi. **UTF-8** è un valore valido solo per l'elemento **activeCodePage** .

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

Specifica se l'elevazione automatica è abilitata. **True** indica che è abilitato. Non ha attributi.

<span id="disableTheming"></span><span id="disabletheming"></span><span id="DISABLETHEMING"></span>

### <a name="disabletheming"></a>disableTheming

Specifica se assegnare elementi dell'interfaccia utente un tema è disabilitato. **True** indica disabilitato. Non ha attributi.

<span id="disableWindowFiltering"></span><span id="disablewindowfiltering"></span><span id="DISABLEWINDOWFILTERING"></span>

### <a name="disablewindowfiltering"></a>disableWindowFiltering

Specifica se disabilitare il filtro della finestra. **True** Disabilita il filtro della finestra in modo che sia possibile enumerare le finestre immersive dal desktop. **disableWindowFiltering** è stato aggiunto in Windows 8 e non ha attributi.

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

**Windows 10, versione 1607:** L'elemento **dpiAware** viene ignorato se è presente l'elemento **dpiAwareness** . È possibile includere entrambi gli elementi in un manifesto se si desidera specificare un comportamento diverso per Windows 10, versione 1607, rispetto a una versione precedente del sistema operativo.

Nella tabella seguente viene descritto il comportamento che si basa sulla presenza dell'elemento **dpiAware** e sul testo in essa contenuto. Il testo all'interno dell'elemento non fa distinzione tra maiuscole e minuscole.

| Stato dell'elemento **dpiAware** | Descrizione     |
|-----------------------------------|---------|
| Assente                            | Per impostazione predefinita, il processo corrente è a conoscenza di dpi. È possibile modificare a livello di codice questa impostazione chiamando la funzione [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) o [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .                                                                                                                                                            |
| Contiene "true"                   | Il processo corrente è compatibile con i valori dpi del sistema.                                                                                                                                                                                                                                                                                                                                                          |
| Contiene "false"                  | **Windows Vista, Windows 7 e Windows 8:** Il comportamento è identico a quello in cui **dpiAware** è assente.<br/> **Windows 8.1 e Windows 10:** Il processo corrente è a conoscenza di dpi e non è possibile modificare a livello di codice questa impostazione chiamando la funzione [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) o [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .<br/> |
| Contiene "true/PM"                | **Windows Vista, Windows 7 e Windows 8:** Il processo corrente è compatibile con i valori dpi del sistema.<br/> **Windows 8.1 e Windows 10:** Il processo corrente è compatibile con i valori dpi per monitor.<br/>                                                                                                                                                                                                          |
| Contiene "per monitoraggio"            | **Windows Vista, Windows 7 e Windows 8:** Il comportamento è identico a quello in cui **dpiAware** è assente.<br/> **Windows 8.1 e Windows 10:** Il processo corrente è compatibile con i valori dpi per monitor.<br/>                                                                                                                                                                                      |
| Contiene qualsiasi altra stringa         | **Windows Vista, Windows 7 e Windows 8:** Il comportamento è identico a quello in cui **dpiAware** è assente.<br/> **Windows 8.1 e Windows 10:** Il processo corrente è a conoscenza di dpi e non è possibile modificare a livello di codice questa impostazione chiamando la funzione [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) o [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .<br/> |

Per ulteriori informazioni sulle impostazioni di compatibilità dpi, vedere [confronto tra i livelli di riconoscimento dpi](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).

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

La versione minima del sistema operativo che supporta l'elemento **dpiAwareness** è Windows 10, versione 1607. Per le versioni che supportano l'elemento **dpiAwareness** , **dpiAwareness** esegue l'override dell'elemento **dpiAware** . È possibile includere entrambi gli elementi in un manifesto se si desidera specificare un comportamento diverso per Windows 10, versione 1607, rispetto a una versione precedente del sistema operativo.

L'elemento **dpiAwareness** può contenere un singolo elemento o un elenco di elementi separati da virgole. Nel secondo caso, viene utilizzato il primo elemento (a sinistra) nell'elenco riconosciuto dal sistema operativo. In questo modo, è possibile specificare comportamenti diversi supportati nelle versioni future del sistema operativo Windows.

Nella tabella seguente viene descritto il comportamento che si basa sulla presenza dell'elemento **dpiAwareness** e sul testo contenuto nell'elemento riconosciuto più a sinistra. Il testo all'interno dell'elemento non fa distinzione tra maiuscole e minuscole.

| stato elemento **dpiAwareness** :        | Descrizione                          |
|-----------------------------------------|-------------------------------------------|
| Elemento assente                       | L'elemento **dpiAware** specifica se il processo è compatibile con dpi.                                                                                                                                                                   |
| Non contiene elementi riconosciuti            | Per impostazione predefinita, il processo corrente è a conoscenza di dpi. È possibile modificare a livello di codice questa impostazione chiamando la funzione [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) o [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) . |
| Il primo elemento riconosciuto è "System"       | Il processo corrente è compatibile con i valori dpi del sistema.                                                                                                                                                                                               |
| Il primo elemento riconosciuto è "permonitor"   | Il processo corrente è compatibile con i valori dpi per monitor.                                                                                                                                                                                          |
| Il primo elemento riconosciuto è "permonitorv2" | Il processo corrente usa il contesto di riconoscimento dpi per monitor-V2. Questo elemento verrà riconosciuto solo in Windows 10 versione 1703 o successiva.                                                                                              |
| Il primo elemento riconosciuto è "ignaro"      | Il processo corrente è a conoscenza di dpi. **Non è possibile** modificare a livello di codice questa impostazione chiamando la funzione [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) o [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .      |

Per ulteriori informazioni sulle impostazioni di riconoscimento dpi supportate da questo elemento, vedere [dpi \_ Awareness](/windows/desktop/api/windef/ne-windef-dpi_awareness) and [dpi \_ Awareness \_ context](/windows/desktop/hidpi/dpi-awareness-context).

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

Specifica se è abilitata la scalabilità GDI. La versione minima del sistema operativo che supporta l'elemento **gdiScaling** è Windows 10 versione 1703.

Il Framework GDI (Graphics Device Interface) può applicare la scalabilità DPI alle primitive e al testo in base al monitoraggio senza aggiornamenti per l'applicazione stessa. Questa operazione può essere utile per le applicazioni GDI che non sono più attivamente aggiornate.

L'elemento non può ridimensionare elementi grafici non vettoriali, ad esempio bitmap, icone o barre degli strumenti. Inoltre, la grafica e il testo visualizzati all'interno di bitmap costruite dinamicamente dalle applicazioni non possono essere ridimensionati in base a questo elemento.

**True** indica che questo elemento è abilitato. Non ha attributi.


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

Specifica se è abilitata la funzionalità di scorrimento a risoluzione elevata. **True** indica che è abilitato. Non ha attributi.

<span id="longPathAware"></span><span id="longpathaware"></span><span id="LONGPATHAWARE"></span>

### <a name="longpathaware"></a>longPathAware

Abilita percorsi lunghi che superano **MAX_PATH** lunghezza. Questo elemento è supportato in Windows 10, versione 1607 e versioni successive. Per altre informazioni, vedi [questo articolo](../fileio/maximum-file-path-limitation.md).

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

Specifica se l'isolamento del driver della stampante è abilitato. **True** indica che è abilitato. Non ha attributi. L'isolamento dei driver della stampante migliora l'affidabilità del servizio di stampa Windows consentendo ai driver della stampante di essere eseguiti in processi distinti dal processo in cui viene eseguito lo spooler di stampa. Supporto per l'isolamento dei driver della stampante avviato in Windows 7 e Windows Server 2008 R2. Un'app può dichiarare l'isolamento dei driver della stampante nel manifesto dell'applicazione per isolarsi dal driver della stampante e migliorarne l'affidabilità. Ovvero l'app non si arresterà in modo anomalo se il driver della stampante presenta un errore.


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

Specifica se è abilitata la funzionalità di scorrimento a risoluzione elevata. **True** indica che è abilitato. Non ha attributi.

<span id="msix"></span><span id="MSIX"></span>

### <a name="msix"></a>msix

Specifica le informazioni di identità di un [pacchetto MSIX di tipo sparse](/windows/apps/desktop/modernize/grant-identity-to-nonpackaged-apps) per l'applicazione corrente. Questo elemento è supportato in Windows 10, versione 2004 e versioni successive.

L'elemento **msix** deve trovarsi nello spazio dei nomi `urn:schemas-microsoft-com:msix.v1` . Dispone degli attributi illustrati nella tabella seguente.

| Attributo   | Descrizione                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| **pubblicazione**    | Descrive le informazioni del server di pubblicazione. Questo valore deve corrispondere all'attributo **Publisher** nell'elemento [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) del manifesto del pacchetto sparse. |
| **packageName** | Descrive il contenuto del pacchetto. Questo valore deve corrispondere all'attributo **Name** nell'elemento [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) del manifesto del pacchetto sparse.    |
| **applicationId**    | Identificatore univoco dell'applicazione. Questo valore deve corrispondere all'attributo **ID** nell'elemento [Application](/uwp/schemas/appxpackage/uapmanifestschema/element-application) nel manifesto del pacchetto sparse.  |

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

Esegue l'override dell'implementazione dell'heap predefinita per le [API dell'heap Win32](../Memory/heap-functions.md) da usare.

* Il valore **SegmentHeap** indica che verrà utilizzato l'heap del segmento. Heap segmenti è un'implementazione moderna dell'heap che in genere riduce l'utilizzo complessivo della memoria. Questo elemento è supportato in Windows 10, versione 2004 (Build 19041) e versioni successive.
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

Di seguito è riportato un esempio di un manifesto dell'applicazione per un'applicazione denominata MySampleApp.exe. L'applicazione utilizza l'assembly side-by-side di SampleAssembly.

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
