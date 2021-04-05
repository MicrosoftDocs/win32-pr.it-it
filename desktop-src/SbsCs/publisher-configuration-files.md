---
description: Un file di configurazione del server di pubblicazione è un file XML che reindirizza a livello globale le applicazioni e gli assembly usando una versione di un assembly affiancato a un'altra versione dello stesso assembly.
ms.assetid: b10752af-80a7-4027-b525-90333d0d010a
title: File di configurazione del server di pubblicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cc5d7d7b7ffdad3d1179a7f8c66a347d91e0a03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884533"
---
# <a name="publisher-configuration-files"></a>File di configurazione del server di pubblicazione

Un file di configurazione del server di pubblicazione è un file XML che reindirizza a livello globale le applicazioni e gli assembly usando una versione di un assembly affiancato a un'altra versione dello stesso assembly. In genere, l'autore dell'assembly rilascia un aggiornamento compatibile o una correzione della sicurezza per ogni assembly mediante l'emissione di un file di configurazione dell'editore da installare insieme a un Service Pack aggiornamento. Questa operazione viene definita [configurazione del server di pubblicazione](publisher-configuration.md). Per ulteriori informazioni su questo tipo di [configurazione](configuration.md) , vedere Configurazione del server di pubblicazione.

I file di configurazione del server di pubblicazione presentano gli elementi e gli attributi seguenti. Per un elenco completo dei XML Schema, vedere [schema del file di configurazione dell'editore](publisher-configuration-file-schema.md).



| Elemento               | Attributi                | Necessario |
|-----------------------|---------------------------|----------|
| **assembly**          |                           | Sì      |
|                       | **manifestVersion**       | Sì      |
| **assemblyIdentity**  |                           | Sì      |
|                       | **type**                  | Sì      |
|                       | **nome**                  | Sì      |
|                       | **language**              | No       |
|                       | **processorArchitecture** | No       |
|                       | **version**               | Sì      |
|                       | **publicKeyToken**        | No       |
| **dipendenza**        |                           | No       |
| **dependentAssembly** |                           | No       |
| **bindingRedirect**   |                           | Sì      |
|                       | **oldVersion**            | Sì      |
|                       | **newVersion**            | Sì      |



 

## <a name="file-location"></a>Percorso file

I file di configurazione del server di pubblicazione devono essere installati nella cartella WinSxS. Vengono in genere installate come file separati, ma i file di configurazione del server di pubblicazione possono essere inclusi anche come risorsa in una DLL. Un file di configurazione del server di pubblicazione non può essere incluso come risorsa in un file EXE. Un file EXE può includere un [manifesto dell'applicazione](application-manifests.md) come risorsa.

## <a name="file-name-syntax"></a>Sintassi del nome file

Il nome file di un file di configurazione del server di pubblicazione ha il formato *criterio*. *principale*. *minore*. *AssemblyName* dove *Major* e *minor* fanno riferimento alle parti principali e secondarie della [versione dell'assembly](assembly-versions.md) interessata. *AssemblyName* fa riferimento al nome dell'assembly.

Ad esempio, un file di configurazione del server di pubblicazione per la versione 6,0 dell'assembly Microsoft. Windows. Common-Controls avrà il nome seguente:

<dl> Policy. 6.0. Microsoft. Windows. Common-Controls  
</dl>

Non usare i file di configurazione dei criteri per incrementare la versione principale o secondaria di un assembly. Ad esempio, non reindirizzare la versione 6.0.0.0 a 7.0.0.0 o versione 6.1.0.0. Quando un'applicazione fa riferimento a una versione dell'assembly, ad esempio 6.0.0.0, viene verificata la presenza di eventuali file di configurazione dei criteri con le versioni principale e secondaria specificate, ad esempio 6,0. L'applicazione viene quindi reindirizzata a un'altra versione dell'assembly, ad esempio 6.0.1.0. Se un file di configurazione del server di pubblicazione incrementa la versione principale o secondaria di un assembly, il reindirizzamento successivo dell'assembly potrebbe richiedere l'emissione di più file di configurazione dei criteri.

## <a name="elements"></a>Elementi

<dl> <dt>

<span id="assembly"></span><span id="ASSEMBLY"></span>**assembly**
</dt> <dd>

Elemento contenitore. Il primo sottoelemento deve essere un elemento **assemblyIdentity**. Obbligatorio.

L'elemento assembly deve trovarsi nello spazio dei nomi **urn: schemas-microsoft-com: ASM. V1**. Gli elementi figlio dell'assembly devono trovarsi anche in questo spazio dei nomi, in base all'ereditarietà o all'assegnazione di tag.

L'elemento **assembly** ha gli attributi seguenti.



| Attributo           | Descrizione                                           |
|---------------------|-------------------------------------------------------|
| **manifestVersion** | L'attributo **manifestVersion** deve essere impostato su 1,0. |



 

</dd> <dt>

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>**assemblyIdentity**
</dt> <dd>

Descrive e identifica in modo univoco un assembly side-by-side.

Come primo sottoelemento di un elemento **assembly** , **assemblyIdentity** descrive l'assembly affiancato in cui sono state modificate una o più delle relative dipendenze di assembly. Il file di configurazione del server di pubblicazione reindirizza le dipendenze dell'assembly identificato. Il seguente **assemblyIdentity** indica, ad esempio, che il file di configurazione del server di pubblicazione influisca sulle dipendenze dell'assembly Microsoft. Windows. pop 6.0.0.0 x86.

``` syntax
<assemblyIdentity 
     type="win32-policy" 
     publicKeyToken="0000000000000000" 
     name="policy.6.0.Microsoft.Windows.Pop" 
     version="2.1.0.0" 
     processorArchitecture="x86"/>
```

Come primo sottoelemento di un elemento **dependentAssembly** , **assemblyIdentity** descrive una dipendenza di assembly side-by-side. Il file di configurazione del server di pubblicazione riconfigura l'identità dell'assembly side-by-side richiesto. La modifica viene specificata in un **bindingRedirect**. Ad esempio, il codice **assemblyIdentity** seguente modifica qualsiasi dipendenza da Microsoft. Windows. SampleAssembly versione 2.0.0.0 a una dipendenza da Microsoft. Windows. SampleAssembly versione 2.0.1.0.

``` syntax
<dependency>
      <dependentAssembly>
         <assemblyIdentity 
type="win32" 
name="Microsoft.Windows.SampleAssembly"  
processorArchitecture="x86"
publicKeyToken="0000000000000000"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.1.0"/>
      </dependentAssembly>
</dependency>
```

L'elemento **assemblyIdentity** ha gli attributi seguenti. Non contiene sottoelementi.



| Attributo                 | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **type**                  | Specifica il tipo di assembly. Obbligatorio. In **assemblyIdentity** per l'assembly interessato, il valore dell'attributo **Type** deve essere impostato su Win32-Policy. Il valore Win32-Policy deve essere in lettere minuscole.<br/> In **assemblyIdentity** per la dipendenza di assembly modificabile, il valore dell'attributo **Type** deve essere impostato su Win32. Il valore Win32 deve essere in lettere minuscole.<br/>                                                                                                                                                                                                             |
| **nome**                  | Assegna un nome univoco a un assembly. Obbligatorio. In **assemblyIdentity** per l'assembly interessato, il nome ha i *criteri* del modulo. *principale*. *minore*. *AssemblyName* dove *Major* e *minor* fanno riferimento alle parti principali e secondarie della [versione dell'assembly](assembly-versions.md).<br/> In **assemblyIdentity** per la dipendenza di assembly in modifica, il nome ha il formato Organization.Division.Name. Ad esempio, Microsoft. Windows. MysampleApp.<br/>                                                                                                                                                                                 |
| **language**              | Identifica la lingua dell'assembly. facoltativo. In **assemblyIdentity** per l'assembly interessato, se l'assembly è specifico della lingua, specificare il codice della lingua DHTML. Se l'assembly è per l'uso in tutto il mondo (indipendente dalla lingua), omettere questo attributo.<br/> In **assemblyIdentity** per la dipendenza di assembly modificabile, se l'assembly è specifico della lingua, specificare il codice della lingua DHTML. Se l'assembly è per l'uso in tutto il mondo (indipendente dalla lingua), impostare il valore come " \* ".<br/>                                                                                                                            |
| **processorArchitecture** | Specifica il processore che esegue l'applicazione.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **version**               | Specifica la versione dell'assembly. Usare la sintassi di versione in quattro parti: mmmm. nnnn. oooo. pppp Obbligatorio solo nel contesto di definizione **assemblyIdentity**. Non specificare l'attributo Version nell'oggetto **assemblyIdentity** del contesto di riferimento.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **publicKeyToken**        | Stringa esadecimale di 16 caratteri che rappresenta gli ultimi 8 byte dell'hash SHA-1 della chiave pubblica in cui è firmato l'assembly. La chiave pubblica usata per firmare il catalogo deve essere di 2048 bit o superiore. Un publicKeyToken è obbligatorio per tutti gli assembly affiancati condivisi. Il publicKeyToken utilizzato per il file di configurazione del server di pubblicazione deve essere la stessa chiave utilizzata per l'assembly firmato. I file di configurazione del server di pubblicazione possono essere firmati usando gli stessi strumenti usati con gli assembly, vedere [esempio di firma di assembly](assembly-signing-example.md) e creazione di [file e cataloghi firmati](creating-signed-files-and-catalogs.md). |



 

</dd> <dt>

<span id="dependency"></span><span id="DEPENDENCY"></span>**dipendenza**
</dt> <dd>

Elemento contenitore facoltativo per almeno un **dependentAssembly**. Non ha attributi.

</dd> <dt>

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>**dependentAssembly**
</dt> <dd>

Ogni **dependentAssembly** deve trovarsi all'interno di una sola **dipendenza**. Un **dependentAssembly** non ha attributi. Il primo sottoelemento di **dependentAssembly** deve essere un **assemblyIdentity** per l'assembly affiancato riconfigurato dalla configurazione del server di pubblicazione.

</dd> <dt>

<span id="bindingRedirect"></span><span id="bindingredirect"></span><span id="BINDINGREDIRECT"></span>**bindingRedirect**
</dt> <dd>

L'elemento **bindingRedirect** contiene informazioni di reindirizzamento per l'associazione dell'assembly.

Questo elemento ha gli attributi mostrati nella tabella seguente.



| Attributo      | Descrizione                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **oldVersion** | Specifica la versione dell'assembly sottoposta a override e reindirizzato. Usare la sintassi di versione in quattro parti nnnnn. NNNNN. NNNNN. NNNNN. Specificare un intervallo di versioni di un trattino senza spazi. Ad esempio, 2.14.3.0 o 2.14.3.0 2.16.0.0. Obbligatorio. |
| **newVersion** | Specifica la versione dell'assembly sostitutivo. Usare la sintassi di versione in quattro parti nnnnn. NNNNN. NNNNN. NNNNN.                                                                                                                                     |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

I file di configurazione del server di pubblicazione non specificano i file. Si noti che i file di criteri specifici della lingua sono separati dal file di configurazione del server di pubblicazione.

## <a name="example"></a>Esempio

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity type="win32-policy" publicKeyToken="0000000000000000" name="policy.6.0.Proseware.Research.SampleAssembly" version="1.0.1.0" language="en-us" processorArchitecture="x86"/>
<dependency>
<dependentAssembly>
<assemblyIdentity type="win32" publicKeyToken="0000000000000000" name="Proseware.Research.SampleAssembly" language="en-us" processorArchitecture="x86"/>
<bindingRedirect oldVersion="1.0.0.0" newVersion="1.0.1.0"/>
</dependentAssembly>
</dependency>
</assembly>
```

 

 




