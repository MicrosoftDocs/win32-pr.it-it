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
ms.openlocfilehash: a7b904c090852ea3990ac78e37a7ca851e152968
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465218"
---
# <a name="callback-parameters"></a>Parametri di callback


_**Si applica a:** Windows | Windows Server_

## <a name="callback-parameters"></a>Parametri di callback

Questo argomento contiene i parametri usati per i callback.

*JET_paramDisableCallbacks*  
65  

Questo parametro disabilita tutti i callback del motore di database per le funzioni fornite dall'applicazione. È destinato principalmente a supportare le utilità del motore di database e non deve essere usato nell'applicazione.


| | | <p>Valore predefinito:</p> | <p>Falso</p> | | <p>Digitare:</p> | <p>Boolean</p> | | <p>Intervallo valido:</p> | <p>False, True</p> | | <p>Ambito:</p> | <p>Istanza</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sì</p> | | <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | | <p>Influisce sul layout fisico:</p> | <p>No</p> | | <p>Influisce sull'affidabilità:</p> | <p>No</p> | | <p>Influisce sulle prestazioni:</p> | <p>No</p> | | <p>Influisce sulle risorse:</p> | <p>No</p> | | <p>Disponibilità:</p> | <p>Windows XP e versioni successive</p> | 



*JET_paramEnablePersistedCallbacks*  
156  

Questo parametro consente l'uso di callback persistenti nel database. Nelle versioni precedenti a Windows Vista, l'uso di callback persistenti era abilitato per impostazione predefinita. Le applicazioni devono ora abilitare in modo esplicito l'uso di callback persistenti in fase di esecuzione usando questo parametro. Se questo parametro non è impostato, qualsiasi operazione di database che richiede la chiamata di un callback avrà esito negativo con JET_errCallbackFailed. Questo parametro non influisce sui callback specificati in fase di esecuzione con i meccanismi seguenti: JET_paramRuntimeCallback, [JetRegisterCallback](./jetregistercallback-function.md)o un parametro di callback esplicito a un'API JET. È comunque possibile creare elementi dello schema che contengono callback persistenti anche quando l'uso di tali callback persistenti non è consentito. Quando questo parametro è impostato su false, esegue l'override JET_paramDisableCallbacks.


| | | <p>Valore predefinito:</p> | <p>Falso</p> | | <p>Digitare:</p> | <p>Boolean</p> | | <p>Intervallo valido:</p> | <p>False, True</p> | | <p>Ambito:</p> | <p>Istanza</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sì</p> | | <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | | <p>Influisce sul layout fisico:</p> | <p>No</p> | | <p>Influisce sull'affidabilità:</p> | <p>No</p> | | <p>Influisce sulle prestazioni:</p> | <p>No</p> | | <p>Influisce sulle risorse:</p> | <p>No</p> | | <p>Disponibilità:</p> | <p>Windows Vista e versioni successive</p> | 



*JET_paramRuntimeCallback*  
73  

Questo parametro configura il motore con una [](./jet-callback-callback-function.md) funzione di callback di runtime che implementa l JET_CALLBACK intervazione. Questo callback può essere chiamato per i motivi [seguenti:](./jet-cbtyp.md)JET_cbtypFreeCursorLS , [JET_cbtypFreeTableLS](./jet-cbtyp.md)o [JET_cbtypNull](./jet-cbtyp.md). Per altre [informazioni, vedere JetSetLS.](./jetsetls-function.md)


| | | <p>Valore predefinito:</p> | <p>NULL</p> | | <p>Digitare:</p> | <p>Puntatore a funzione (JET_API_PTR)</p> | | <p>Intervallo valido:</p> | <p>NULL, <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>*</p> | | <p>Ambito:</p> | <p>Istanza</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sì</p> | | <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | | <p>Influisce sul layout fisico:</p> | <p>No</p> | | <p>Influisce sull'affidabilità:</p> | <p>No</p> | | <p>Influisce sulle prestazioni:</p> | <p>No</p> | | <p>Influisce sulle risorse:</p> | <p>No</p> | | <p>Disponibilità:</p> | <p>Windows XP e versioni successive</p> | 



### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista o Windows XP.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008 o Windows Server 2003.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JET_API_PTR](./jet-api-ptr.md)  
[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_CBTYP](./jet-cbtyp.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetLS](./jetsetls-function.md)
