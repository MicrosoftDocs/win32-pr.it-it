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
ms.openlocfilehash: d4a7433b6e2882a90c9c6fdfe0180b5f5ab7a8e6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476877"
---
# <a name="jet_coltyp"></a>JET_COLTYP


_**Si applica a:** Windows | Windows Server_

## <a name="jet_coltyp"></a>JET_COLTYP

Il **JET_COLTYP** di costanti descrive tutti i possibili tipi di colonna disponibili in una tabella.


| <p>Costante/valore</p> | <p>Descrizione</p> | 
|-----------------------|--------------------|
| <p>JET_coltypNil<br />0</p> | <p>Tipo di colonna non valido.</p> | 
| <p>JET_coltypBit<br />1</p> | <p>Tipo di colonna che consente tre valori: <strong>True,</strong> <strong>False</strong>o <strong>NULL.</strong> Questo tipo di colonna ha una lunghezza di un byte e ha una dimensione fissa. <strong>False</strong> ordina prima di <strong>True.</strong> Si noti che le dimensioni di questo tipo non corrispondono alle dimensioni del tipo booleano variant.</p> | 
| <p>JET_coltypUnsignedByte<br />2</p> | <p>Intero senza segno a 1 byte che può assumere valori compresi tra 0 (zero) e 255.</p> | 
| <p>JET_coltypShort<br />3</p> | <p>Intero con segno a 2 byte che può assumere valori compresi tra -32768 e 32767. I valori negativi vengono ordinati prima dei valori positivi.</p> | 
| <p>JET_coltypLong<br />4</p> | <p>Intero con segno a 4 byte che può assumere valori compresi tra - 2147483648 e 2147483647. I valori negativi vengono ordinati prima dei valori positivi.</p> | 
| <p>JET_coltypCurrency<br />5</p> | <p>Intero con segno a 8 byte che può assumere valori compresi tra - 9223372036854775808 e 9223372036854775807. I valori negativi vengono ordinati prima dei valori positivi. Questo tipo di colonna è identico al tipo di valuta variante. Questo tipo di colonna può essere utilizzato anche come intero con segno a 8 byte nativo.</p> | 
| <p>JET_coltypIEEESingle<br />6</p> | <p>Numero a virgola mobile a precisione singola (4 byte).</p> | 
| <p>JET_coltypIEEEDouble<br />7</p> | <p>Numero a virgola mobile a precisione doppia (8 byte).</p> | 
| <p>JET_coltypDateTime<br />8</p> | <p>Numero a virgola mobile a precisione doppia (8 byte) che rappresenta una data in giorni frazionari a partire dall'anno 1900. Questo tipo di colonna è identico al tipo di data variant.</p> | 
| <p>JET_coltypBinary<br />9</p> | <p>Colonna binaria non elaborata a lunghezza fissa o variabile che può avere una lunghezza massima di 255 byte.</p><p>Questo tipo di colonna può essere usato per implementare un GUID se configurato come colonna binaria a lunghezza fissa a 16 byte. L'unica avvertenza è che l'ordinamento relativo dei valori in un indice su tale colonna non corrisponderà all'ordinamento relativo del rendering standard delle stringhe del Registro di sistema di un GUID (ovvero "{ 0d6cec99-3f3f-4dc7-a5e6-f87aefeb908b}").</p> | 
| <p>JET_coltypText<br />10</p> | <p>Colonna di testo a lunghezza fissa o variabile che può avere una lunghezza massima di 255 caratteri ASCII o 127 caratteri Unicode.</p><p>Tutte le stringhe vengono archiviate come numero conteggiato di caratteri. Le stringhe non devono avere terminazione Null. Inoltre, non è necessario che il conteggio includa un carattere di terminazione Null. Infine, è possibile archiviare i caratteri Null incorporati.</p><p>Le stringhe ASCII vengono sempre considerate come senza distinzione tra maiuscole e minuscole ai fini dell'ordinamento e della ricerca. Inoltre, solo i caratteri che precedono il primo carattere Null (se presente) vengono considerati per l'ordinamento e la ricerca.</p><p>Le stringhe Unicode usano l'API Win32 <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a> per creare chiavi di ordinamento che vengono successivamente usate per ordinare e cercare i dati. Per impostazione predefinita, le stringhe Unicode vengono considerate nelle impostazioni locali inglese (Stati Uniti) e vengono ordinate e ricercate usando i flag di normalizzazione seguenti: NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH. In Windows 2000 è possibile personalizzare questi flag per ogni indice in modo da includere NORM_IGNORENONSPACE. In Windows XP e versioni successive è possibile richiedere qualsiasi combinazione dei flag di normalizzazione seguenti per indice: LCMAP_SORTKEY, LCMAP_BYTEREV, NORM_IGNORECASE, NORM_IGNORENONSPACE, NORM_IGNORESYMBOLS, NORM_IGNOREKANATYPE, NORM_IGNOREWIDTH e SORT_STRINGSORT.</p><p>In tutte le versioni è possibile personalizzare le impostazioni locali per ogni indice. È possibile usare tutte le impostazioni locali purché nel computer siano language pack le impostazioni locali appropriate. Infine, tutti i caratteri Null rilevati in una stringa Unicode vengono completamente ignorati.</p> | 
| <p>JET_coltypLongBinary<br />11</p> | <p>Colonna binaria non elaborata a lunghezza fissa o variabile che può avere una lunghezza massima di 2147483647 byte. Questo tipo è considerato un valore long. Un valore long è speciale perché può essere di grandi dimensioni e perché è accessibile come flusso. Questo tipo è altrimenti identico a JET_coltypBinary.</p> | 
| <p>JET_coltypLongText<br />12</p> | <p>Colonna di testo a lunghezza fissa o variabile che può avere una lunghezza massima di 2147483647 caratteri ASCII o 1073741823 caratteri Unicode. Questo tipo è considerato un valore long. Un valore long è speciale perché può essere di grandi dimensioni e perché è accessibile come flusso. Questo tipo è altrimenti identico a JET_coltypText.</p> | 
| <p>JET_coltypSLV<br />13</p> | <p>Questo tipo di colonna è obsoleto.</p> | 
| <p>JET_coltypUnsignedLong<br />14</p> | <p>Intero senza segno a 4 byte che può assumere valori compresi tra 0 (zero) e 4294967295.</p><p><strong>Windows Vista e Windows Server 2008:</strong>  Questo tipo di colonna è supportato Windows Vista, Windows Server 2008 e versioni successive.</p> | 
| <p>JET_coltypLongLong<br />15</p> | <p>Intero con segno a 8 byte che può assumere valori compresi tra - 9223372036854775808 e 9223372036854775807. I valori negativi vengono ordinati prima dei valori positivi.</p><p><strong>Windows Vista e Windows Server 2008:</strong>  Questo tipo di colonna è supportato Windows Vista, Windows Server 2008 e versioni successive.</p> | 
| <p>JET_coltypGUID<br />16</p> | <p>Colonna binaria a 16 byte a lunghezza fissa che rappresenta in modo nativo il tipo di dati GUID. I valori delle colonne GUID vengono ordinati nello stesso modo in cui tali valori vengono ordinati come stringhe in formato standard ,ad esempio {4999b5c0-7657-42d9-bdc1-4b779784e013}.</p><p><strong>Windows Vista e Windows Server 2008:</strong>  Questo tipo di colonna è supportato Windows Vista, Windows Server 2008 e versioni successive.</p> | 
| <p>JET_coltypUnsignedShort<br />17</p> | <p>Intero senza segno a 2 byte che può assumere valori compresi tra 0 e 65535.</p><p><strong>Windows Vista e Windows Server 2008:</strong>  Questo tipo di colonna è supportato Windows Vista, Windows Server 2008 e versioni successive.</p> | 
| <p>JET_coltypMax<br />18</p> | <p>Costante che descrive il tipo di colonna massimo (ovvero uno oltre il più grande valido) supportato dal motore.</p><p>Questo valore deve essere usato con cautela perché cambierà quando sono supportati nuovi tipi di colonna. Ad esempio, ha un valore letterale diverso Windows 2000 rispetto a quello in Windows XP e versioni successive.</p> | 



### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JetAddColumn](./jetaddcolumn-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)
