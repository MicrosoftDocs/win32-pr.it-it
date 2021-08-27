---
description: 'Altre informazioni su: Parametri in informazioni'
title: Parametri in informazioni
TOCTitle: Informational Parameters
ms:assetid: 48500fc9-6d89-45b8-92ad-afb997b729f3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269241(v=EXCHG.10)
ms:contentKeyID: 32765543
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
ms.openlocfilehash: cd932f64956e1a00aae5925b97dbf6c35ecc2661
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987604"
---
# <a name="informational-parameters"></a>Parametri in informazioni


_**Si applica a:** Windows | Windows Server_

## <a name="informational-parameters"></a>Parametri in informazioni

Questo argomento contiene i parametri usati per esporre informazioni sul motore di database.

*JET_paramKeyMost*  
134  

Questo parametro di sola lettura indica la lunghezza massima consentita della chiave di indice che può essere selezionata per le dimensioni correnti della pagina del database (come configurato da JET_paramDatabasePageSize).


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>JET_cbKeyMost4KBytePage</p> | 
| <p>Digitare:</p> | <p>Intero</p> | 
| <p>Intervallo valido:</p> | <p>255 – 65535</p> | 
| <p>Ambito:</p> | <p>Globale</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>N/A</p> | 
| <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>N/A</p> | 
| <p>Influisce sul layout fisico:</p> | <p>No</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>No</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>No</p> | 
| <p>Influisce sulle risorse:</p> | <p>No</p> | 
| <p>Disponibilità:</p> | <p>A partire da Windows Server 2008 e Windows Vista</p> | 



*JET_paramMaxColtyp*  
131  

Questo parametro di sola lettura restituisce il numero [massimo JET_COLTYP](./jet-coltyp.md) (JET_coltypMax) per tale versione del motore di database. Questo valore può essere usato per testare il supporto di una [specifica](./jet-coltyp.md)JET_COLTYP . Se un determinato [JET_COLTYP](./jet-coltyp.md) è minore del valore di questo parametro, è supportato dal motore di database.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>JET_coltypUnsignedShort + 1</p> | 
| <p>Digitare:</p> | <p>Intero</p> | 
| <p>Intervallo valido:</p> | <p>0 – 255</p> | 
| <p>Ambito:</p> | <p>Globale</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>N/A</p> | 
| <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>N/A</p> | 
| <p>Influisce sul layout fisico:</p> | <p>No</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>No</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>No</p> | 
| <p>Influisce sulle risorse:</p> | <p>No</p> | 
| <p>Disponibilità:</p> | <p>A partire da Windows Server 2008 e Windows Vista</p> | 



*JET_paramLVChunkSizeMost*  
163  

Parametro di sola lettura che restituisce le dimensioni del blocco di valore lungo in base alle dimensioni di pagina configurate. Se un valore long deve essere letto o scritto con più chiamate Jet{Set,Retrieve}Column, l'uso di un buffer la cui dimensione è un multiplo delle dimensioni del blocco è più efficiente.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>Pagina da 2 kb = 1966 byte<br />Pagina da 4 kb = 4014 byte<br />Pagina da 8 kb = 8110 byte<br />Pagina da 16 kb = 4050 byte<br />Pagina da 32 kb = 8150 byte</p> | 
| <p>Digitare:</p> | <p>Intero</p> | 
| <p>Intervallo valido:</p> | <p>0-10000</p> | 
| <p>Ambito:</p> | <p></p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p></p> | 
| <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p></p> | 
| <p>Influisce sul layout fisico:</p> | <p></p> | 
| <p>Influisce sull'affidabilità:</p> | <p></p> | 
| <p>Influisce sulle prestazioni:</p> | <p></p> | 
| <p>Influisce sulle risorse:</p> | <p></p> | 
| <p>Disponibilità:</p> | <p></p> | 



### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JET_COLTYP](./jet-coltyp.md)
