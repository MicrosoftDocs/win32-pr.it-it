---
description: La funzione FindClosePrinterChangeNotification chiude un oggetto notifica di modifica creato chiamando la funzione FindFirstPrinterChangeNotification.
ms.assetid: 2b4758f8-af0a-494b-8f1b-8ea6ee73c79b
title: Funzione FindClosePrinterChangeNotification (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindClosePrinterChangeNotification
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 17ec31b1f2992b4311e42e149d39b68b3d724a3d943d67df7c4c5fce88122606
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112491"
---
# <a name="findcloseprinterchangenotification-function"></a>Funzione FindClosePrinterChangeNotification

La **funzione FindClosePrinterChangeNotification** chiude un oggetto notifica di modifica creato chiamando la [**funzione FindFirstPrinterChangeNotification.**](findfirstprinterchangenotification.md) La stampante o il server di stampa associato all'oggetto notifica di modifica non verrà più monitorato da tale oggetto.

## <a name="syntax"></a>Sintassi


```C++
BOOL FindClosePrinterChangeNotification(
  _In_ HANDLE hChange
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hChange* \[ Pollici\]
</dt> <dd>

Handle per l'oggetto notifica di modifica da chiudere. Si tratta di un handle creato chiamando la [**funzione FindFirstPrinterChangeNotification.**](findfirstprinterchangenotification.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona che potrebbe non essere restituita immediatamente. La velocità di ritorno di questa funzione dipende da fattori di run-time, ad esempio lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante, difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

Dopo aver chiamato la **funzione FindClosePrinterChangeNotification,** non è possibile usare l'handle *hChange* nelle chiamate successive a [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) o [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)
</dt> <dt>

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> </dl>

 

 




