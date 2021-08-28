---
description: 'Altre informazioni su: Parametri del registro eventi'
title: Parametri del registro eventi
TOCTitle: Event Log Parameters
ms:assetid: c660f555-2627-4d25-8f1c-8c1dc8a3a381
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294086(v=EXCHG.10)
ms:contentKeyID: 32765701
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
ms.openlocfilehash: a1c127f538ae80e8bec3dc5a34d5924b838b51ee
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465878"
---
# <a name="event-log-parameters"></a>Parametri del registro eventi


_**Si applica a:** Windows | Windows Server_

## <a name="event-log-parameters"></a>Parametri del registro eventi

Questo argomento contiene i parametri usati per il registro eventi.

JET_paramEventLogCache  
Questo parametro controlla le dimensioni (in byte) di una cache dei messaggi del registro eventi che contenerà i messaggi del registro eventi generati dal motore di database mentre il servizio eventlog viene arrestato. Questi messaggi memorizzati nella cache verranno scaricati nel registro eventi quando il servizio diventa operativo. Tutti i messaggi che causano un overflow della cache verranno eliminati.


| | | <p>Valore predefinito:</p> | <p>0</p> | | <p>Digitare:</p> | <p>Intero</p> | | <p>Intervallo valido:</p> | <p>0 – 2147483647</p> | | <p>Ambito:</p> | <p>Globale</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>No</p> | | <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | | <p>Influisce sul layout fisico:</p> | <p>No</p> | | <p>Influisce sull'affidabilità:</p> | <p>No</p> | | <p>Influisce sulle prestazioni:</p> | <p>No</p> | | <p>Influisce sulle risorse:</p> | <p>Sì</p> | | <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramEventLoggingLevel*  
  
Questo parametro configura il livello di dettaglio dei messaggi eventlog generati al registro eventi dal motore di database. I numeri più elevati comportano messaggi di log eventi più dettagliati.


| | | <p>Valore predefinito:</p> | <p>JET_EventLoggingLevelMax</p> | | <p>Digitare:</p> | <p>Intero</p> | | <p>Intervallo valido:</p> | <p>JET_EventLoggingDisable : JET_EventLoggingLevelMax</p> | | <p>Ambito:</p> | <p>Istanza</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sì</p> | | <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | | <p>Influisce sul layout fisico:</p> | <p>No</p> | | <p>Influisce sull'affidabilità:</p> | <p>No</p> | | <p>Influisce sulle prestazioni:</p> | <p>No</p> | | <p>Influisce sulle risorse:</p> | <p>No</p> | | <p>Disponibilità:</p> | <p>Windows XP e versioni successive</p> | 



*JET_paramEventSource*  
4  

Questo parametro fornisce una stringa specifica dell'applicazione che verrà aggiunta a tutti i messaggi del log eventi generati dal motore di database. In questo modo è possibile correlare facilmente i messaggi del log eventi con l'applicazione di origine. Se viene specificata una stringa vuota (come è l'impostazione predefinita), verrà usato il nome eseguibile dell'applicazione host.


| | | <p>Valore predefinito:</p> | <p>""</p> | | <p>Digitare:</p> | <p>string</p> | | <p>Intervallo valido:</p> | <p>Da 0 a 259 caratteri</p> | | <p>Ambito:</p> | <p>Istanza</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sì</p> | | <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | | <p>Influisce sul layout fisico:</p> | <p>No</p> | | <p>Influisce sull'affidabilità:</p> | <p>No</p> | | <p>Influisce sulle prestazioni:</p> | <p>No</p> | | <p>Influisce sulle risorse:</p> | <p>No</p> | | <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramEventSourceKey*  
49  

Questo parametro può essere usato per controllare il registro eventi usato dal motore di database per i messaggi del log eventi. Per impostazione predefinita, tutti i messaggi del registro eventi verranno inviati al registro eventi dell'applicazione. Se il nome della chiave del Registro di sistema per un altro registro eventi è configurato, i messaggi del registro eventi verranno visualizzati.


| | | <p>Valore predefinito:</p> | <p>""</p> | | <p>Digitare:</p> | <p>string</p> | | <p>Intervallo valido:</p> | <p>Da 0 a 259 caratteri</p> | | <p>Ambito:</p> | <p>Istanza</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sì</p> | | <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | | <p>Influisce sul layout fisico:</p> | <p>No</p> | | <p>Influisce sull'affidabilità:</p> | <p>No</p> | | <p>Influisce sulle prestazioni:</p> | <p>No</p> | | <p>Influisce sulle risorse:</p> | <p>No</p> | | <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramNoInformationEvent*  
50  

Quando questo parametro è true, i messaggi del registro eventi informativi che normalmente verrebbero generati dal motore di database verranno eliminati.


| | | <p>Valore predefinito:</p> | <p>Falso</p> | | <p>Digitare:</p> | <p>Boolean</p> | | <p>Intervallo valido:</p> | <p>False, True</p> | | <p>Ambito:</p> | <p>Istanza</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sì</p> | | <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>No</p> | | <p>Influisce sul layout fisico:</p> | <p>No</p> | | <p>Influisce sull'affidabilità:</p> | <p>No</p> | | <p>Influisce sulle prestazioni:</p> | <p>No</p> | | <p>Influisce sulle risorse:</p> | <p>No</p> | | <p>Disponibilità:</p> | <p>Tutti</p> | 



### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)
