---
description: Il Mt.exe file è uno strumento che genera cataloghi e file firmati. È disponibile in Microsoft Windows Software Development Kit (SDK). Mt.exe necessario che il file a cui si fa riferimento nel manifesto sia presente nella stessa directory del manifesto.
ms.assetid: 37f010ee-2658-4547-9871-c913201042de
title: Mt.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb81f3e0b7bf6b67236f1bd6037d1eceb11e0b89
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623907"
---
# <a name="mtexe"></a>Mt.exe

Il Mt.exe file è uno strumento che genera cataloghi e file firmati. È disponibile in Microsoft Windows Software Development Kit (SDK). Mt.exe necessario che il file a cui si fa riferimento nel manifesto sia presente nella stessa directory del manifesto.

Mt.exe genera hash usando l'implementazione CryptoAPI di Secure Hash Algorithm (SHA-1). Per altre informazioni sugli algoritmi hash, vedere [Algoritmi hash e di firma](/windows/desktop/SecCrypto/hash-and-signature-algorithms). Gli hash vengono inseriti come stringa esadecimale nei **tag del file** nel manifesto. Attualmente lo strumento genera solo hash SHA-1, anche se i file nei manifesti possono usare altri schemi hash.

Mt.exe usa Makecat.exe per generare file di catalogo (con estensione cat) dai file di definizione del catalogo (con estensione cdf). Questo strumento compila un modello standard CDF con il nome e il percorso del manifesto. È possibile usarlo con Makecat.exe per generare il catalogo di assembly.

La versione di Mt.exe disponibile nelle versioni recenti di Windows SDK può essere usata anche per generare manifesti per assembly gestiti e assembly side-by-side non gestiti.

## <a name="syntax"></a>Sintassi

