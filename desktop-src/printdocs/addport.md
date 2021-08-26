---
description: La funzione AddPort aggiunge il nome di una porta all'elenco delle porte supportate. La funzione AddPort viene esportata dal monitoraggio delle porte.
ms.assetid: 9191d507-9167-4488-a4b4-286590a8a62a
title: Funzione AddPort (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPort
- AddPortA
- AddPortW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: abbb2e4b836c64ddff47c92681e32bd0d5f9f0c38224d6c710fb10bc3435ac96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112691"
---
# <a name="addport-function"></a>Funzione AddPort

La **funzione AddPort** aggiunge il nome di una porta all'elenco delle porte supportate. La **funzione AddPort** viene esportata dal monitoraggio delle porte.

## <a name="syntax"></a>Sintassi


```C++
BOOL AddPort(
  _In_ LPTSTR pName,
  _In_ HWND   hWnd,
  _In_ LPTSTR pMonitorName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione zero che specifica il nome del server a cui è connessa la porta. Se questo parametro è **NULL,** la porta è locale.

</dd> <dt>

*hWnd* \[ Pollici\]
</dt> <dd>

Handle per la finestra padre della **finestra di dialogo AddPort.**

</dd> <dt>

*pMonitorName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione zero che specifica il monitoraggio associato alla porta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona che potrebbe non essere restituita immediatamente. La velocità di ritorno di questa funzione dipende da fattori di run-time, ad esempio lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante, difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

La **funzione AddPort** esplora la rete per trovare le porte esistenti e visualizza una finestra di dialogo per l'utente. La **funzione AddPort** deve convalidare il nome della porta immesso dall'utente chiamando [**EnumPorts**](enumports.md) per assicurarsi che non esistano nomi duplicati.

Il chiamante della **funzione AddPort** deve disporre dell'accesso SERVER \_ ACCESS ADMINISTER al server a cui è \_ connessa la porta.

Per aggiungere una porta senza visualizzare una finestra di dialogo, chiamare la **funzione XcvData** anziché **AddPort**. Per altre informazioni su **XcvData,** vedere Microsoft Windows Driver Development Kit (DDK).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Nomi Unicode e ANSI<br/>   | **AddPortW** (Unicode) e **AddPortA** (ANSI)<br/>                                                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePort**](deleteport.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> <dt>

[**SetPort**](setport.md)
</dt> </dl>

 

 




