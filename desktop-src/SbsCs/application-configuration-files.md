---
description: Un file di configurazione dell'applicazione è un file XML utilizzato per controllare l'associazione di assembly.
ms.assetid: b7453f2b-52a4-4af9-8410-ebbb430ada67
title: File di configurazione dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b1a2e0f6b493c217aded9e11507f660d517b400
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128834"
---
# <a name="application-configuration-files"></a>File di configurazione dell'applicazione

Un file di configurazione dell'applicazione è un file XML utilizzato per controllare l'associazione di assembly. Può reindirizzare un'applicazione utilizzando una versione di un assembly affiancato a un'altra versione dello stesso assembly. Questa operazione viene definita [configurazione per ogni applicazione](per-application-configuration.md). Un file di configurazione dell'applicazione si applica solo a uno specifico manifesto dell'applicazione e ad assembly dipendenti. Per i componenti isolati compilati con un \_ manifesto di ID risorsa manifesto ISOLATIONAWARE incorporato è \_ \_ necessario un file di configurazione dell'applicazione separato. I manifesti gestiti con [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) richiedono un file di configurazione dell'applicazione separato.

Il reindirizzamento specificato da un file di configurazione dell'applicazione può sostituire le versioni degli assembly specificate dai [manifesti dell'applicazione](application-manifests.md) e dai [file di configurazione del server di pubblicazione](publisher-configuration-files.md). Se, ad esempio, un file di configurazione del server di pubblicazione specifica che tutti i riferimenti a un assembly vengono reindirizzati dalla versione 1.0.0.0 a 1.1.0.0, è possibile usare un file di configurazione dell'applicazione per reindirizzare un'applicazione specifica per l'uso della versione 1.0.0.0. Un file di configurazione dell'applicazione si applica solo al manifesto dell'applicazione e agli assembly dipendenti specificati.

