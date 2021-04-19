---
description: Elimina un pacchetto di driver della stampante dall'archivio driver.
ms.assetid: a43a94d1-097e-457c-bce9-d4c434ecfa93
title: Funzione DeletePrinterDriverPackage (winspool. h)
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
ms.openlocfilehash: 54d1cda53795f4feab60e397ce7e38402f22374f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311548"
---
# <a name="deleteprinterdriverpackage-function"></a>DeletePrinterDriverPackage (funzione)

Elimina un pacchetto di driver della stampante dall'archivio driver.

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

*pszServer* \[ in\]
</dt> <dd>

Puntatore a una stringa costante a terminazione null che specifica il nome del server di stampa da cui viene eliminato il pacchetto driver. Un valore di puntatore **null** indica il computer locale.

</dd> <dt>

*pszInfPath* \[ in\]
</dt> <dd>

Puntatore a una stringa costante a terminazione null che specifica il percorso del \* file. inf del driver.

</dd> <dt>

*pszEnvironment* \[ in\]
</dt> <dd>

Puntatore a una stringa costante a terminazione null che specifica l'architettura del processore, ad esempio Windows NT x86. Può essere **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

S \_ OK, se l'operazione ha esito positivo.

E \_ AccessDenied, se il pacchetto è stato fornito con Windows.

\_Codice HRESULT ( \_ \_ \_ pacchetto driver di stampa \_ di errore in \_ uso), se il pacchetto viene usato.

In caso contrario, **HRESULT** conterrà un codice di errore.

Per ulteriori informazioni sui codici di errore COM, vedere [gestione degli errori](../com/error-handling-in-com.md).

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

L'archivio driver è in genere% windir% \\ inf o% windir% \\ system32 \\ DriverStore \\ FileRepository.

Non è possibile rimuovere con questa funzione un pacchetto driver fornito con Windows.

L'utente deve disporre dei privilegi di amministrazione della stampante.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Nomi Unicode e ANSI<br/>   | **DeletePrinterDriverPackageW** (Unicode) e **DeletePrinterDriverPackageA** (ANSI)<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> </dl>

 

