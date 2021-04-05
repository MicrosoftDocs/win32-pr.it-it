---
description: 'Altre informazioni su: JET_COLTYP'
title: JET_COLTYP
TOCTitle: JET_COLTYP
ms:assetid: 2c30c025-629d-4b94-bcb9-9c8fc3d4e039
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269213(v=EXCHG.10)
ms:contentKeyID: 32765516
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 04588d6a057c25c0d39e42997a67a611fdfd92d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884709"
---
# <a name="jet_coltyp"></a>JET_COLTYP


_**Si applica a:** Windows | Windows Server_

## <a name="jet_coltyp"></a>JET_COLTYP

Il gruppo **JET_COLTYP** di costanti descrive tutti i possibili tipi di colonna che è possibile trovare in una tabella.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Costante/valore</p></th>
<th><p>Descrizione</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_coltypNil<br />
0</p></td>
<td><p>Tipo di colonna non valido.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypBit<br />
1</p></td>
<td><p>Tipo di colonna che consente tre valori: <strong>true</strong>, <strong>false</strong>o <strong>null</strong>. Questo tipo di colonna ha una lunghezza di un byte e è di dimensioni fisse. <strong>False</strong> Ordina prima di <strong>true</strong>. Si noti che la dimensione di questo tipo non corrisponde alla dimensione del tipo Boolean Variant.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypUnsignedByte<br />
2</p></td>
<td><p>Unsigned Integer a 1 byte che può assumere valori compresi tra 0 (zero) e 255.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypShort<br />
3</p></td>
<td><p>Intero con segno a 2 byte che può assumere valori compresi tra-32768 e 32767. I valori negativi vengono ordinati prima dei valori positivi.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypLong<br />
4</p></td>
<td><p>Intero con segno a 4 byte che può assumere valori compresi tra-2147483648 e 2147483647. I valori negativi vengono ordinati prima dei valori positivi.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypCurrency<br />
5</p></td>
<td><p>Intero con segno a 8 byte che può assumere valori compresi tra-9.223.372.036.854.775.808 e 9223372036854775807. I valori negativi vengono ordinati prima dei valori positivi. Questo tipo di colonna è identico al tipo di valuta Variant. Questo tipo di colonna può essere utilizzato anche come intero con segno a 8 byte nativo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypIEEESingle<br />
6</p></td>
<td><p>Numero a virgola mobile A precisione singola (4 byte).</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypIEEEDouble<br />
7</p></td>
<td><p>Numero a virgola mobile a precisione doppia (8 byte).</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypDateTime<br />
8</p></td>
<td><p>Numero a virgola mobile a precisione doppia (8 byte) che rappresenta una data in giorni frazionari dall'anno 1900. Questo tipo di colonna è identico al tipo di data Variant.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypBinary<br />
9</p></td>
<td><p>Una colonna binaria non elaborata a lunghezza fissa o variabile che può avere una lunghezza fino a 255 byte.</p>
<p>Questo tipo di colonna può essere utilizzato per implementare un GUID se configurato come colonna binaria a 16 byte a lunghezza fissa. L'unica avvertenza è che l'ordinamento relativo dei valori in un indice su tale colonna non corrisponderà all'ordinamento relativo del rendering della stringa del registro di sistema standard di un GUID (ovvero &quot; {0d6cec99-3f3f-4dc7-a5e6-f87aefeb908b} &quot; ).</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypText<br />
10</p></td>
<td><p>Una colonna di testo a lunghezza fissa o variabile che può avere una lunghezza fino a 255 caratteri ASCII o 127 caratteri Unicode.</p>
<p>Tutte le stringhe vengono archiviate come numero conteggiato di caratteri. Non è necessario terminare con null le stringhe. Non è inoltre necessario che il conteggio includa un carattere di terminazione null. Infine, è possibile archiviare i caratteri null incorporati.</p>
<p>Le stringhe ASCII vengono sempre considerate senza distinzione tra maiuscole e minuscole per scopi di ordinamento e ricerca. Inoltre, per l'ordinamento e la ricerca vengono considerati solo i caratteri che precedono il primo carattere null (se presente).</p>
<p>Le stringhe Unicode utilizzano l'API Win32 <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a> per creare chiavi di ordinamento che vengono successivamente utilizzate per l'ordinamento e la ricerca di tali dati. Per impostazione predefinita, le stringhe Unicode sono considerate nelle impostazioni locali per l'inglese (Stati Uniti) e vengono ordinate e cercate usando i flag di normalizzazione seguenti: NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH. In Windows 2000 è possibile personalizzare questi flag per ogni indice in modo da includere anche NORM_IGNORENONSPACE. In Windows XP e versioni successive, è possibile richiedere qualsiasi combinazione dei seguenti flag di normalizzazione per indice: LCMAP_SORTKEY, LCMAP_BYTEREV, NORM_IGNORECASE, NORM_IGNORENONSPACE, NORM_IGNORESYMBOLS, NORM_IGNOREKANATYPE, NORM_IGNOREWIDTH e SORT_STRINGSORT.</p>
<p>In tutte le versioni, è possibile personalizzare le impostazioni locali per ogni indice. Le impostazioni locali possono essere usate purché nel computer sia installato il Language Pack appropriato. Infine, tutti i caratteri null rilevati in una stringa Unicode vengono completamente ignorati.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypLongBinary<br />
11</p></td>
<td><p>Una colonna binaria non elaborata a lunghezza fissa o variabile che può avere una lunghezza fino a 2147483647 byte. Questo tipo è considerato un valore Long. Un valore Long è speciale perché può essere di grandi dimensioni e perché può essere accessibile come flusso. Questo tipo è altrimenti identico a JET_coltypBinary.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypLongText<br />
12</p></td>
<td><p>Lunghezza fissa o variabile, colonna di testo che può contenere fino a 2147483647 caratteri ASCII di lunghezza o 1073741823 caratteri Unicode di lunghezza. Questo tipo è considerato un valore Long. Un valore Long è speciale perché può essere di grandi dimensioni e perché può essere accessibile come flusso. Questo tipo è altrimenti identico a JET_coltypText.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypSLV<br />
13</p></td>
<td><p>Questo tipo di colonna è obsoleto.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypUnsignedLong<br />
14</p></td>
<td><p>Unsigned Integer a 4 byte che può assumere valori compresi tra 0 (zero) e 4294967295.</p>
<p><strong>Windows Vista e Windows Server 2008:</strong>  Questo tipo di colonna è supportato in Windows Vista, Windows Server 2008 e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypLongLong<br />
15</p></td>
<td><p>Intero con segno a 8 byte che può assumere valori compresi tra-9.223.372.036.854.775.808 e 9223372036854775807. I valori negativi vengono ordinati prima dei valori positivi.</p>
<p><strong>Windows Vista e Windows Server 2008:</strong>  Questo tipo di colonna è supportato in Windows Vista, Windows Server 2008 e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypGUID<br />
16</p></td>
<td><p>Una colonna binaria A 16 byte A lunghezza fissa che rappresenta in modo nativo il tipo di dati GUID. I valori della colonna GUID vengono ordinati nello stesso modo in cui tali valori verrebbero ordinati come stringhe nel formato standard (ad esempio {4999b5c0-7657-42D9-BDC1-4b779784e013}).</p>
<p><strong>Windows Vista e Windows Server 2008:</strong>  Questo tipo di colonna è supportato in Windows Vista, Windows Server 2008 e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypUnsignedShort<br />
17</p></td>
<td><p>Unsigned Integer a 2 byte che può assumere valori compresi tra 0 e 65535.</p>
<p><strong>Windows Vista e Windows Server 2008:</strong>  Questo tipo di colonna è supportato in Windows Vista, Windows Server 2008 e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypMax<br />
18</p></td>
<td><p>Costante che descrive il tipo di colonna massimo, ovvero uno oltre il valore valido più grande, supportato dal motore.</p>
<p>Questo valore deve essere utilizzato con cautela perché verrà modificato quando sono supportati i nuovi tipi di colonna. Ad esempio, ha un valore letterale diverso in Windows 2000 rispetto a Windows XP e versioni successive.</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Intestazione</strong></p></td>
<td><p>Dichiarata in esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Vedere anche

[JetAddColumn](./jetaddcolumn-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)