Per un elenco completo dei XML Schema, vedere [schema del file di configurazione dell'applicazione](application-configuration-file-schema.md).

I file di configurazione dell'applicazione hanno gli elementi e gli attributi illustrati nella tabella seguente.



| Elemento               | Attributi                | Necessario |
|-----------------------|---------------------------|----------|
| **configurazione**     |                           | Sì      |
| **windows**           |                           | Sì      |
| **publisherPolicy apply**   |                           | Sì      |
|                       | **applicare**                 | Sì      |
| **runtime**           |                           | No       |
| **assemblyBinding**   |                           | Sì      |
| **sondaggio**           |                           | No       |
|                       | **privatePath**           | Sì      |
| **dipendenza**        |                           | No       |
| **dependentAssembly** |                           | Sì      |
| **assemblyIdentity**  |                           | Sì      |
|                       | **type**                  | Sì      |
|                       | **nome**                  | Sì      |
|                       | **language**              | No       |
|                       | **processorArchitecture** | Sì      |
|                       | **version**               | Sì      |
|                       | **publicKeyToken**        | No       |
| **bindingRedirect**   |                           | Sì      |
|                       | **oldVersion**            | Sì      |
|                       | **newVersion**            | Sì      |



 

## <a name="file-location"></a>Percorso file

I file di configurazione dell'applicazione devono essere installati nello stesso percorso del [manifesto](application-manifests.md)dell'applicazione.

## <a name="file-name-syntax"></a>Sintassi del nome file

Il nome di un file di configurazione dell'applicazione è il nome dell'eseguibile dell'applicazione seguito da. config.

Ad esempio, un file di configurazione dell'applicazione che fa riferimento a Example.exe o Example.dll utilizzerà la sintassi del nome file illustrata nell'esempio seguente. È possibile omettere il campo per <*ID risorsa*> se si installa il file di configurazione come file separato o se l'ID risorsa è 1.

**example.exe. <*ID risorsa* # C1.config**

**example.dll. <*ID risorsa* # C1.config**

## <a name="elements"></a>Elementi

I nomi degli elementi e degli attributi distinguono tra maiuscole e minuscole. I valori degli elementi e degli attributi non fanno distinzione tra maiuscole e minuscole, ad eccezione del valore dell'attributo Type.

<span id="configuration"></span><span id="CONFIGURATION"></span>

### <a name="configuration"></a>configurazione

Elemento contenitore per gli elementi **Windows** e **Runtime** di un file di configurazione dell'applicazione. Obbligatorio.

<span id="windows"></span><span id="WINDOWS"></span>

### <a name="windows"></a>windows

Include le parti del file di configurazione dell'applicazione che si applicano al reindirizzamento degli assembly Win32.

> [!Note]  
> L'autore di un'applicazione non deve includere un file di configurazione con un sottoelemento **Windows** come parte dell'applicazione. Questo può essere consentito se l'unico scopo del file di configurazione è abilitare la funzionalità **privatePath** di un elemento **Probe** . L'elemento **Probe** non è disponibile nei sistemi precedenti a windows Server 2008 R2 e Windows 7.

<span id="publisherPolicy"></span><span id="publisherpolicy"></span><span id="PUBLISHERPOLICY"></span>

### <a name="publisherpolicy"></a>publisherPolicy apply

Specifica se applicare i criteri dell'editore.

Questo elemento ha gli attributi mostrati nella tabella seguente.



| Attributo | Descrizione                                                                                                                     |
|-----------|---------------------------------------------------------------------------------------------------------------------------------|
| **applicare** | Il valore "Yes" applica i criteri dell'editore. Si tratta dell'impostazione predefinita. Il valore "No" non applica i criteri dell'editore. |

<span id="runtime"></span><span id="RUNTIME"></span>

### <a name="runtime"></a>runtime

Include le parti del file di configurazione dell'applicazione che si applicano al reindirizzamento degli assembly .NET.

<span id="assemblyBinding"></span><span id="assemblybinding"></span><span id="ASSEMBLYBINDING"></span>

### <a name="assemblybinding"></a>assemblyBinding

Include le informazioni di reindirizzamento per l'applicazione e l'assembly interessato da questo file di configurazione dell'applicazione. Il primo sottoelemento di **assembly** deve essere un **assemblyIdentity** che identifica l'applicazione.

A partire da Windows Server 2008 R2 e Windows 7 un elemento **assembly** può includere un sottoelemento **Probe** .

<span id="probing"></span><span id="PROBING"></span>

### <a name="probing"></a>esecuzione del probe

Sottoelemento facoltativo di un elemento **assembler** che estende la ricerca di assembly in directory aggiuntive. Non è necessario che le directory aggiuntive siano sottodirectory della directory dell'assembly.

> [!Note]  
> Questo elemento non è disponibile nei sistemi precedenti a Windows Server 2008 R2 e Windows 7 e può essere utilizzato solo all'interno di un elemento di **Windows** .

Questo elemento ha gli attributi mostrati nella tabella seguente.

| Attributo       | Descrizione                                                                                                                                                                                                                                   |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **privatePath** | Specifica i [percorsi relativi](/windows/desktop/FileIO/naming-a-file) delle sottodirectory della directory di base dell'applicazione che potrebbero contenere assembly. È possibile specificare un massimo di nove percorsi di sottodirectory. Delimita il percorso di ogni sottodirectory con un punto e virgola. |

È possibile utilizzare l'identificatore speciale a doppio punti in un percorso per indicare la directory padre della directory corrente. Non è possibile specificare più di due livelli al di sopra della directory corrente usando i doppi punti. Non usare i puntini di sospensione. Ad esempio, un'applicazione che usa l'elemento di **sondaggio** seguente controlla le directory aggiuntive per un assembly.

``` XML
<probing privatePath="bin;..\bin2\subbin;bin3"/>
```

<span id="dependency"></span><span id="DEPENDENCY"></span>

### <a name="dependency"></a>dependency
Elemento contenitore per almeno un **dependentAssembly**. Ogni **dependentAssembly** può trovarsi all'interno di una sola **dipendenza**. Questo elemento non ha attributi. facoltativo.

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>

### <a name="dependentassembly"></a>dependentAssembly

Il primo sottoelemento deve essere un elemento **assemblyIdentity** che identifica l'assembly affiancato che viene reindirizzato dal file di configurazione dell'applicazione. Un **dependentAssembly** non ha attributi.

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>

### <a name="assemblyidentity"></a>assemblyIdentity

Come primo sottoelemento di un elemento **assembly** , **assemblyIdentity** descrive e identifica in modo univoco un'applicazione. Il file di configurazione dell'applicazione reindirizza l'associazione dell'applicazione agli assembly affiancati. Il seguente **assemblyIdentity** indica, ad esempio, che il file di configurazione dell'applicazione influisca sull'associazione dell'applicazione mysampleApp agli assembly affiancati. Gli assembly da reindirizzare verranno identificati in un **dependentAssembly**.

``` XML
<assemblyIdentity processorArchitecture="X86" name="Microsoft.Windows.mysampleApp" type="win32" version="1.0.0.0"/>
```

Come primo sottoelemento di un elemento **dependentAssembly** , **assemblyIdentity** descrive un assembly affiancato da cui dipende l'applicazione. Il file di configurazione dell'applicazione riconfigura l'identità dell'assembly richiesto. Ad esempio, i seguenti elementi **assemblyIdentity** e **bindingRedirect** riconfigurano una dipendenza in Microsoft. Windows. SampleAssembly dalla versione 2.0.0.0 alla versione 2.1.0.0.

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

Si noti che ogni **assemblyIdentity** incluso in un **dependentAssembly** deve corrispondere esattamente a **assemblyIdentity** nel [manifesto](assembly-manifests.md)dell'assembly.

L'elemento **assemblyIdentity** ha gli attributi seguenti. Non contiene sottoelementi.

| Attributo                 | Descrizione                                                                                                                                                                                                                                                                                                          |
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **type**                  | Il valore deve essere Win32 (lettere minuscole). Obbligatorio.                                                                                                                                                                                                                                                                      |
| **nome**                  | L'attributo Name identifica l'applicazione interessata dal file di configurazione dell'applicazione o dall'assembly da reindirizzare. Usare il formato seguente per il nome: Organization.Division.Name. Obbligatorio. Ad esempio: Microsoft. Windows. MysampleApp o Microsoft. Windows. MysampleAsm.<br/>            |
| **language**              | Identifica la lingua. facoltativo. Per un oggetto **assemblyIdentity** che fa riferimento a un assembly, se l'assembly è specifico della lingua, specificare il codice della lingua DHTML. Se l'assembly è per l'uso in tutto il mondo (indipendente dalla lingua), impostare il valore come " \* ".<br/>                                                            |
| **processorArchitecture** | Specifica il processore che esegue l'applicazione.                                                                                                                                                                                                                                                                     |
| **version**               | Specifica la versione dell'applicazione o dell'assembly. Usare la sintassi di versione in quattro parti: mmmm. nnnn. oooo. pppp. Obbligatorio.                                                                                                                                                                                                   |
| **publicKeyToken**        | Per un oggetto **assemblyIdentity** che fa riferimento a un assembly, una stringa esadecimale di 16 caratteri che rappresenta gli ultimi 8 byte dell'hash SHA-1 della chiave pubblica in cui è firmato l'assembly. La chiave pubblica usata per firmare il catalogo deve essere di 2048 bit o superiore. Obbligatorio per tutti gli assembly affiancati condivisi. |

<span id="bindingRedirect"></span><span id="bindingredirect"></span><span id="BINDINGREDIRECT"></span>

### <a name="bindingredirect"></a>bindingRedirect

L'elemento **bindingRedirect** contiene informazioni di reindirizzamento per l'associazione dell'assembly. Ogni **bindingRedirect** deve essere incluso esattamente in un **dependentAssembly**. La sintassi di versione in quattro parti della nuova versione e della versione precedente deve specificare le stesse versioni principale e secondaria.

Questo elemento ha gli attributi mostrati nella tabella seguente.

| Attributo      | Descrizione                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **oldVersion** | Specifica la versione dell'assembly sottoposta a override e reindirizzato. Usare la sintassi di versione in quattro parti nnnnn. NNNNN. NNNNN. NNNNN. Specificare un intervallo di versioni di un trattino senza spazi. Ad esempio, 2.14.3.0 o 2.14.3.0 2.16.0.0. Obbligatorio. |
| **newVersion** | Specifica la versione dell'assembly sostitutivo. Usare la sintassi di versione in quattro parti nnnnn. NNNNN. NNNNN. NNNNN.                                                                                                                                     |

## <a name="remarks"></a>Commenti

I file di configurazione dell'applicazione non specificano i file.

## <a name="example"></a>Esempio

``` XML
<bindingRedirect oldVersion="1.0.0.0" newVersion="1.0.10.0"/>
<bindingRedirect oldVersion="1.0.50.2011-1.0.60.65535" newVersion="1.0.70.0"/>
```
