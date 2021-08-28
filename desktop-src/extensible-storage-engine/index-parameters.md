---
description: 'Altre informazioni su: Parametri di indice'
title: Parametri dell'indice
TOCTitle: Index Parameters
ms:assetid: df3dfbc7-71fb-4ae2-a94a-b00eaa1572ec
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294119(v=EXCHG.10)
ms:contentKeyID: 32765733
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
ms.openlocfilehash: f53430a6b624b6b65a5d02727dc16d7f1fba669d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470897"
---
# <a name="index-parameters"></a>Parametri dell'indice


_**Si applica a:** Windows | Windows Server_

## <a name="index-parameters"></a>Parametri dell'indice

Questo argomento contiene i parametri usati per l'indice.

*JET_paramIndexTupleIncrement*  
132  

Questo parametro specifica il valore predefinito per l'incremento dell'offset usato per scorrere il valore della colonna di origine durante la generazione di ogni tupla. Per altre informazioni, vedere la struttura [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) dati.


| | | <p>Valore predefinito:</p> | <p>1</p> | | <p>Digitare:</p> | <p>Intero</p> | | <p>Intervallo valido:</p> | <p>0 - 32767</p> | | <p>Ambito:</p> | <p>Istanza</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sì</p> | | <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | | <p>Influisce sul layout fisico:</p> | <p>No</p> | | <p>Influisce sull'affidabilità:</p> | <p>No</p> | | <p>Influisce sulle prestazioni:</p> | <p>No</p> | | <p>Influisce sulle risorse:</p> | <p>No</p> | | <p>Disponibilità:</p> | <p>Windows Vista e versioni successive</p> | 



*JET_paramIndexTupleStart*  
133  

Questo parametro specifica l'impostazione predefinita per l'offset nel valore della colonna di origine in corrispondenza del quale inizierà la generazione della tupla. Per altre informazioni, vedere la struttura [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) dati.


| | | <p>Valore predefinito:</p> | <p>0</p> | | <p>Digitare:</p> | <p>Intero</p> | | <p>Intervallo valido:</p> | <p>0 - 32767</p> | | <p>Ambito:</p> | <p>Istanza</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sì</p> | | <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | | <p>Influisce sul layout fisico:</p> | <p>No</p> | | <p>Influisce sull'affidabilità:</p> | <p>No</p> | | <p>Influisce sulle prestazioni:</p> | <p>No</p> | | <p>Influisce sulle risorse:</p> | <p>No</p> | | <p>Disponibilità:</p> | <p>Windows Vista e versioni successive</p> | 



*JET_paramIndexTuplesLengthMax*  
111  

Questo parametro specifica il valore predefinito per la lunghezza massima della tupla in un indice di tupla. Per altre informazioni, vedere la struttura [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) dati.

**Windows Vista:**  Prima di Windows Vista, l'impostazione di questo parametro su zero lo riporta al valore predefinito. Per Windows Vista, questo non è più supportato.


| | | <p>Valore predefinito:</p> | <p>10</p> | | <p>Digitare:</p> | <p>Intero</p> | | <p>Intervallo valido:</p> | <p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> 0, 2-255</p><p><strong>Windows Vista:</strong> 2-255</p> | | <p>Ambito:</p> | <p>Istanza</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sì</p> | | <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | | <p>Influisce sul layout fisico:</p> | <p>No</p> | | <p>Influisce sull'affidabilità:</p> | <p>No</p> | | <p>Influisce sulle prestazioni:</p> | <p>No</p> | | <p>Influisce sulle risorse:</p> | <p>No</p> | | <p>Disponibilità:</p> | <p>Windows XP e versioni successive</p> | 



*JET_paramIndexTuplesLengthMin*  
110  

Questo parametro specifica il valore predefinito per la lunghezza minima della tupla in un indice di tupla. Vedere [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) per altre informazioni.

**Windows Vista:**  Prima di Windows Vista, l'impostazione di questo parametro su zero lo riporta al valore predefinito. Per Windows Vista, questo non è più supportato.


