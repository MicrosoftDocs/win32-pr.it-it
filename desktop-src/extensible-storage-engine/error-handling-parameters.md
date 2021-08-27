---
description: 'Altre informazioni su: Parametri di gestione degli errori'
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
ms.openlocfilehash: 7a0556d97a0dda0182ee4fe229599030f523accd
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474827"
---
# <a name="error-handling-parameters"></a>Parametri di gestione degli errori


_**Si applica a:** Windows | Windows Server_

## <a name="error-handling-parameters"></a>Parametri di gestione degli errori

Questo argomento contiene i parametri utilizzati per la gestione degli errori.

*JET_paramErrorToString* 70  

Questo parametro può essere usato per convertire un [JET_ERR](./jet-err.md) in una stringa. Questa operazione viene eseguita usando una chiamata speciale a [JetGetSystemParameter](./jetgetsystemparameter-function.md) in cui il buffer di output integer contiene il valore [JET_ERR da](./jet-err.md) convertire (come parametro di input) e il buffer di output della stringa restituisce la stringa di errore corrispondente. La stringa sarà simile alla seguente: "JET_errSuccess,Operazione riuscita". La stringa è costituita dal nome simbolico per la stringa, quindi da una virgola e quindi da una semplice descrizione di testo dell'errore. La stringa di descrizione può contenere virgole. Se l'errore non viene riconosciuto, la stringa sarà "Errore sconosciuto,Errore sconosciuto".

**Nota**  Questo parametro è di sola lettura.


| | | <p>Valore predefinito:</p> | <p>Speciali</p> | | <p>Digitare:</p> | <p>Speciali</p> | | <p>Intervallo valido:</p> | <p>Speciali</p> | | <p>Ambito:</p> | <p>Globale</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>No</p> | | <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>No</p> | | <p>Influisce sul layout fisico:</p> | <p>No</p> | | <p>Influisce sull'affidabilità:</p> | <p>No</p> | | <p>Influisce sulle prestazioni:</p> | <p>No</p> | | <p>Influisce sulle risorse:</p> | <p>No</p> | | <p>Disponibilità:</p> | <p>Tutti</p> | 


*JET_paramExceptionAction*  
98  

Questo parametro controlla cosa accade quando viene generata un'eccezione dal motore di database o dal codice chiamato dal motore di database. Se impostato su JET_ExceptionMsgBox, qualsiasi eccezione verrà generata al Windows di eccezioni non gestite. In questo modo l'eccezione verrà gestita come errore dell'applicazione. Lo scopo è impedire al codice dell'applicazione di tentare erroneamente di rilevare e ignorare un'eccezione generata dal motore di database. Questa operazione non può essere consentita perché potrebbe verificarsi un danneggiamento del database. Se l'applicazione vuole gestire correttamente queste eccezioni, la protezione può essere disabilitata impostando questo parametro su JET_ExceptionNone.


| | | <p>Valore predefinito:</p> | <p>JET_ExceptionMsgBox</p> | | <p>Digitare:</p> | <p>Intero</p> | | <p>Intervallo valido:</p> | <p>JET_ExceptionMsgBox, JET_ExceptionNone</p> | | <p>Ambito:</p> | <p>Globale</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong>  No</p><p><strong>Windows Vista:</strong>  Sì</p> | | <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong>  No</p><p><strong>Windows Vista:</strong>  Sì</p> | | <p>Influisce sul layout fisico:</p> | <p>No</p> | | <p>Influisce sull'affidabilità:</p> | <p>Sì</p> | | <p>Influisce sulle prestazioni:</p> | <p>No</p> | | <p>Influisce sulle risorse:</p> | <p>No</p> | | <p>Disponibilità:</p> | <p>Tutti</p> | 


### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 


### <a name="see-also"></a>Vedere anche

[Costanti di gestione degli errori](./error-handling-constants.md)  
[Codici di errore del Archiviazione estendibile](./extensible-storage-engine-error-codes.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JetInit](./jetinit-function.md)
