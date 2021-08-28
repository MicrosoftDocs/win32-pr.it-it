---
description: 'Altre informazioni su: Costanti Impostazioni massime'
title: Numero massimo Impostazioni costanti
TOCTitle: Maximum Settings Constants
ms:assetid: 1111051f-55af-4c33-be38-6a3973c2c815
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269189(v=EXCHG.10)
ms:contentKeyID: 32765492
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
ms.openlocfilehash: 38184176e5803cfd22d7b63f9d85e5b62f7ecff1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478967"
---
# <a name="maximum-settings-constants"></a>Numero massimo Impostazioni costanti


_**Si applica a:** Windows | Windows Server_

## <a name="maximum-settings-constants"></a>Numero massimo Impostazioni costanti

Queste costanti forniscono le impostazioni massime consentite per gli elementi in un database ESE.


| <p>Costante/valore</p> | <p>Descrizione</p> | 
|-----------------------|--------------------|
| <p>JET_BASE_NAME_LENGTH<br />3</p> | <p>Imposta la lunghezza del prefisso utilizzato per assegnare un nome ai file utilizzati dal motore di database. Questa lunghezza è applicabile al nome impostato per il parametro <a href="gg269235(v=exchg.10).md">JET_paramBaseName</a> di sistema.</p> | 
| <p>JET_MAX_COMPUTERNAME_LENGTH<br />15</p> | <p>Imposta la lunghezza massima per <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a>.</p> | 
| <p>JET_cbBookmarkMost<br />256</p> | <p>Dimensione massima predefinita di un segnalibro. Questo valore è valido quando la dimensione della chiave viene lasciata al valore predefinito.</p> | 
| <p>JET_cbBookmarkMostMost<br />2000</p> | <p>Dimensione massima di un segnalibro quando esent è configurato per avere le chiavi più grandi possibili.</p><p><strong>Windows 7:</strong> JET_cbBookmarkMostMost è stato introdotto in Windows 7.</p> | 
| <p>JET_cbNameMost<br />64</p> | <p>Lunghezza massima di un oggetto, una colonna, un indice o un nome di proprietà.</p><p><strong>Nota</strong>  Se Unicode, il valore è 128.</p> | 
| <p>JET_cbFullNameMost<br />255</p> | <p>Lunghezza massima di un oggetto "name.name.name..." Costruire.</p><p><strong>Nota</strong>  Se Unicode, il valore è 510.</p> | 
| <p>JET_cbColumnLVPageOverhead<br />82</p> | <p>Questo numero può essere usato per calcolare la quantità massima di UN BLOB che può essere archiviata dal motore di database in una singola pagina di database. La formula è max size = JET_paramDatabasePageSize-JET_cbColumnLVPageOverhead.</p><p>Questo valore è ora obsoleto. La dimensione del blocco di valore lungo deve essere recuperata con il JET_paramLVChunkSizeMost parametro .</p> | 
| <p>JET_cbColumnMost<br />255</p> | <p>Dimensione massima dei dati delle colonne con valori non lunghi.</p> | 
| <p>JET_cbLVDefaultValueMost<br />255</p> | <p>Dimensione massima del valore predefinito di una colonna long-value (LongBinary o LongText).</p> | 
| <p>JET_cbKeyMost<br />255</p> | <p>Dimensione massima predefinita di una chiave di ordinamento o di indice.</p> | 
| <p>JET_cbKeyMostMost<br />2000</p> | <p>Dimensione massima configurabile di una chiave di ordinamento o di indice per qualsiasi dimensione di pagina. (Vedere JET_INDEXCREATE2.cbKeyMost)</p><p><strong>Windows 7:</strong> JET_cbKeyMostMost è stato introdotto nel sistema operativo Windows 7.</p> | 
| <p>JET_cbKeyMost2KBytePage<br />500</p> | <p>Dimensione massima configurabile consentita per una chiave di indice in un database che utilizza pagine di 2048 byte. Vedere <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> per altre informazioni.</p><p><strong>Windows Vista:</strong> JET_cbKeyMost2KBytePage è stato introdotto nel sistema operativo Windows Vista.</p> | 
| <p>JET_cbKeyMost4KBytePage<br />1000</p> | <p>Dimensione massima configurabile consentita per una chiave di indice in un database che usa pagine di 4096 byte. Vedere <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> per altre informazioni.</p><p><strong>Windows Vista:</strong> JET_cbKeyMost4KBytePage è stato introdotto in Windows Vista.</p> | 
| <p>JET_cbKeyMost8KBytePage<br />2000</p> | <p>Dimensione massima configurabile consentita per una chiave di indice in un database che usa pagine di 8192 byte. Vedere <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> per altre informazioni.</p><p><strong>Windows Vista:</strong> JET_cbKeyMost8KBytePage è stato introdotto in Windows Vista</p> | 
| <p>JET_cbKeyMostMin<br />255</p> | <p>Dimensione massima minima consentita per una chiave di indice. Vedere <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> per altre informazioni.</p><p><strong>Windows Vista:</strong> JET_cbKeyMostMin è stato introdotto in Windows Vista.</p> | 
| <p>JET_cbLimitKeyMost<br />256</p> | <p>Dimensione massima della chiave quando la chiave viene formata usando un <em>grbit</em>limite, ad esempio JET_bitStrLimit, usato nella <a href="gg269329(v=exchg.10).md">funzione JetMakeKey.</a></p> | 
| <p>JET_cbPrimaryKeyMost<br />255</p> | <p>Dimensione massima dell'indice primario. Questo è ora obsoleto.</p> | 
| <p>JET_cbSecondaryKeyMost<br />255</p> | <p>Dimensione massima dell'indice secondario. Questo è ora obsoleto.</p> | 
| <p>JET_ccolKeyMost<br />12</p> | <p>Numero massimo di componenti in una chiave di ordinamento o di indice.</p><p><strong>Windows Vista:</strong> In Windows Vista e versioni successive di Windows il valore è 16.</p> | 
| <p>JET_ccolMost<br />0x0000fee0</p> | <p>Numero massimo di colonne consentite in una tabella.</p><p><strong>Windows XP:</strong> Il valore 0x0000fee0 viene usato in Windows XP e versioni successive e successive di Windows</p><p><strong>Windows 2000:</strong> Il valore 0x00007ffe viene usato in Windows 2000.</p> | 
| <p>JET_ccolFixedMost<br />0x0000007f</p> | <p>Numero massimo di colonne fisse consentite in una tabella, attualmente 127.</p> | 
| <p>JET_ccolVarMost<br />0x00000080</p> | <p>Numero massimo di colonne a lunghezza variabile che possono essere contenute in una tabella, attualmente 128.</p> | 
| <p>JET_ccolTaggedMost<br />( JET_ccolMost - 0x000000ff )</p> | <p>Numero massimo di colonne con tag che possono essere contenute in una tabella, attualmente 64993.</p> | 



### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 


