---
description: La funzione AddMonitor installa un monitoraggio porta locale e collega i file di configurazione, dati e monitoraggio.
ms.assetid: 6a556422-5360-42d2-b177-dba0498c06d8
title: Funzione AddMonitor (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddMonitor
- AddMonitorA
- AddMonitorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 40b45c4dc05580837a2cf4a001cf8d18e646e5cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058246"
---
# <a name="addmonitor-function"></a>AddMonitor (funzione)

La funzione **AddMonitor** installa un monitoraggio porta locale e collega i file di configurazione, dati e monitoraggio.

## <a name="syntax"></a>Sintassi


```C++
BOOL AddMonitor(
  _In_ LPTSTR pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pMonitors
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pname* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome del server in cui deve essere installato il monitoraggio. Per i sistemi che supportano solo l'installazione locale dei monitoraggi, la stringa deve essere **null**.

</dd> <dt>

*Livello* \[ di in\]
</dt> <dd>

Versione della struttura a cui punta *pMonitors* . Questo valore deve essere 2.

</dd> <dt>

*pMonitors* \[ in\]
</dt> <dd>

Puntatore a una struttura di [**monitoraggio \_ info \_ 2**](monitor-info-2.md) . Se il membro **pEnvironment** della struttura *pMonitors* è **null**, viene utilizzato l'ambiente corrente del chiamante (client), non della destinazione (Server).

Si noti che la chiamata avrà esito negativo se l'ambiente non corrisponde all'ambiente del server, ovvero è possibile aggiungere solo un monitoraggio scritto per l'architettura del server.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

Il chiamante deve avere [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).

Prima che un'applicazione chiami la funzione **AddMonitor** , tutti i file richiesti dal monitoraggio devono essere copiati nella directory system32.

Per determinare i monitoraggi delle porte attualmente installati, chiamare la funzione [**EnumMonitors**](enummonitors.md) .

Per rimuovere un monitoraggio aggiunto da **AddMonitor**, chiamare la funzione [**DeleteMonitor**](deletemonitor.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **AddMonitorW** (Unicode) e **AddMonitorA** (ANSI)<br/>                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeleteMonitor**](deletemonitor.md)
</dt> <dt>

[**EnumMonitors**](enummonitors.md)
</dt> <dt>

[**Informazioni sul monitoraggio \_ \_ 2**](monitor-info-2.md)
</dt> </dl>

 

