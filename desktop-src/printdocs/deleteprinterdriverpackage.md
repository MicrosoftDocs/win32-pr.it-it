---
description: Elimina un pacchetto driver della stampante dall'archivio driver.
ms.assetid: a43a94d1-097e-457c-bce9-d4c434ecfa93
title: Funzione DeletePrinterDriverPackage (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDriverPackage
- DeletePrinterDriverPackageA
- DeletePrinterDriverPackageW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: d7247f4f0ef4d1f77f00664792d0b7b36bc991b19d437017b54db676731ccc70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112551"
---
# <a name="deleteprinterdriverpackage-function"></a>Funzione DeletePrinterDriverPackage

Elimina un pacchetto driver della stampante dall'archivio driver.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DeletePrinterDriverPackage(
  _In_ LPCTSTR pszServer,
  _In_ LPCTSTR pszInfPath,
  _In_ LPCTSTR pszEnvironment
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pszServer* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa costante con terminazione Null che specifica il nome del server di stampa da cui viene eliminato il pacchetto driver. Un **valore del** puntatore NULL indica il computer locale.

</dd> <dt>

*pszInfPath* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa costante con terminazione Null che specifica il percorso del \* file inf del driver.

</dd> <dt>

*pszEnvironment* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa costante con terminazione Null che specifica l'architettura del processore, ad esempio Windows NT x86. Può essere **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

S \_ OK, se l'operazione ha esito positivo.

E \_ ACCESSDENIED, se il pacchetto è stato fornito con Windows.

HRESULT \_ CODE(ERROR \_ PRINT DRIVER PACKAGE IN \_ \_ \_ \_ USE), se il pacchetto è in uso.

In caso **contrario, HRESULT** conterrà un codice di errore.

Per altre informazioni sui codici di errore COM, vedere [Gestione degli errori.](../com/error-handling-in-com.md)

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona che potrebbe non essere restituita immediatamente. La velocità di ritorno di questa funzione dipende da fattori di run-time, ad esempio lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante, difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

L'archivio driver è in genere %windir% \\ inf o %windir% \\ System32 \\ DriverStore \\ FileRepository.

Un pacchetto driver fornito con Windows non può essere rimosso con questa funzione.

L'utente deve disporre dei privilegi di amministrazione della stampante.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Nomi Unicode e ANSI<br/>   | **DeletePrinterDriverPackageW** (Unicode) e **DeletePrinterDriverPackageA** (ANSI)<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> </dl>

 

