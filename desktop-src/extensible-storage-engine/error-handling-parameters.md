---
description: 'Altre informazioni su: parametri di gestione degli errori'
title: Parametri di gestione degli errori
TOCTitle: Error Handling Parameters
ms:assetid: 014996a1-5674-40c7-9538-54cae1681fec
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269173(v=EXCHG.10)
ms:contentKeyID: 32765476
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eb225d7dbb67655286635320352060bcf2cb8a5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885378"
---
# <a name="error-handling-parameters"></a>Parametri di gestione degli errori


_**Si applica a:** Windows | Windows Server_

## <a name="error-handling-parameters"></a>Parametri di gestione degli errori

Questo argomento contiene i parametri utilizzati per la gestione degli errori.

*JET_paramErrorToString* 70  

Questo parametro può essere usato per convertire un [JET_ERR](./jet-err.md) in una stringa. Questa operazione viene eseguita tramite una chiamata speciale a [JetGetSystemParameter](./jetgetsystemparameter-function.md) in cui il buffer di output Integer contiene il valore [JET_ERR](./jet-err.md) da convertire (come parametro di input) e il buffer di output della stringa restituisce la stringa di errore corrispondente. La stringa avrà un aspetto simile al seguente: "JET_errSuccess, operazione riuscita". La stringa è costituita dal nome simbolico della stringa, quindi da una virgola e quindi da una semplice descrizione di testo dell'errore. La stringa di descrizione può contenere virgole. Se l'errore non viene riconosciuto, la stringa sarà "errore sconosciuto, errore sconosciuto".

**Nota**  Questo parametro è di sola lettura.

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
<td><p>Speciali</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>Speciali</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Globale</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>No</p></td>
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

*JET_paramExceptionAction*  
98  

Questo parametro controlla ciò che accade quando un'eccezione viene generata dal motore di database o dal codice chiamato dal motore di database. Se impostato su JET_ExceptionMsgBox, qualsiasi eccezione verrà generata al filtro eccezioni non gestite di Windows. In questo modo l'eccezione viene gestita come un errore dell'applicazione. Lo scopo è impedire che il codice dell'applicazione tenti erroneamente di rilevare e ignorare un'eccezione generata dal motore di database. Questa operazione non può essere consentita perché potrebbe verificarsi un danneggiamento del database. Se l'applicazione desidera gestire correttamente queste eccezioni, è possibile disabilitare la protezione impostando questo parametro su JET_ExceptionNone.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>JET_ExceptionMsgBox</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>JET_ExceptionMsgBox, JET_ExceptionNone</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Globale</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p><strong>Windows 2000, Windows XP e Windows Server 2003:  </strong>  No</p>
<p><strong>Windows Vista:</strong>  Sì</p></td>
</tr>
<tr class="even">
<td><p>Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p><strong>Windows 2000, Windows XP e Windows Server 2003:  </strong>  No</p>
<p><strong>Windows Vista:</strong>  Sì</p></td>
</tr>
<tr class="odd">
<td><p>Influiscono sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influire sull'affidabilità:</p></td>
<td><p>Sì</p></td>
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

[Costanti di gestione degli errori](./error-handling-constants.md)  
[Codici di errore di Extensible Storage Engine](./extensible-storage-engine-error-codes.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JetInit](./jetinit-function.md)
