---
description: La funzione DeleteMonitor rimuove un monitoraggio delle porte aggiunto dalla funzione AddMonitor.
ms.assetid: 32548d4f-830a-471d-8a72-c0f62f43ffa2
title: Funzione DeleteMonitor (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteMonitor
- DeleteMonitorA
- DeleteMonitorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 5eaeadf7512a71cf0bb67028165ded9c37c8a80750b34dac1cbec70075c5cdaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112651"
---
# <a name="deletemonitor-function"></a>Funzione DeleteMonitor

La **funzione DeleteMonitor** rimuove un monitoraggio delle porte aggiunto dalla [**funzione AddMonitor.**](addmonitor.md)

## <a name="syntax"></a>Sintassi


```C++
BOOL DeleteMonitor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pMonitorName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome del server da cui deve essere rimosso il monitoraggio. Se questo parametro è **NULL,** il monitoraggio delle porte viene rimosso in locale.

</dd> <dt>

*pEnvironment* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica l'ambiente da cui deve essere rimosso il monitoraggio, ad esempio Windows x86, Windows IA64 o Windows x64). Se questo parametro è **NULL,** il monitoraggio viene rimosso dall'ambiente corrente dell'applicazione chiamante e del computer client (non dell'applicazione di destinazione e del server di stampa).

</dd> <dt>

*pMonitorName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome del monitoraggio da rimuovere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non restituire immediatamente . La velocità di ritorno di questa funzione dipende da fattori in fase di esecuzione, ad esempio lo stato di rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

Il chiamante deve avere [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **DeleteMonitorW** (Unicode) e **DeleteMonitorA** (ANSI)<br/>                                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddMonitor**](addmonitor.md)
</dt> </dl>

 

