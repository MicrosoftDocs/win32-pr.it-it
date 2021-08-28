---
description: Strumento CryptoAPI che crea un file di catalogo.
ms.assetid: 233b3644-f2a5-4166-bac0-30bf2f54e957
title: MakeCat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 980c58530c55006d28ecd7589b0313844e9dbe46
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886261"
---
# <a name="makecat"></a>MakeCat

Lo strumento MakeCat è uno strumento CryptoAPI che crea un file di catalogo. MakeCat è disponibile come parte di Microsoft Windows Software Development Kit (SDK) per Windows 7 e .NET Framework 4.0 e viene installato, per impostazione predefinita, nella cartella Bin del percorso di installazione \\ dell'SDK.

Lo strumento MakeCat usa la sintassi di comando seguente:

**MakeCat** \[ **-n** \| **-r** \| **-v** \] *FileName*

## <a name="parameters"></a>Parametri



| Parametro             | Descrizione                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **-n**<br/>     | Non arrestarsi in caso di errore reversibile.<br/>                                                                                                                           |
| **-r**<br/>     | Forza la terminazione di MakeCat se si verificano errori ripristinabili. In particolare, terminerà durante l'elaborazione delle voci nella sezione dei file di catalogo di un file con estensione cdf.<br/> |
| **-v**<br/>     | Dettagliato. Visualizza tutti i messaggi di stato e di errore.<br/>                                                                                                            |
| *FileName*<br/> | Nome del file con estensione cdf da analizzare. Per la struttura e il contenuto necessari, vedere la sezione Osservazioni.<br/>                                                                         |



 

## <a name="remarks"></a>Commenti

Il file con estensione cdf deve essere compilato con le specifiche seguenti.

``` syntax
[CatalogHeader]
Name=Name              
ResultDir=ResultDir   
PublicVersion=[|1]
CatalogVersion = [|1|2]
HashAlgorithms=[|SHA1|SHA256]
PageHashes=[true|false]
EncodingType=Encodingtype 
CATATTR1={type}:{oid}:{value} (optional)
CATATTR2={type}:{oid}:{value} (optional)

[CatalogFiles]
{reference tag}=file path and name
{reference tag}ALTSIPID={guid} (optional)
{reference tag}ATTR1={type}:{oid}:{value} (optional)
{reference tag}ATTR2={type}:{oid}:{value} (optional)
<HASH>kernel32.dll=kernel32.dll
<HASH>ntdll.dll=ntdll.dll
```

> [!Note]  
> L'ultima voce nel file con estensione cdf deve sempre contenere un carattere di nuova riga esplicito alla fine della riga.

 

La \[ sezione CatalogHeader \] definisce le informazioni sull'intero file di catalogo.



| Opzione                    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nome<br/>           | Nome del file di catalogo, inclusa l'estensione.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| ResultDir<br/>      | Directory in cui verrà inserito il file cat creato. Se non indicato, viene usata la directory corrente predefinita. Se la directory non esiste, viene creata.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Versione pubblica<br/>  | Questa opzione non è supportata. <br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Versione del catalogo. Se viene lasciato vuoto, viene usato il valore predefinito 1.<br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| CatalogVersion<br/> | Versione del catalogo. Se la versione non è presente o è impostata su 1, "0x100" viene passato al *parametro dwPublicVersion* della funzione [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) e viene creato un file di catalogo della versione 1. L'opzione HashAlgorithms deve essere vuota o contenere SHA1.<br/> Se la versione è impostata su 2, "0x200" viene passato al parametro *dwPublicVersion* della funzione [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) e viene creato un file di catalogo della versione 2. L'opzione HashAlgorithms deve contenere SHA256.<br/> Se questa opzione è presente ma contiene un valore diverso da 1 o 2, lo strumento MakeCat restituirà un errore.<br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Questa opzione non è supportata.<br/> <br/> |
| HashAlgorithms<br/> | Nome dell'algoritmo hash utilizzato. Per altre informazioni, vedere l'opzione CatalogVersion.<br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Questa opzione non è supportata.<br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| PageHashes<br/>     | Specifica se eseguire l'hashing dei file elencati &lt; nell'opzione HASH &gt; nella \[ sezione \] CatalogFiles<br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Questa opzione non è supportata.<br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| EncodingType<br/>   | Tipo di codifica dei messaggi utilizzata. Se lasciato vuoto, il valore predefinito di EncodingType è PKCS \_ 7 \_ ASN \_ ENCODING \| X509 \_ ASN \_ ENCODING, 0x00010001. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