**mt.exe \[ -manifest** _<component1.manifest><component2.manifest>_ *_\] \[ -identity:_* *<identity string> * **\] \[ -rgs:**<_file1.rgs>_* _\] \[ -tlb:_<*_file2.tlb>_* _\] \[ -dll:_ *_<file3.dll>_* _\] \[ -replacements:_ *_<XML filename>_* _\] \[ -managedassemblyname:_ *_<managed assembly>_* _\] \[ -nodependency \] \[ -category \] \[ -out:_ *_<output manifest name>_* _\] \[ -inputresource:_ *_<file4>_* _; \[ \# \]_ *_\_><0'ID risorsa><1_* _\] \[ -outputresource:_ *_<file5>_* _; \[ \# \]_ *_\_><2'ID risorsa><3_* _\] \[ -updateresource:_ *_<file6>_* _; \[ \# \]_ *_><4 \_ id_* risorsa><5 _\] \[ -hashupdate \[ :_ *_<path to files>_* _\] \] \[ -makecdfs \] \[ -validate \_ manifest \] \[ -validate \_ file \_ hashes:_ *_<path to files>_* _\] \[ -canonicalize \] \[ -check \_ for \_ duplicates \] \[ -nologo \] \[ -verbose \]_*

## <a name="command-line-options"></a>Opzioni da riga di comando

Mt.exe usa le opzioni della riga di comando senza distinzione tra maiuscole e minuscole seguenti.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Opzione</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>-manifest</td>
<td>Specifica il nome del file manifesto. Per modificare un singolo manifesto, specificare un nome di file manifesto. Ad esempio, component.manifest.<br/> Per unire più manifesti, specificare qui i nomi dei manifesti di origine. Specificare il nome del manifesto aggiornato con le opzioni <strong>-out</strong>, <strong>-outputresource</strong>o <strong>-updateresource.</strong> Ad esempio, la riga di comando seguente richiede un'operazione che unisce due manifesti, man1.manifest e man2.manifest, in un nuovo manifesto, man3.manifest.<br/> <strong>mt.exe -manifest man1.manifest man2.manifest -out:man3.manifest</strong><br/>
<blockquote>
[!Note]<br />
Nessun due punti (:) è obbligatorio con <strong>l'opzione -manifest.</strong>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td>-identity</td>
<td>Fornisce i valori degli attributi <strong>dell'elemento assemblyIdentity</strong> del manifesto. L'argomento <strong>dell'opzione -identity</strong> è un valore stringa contenente i valori dell'attributo nei campi separati da virgole. Specificare il valore <strong>dell'attributo name</strong> nel primo campo, senza includere una &quot; &quot; sottostringa name=. Tutti i campi rimanenti specificano gli attributi e i relativi valori nel formato: <em> <attribute name> </em> = <em> <attribute_value> </em> .<br/> Ad esempio, per aggiornare <strong>l'elemento assemblyIdentity</strong> del manifesto con le informazioni seguenti:<br/> <assemblyIdentity type=&quot;win32&quot; name=&quot;Microsoft.Windows.SampleAssembly&quot; version=&quot;6.0.0.0&quot; processorArchitecture=&quot;x86&quot; publicKeyToken=&quot;a5aaf5ba15723d5&quot;/> <br/> includere <strong>l'opzione -identity</strong> seguente nella riga di comando:<br/> <strong>-identity:</strong> &quot; Microsoft. Windows. SampleAssembly, processorArchitecture=x86, version=6.0.0.0, type=win32, publicKeyToken=a5aaf5ba15723d5&quot;<br/></td>
</tr>
<tr class="odd">
<td>-rgs</td>
<td>Specifica il nome del file di script di registrazione (con estensione rgs). <strong>L'opzione -dll</strong> è necessaria per usare l'opzione <strong>-rgs.</strong><br/></td>
</tr>
<tr class="even">
<td>-tlb</td>
<td>Specifica il nome del file di libreria dei tipi (TLB). <strong>L'opzione -dll</strong> è necessaria per usare l'opzione <strong>-tlb.</strong><br/></td>
</tr>
<tr class="odd">
<td>-dll</td>
<td>Specifica il nome del file della libreria a collegamento dinamico (DLL). <strong>L'opzione -dll</strong> è necessaria <strong>mt.exe</strong> se vengono usate le opzioni <strong>-rgs</strong> o <strong>-tlb.</strong> Specificare il nome della DLL che si intende compilare dai file con estensione rgs o tlb.<br/> Ad esempio, il comando seguente richiede un'operazione che genera un manifesto da file con estensione rgs e tlb.<br/> <strong>mt.exe -rgs:testreg1.rgs -tlb:testlib1.tlb -dll:test.dll -replacements:rep.manifest -identity: &quot; Microsoft.Windows. SampleAssembly, processorArchitecture=x86, version=6.0.0.0, type=win32, publicKeyToken=a5aaf5ba15723d5 &quot; -out:rgstlb.manifest</strong><br/></td>
</tr>
<tr class="even">
<td>-replacements</td>
<td>Specifica il file che contiene i valori per la stringa sostituibile nel file con estensione rgs.<br/></td>
</tr>
<tr class="odd">
<td>-managedassemblyname</td>
<td>Genera un manifesto dall'assembly gestito specificato. Usare con <strong>l'opzione -nodependency</strong> per generare un manifesto senza elementi di dipendenza. Usare con <strong>l'opzione -category</strong> per generare un manifesto con tag di categoria. Ad esempio, se managed.dll è un assembly gestito, la riga di comando seguente genera out.manifest da managed.dll.<br/> <strong>mt.exe -managedassemblyname:managed.dll -out:out.manifest</strong> <br/></td>
</tr>
<tr class="even">
<td>-nodependency</td>
<td>Specifica un'operazione che genera un manifesto senza elementi di dipendenza. <strong>L'opzione -nodependency</strong> richiede l'opzione <strong>-managedassemblyname.</strong> Ad esempio, se managed.dll è un assembly gestito, la riga di comando seguente genera out.manifest dal managed.dll senza informazioni sulle dipendenze.<br/> <strong>mt.exe -managedassemblyname:managed.dll -out:out.manifest -nodependency</strong><br/></td>
</tr>
<tr class="odd">
<td>-category</td>
<td>Specifica un'operazione che genera un manifesto con tag di categoria. <strong>L'opzione -category</strong> richiede l'opzione <strong>-managedassemblyname.</strong> Ad esempio, se managed.dll è un assembly gestito, la riga di comando seguente genera out.manifest managed.dll con tag di categoria.<br/> <strong>mt.exe -managedassemblyname:managed.dll -out:out.manifest -category</strong><br/></td>
</tr>
<tr class="even">
<td>-nologo</td>
<td>Specifica un'operazione eseguita senza visualizzare i dati standard sul copyright Microsoft. Se <strong>mt.exe</strong> come parte di un processo di compilazione, questa opzione può essere usata per impedire la scrittura di informazioni indesiderate nei file di log. <br/></td>
</tr>
<tr class="odd">
<td>-out</td>
<td>Specifica il nome del manifesto aggiornato. Se si tratta di un'operazione a manifesto singolo e l'opzione <strong>-out</strong> viene omessa, il manifesto originale viene modificato. <br/></td>
</tr>
<tr class="even">
<td>-inputresource</td>
<td>Specifica un'operazione eseguita su un manifesto ottenuto da una risorsa di tipo RT_MANIFEST. Se si <strong>usa l'opzione -inputresource</strong> senza specificare l'identificatore di <em> <resource_id> </em> risorsa, , l'operazione usa il valore CREATEPROCESS_MANIFEST_RESOURCE. <br/> Ad esempio, il comando seguente richiede un'operazione che unisce un manifesto da una DLL, dll_with_manifest.dll e un file manifesto, man2.manifest. I manifesti uniti vengono ricevuti da un manifesto nel file di risorse di un'altra DLL, dll_with_merged_manifests. <br/> <strong>mt.exe -inputresource:dll_with_manifest.dll;#1 -manifest man2.manifest -outputresource:dll_with_merged_manifest.dll;#3</strong><br/> Per estrarre il manifesto da una DLL, specificare il nome del file DLL. Ad esempio, il comando seguente estrae il manifesto lib1.dll e man3.manifest riceve il manifesto estratto.<br/> <strong>mt.exe -inputresource:lib.dll;#1 -out:man3.manifest</strong><br/></td>
</tr>
<tr class="odd">
<td>-outputresource</td>
<td>Specifica un'operazione che genera un manifesto che deve essere ricevuto da una risorsa di tipo RT_MANIFEST. Se si <strong>usa l'opzione -outputresource</strong> senza specificare l'identificatore di <em> <resource_id> </em> risorsa, , l'operazione usa il valore CREATEPROCESS_MANIFEST_RESOURCE. <br/></td>
</tr>
<tr class="even">
<td>-updateresource</td>
<td>Specifica un'operazione equivalente all'uso delle opzioni <strong>-inputresource</strong> e <strong>-outputresource</strong> con argomenti identici. Ad esempio, il comando seguente richiede un'operazione che calcola un hash dei file nel percorso specificato e aggiorna il manifesto di una risorsa di un eseguibile portabile (PE).<br/> <strong>mt.exe -updateresource:dll_with_manifest.dll;#1 -hashupdate:f:\files</strong>.<br/></td>
</tr>
<tr class="odd">
<td>-hashupdate</td>
<td>Calcola il valore hash dei file nei percorsi specificati e aggiorna il valore dell'attributo <strong>hash</strong> dell'elemento <strong>File</strong> con questo valore. <br/> Ad esempio, il comando seguente richiede un'operazione che unisce due file manifesto, man1.manifest e man2.manifest, e aggiorna il valore dell'attributo <strong>hash</strong> dell'elemento <strong>File</strong> nel manifesto che riceve le informazioni unite, merged.manifest.<br/> <strong>mt.exe -manifest man1.manifest man2.manifest -hashupdate:d:\filerepository -out:merged.manifest</strong><br/> Se i percorsi dei file non vengono specificati, l'operazione cerca il percorso del manifesto specificato per ricevere l'aggiornamento. Ad esempio, il comando seguente richiede un'operazione che calcola il valore hash aggiornato usando i file trovati cercando il percorso di updated.manifest.<br/> <strong>mt.exe -manifest yourComponent.manifest -hashupdate -out:updated.manifest</strong><br/></td>
</tr>
<tr class="even">
<td>-validate_manifest</td>
<td>Specifica un'operazione che esegue un controllo della sintassi della conformità del manifesto con lo schema del manifesto. Ad esempio, il comando seguente richiede un controllo per convalidare la conformità di man1.manifest con il relativo schema. <br/> <strong>mt.exe -manifest man1.manifest -validate_manifest</strong><br/></td>
</tr>
<tr class="odd">
<td>-validate_file_hashes</td>
<td>Specifica un'operazione che convalida i valori hash degli <strong>elementi File</strong> del manifesto. Ad esempio, il comando seguente richiede un'operazione che convalida i valori hash di tutti gli <strong>elementi File</strong> di man1.manifest.<br/> <strong>mt.exe -manifest man1.manifest -validate_file_hashes: &quot; c;\files&quot;</strong><br/></td>
</tr>
<tr class="even">
<td>-canonicalize</td>
<td>Specifica un'operazione per aggiornare il manifesto in formato canonico. Ad esempio, il comando seguente aggiorna man1.manifest in formato canonico.<br/> <strong>mt.exe -manifest man1.manifest</strong><br/></td>
</tr>
<tr class="odd">
<td>-check_for_duplicates</td>
<td>Specifica un'operazione che verifica la presenza di elementi duplicati nel manifesto. Ad esempio, il comando seguente verifica la presenza di elementi duplicati in man1.manifest.<br/> <strong>mt.exe -man1.manifest -check_for_duplicates</strong><br/></td>
</tr>
<tr class="even">
<td>-makecdfs</td>
<td>Genera file con estensione cdf per creare cataloghi. Ad esempio, per il comando seguente richiede un'operazione che aggiorna il valore hash e genera un file con estensione cdf.<br/> <strong>mt.exe -manifest comp1.manifest -hashupdate -makecdfs -out:updated.manifest</strong><br/></td>
</tr>
<tr class="odd">
<td>-verbose</td>
<td>Visualizza informazioni di debug dettagliate.</td>
</tr>
<tr class="even">
<td>-?</td>
<td>Quando viene eseguito con -?, o senza opzioni e argomenti, Mt.exe visualizza il testo della Guida.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Strumenti di sviluppo di assembly side-by-side](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

