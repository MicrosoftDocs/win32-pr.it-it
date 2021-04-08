---
description: 'Altre informazioni su: parametri di indice'
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
ms.openlocfilehash: 2901887233ff8b25114334c97e6a731072a69ce1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058292"
---
# <a name="index-parameters"></a>Parametri dell'indice


_**Si applica a:** Windows | Windows Server_

## <a name="index-parameters"></a>Parametri dell'indice

Questo argomento contiene i parametri usati per l'indice.

*JET_paramIndexTupleIncrement*  
132  

Questo parametro specifica l'impostazione predefinita per l'incremento di offset utilizzato per scorrere il valore della colonna di origine durante la generazione di ogni tupla. Per ulteriori informazioni, vedere la struttura [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .

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
<td><p>Integer</p></td>
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
<td><p>Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influiscono sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influire sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influire sulle prestazioni:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influiscono sulle risorse:</p></td>
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

Questo parametro specifica il valore predefinito per l'offset nel valore della colonna di origine in corrispondenza del quale verrà avviata la generazione della tupla. Per ulteriori informazioni, vedere la struttura [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .

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
<td><p>Integer</p></td>
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
<td><p>Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influiscono sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influire sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influire sulle prestazioni:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influiscono sulle risorse:</p></td>
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

Questo parametro specifica il valore predefinito per la lunghezza massima della tupla in un indice della tupla. Per ulteriori informazioni, vedere la struttura [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .

**Windows Vista:**  Prima di Windows Vista, impostando questo parametro su zero sarebbe stato impostato il valore predefinito. Per Windows Vista, questa operazione non è più supportata.

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
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p><strong>Windows 2000, Windows XP e Windows Server 2003: </strong>  0, 2-255</p>
<p><strong>Windows Vista:</strong>  2-255</p></td>
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
<td><p>Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influiscono sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influire sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influire sulle prestazioni:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influiscono sulle risorse:</p></td>
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

Questo parametro specifica il valore predefinito per la lunghezza minima della tupla in un indice della tupla. Per ulteriori informazioni, vedere [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .

**Windows Vista:**  Prima di Windows Vista, impostando questo parametro su zero sarebbe stato impostato il valore predefinito. Per Windows Vista, questa operazione non è più supportata.

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
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p><strong>Windows 2000, Windows XP e Windows Server 2003: </strong>  0, 2-255</p>
<p><strong>Windows Vista:</strong>  2-255</p></td>
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
<td><p>Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influiscono sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influire sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influire sulle prestazioni:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influiscono sulle risorse:</p></td>
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

Questo parametro specifica il valore predefinito per la lunghezza massima di una stringa di origine per suddividere le tuple per un indice di tupla. Per ulteriori informazioni, vedere [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .

**Windows Vista:**  Prima di Windows Vista, impostando questo parametro su zero sarebbe stato impostato il valore predefinito. Per Windows Vista, questa operazione non è più supportata.

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
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong>  0 – 32767</p>
<p><strong>Windows Vista:</strong>  1 – 32767</p></td>
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
<td><p>Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influiscono sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influire sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influire sulle prestazioni:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influiscono sulle risorse:</p></td>
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

Questo parametro controlla i parametri Unicode predefiniti utilizzati da qualsiasi indice su una colonna chiave Unicode. Il tipo di questo parametro è [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) e viene effettivamente passato utilizzando un puntatore del buffer archiviato nel parametro integer di [JetGetSystemParameter](./jetgetsystemparameter-function.md) e [JetSetSystemParameter](./jetsetsystemparameter-function.md). Le dimensioni del buffer devono essere uguali a quelle del [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) e devono essere passate a [JetGetSystemParameter](./jetgetsystemparameter-function.md) utilizzando il parametro della dimensione del buffer di stringa. Questo comportamento è chiaramente incoerente, ma questo è il comportamento di questo parametro.

Il valore predefinito di questo parametro contiene un LCID per le impostazioni locali per l'inglese (Stati Uniti) e i flag [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)seguenti: LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH.

**Windows 2000:**  SORTID nell'LCID viene ignorato. Viene sempre usato un SORTID di SORT_DEFAULT.

**Windows 2000:**  I flag [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) devono contenere i flag seguenti: LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH. Inoltre, i flag [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)possono contenere i flag seguenti: NORM_IGNORENONSPACE.

**Nota**  Se l'applicazione desidera archiviare dati Unicode, è consigliabile non fare affidamento sui parametri Unicode predefiniti per gli indici. L'uso dell'inglese (Stati Uniti) equivale all'uso delle impostazioni locali invariabili e i flag [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)predefiniti sono noti per interferire seriamente con alcune lingue. È necessario specificare sempre le proprie impostazioni per i parametri Unicode in JetCreateIndex2 usando [JET_INDEXCREATE](./jet-indexcreate-structure.md).

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
<td><p>JET_UNICODEINDEX * (JET_UNICODEINDEX)</p></td>
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
<td><p>Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influiscono sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influire sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influire sulle prestazioni:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influiscono sulle risorse:</p></td>
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
<td><p>Dichiarata in esent. h.</p></td>
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
