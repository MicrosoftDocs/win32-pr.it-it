---
description: Un file di configurazione dell'applicazione è un file XML usato per controllare l'associazione di assembly.
ms.assetid: b7453f2b-52a4-4af9-8410-ebbb430ada67
title: File di configurazione dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cf4b22d3710c0dd38e83f827a175ad591309f22ab8ac2d81e93438f27d07dc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142524"
---
# <a name="application-configuration-files"></a>File di configurazione dell'applicazione

Un file di configurazione dell'applicazione è un file XML usato per controllare l'associazione di assembly. Può reindirizzare un'applicazione dall'uso di una versione di un assembly side-by-side a un'altra versione dello stesso assembly. Questa operazione è denominata [configurazione per applicazione.](per-application-configuration.md) Un file di configurazione dell'applicazione si applica solo a un manifesto dell'applicazione specifico e ad assembly dipendenti. I componenti isolati compilati con un manifesto DI RISORSA MANIFESTO ISOLATIONAWARE incorporato \_ richiedono un file di configurazione \_ \_ dell'applicazione separato. I manifesti gestiti con [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) richiedono un file di configurazione dell'applicazione separato.

Il reindirizzamento specificato da un file di configurazione dell'applicazione può eseguire l'override delle versioni dell'assembly specificate dai [manifesti dell'applicazione](application-manifests.md) e dai file di configurazione [dell'editore.](publisher-configuration-files.md) Ad esempio, se un file di configurazione dell'editore specifica che tutti i riferimenti a un assembly devono essere reindirizzati dalla versione 1.0.0.0 alla 1.1.0.0, è possibile usare un file di configurazione dell'applicazione per reindirizzare una particolare applicazione per l'uso della versione 1.0.0.0. Un file di configurazione dell'applicazione si applica solo al manifesto dell'applicazione e agli assembly dipendenti specificati.

Per un elenco completo dello schema XML, vedere [Schema del file di configurazione dell'applicazione](application-configuration-file-schema.md).

I file di configurazione dell'applicazione hanno gli elementi e gli attributi illustrati nella tabella seguente.



| Elemento               | Attributi                | Necessario |
|-----------------------|---------------------------|----------|
| **configurazione**     |                           | Sì      |
| **windows**           |                           | Sì      |
| **publisherPolicy**   |                           | Sì      |
|                       | **Applicare**                 | Sì      |
| **Runtime**           |                           | No       |
| **assemblyBinding**   |                           | Sì      |
| **Sondaggio**           |                           | No       |
|                       | **privatePath**           | Sì      |
| **Dipendenza**        |                           | No       |
| **dependentAssembly** |                           | Sì      |
| **Assemblyidentity**  |                           | Sì      |
|                       | **type**                  | Sì      |
|                       | **nome**                  | Sì      |
|                       | **language**              | No       |
|                       | **processorArchitecture** | Sì      |
|                       | **version**               | Sì      |
|                       | **Publickeytoken**        | No       |
| **bindingRedirect**   |                           | Sì      |
|                       | **oldVersion**            | Sì      |
|                       | **newVersion**            | Sì      |



 

## <a name="file-location"></a>Percorso file

I file di configurazione dell'applicazione devono essere installati nello stesso percorso del manifesto [dell'applicazione.](application-manifests.md)

## <a name="file-name-syntax"></a>Sintassi del nome file

Il nome di un file di configurazione dell'applicazione è il nome del file eseguibile dell'applicazione seguito da .config.

Ad esempio, un file di configurazione dell'applicazione che fa riferimento Example.exe o Example.dll usa la sintassi del nome file illustrata nell'esempio seguente. È possibile omettere il campo per <*ID* risorsa> se si installa il file di configurazione come file separato o se l'ID risorsa è 1.

**example.exe.<*risorsa>.config***

**example.dll.<*risorsa>.config***

## <a name="elements"></a>Elementi

Per i nomi di elementi e attributi viene fatto distinzione tra maiuscole e minuscole. Per i valori di elementi e attributi non viene fatta distinzione tra maiuscole e minuscole, ad eccezione del valore dell'attributo type.

<span id="configuration"></span><span id="CONFIGURATION"></span>

### <a name="configuration"></a>configurazione

Elemento contenitore per gli elementi **windows e** **runtime** di un file di configurazione dell'applicazione. Obbligatorio.

<span id="windows"></span><span id="WINDOWS"></span>

### <a name="windows"></a>windows

Include le parti del file di configurazione dell'applicazione che si applicano al reindirizzamento degli assembly Win32.

> [!Note]  
> L'autore di un'applicazione non deve includere un file di configurazione con un sottoelemento **di Windows** come parte dell'applicazione. Questa operazione può essere consentita se l'unico scopo del file di configurazione è abilitare la **funzionalità privatePath** di un elemento **di probe.** **L'elemento di** probe non è disponibile nei sistemi precedenti Windows Server 2008 R2 e Windows 7.

<span id="publisherPolicy"></span><span id="publisherpolicy"></span><span id="PUBLISHERPOLICY"></span>

### <a name="publisherpolicy"></a>publisherPolicy

Specifica se applicare i criteri dell'editore.

Questo elemento ha gli attributi illustrati nella tabella seguente.



| Attributo | Descrizione                                                                                                                     |
|-----------|---------------------------------------------------------------------------------------------------------------------------------|
| **Applicare** | Il valore "yes" applica i criteri dell'editore. Si tratta dell'impostazione predefinita. Il valore "no" non applica i criteri dell'editore. |

<span id="runtime"></span><span id="RUNTIME"></span>

### <a name="runtime"></a>runtime

Include le parti del file di configurazione dell'applicazione che si applicano al reindirizzamento degli assembly .NET.

<span id="assemblyBinding"></span><span id="assemblybinding"></span><span id="ASSEMBLYBINDING"></span>

### <a name="assemblybinding"></a>assemblyBinding

Include le informazioni di reindirizzamento per l'applicazione e l'assembly interessato da questo file di configurazione dell'applicazione. Il primo sottoelemento **di assemblyBinding** deve essere **un elemento assemblyIdentity** che identifica l'applicazione.

A partire da Windows Server 2008 R2 e Windows 7 un **elemento assemblyBinding** può includere un **sottoelemento di** probe.

<span id="probing"></span><span id="PROBING"></span>

### <a name="probing"></a>esecuzione del probe

Sottoelemento facoltativo di **un elemento assemblyBinding** che estende la ricerca di assembly in directory aggiuntive. Le directory aggiuntive non devono essere sottodirectory della directory dell'assembly.

> [!Note]  
> Questo elemento non è disponibile nei sistemi precedenti Windows Server 2008 R2 e Windows 7 e può essere usato solo all'interno di un **elemento windows.**

Questo elemento ha gli attributi illustrati nella tabella seguente.

| Attributo       | Descrizione                                                                                                                                                                                                                                   |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **privatePath** | Specifica i [percorsi relativi](/windows/desktop/FileIO/naming-a-file) delle sottodirectory della directory di base dell'applicazione che potrebbero contenere assembly. È possibile specificare un massimo di nove percorsi di sottodirectory. Delimitare ogni percorso di sottodirectory con un punto e virgola. |

È possibile usare l'identificatore speciale con due punti in un percorso per indicare la directory padre della directory corrente. Non è possibile specificare più di due livelli oltre la directory corrente usando due punti. Non usare tre punti. Ad esempio, un'applicazione che usa l'elemento **di probe seguente** verifica la presenza di un assembly in directory aggiuntive.

``` XML
<probing privatePath="bin;..\bin2\subbin;bin3"/>
```

<span id="dependency"></span><span id="DEPENDENCY"></span>

### <a name="dependency"></a>dependency
Elemento contenitore per almeno un **dependentAssembly.** Ogni **dependentAssembly può** essere all'interno di una **sola dipendenza.** Questo elemento non ha attributi. facoltativo.

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>

### <a name="dependentassembly"></a>dependentAssembly

Il primo sottoelemento deve essere un **elemento assemblyIdentity** che identifica l'assembly side-by-side reindirizzato dal file di configurazione dell'applicazione. Un **dependentAssembly** non ha attributi.

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>

### <a name="assemblyidentity"></a>assemblyIdentity

Come primo sottoelemento di un **elemento assemblyBinding,** **assemblyIdentity** descrive e identifica in modo univoco un'applicazione. Il file di configurazione dell'applicazione reindirizza l'associazione di questa applicazione ad assembly side-by-side. Ad esempio, **l'elemento assemblyIdentity** seguente indica che il file di configurazione dell'applicazione influisce sull'associazione dell'applicazione mysampleApp agli assembly side-by-side. Gli assembly da reindirizzare verrebbero identificati in **un dependentAssembly.**

``` XML
<assemblyIdentity processorArchitecture="X86" name="Microsoft.Windows.mysampleApp" type="win32" version="1.0.0.0"/>
```

Come primo sottoelemento di un **elemento dependentAssembly,** **assemblyIdentity** descrive un assembly side-by-side da cui dipende l'applicazione. Il file di configurazione dell'applicazione riconfigura l'identità di questo assembly richiesto. Ad esempio, il **seguente assemblyIdentity** e **bindingRedirect** riconfigura una dipendenza da Microsoft. Windows. SampleAssembly dalla versione 2.0.0.0 alla versione 2.1.0.0.

``` XML
<dependency>
      <dependentAssembly>
         <assemblyIdentity type="win32"
          name="Microsoft.Windows.SampleAssembly"
          processorArchitecture="x86"
          publicKeyToken="0000000000000000"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.1.0.0"/>
      </dependentAssembly>
</dependency>
```

Si noti che **ogni assemblyIdentity** incluso in **un dependentAssembly** deve corrispondere esattamente a **assemblyIdentity** nel manifesto dell'assembly. [](assembly-manifests.md)

**L'elemento assemblyIdentity** ha gli attributi seguenti. Non dispone di sottoelementi.

| Attributo                 | Descrizione                                                                                                                                                                                                                                                                                                          |
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **type**                  | Il valore deve essere win32 (minuscolo). Obbligatorio.                                                                                                                                                                                                                                                                      |
| **nome**                  | L'attributo name identifica l'applicazione interessata dal file di configurazione dell'applicazione o dall'assembly da reindirizzare. Usare il formato seguente per il nome: Organization.Division.Name. Obbligatorio. Ad esempio: Microsoft. Windows. MysampleApp o Microsoft. Windows. MysampleAsm.<br/>            |
| **language**              | Identifica la lingua. facoltativo. Per un **assemblyIdentity** che fa riferimento a un assembly, se l'assembly è specifico del linguaggio, specificare il codice del linguaggio DHTML. Se l'assembly è per l'uso in tutto il mondo (indipendente dalla lingua), impostare il valore su " \* ".<br/>                                                            |
| **processorArchitecture** | Specifica il processore che esegue l'applicazione.                                                                                                                                                                                                                                                                     |
| **version**               | Specifica la versione dell'applicazione o dell'assembly. Usare la sintassi della versione in quattro parti: mmmm.nnnn.oooo.pppp. Obbligatorio.                                                                                                                                                                                                   |
| **Publickeytoken**        | Per **un assemblyIdentity** che fa riferimento a un assembly, stringa esadecimale di 16 caratteri che rappresenta gli ultimi 8 byte dell'hash SHA-1 della chiave pubblica con cui viene firmato l'assembly. La chiave pubblica usata per firmare il catalogo deve essere di 2048 bit o superiore. Obbligatorio per tutti gli assembly side-by-side condivisi. |

<span id="bindingRedirect"></span><span id="bindingredirect"></span><span id="BINDINGREDIRECT"></span>

### <a name="bindingredirect"></a>bindingRedirect

**L'elemento bindingRedirect** contiene informazioni di reindirizzamento per l'associazione dell'assembly. Ogni **bindingRedirect** deve essere incluso esattamente in **un dependentAssembly.** La sintassi della versione in quattro parti della nuova versione e della versione precedente deve specificare le stesse versioni principali e secondarie.

Questo elemento presenta gli attributi illustrati nella tabella seguente.

| Attributo      | Descrizione                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **oldVersion** | Specifica la versione dell'assembly sottoposta a override e reindirizzata. Usare la sintassi della versione in quattro parti nnnnn.nnnnn.nnnnn.nnnnn. Specificare un intervallo di versioni con un trattino senza spazi. Ad esempio, 2.14.3.0 o 2.14.3.0 2.16.0.0. Obbligatorio. |
| **newVersion** | Specifica la versione dell'assembly di sostituzione. Usare la sintassi della versione in quattro parti nnnnn.nnnnn.nnnnn.nnnnn.                                                                                                                                     |

## <a name="remarks"></a>Commenti

I file di configurazione dell'applicazione non specificano file.

## <a name="example"></a>Esempio

``` XML
<bindingRedirect oldVersion="1.0.0.0" newVersion="1.0.10.0"/>
<bindingRedirect oldVersion="1.0.50.2011-1.0.60.65535" newVersion="1.0.70.0"/>
```
