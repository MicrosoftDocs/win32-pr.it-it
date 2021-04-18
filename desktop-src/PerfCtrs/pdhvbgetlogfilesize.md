---
description: La funzione PdhVbGetLogFileSize restituisce le dimensioni del file di log specificato. Questa funzione chiama PdhGetLogFileSize.
ms.assetid: 8f4fbb68-b0f5-4163-ae6e-5b7139a35adf
title: PdhVbGetLogFileSize (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetLogFileSize
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 0b9f490477704086bd9aa8c53dd32456d486471e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312148"
---
# <a name="pdhvbgetlogfilesize-function"></a>PdhVbGetLogFileSize (funzione)

La funzione **PdhVbGetLogFileSize** restituisce le dimensioni del file di log specificato. Questa funzione chiama [**PdhGetLogFileSize**](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize).

> [!IMPORTANT]
> La funzione descritta in questo argomento può essere modificata o non disponibile in futuro. Microsoft consiglia invece di utilizzare le funzioni descritte in [funzioni dei contatori delle prestazioni](performance-counters-functions.md).

Funzione PdhVbGetLogFileSize ( \_ ByVal numero As PDH \_ numero, \_ ByRef llSize Long \_ ) As DWORD

## <a name="parameters"></a>Parametri

<dl> <dt>

*numero* \[ in\]
</dt> <dd>

Handle per il file di log. Questo handle viene restituito dalla funzione [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga) .

</dd> <dt>

*llSize* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve le dimensioni, in byte, del file di log.

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



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Libreria<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PdhGetLogFileSize**](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize)
</dt> <dt>

[**PdhVbOpenLog**](pdhvbopenlog.md)
</dt> <dt>

[**PdhVbUpdateLog**](pdhvbupdatelog.md)
</dt> </dl>

 

