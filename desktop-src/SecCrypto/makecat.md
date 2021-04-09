---
description: Strumento CryptoAPI che consente di creare un file di catalogo.
ms.assetid: 233b3644-f2a5-4166-bac0-30bf2f54e957
title: MakeCat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e6c2c3cb1d7df5a9f717143465d48d4c066466d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879486"
---
# <a name="makecat"></a>MakeCat

Lo strumento MakeCat è uno strumento CryptoAPI che consente di creare un file di catalogo. MakeCat è disponibile come parte di Microsoft Windows Software Development Kit (SDK) per Windows 7 e .NET Framework 4,0 ed è installato, per impostazione predefinita, nella \\ cartella bin del percorso di installazione di SDK.

Lo strumento MakeCat usa la sintassi del comando seguente:

**MakeCat** \[ **-n** \| **-r** \| **-v** \] *Nome file*

## <a name="parameters"></a>Parametri



| Parametro             | Descrizione                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **-n**<br/>     | Non arrestare in caso di errore reversibile.<br/>                                                                                                                           |
| **-r**<br/>     | Impone la chiusura di MakeCat se rileva errori reversibili. In particolare, termina quando si elaborano le voci nella sezione dei file di catalogo di un file con estensione CDF.<br/> |
| **-v**<br/>     | Dettagliato. Visualizza tutti i messaggi di stato e di errore.<br/>                                                                                                            |
| *FileName*<br/> | Nome del file con estensione CDF da analizzare. Per la struttura e il contenuto richiesti, vedere la sezione Osservazioni.<br/>                                                                         |



 

## <a name="remarks"></a>Commenti

Il file con estensione CDF deve essere compilato con le specifiche seguenti.

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
> L'ultima voce nel file con estensione CDF deve avere sempre un carattere di nuova riga esplicito alla fine della riga.

 

La \[ \] sezione CatalogHeader definisce le informazioni sull'intero file di catalogo.



| Opzione                    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nome<br/>           | Nome del file di catalogo, inclusa la relativa estensione.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| ResultDir<br/>      | Directory in cui verrà inserito il file con estensione cat creato. Se non è indicato, viene utilizzata la directory corrente predefinita. Se la directory non esiste, viene creata.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| PublicVersion<br/>  | Questa opzione non è supportata. <br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Versione del catalogo. Se viene lasciato vuoto, viene usato il valore predefinito 1.<br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| CatalogVersion<br/> | Versione del catalogo. Se la versione non è presente o è impostata su 1, "0x100" viene passato al parametro *dwPublicVersion* della funzione [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) e viene creato un file di catalogo della versione 1. L'opzione HashAlgorithms deve essere vuota o contenere SHA1.<br/> Se la versione è impostata su 2, "0x200" viene passato al parametro *dwPublicVersion* della funzione [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) e viene creato un file di catalogo della versione 2. L'opzione HashAlgorithms deve contenere SHA256.<br/> Se questa opzione è presente ma contiene un valore diverso da 1 o 2, lo strumento MakeCat verrà visualizzato in errore.<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questa opzione non è supportata.<br/> <br/> |
| HashAlgorithms<br/> | Nome dell'algoritmo hash utilizzato. Per ulteriori informazioni, vedere l'opzione CatalogVersion.<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questa opzione non è supportata.<br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| PageHashes<br/>     | Specifica se eseguire l'hashing dei file elencati nell' <HASH> opzione nella \[ sezione CatalogFiles \]<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questa opzione non è supportata.<br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| EncodingType<br/>   | Tipo di codifica del messaggio utilizzata. Se viene lasciato vuoto, il valore predefinito di EncodingType è PKCS \_ 7 \_ ASN \_ Encoding \| X509 \_ ASN \_ Encoding, 0x00010001. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

La \[ \] sezione CatalogFiles definisce ogni membro del file di catalogo con file di diversi tipi e attributi di diversi tipi in gruppi distinti.



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
<td>Tag di riferimento<br/></td>
<td>Riferimento di testo al file. Può includere qualsiasi carattere di testo ASCII eccetto il segno di uguale (=). Il sistema deve essere in grado di riprodurre questo tag dopo l'installazione. <br/> Utilizzare <HASH> come prefisso del nome file. In questo modo il tag è l'hash del file nel formato stringa ASCII. <br/></td>
</tr>
<tr class="even">
<td>nome e percorso del file<br/></td>
<td>Nome del file, inclusa l'estensione da analizzare e il percorso relativo del file. Tutti i tipi di file che possono essere firmati con SignTool possono essere aggiunti a un catalogo. Ad esempio, i nomi di file con le seguenti estensioni, tra gli altri, possono essere aggiunti a un catalogo:. exe,. cab,. cat,. ocx,. dll e. STL.<br/></td>
</tr>
<tr class="odd">
<td>ALTSIPID<br/></td>
<td>GUID SIP da usare per l'hashing anziché il SIP standard in base al tipo di file. Questa voce è facoltativa. Se questa voce viene omessa, verrà eseguito l'hashing del membro utilizzando il SIP predefinito. Se non viene trovato alcun SIP installato predefinito, verrà usato il SIP flat.<br/></td>
</tr>
<tr class="even">
<td>guid<br/></td>
<td>Rappresentazione testuale di un GUID.<br/></td>
</tr>
<tr class="odd">
<td>ATTRx<br/></td>
<td>facoltativo. Attributo o istruzione relativa al file o al contenuto. Può essere presente un numero qualsiasi di attributi, incluso None.<br/></td>
</tr>
<tr class="even">
<td>tipo<br/></td>
<td>Definisce il tipo di attributo da aggiungere nel formato 0x00000000 (testo). Questa opzione può essere una combinazione OR bit per bit di<strong>zero o più</strong> dei valori seguenti:<br/>
<ul>
<li>attributo autenticato 0x10000000 (firmato, incluso nell'hash).</li>
<li>0x20000000 attributo non autenticato (senza segno, non incluso nell'hash, non verificabile).</li>
<li>l'attributo 0x01000000 non verrà replicato in voci SHA1 in un catalogo CatalogVersion 2.</li>
<li>l'attributo 0x00010000 è rappresentato in testo non crittografato. Non verrà eseguita alcuna conversione.</li>
<li>l'attributo 0x00020000 è rappresentato nella codifica base-64. Viene utilizzato per rappresentare i dati binari.</li>
<li>l'attributo 0x00000001 è una coppia nome-valore. Usare l'opzione OID per il nome. Questo attributo è lento; Pertanto, utilizzare questa opzione con moderazione.</li>
<li>all'attributo 0x00000002 viene fatto riferimento da un <a href="/windows/desktop/SecGloss/o-gly"><em>identificatore di oggetto</em></a> (OID).</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td>oid<br/></td>
<td>Rappresentazione testuale della chiave di riferimento dell'attributo. Si tratta di un OID sotto forma di una stringa di testo in notazione Quad punteggiata (ad esempio, a. b. c. d) o di un nome di testo.<br/></td>
</tr>
<tr class="even">
<td>Valore<br/></td>
<td>Rappresentazione testuale del valore dell'attributo. Il tipo di rappresentazione testuale utilizzato dipende dal valore dell'opzione Type. I caratteri EOL determinano la lunghezza.<br/></td>
</tr>
<tr class="odd">
<td><HASH><br/></td>
<td>Hashing del file specificato.<br/></td>
</tr>
</tbody>
</table>



 

Il file di catalogo generato è senza segno. Se deve essere firmato prima della trasmissione, viene firmato usando [SignTool](signtool.md).

 

 
