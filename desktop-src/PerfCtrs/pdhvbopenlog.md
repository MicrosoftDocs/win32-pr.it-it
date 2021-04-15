---
description: La funzione PdhVbOpenLog apre il file di log specificato per la lettura e la scrittura. Questa funzione chiama PdhOpenLog.
ms.assetid: d9b8d98c-64f2-4319-8ab2-67b776143cf7
title: PdhVbOpenLog (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbOpenLog
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 7921585039cab285589f2cdde0f328c033069a87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529113"
---
# <a name="pdhvbopenlog-function"></a>PdhVbOpenLog (funzione)

La funzione **PdhVbOpenLog** apre il file di log specificato per la lettura e la scrittura. Questa funzione chiama [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga).

> [!IMPORTANT]
> La funzione descritta in questo argomento può essere modificata o non disponibile in futuro. Microsoft consiglia invece di utilizzare le funzioni descritte in [funzioni dei contatori delle prestazioni](performance-counters-functions.md).

Funzione PdhVbOpenLog ( \_ ByVal SzLogFileName As LPCTSTR, \_ ByVal DWACCESSFLAGS As DWORD, \_ ByVal lpdwLogType As LPDWORD, \_ ByVal hQuery As PDH \_ HQUERY, \_ ByVal DwMaxSize As DWORD, \_ ByVal SZUSERCAPTION As LPCSTR, \_ ByRef phLog As PDH \_ numero \_ ) As DWORD

## <a name="parameters"></a>Parametri

<dl> <dt>

*szLogFileName* \[ in\]
</dt> <dd>

Puntatore a una stringa che specifica il nome del file di log da aprire.

Se il file di log contiene dati SQL, il formato del nome del file di log è **SQL:**_DataSourceName_*_!_* _LogFileName_. In questo caso, il valore del parametro *lpdwLogType* è PDH \_ log \_ Type \_ SQL.

</dd> <dt>

*dwAccessFlags* \[ in\]
</dt> <dd>

Tipo di accesso da specificare quando viene aperto il file di log. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                   | Significato                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="PDH_LOG_READ_ACCESS"></span><span id="pdh_log_read_access"></span><dl> <dt>**\_accesso in \_ lettura \_ al log PDH**</dt> </dl>       | Viene aperto un file di log per un'operazione di lettura.<br/>            |
| <span id="PDH_LOG_WRITE_ACCESS"></span><span id="pdh_log_write_access"></span><dl> <dt>**\_accesso in \_ scrittura \_ log PDH**</dt> </dl>    | Viene aperto un nuovo file di log per un'operazione di scrittura.<br/>       |
| <span id="PDH_LOG_UPDATE_ACCESS"></span><span id="pdh_log_update_access"></span><dl> <dt>**\_ \_ accesso aggiornamento log \_ PDH**</dt> </dl> | Per un'operazione di scrittura viene aperto un file di log esistente.<br/> |



 

Il valore selezionato dalla tabella precedente può essere combinato usando l'operatore OR con uno dei seguenti flag di creazione di accesso.



| Valore                                                                                                                                                                                   | Significato                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PDH_LOG_CREATE_NEW"></span><span id="pdh_log_create_new"></span><dl> <dt>**\_creazione di \_ un \_ nuovo log PDH**</dt> </dl>          | Viene creato un nuovo file di log con il nome specificato.<br/>                                                                                                    |
| <span id="PDH_LOG_CREATE_ALWAYS"></span><span id="pdh_log_create_always"></span><dl> <dt>**PDH \_ log \_ Crea \_ sempre**</dt> </dl> | Viene creato un nuovo file di log con il nome specificato e viene cancellato qualsiasi file di log esistente con lo stesso nome.<br/>                                             |
| <span id="PDH_LOG_OPEN_EXISTING"></span><span id="pdh_log_open_existing"></span><dl> <dt>**\_Registro PDH \_ aperto \_ esistente**</dt> </dl> | Viene aperto un file di log esistente con il nome specificato. Se non esiste un file di log con il nome specificato, è uguale a PDH \_ log \_ Create \_ New.<br/> |
| <span id="PDH_LOG_OPEN_ALWAYS"></span><span id="pdh_log_open_always"></span><dl> <dt>**PDH \_ log \_ aperto \_ sempre**</dt> </dl>       | Viene aperto un file di log esistente con il nome specificato oppure viene creato un nuovo file di log con il nome specificato.<br/>                                          |



 

</dd> <dt>

*lpdwLogType* \[ in\]
</dt> <dd>

Puntatore a una variabile che indica il tipo di file di log da aprire. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                      | Significato                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span id="PDH_LOG_TYPE_UNDEFINED"></span><span id="pdh_log_type_undefined"></span><dl> <dt>**tipo di log PDH non \_ \_ \_ definito**</dt> </dl> | Formato del file di log non definito.<br/>                                                                                   |
| <span id="PDH_LOG_TYPE_CSV"></span><span id="pdh_log_type_csv"></span><dl> <dt>**\_tipo di log PDH \_ \_ CSV**</dt> </dl>                   | File di testo contenenti le intestazioni di colonna nella prima riga e singoli campioni di dati in ogni riga successiva.<br/> |
| <span id="PDH_LOG_TYPE_SQL"></span><span id="pdh_log_type_sql"></span><dl> <dt>**\_tipo di log PDH \_ \_ SQL**</dt> </dl>                   | I dati nel file di log sono in SQL.<br/>                                                                          |
| <span id="PDH_LOG_TYPE_TSV"></span><span id="pdh_log_type_tsv"></span><dl> <dt>**\_tipo di log PDH \_ \_ TSV**</dt> </dl>                   | Uguale al \_ tipo di log PDH \_ \_ CSV.<br/>                                                                                 |
| <span id="PDH_LOG_TYPE_BINARY"></span><span id="pdh_log_type_binary"></span><dl> <dt>**\_ \_ Binary tipo di log PDH \_**</dt> </dl>          | Formato binario del file di log. Include i file di log circolari.<br/>                                                         |
| <span id="PDH_LOG_TYPE_PERFMON"></span><span id="pdh_log_type_perfmon"></span><dl> <dt>**\_tipo di log PDH \_ \_ PerfMon**</dt> </dl>       | Formato del file di log PerfMon.<br/>                                                                                     |



 

</dd> <dt>

*hQuery* \[ in\]
</dt> <dd>

Handle di query. Questo handle viene restituito dalla funzione [**PdhVbOpenQuery**](pdhvbopenquery.md) .

Questo parametro può essere **null** se il file di log deve essere aperto per la lettura.

</dd> <dt>

*dwMaxSize* \[ in\]
</dt> <dd>

Dimensioni massime del file di log in byte. Questo valore viene utilizzato solo se il file di log è un file di log di dimensioni limitate o circolari.

</dd> <dt>

*szUserCaption* \[ in\]
</dt> <dd>

Puntatore a una stringa che specifica la didascalia definita dall'utente del file di log. Una didascalia del file di log descrive in genere il contenuto del file di log. Quando viene aperto un file di log esistente, il valore di questo parametro viene ignorato.

</dd> <dt>

*phLog* \[ in, Ref\]
</dt> <dd>

Puntatore a un buffer che riceve un handle per il file di log aperto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce 0.

Se la funzione ha esito negativo, il valore restituito è un [codice di errore di sistema](/windows/desktop/Debug/system-error-codes) o un codice di [errore PDH](pdh-error-codes.md). Di seguito sono riportati i valori possibili.



| Codice restituito                                                                                                | Descrizione                                                                                            |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_buffer insufficiente PDH \_**</dt> </dl>   | I dati richiesti sono maggiori del buffer fornito. Impossibile restituire i dati richiesti.<br/> |
| <dl> <dt>**\_argomento PDH non valido \_**</dt> </dl>      | La dimensione di uno o più buffer di stringa non è corretta.<br/>                                  |
| <dl> <dt>**\_handle PDH non valido \_**</dt> </dl>        | L'handle non è un oggetto PDH valido.<br/>                                                       |
| <dl> <dt>**\_errore di \_ apertura del file di registro PDH \_ \_**</dt> </dl> | Impossibile aprire il file di log specificato.<br/>                                                      |
| <dl> <dt>**il \_ file PDH non è stato \_ \_ trovato**</dt> </dl>       | Impossibile trovare il file specificato.<br/>                                                          |



 

## <a name="remarks"></a>Commenti

Quando si utilizza questa funzione per scrivere i dati sulle prestazioni in un file di log, è necessario innanzitutto aprire una query utilizzando [**PdhVbOpenQuery**](pdhvbopenquery.md).

È necessario che sia presente una query attualmente aperta ed è necessario aggiungervi i contatori desiderati, prima di chiamare questa funzione.

Si noti che i file di log nel formato Perfmon possono essere aperti solo per la lettura.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Libreria<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga)
</dt> <dt>

[**PdhVbGetLogFileSize**](pdhvbgetlogfilesize.md)
</dt> <dt>

[**PdhVbUpdateLog**](pdhvbupdatelog.md)
</dt> </dl>

 