| | | <p>Valore predefinito:</p> | <p>3</p> | | <p>Digitare:</p> | <p>Intero</p> | | <p>Intervallo valido:</p> | <p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> 0, 2-255</p><p><strong>Windows Vista:</strong> 2-255</p> | | <p>Ambito:</p> | <p>Istanza</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sì</p> | | <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>No</p> | | <p>Influisce sul layout fisico:</p> | <p>No</p> | | <p>Influisce sull'affidabilità:</p> | <p>No</p> | | <p>Influisce sulle prestazioni:</p> | <p>No</p> | | <p>Influisce sulle risorse:</p> | <p>No</p> | | <p>Disponibilità:</p> | <p>Windows XP e versioni successive</p> | 



*JET_paramIndexTuplesToIndexMax*  
112  

Questo parametro specifica il valore predefinito per la lunghezza massima di una stringa di origine da suddividere in tuple per un indice di tupla. Vedere [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) per altre informazioni.

**Windows Vista:**  Prima di Windows Vista, l'impostazione di questo parametro su zero ne riporta il valore predefinito. Per Windows Vista, questa funzionalità non è più supportata.


| | | <p>Valore predefinito:</p> | <p>32767</p> | | <p>Digitare:</p> | <p>Intero</p> | | <p>Intervallo valido:</p> | <p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> 0 – 32767</p><p><strong>Windows Vista:</strong> 1 - 32767</p> | | <p>Ambito:</p> | <p>Istanza</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sì</p> | | <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>No</p> | | <p>Influisce sul layout fisico:</p> | <p>No</p> | | <p>Influisce sull'affidabilità:</p> | <p>No</p> | | <p>Influisce sulle prestazioni:</p> | <p>No</p> | | <p>Influisce sulle risorse:</p> | <p>No</p> | | <p>Disponibilità:</p> | <p>Windows XP e versioni successive</p> | 



*JET_paramUnicodeIndexDefault*  
72  

Questo parametro controlla i parametri Unicode predefiniti utilizzati da qualsiasi indice su una colonna chiave Unicode. Il tipo di questo parametro è [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) e viene effettivamente passato usando un puntatore del buffer archiviato nel parametro Integer di [JetGetSystemParameter](./jetgetsystemparameter-function.md) e [JetSetSystemParameter](./jetsetsystemparameter-function.md). Le dimensioni del buffer devono essere uguali a JET_UNICODEINDEX [e](./jet-unicodeindex-structure.md) devono essere passate a [JetGetSystemParameter](./jetgetsystemparameter-function.md) usando il parametro string buffer size. Si tratta di un comportamento chiaramente incoerente, ma questo è il comportamento di questo parametro.

Il valore predefinito di questo parametro contiene un LCID per le impostazioni locali inglese (Stati Uniti) e i flag [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)seguenti: LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH.

**Windows 2000:**  SortID nell'LCID viene ignorato. Viene sempre usato un VALORE SORTID SORT_DEFAULT'oggetto .

**Windows 2000:**  I [flag LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) devono contenere i flag seguenti: LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH. Inoltre, i flag [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)possono contenere i flag seguenti: NORM_IGNORENONSPACE.

**Nota**  Se l'applicazione vuole archiviare dati Unicode, è consigliabile non basarsi sui parametri Unicode predefiniti per gli indici. L'uso dell'inglese (Stati Uniti) è in grado di usare le impostazioni locali invarianti e i flag [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)predefiniti interferiscono in modo grave con alcune lingue. È sempre necessario specificare le proprie impostazioni per i parametri Unicode su JetCreateIndex2 [usando JET_INDEXCREATE](./jet-indexcreate-structure.md).


| | | <p>Valore predefinito:</p> | <p>Speciali</p> | | <p>Digitare:</p> | <p>JET_UNICODEINDEX* (JET_UNICODEINDEX)</p> | | <p>Intervallo valido:</p> | <p>Speciali</p> | | <p>Ambito:</p> | <p>Istanza</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sì</p> | | <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>No</p> | | <p>Influisce sul layout fisico:</p> | <p>No</p> | | <p>Influisce sull'affidabilità:</p> | <p>No</p> | | <p>Influisce sulle prestazioni:</p> | <p>No</p> | | <p>Influisce sulle risorse:</p> | <p>No</p> | | <p>Disponibilità:</p> | <p>Tutti</p> | 



### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_TUPLELIMITS](./jet-tuplelimits-structure.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
