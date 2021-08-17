---
description: La funzione FreePrinterNotifyInfo libera un buffer allocato dal sistema creato dalla funzione FindNextPrinterChangeNotification.
ms.assetid: e50d4718-3682-486b-9d07-ddddd0b284dc
title: Funzione FreePrinterNotifyInfo (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreePrinterNotifyInfo
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 37340bc7d5ba576735c7bf4cc1ef8ac40b07377e829353d35452ed0fa5307891
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091951"
---
# <a name="freeprinternotifyinfo-function"></a>Funzione FreePrinterNotifyInfo

La **funzione FreePrinterNotifyInfo** libera un buffer allocato dal sistema creato dalla [**funzione FindNextPrinterChangeNotification.**](findnextprinterchangenotification.md)

## <a name="syntax"></a>Sintassi


```C++
BOOL FreePrinterNotifyInfo(
  _In_ PPRINTER_NOTIFY_INFO pPrinterNotifyInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pPrinterNotifyInfo* \[ Pollici\]
</dt> <dd>

Puntatore a un buffer [**PRINTER \_ NOTIFY \_ INFO**](printer-notify-info.md) restituito da una chiamata alla [**funzione FindNextPrinterChangeNotification.**](findnextprinterchangenotification.md) **FreePrinterNotifyInfo** dealloca questo buffer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non restituire immediatamente . La velocità di ritorno di questa funzione dipende da fattori in fase di esecuzione, ad esempio lo stato di rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> <dt>

[**INFORMAZIONI DI \_ NOTIFICA \_ STAMPANTE**](printer-notify-info.md)
</dt> </dl>

 

 