La sezione CatalogFiles definisce ogni membro del file di catalogo con file di vari tipi e \[ attributi di vari tipi in gruppi \] separati.



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
<td>tag di riferimento<br/></td>
<td>Riferimento di testo al file. Può includere qualsiasi carattere di testo ASCII ad eccezione del segno di uguale (=). Il sistema deve essere in grado di riprodurre questo tag dopo l'installazione. <br/> Usare &lt; HASH come prefisso del nome del &gt; file. Il tag è quindi l'hash del file in formato stringa ASCII. <br/></td>
</tr>
<tr class="even">
<td>percorso e nome del file<br/></td>
<td>Nome del file, inclusa l'estensione da analizzare e il percorso relativo del file. Qualsiasi tipo di file che può essere firmato con SignTool può essere aggiunto a un catalogo. Ad esempio, i nomi di file con le estensioni seguenti, tra le altre, possono essere aggiunti a un catalogo: .exe, .cab, cat, ocx, .dll e stl.<br/></td>
</tr>
<tr class="odd">
<td>ALTSIPID<br/></td>
<td>GUID SIP da usare per l'hashing anziché il SIP standard in base al tipo di file. Questa voce è facoltativa. Se questa voce viene omessa, verrà eseguito l'hashing del membro usando il sip predefinito. Se non viene trovato alcun SIP installato predefinito, verrà usato flat SIP.<br/></td>
</tr>
<tr class="even">
<td>guid<br/></td>
<td>Rappresentazione testuale di un GUID.<br/></td>
</tr>
<tr class="odd">
<td>ATTRx<br/></td>
<td>facoltativo. Attributo o istruzione sul file o sul contenuto. Può essere presente un numero qualsiasi di attributi, incluso nessuno.<br/></td>
</tr>
<tr class="even">
<td>tipo<br/></td>
<td>Definisce il tipo di attributo aggiunto nel formato 0x00000000 (testo). Questa opzione può essere una combinazione<strong>OR</strong> bit per bit di zero o più dei valori seguenti:<br/>
<ul>
<li>0x10000000 attributo Authenticated (con segno, incluso nell'hash).</li>
<li>0x20000000 attributo Unauthenticated (senza segno, non incluso nell'hash, non verificabile).</li>
<li>0x01000000'attributo non verrà replicato nelle voci SHA1 in un catalogo CatalogVersion 2.</li>
<li>0x00010000 attributo è rappresentato in testo non crittografato. Non verrà eseguita alcuna conversione.</li>
<li>0x00020000 attributo è rappresentato nella codifica Base 64. Viene usato per rappresentare i dati binari.</li>
<li>0x00000001 attributo è una coppia nome-valore. Usare l'opzione oid per il nome. Questo attributo è lento. Pertanto, utilizzare questa opzione con modermente.</li>
<li>0x00000002'attributo viene fatto riferimento da <a href="/windows/desktop/SecGloss/o-gly"><em>un identificatore</em></a> di oggetto (OID).</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td>oid<br/></td>
<td>Rappresentazione testuale della chiave di riferimento dell'attributo. Si tratta di un OID nel formato di una stringa di testo in notazione a quattro punti (ad esempio, a.b.c.d) o di un nome di testo.<br/></td>
</tr>
<tr class="even">
<td>Valore<br/></td>
<td>Rappresentazione testuale del valore dell'attributo. Il tipo di rappresentazione di testo usato dipende dal valore dell'opzione type. I caratteri EOL determinano la lunghezza.<br/></td>
</tr>
<tr class="odd">
<td>&lt;HASH&gt;<br/></td>
<td>Esegue l'hashing del file specificato.<br/></td>
</tr>
</tbody>
</table>



 

Il file di catalogo generato non è firmato. Se deve essere firmato prima della trasmissione, viene firmato usando [SignTool](signtool.md).

 

 
