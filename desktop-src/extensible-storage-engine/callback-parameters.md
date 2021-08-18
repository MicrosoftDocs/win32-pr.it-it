---
description: 'Altre informazioni su: Parametri di callback'
title: Parametri di callback
TOCTitle: Callback Parameters
ms:assetid: 7f3cdc13-ffbd-4e5a-b650-1c6388e784dc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269310(v=EXCHG.10)
ms:contentKeyID: 32765600
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
ms.openlocfilehash: a9c14940ee98d4f664914794cd4ff6185b78dd04f438b982179a7ab3c5eb6504
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118982811"
---
# <a name="callback-parameters"></a>Parametri di callback


_**Si applica a:** Windows | Windows Server_

## <a name="callback-parameters"></a>Parametri di callback

Questo argomento contiene i parametri usati per i callback.

*JET_paramDisableCallbacks*  
65  

Questo parametro disabilita tutti i callback del motore di database per le funzioni fornite dall'applicazione. È destinato principalmente a supportare le utilità del motore di database e non deve essere usato nell'applicazione.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>Falso</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>False, True</p></td>
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


*JET_paramEnablePersistedCallbacks*  
156  

Questo parametro consente l'uso di callback persistenti nel database. Nelle versioni precedenti a Windows Vista, l'uso di callback persistenti era abilitato per impostazione predefinita. Le applicazioni devono ora abilitare in modo esplicito l'uso di callback persistenti in fase di esecuzione usando questo parametro. Se questo parametro non è impostato, qualsiasi operazione di database che richiede la chiamata di un callback avrà esito negativo JET_errCallbackFailed. Questo parametro non influisce sui callback specificati in fase di esecuzione con i meccanismi seguenti: JET_paramRuntimeCallback, [JetRegisterCallback](./jetregistercallback-function.md)o un parametro di callback esplicito a un'API JET. È comunque possibile creare elementi dello schema che contengono callback persistenti anche quando l'uso di tali callback persistenti non è consentito. Quando questo parametro è impostato su false, esegue l'override JET_paramDisableCallbacks.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>Falso</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>False, True</p></td>
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


*JET_paramRuntimeCallback*  
73  

Questo parametro configura il motore con una [](./jet-callback-callback-function.md) funzione di callback di runtime che implementa l JET_CALLBACK intervazione. Questo callback può essere chiamato per i motivi seguenti: [JET_cbtypFreeCursorLS](./jet-cbtyp.md), [JET_cbtypFreeTableLS](./jet-cbtyp.md)o [JET_cbtypNull](./jet-cbtyp.md). Per altre [informazioni, vedere JetSetLS.](./jetsetls-function.md)

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>NULL</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Puntatore a funzione (JET_API_PTR)</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>NULL, <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>*</p></td>
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


### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista o Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008 o Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Intestazione</strong></p></td>
<td><p>Dichiarato in Esent.h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Vedere anche

[JET_API_PTR](./jet-api-ptr.md)  
[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_CBTYP](./jet-cbtyp.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetLS](./jetsetls-function.md)
