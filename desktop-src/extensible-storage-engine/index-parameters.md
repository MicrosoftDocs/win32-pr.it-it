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
ms.openlocfilehash: 3d322334d5a14439461f903a583e11e78a7b829863c2b55dbf653dc13aa4d22d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119604481"
---
# <a name="index-parameters"></a>Parametri dell'indice


_**Si applica a:** Windows | Windows Server_

## <a name="index-parameters"></a>Parametri dell'indice

Questo argomento contiene i parametri usati per l'indice.

*JET_paramIndexTupleIncrement*  
132  

Questo parametro specifica il valore predefinito per l'incremento dell'offset usato per scorrere il valore della colonna di origine durante la generazione di ogni tupla. Per altre informazioni, vedere la struttura [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) dati.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Intero</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>0 - 32767</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Istanza</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sulle prestazioni:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sulle risorse:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Windows Vista e versioni successive</p></td>
</tr>
</tbody>
</table>


*JET_paramIndexTupleStart*  
133  

Questo parametro specifica l'impostazione predefinita per l'offset nel valore della colonna di origine da cui inizierà la generazione della tupla. Per altre informazioni, vedere la struttura [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) dati.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>0</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Intero</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>0 - 32767</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Istanza</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sulle prestazioni:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sulle risorse:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Windows Vista e versioni successive</p></td>
</tr>
</tbody>
</table>


*JET_paramIndexTuplesLengthMax*  
111  

Questo parametro specifica il valore predefinito per la lunghezza massima della tupla in un indice di tupla. Per altre informazioni, vedere la struttura [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) dati.

**Windows Vista:**  Prima di Windows Vista, l'impostazione di questo parametro su zero lo riporta al valore predefinito. Per Windows Vista, questo non è più supportato.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>10</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Intero</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> 0, 2-255</p>
<p><strong>Windows Vista:</strong> 2-255</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Istanza</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sulle prestazioni:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sulle risorse:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Windows XP e versioni successive</p></td>
</tr>
</tbody>
</table>


*JET_paramIndexTuplesLengthMin*  
110  

Questo parametro specifica il valore predefinito per la lunghezza minima della tupla in un indice di tupla. Vedere [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) per altre informazioni.

**Windows Vista:**  Prima di Windows Vista, l'impostazione di questo parametro su zero lo riporta al valore predefinito. Per Windows Vista, questo non è più supportato.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>3</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Intero</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> 0, 2-255</p>
<p><strong>Windows Vista:</strong> 2-255</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Istanza</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sulle prestazioni:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sulle risorse:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Windows XP e versioni successive</p></td>
</tr>
</tbody>
</table>


*JET_paramIndexTuplesToIndexMax*  
112  

Questo parametro specifica il valore predefinito per la lunghezza massima di una stringa di origine da suddividere in tuple per un indice di tupla. Vedere [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) per altre informazioni.

**Windows Vista:**  Prima di Windows Vista, l'impostazione di questo parametro su zero lo riporta al valore predefinito. Per Windows Vista, questo non è più supportato.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>32767</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Intero</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> 0 – 32767</p>
<p><strong>Windows Vista:</strong> 1 - 32767</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Istanza</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sulle prestazioni:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sulle risorse:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Windows XP e versioni successive</p></td>
</tr>
</tbody>
</table>


*JET_paramUnicodeIndexDefault*  
72  

Questo parametro controlla i parametri Unicode predefiniti usati da qualsiasi indice su una colonna chiave Unicode. Il tipo di questo parametro [è JET_UNICODEINDEX](./jet-unicodeindex-structure.md) e viene effettivamente passato usando un puntatore al buffer archiviato nel parametro Integer di [JetGetSystemParameter](./jetgetsystemparameter-function.md) e [JetSetSystemParameter](./jetsetsystemparameter-function.md). Le dimensioni del buffer devono essere uguali a JET_UNICODEINDEX [e](./jet-unicodeindex-structure.md) devono essere passate a [JetGetSystemParameter](./jetgetsystemparameter-function.md) usando il parametro string buffer size. Questo è chiaramente incoerente, ma questo è il comportamento di questo parametro.

Il valore predefinito di questo parametro contiene un LCID per le impostazioni locali della lingua inglese degli Stati Uniti e i flag [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)seguenti: LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH.

**Windows 2000:**  SortID nell'LCID viene ignorato. Viene sempre usato un VALORE SORTID SORT_DEFAULT valore.

**Windows 2000:**  I [flag LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) devono contenere i flag seguenti: LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH. Inoltre, i flag [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)possono contenere i flag seguenti: NORM_IGNORENONSPACE.

**Nota**  Se l'applicazione vuole archiviare dati Unicode, è consigliabile non basarsi sui parametri Unicode predefiniti per gli indici. L'uso dell'inglese degli Stati Uniti equivale all'uso delle impostazioni locali invarianti e i flag [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)predefiniti sono noti per interferire gravemente con alcune lingue. È necessario specificare sempre le proprie impostazioni per i parametri Unicode in JetCreateIndex2 [usando](./jet-indexcreate-structure.md)JET_INDEXCREATE .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>Speciali</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>JET_UNICODEINDEX* (JET_UNICODEINDEX)</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>Speciali</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Istanza</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sulle prestazioni:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sulle risorse:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Tutti</p></td>
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
<td><p>Dichiarato in Esent.h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Vedere anche

[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_TUPLELIMITS](./jet-tuplelimits-structure.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
