---
description: Il file di Mt.exe è uno strumento che genera file e cataloghi firmati. È disponibile nel Software Development Kit (SDK) di Microsoft Windows. Mt.exe richiede che il file a cui si fa riferimento nel manifesto sia presente nella stessa directory del manifesto.
ms.assetid: 37f010ee-2658-4547-9871-c913201042de
title: Mt.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df654a943bad272a091dc6ac20cc1dcdab1731a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305618"
---
# <a name="mtexe"></a>Mt.exe

Il file di Mt.exe è uno strumento che genera file e cataloghi firmati. È disponibile nel Software Development Kit (SDK) di Microsoft Windows. Mt.exe richiede che il file a cui si fa riferimento nel manifesto sia presente nella stessa directory del manifesto.

Mt.exe genera gli hash usando l'implementazione CryptoAPI dell'algoritmo Secure Hash Algorithm (SHA-1). Per ulteriori informazioni sugli algoritmi hash, vedere [algoritmi hash e di firma](/windows/desktop/SecCrypto/hash-and-signature-algorithms). Gli hash vengono inseriti come stringa esadecimale nei tag del **file** nel manifesto. Lo strumento attualmente genera solo hash SHA-1, anche se i file nei manifesti possono usare altri schemi di hashing.

Mt.exe utilizza Makecat.exe per generare file di catalogo (con estensione cat) dai file di definizione del catalogo (con estensione CDF). Questo strumento compila un modello standard CDF con il nome e il percorso del manifesto. Questa operazione può essere utilizzata con Makecat.exe per generare il catalogo degli assembly.

La versione di Mt.exe fornita nelle versioni recenti del Windows SDK può essere usata anche per generare manifesti per assembly gestiti e assembly side-by-side non gestiti.

## <a name="syntax"></a>Sintassi

**mt.exe \[ -manifest** _<Component1. manifest><Component2. manifest>_ *_\] \[ -Identity:_* *<identity string> * **\] \[ -RGS:** _<file1. RGS>_* _\] \[ -tlb:_ *_<file2. tlb>_* _\] \[ -dll:_ *_<file3.dll_*>_\] \[ -sostituzioni:_ *_<XML filename>_* _\] \[ -managedassemblyname:_ *_<managed assembly>_* _\] \[ -nodependency \] \[ -Category \] \[ -out:_ *_<output manifest name>_* _\] \[ -inputresource:_ *_<file4>_* _; \[ \# \]_ *_ID risorsa><0 \_><1_* _\] \[ -outputresource:_ *_<file5>_* _\[ \# ; \]_ *_ID risorsa><2 \_><3_* _\] \[ -UpdateResource:_ *_<file6>_* _\[ \# ; \]_ *_ID risorsa><4 \_><5_* _\] \[ -hashupdate \[ :_ *_<path to files>_* _\] \] \[ -makecdfs \] \[ -convalidare gli \_ hash di file manifest- \] \[ Validate \_ \_ :_ *_<path to files>_* _\] \[ -Canonicalize \] \[ -Check \_ for \_ Duplicates \] \[ -nologo \] \[ -verbose \]_*

## <a name="command-line-options"></a>Opzioni da riga di comando

Mt.exe usa le seguenti opzioni della riga di comando senza distinzione tra maiuscole e minuscole.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Opzione</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>-manifesto</td>
<td>Specifica il nome del file manifesto. Per modificare un singolo manifesto, specificare un nome di file manifesto. Ad esempio, Component. manifest.<br/> Per unire più manifesti, specificare qui i nomi dei manifesti di origine. Specificare il nome del manifesto aggiornato con le opzioni <strong>-out</strong>, <strong>-outputresource</strong>o <strong>-UpdateResource</strong> . La riga di comando seguente, ad esempio, richiede un'operazione che unisce due manifesti, man1. manifest e man2. manifest, in un nuovo manifesto Man3. manifest.<br/> <strong>mt.exe-manifest man1. manifest man2. manifest-out: man3. manifest</strong><br/>
<blockquote>
[!Note]<br />
Nessun segno di due punti (:) è obbligatorio con l'opzione <strong>-manifest</strong> .
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td>-Identity</td>
<td>Fornisce i valori degli attributi dell'elemento <strong>assemblyIdentity</strong> del manifesto. L'argomento dell'opzione <strong>-Identity</strong> è un valore stringa contenente i valori di attributo nei campi separati da virgole. Specificare il valore dell'attributo <strong>Name</strong> nel primo campo, senza includere un &quot; nome = &quot; substring. Tutti i campi rimanenti specificano gli attributi e i rispettivi valori usando il formato: <em> <attribute name> </em> = <em> <attribute_value> </em> .<br/> Ad esempio, per aggiornare l'elemento <strong>assemblyIdentity</strong> del manifesto con le informazioni seguenti:<br/> <assemblyIdentity type=&quot;win32&quot; name=&quot;Microsoft.Windows.SampleAssembly&quot; version=&quot;6.0.0.0&quot; processorArchitecture=&quot;x86&quot; publicKeyToken=&quot;a5aaf5ba15723d5&quot;/> <br/> includere l'opzione <strong>-Identity</strong> seguente nella riga di comando:<br/> <strong>-Identity:</strong> &quot; Microsoft. Windows. SampleAssembly, processorArchitecture = x86, Version = 6.0.0.0, Type = Win32, publicKeyToken = a5aaf5ba15723d5&quot;<br/></td>
</tr>
<tr class="odd">
<td>-RGS</td>
<td>Specifica il nome del file dello script di registrazione (con estensione RGS). L'opzione <strong>-dll</strong> è necessaria per usare l'opzione <strong>-RGS</strong> .<br/></td>
</tr>
<tr class="even">
<td>-TLB</td>
<td>Specifica il nome del file di libreria dei tipi (TLB). L'opzione <strong>-dll</strong> è necessaria per usare l'opzione <strong>-tlb</strong> .<br/></td>
</tr>
<tr class="odd">
<td>-dll</td>
<td>Specifica il nome del file DLL (Dynamic-Link Library). L'opzione <strong>-dll</strong> è richiesta da <strong>mt.exe</strong> se vengono usate le opzioni <strong>-RGS</strong> o <strong>-tlb</strong> . Consente di specificare il nome della DLL che si desidera compilare successivamente dai file con estensione rgs o tlb.<br/> Il comando seguente, ad esempio, richiede un'operazione che genera un manifesto dai file con estensione rgs e tlb.<br/> <strong>mt.exe-RGS: testreg1. RGS-tlb: testlib1. tlb -dll:test.dll-Replaces: Rep. manifest-Identity: &quot; Microsoft. Windows. SampleAssembly, processorArchitecture = x86, Version = 6.0.0.0, Type = Win32, PublicKeyToken = a5aaf5ba15723d5 &quot; -out: rgstlb. manifest</strong><br/></td>
</tr>
<tr class="even">
<td>-sostituzioni</td>
<td>Specifica il file che contiene i valori per la stringa sostituibile nel file con estensione rgs.<br/></td>
</tr>
<tr class="odd">
<td>-managedassemblyname</td>
<td>Genera un manifesto dall'assembly gestito specificato. Utilizzare con l'opzione <strong>-nodependency</strong> per generare un manifesto senza elementi di dipendenza. Usare con l'opzione <strong>-Category</strong> per generare un manifesto con tag category. Se ad esempio managed.dll è un assembly gestito, la riga di comando seguente genera il file out. manifest da managed.dll.<br/> <strong>mt.exe -managedassemblyname:managed.dll: out. manifest</strong> <br/></td>
</tr>
<tr class="even">
<td>-nodependency</td>
<td>Specifica un'operazione che genera un manifesto senza elementi di dipendenza. L'opzione <strong>-nodependency</strong> richiede l'opzione <strong>-managedassemblyname</strong> . Se ad esempio managed.dll è un assembly gestito, la riga di comando seguente genera il file out. manifest da managed.dll senza informazioni sulle dipendenze.<br/> <strong>mt.exe -managedassemblyname:managed.dll-out: out. manifest-nodependency</strong><br/></td>
</tr>
<tr class="odd">
<td>-Categoria</td>
<td>Specifica un'operazione che genera un manifesto con tag di categoria. L'opzione <strong>-Category</strong> richiede l'opzione <strong>-managedassemblyname</strong> . Se ad esempio managed.dll è un assembly gestito, la riga di comando seguente genera il file out. manifest da managed.dll con i tag category.<br/> <strong>mt.exe -managedassemblyname:managed.dll-out: out. manifest-Category</strong><br/></td>
</tr>
<tr class="even">
<td>-nologo</td>
<td>Specifica un'operazione che viene eseguita senza visualizzare i dati di copyright Microsoft standard. Se <strong>mt.exe</strong> viene eseguito come parte di un processo di compilazione, questa opzione può essere utilizzata per evitare la scrittura di informazioni indesiderate nei file di log. <br/></td>
</tr>
<tr class="odd">
<td>-out</td>
<td>Specifica il nome del manifesto aggiornato. Se si tratta di un'operazione a manifesto singolo e l'opzione <strong>-out</strong> viene omessa, il manifesto originale viene modificato. <br/></td>
</tr>
<tr class="even">
<td>-inputresource</td>
<td>Specifica un'operazione eseguita su un manifesto ottenuto da una risorsa di tipo RT_MANIFEST. Se si usa l'opzione <strong>-inputresource</strong> senza specificare l'identificatore di risorsa, <em> <resource_id> </em> , l'operazione usa il valore CREATEPROCESS_MANIFEST_RESOURCE. <br/> Ad esempio, il comando seguente richiede un'operazione che unisce un manifesto da una DLL, dll_with_manifest.dll e un file manifesto, man2. manifest. I manifesti Uniti vengono ricevuti da un manifesto nel file di risorse di un'altra DLL, dll_with_merged_manifests. <br/> <strong>mt.exe -inputresource:dll_with_manifest.dll; #1-manifest man2. manifest -outputresource:dll_with_merged_manifest.dll; #3</strong><br/> Per estrarre il manifesto da una DLL, specificare il nome del file DLL. Ad esempio, il comando seguente estrae il manifesto da lib1.dll e Man3. manifest riceve il manifesto Estratto.<br/> <strong>mt.exe -inputresource:lib.dll; #1 out: man3. manifest</strong><br/></td>
</tr>
<tr class="odd">
<td>-outputresource</td>
<td>Specifica un'operazione che genera un manifesto che deve essere ricevuto da una risorsa di tipo RT_MANIFEST. Se si usa l'opzione <strong>-outputresource</strong> senza specificare l'identificatore di risorsa, <em> <resource_id> </em> , l'operazione usa il valore CREATEPROCESS_MANIFEST_RESOURCE. <br/></td>
</tr>
<tr class="even">
<td>-UpdateResource</td>
<td>Specifica un'operazione equivalente all'uso delle opzioni <strong>-inputresource</strong> e <strong>-outputresource</strong> con argomenti identici. Ad esempio, il comando seguente richiede un'operazione che calcola un hash dei file nel percorso specificato e aggiorna il manifesto di una risorsa di un eseguibile portabile (PE).<br/> <strong>mt.exe -updateresource:dll_with_manifest.dll; #1-hashupdate: f: \FILES</strong>.<br/></td>
</tr>
<tr class="odd">
<td>-hashupdate</td>
<td>Calcola il valore hash dei file nei percorsi specificati e aggiorna il valore dell'attributo <strong>hash</strong> dell'elemento <strong>file</strong> con questo valore. <br/> Ad esempio, il comando seguente richiede un'operazione che unisce due file manifesto, man1. manifest e man2. manifest, e aggiorna il valore dell'attributo <strong>hash</strong> dell'elemento <strong>file</strong> nel manifesto che riceve le informazioni unite, Merged. manifest.<br/> <strong>mt.exe-manifest man1. manifest man2. manifest-hashupdate: d: \filerepository-out: merged. manifest</strong><br/> Se non si specificano i percorsi dei file, l'operazione cerca il percorso del manifesto specificato per la ricezione dell'aggiornamento. Ad esempio, il comando seguente richiede un'operazione che calcola il valore hash aggiornato usando i file trovati cercando il percorso del file aggiornato. manifest.<br/> <strong>mt.exe-manifest yourComponent. manifest-hashupdate-out: aggiornato. manifest</strong><br/></td>
</tr>
<tr class="even">
<td>-validate_manifest</td>
<td>Specifica un'operazione che esegue un controllo della sintassi della conformità del manifesto con lo schema del manifesto. Ad esempio, il comando seguente richiede un controllo per convalidare la conformità di man1. manifest con il relativo schema. <br/> <strong>mt.exe-manifest man1. manifest-validate_manifest</strong><br/></td>
</tr>
<tr class="odd">
<td>-validate_file_hashes</td>
<td>Specifica un'operazione che convalida i valori hash degli elementi <strong>file</strong> del manifesto. Ad esempio, il comando seguente richiede un'operazione che convalida i valori hash di tutti gli elementi <strong>file</strong> di man1. manifest.<br/> <strong>mt.exe-manifest man1. manifest-validate_file_hashes: &quot; c; \Files&quot;</strong><br/></td>
</tr>
<tr class="even">
<td>-Canonicalize</td>
<td>Specifica un'operazione di aggiornamento del manifesto al formato canonico. Il comando seguente, ad esempio, aggiorna man1. manifest a formato canonico.<br/> <strong>mt.exe-manifest man1. manifest</strong><br/></td>
</tr>
<tr class="odd">
<td>-check_for_duplicates</td>
<td>Specifica un'operazione che controlla il manifesto per gli elementi duplicati. Ad esempio, il comando seguente controlla man1. manifest per gli elementi duplicati.<br/> <strong>mt.exe-man1. manifest-check_for_duplicates</strong><br/></td>
</tr>
<tr class="even">
<td>-makecdfs</td>
<td>Genera file con estensione CDF per creare cataloghi. Ad esempio, per il comando seguente viene richiesta un'operazione che aggiorna il valore hash e genera un file con estensione CDF.<br/> <strong>mt.exe-manifest Comp1. manifest-hashupdate-makecdfs-out: updated. manifest</strong><br/></td>
</tr>
<tr class="odd">
<td>-verbose</td>
<td>Visualizza informazioni dettagliate sul debug.</td>
</tr>
<tr class="even">
<td>-?</td>
<td>Quando viene eseguito con-?, o senza opzioni e argomenti, Mt.exe Visualizza il testo della guida.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Strumenti di sviluppo di assembly affiancati](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

