---
description: La funzione GetPrinterDriver2 recupera i dati del driver per la stampante specificata. Se il driver non è installato nel computer locale, GetPrinterDriver2 lo installa e visualizza qualsiasi interfaccia utente nella finestra specificata.
ms.assetid: 0d482d28-7668-4734-ba71-5b355c18ddec
title: Funzione GetPrinterDriver2 (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriver2
- GetPrinterDriver2W
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: e5217ee8445ce8ccae5f22d7c85a4a88dd33f31a1a714aad4899b539ce4edced
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846011"
---
# <a name="getprinterdriver2-function"></a>Funzione GetPrinterDriver2

La **funzione GetPrinterDriver2** recupera i dati del driver per la stampante specificata. Se il driver non è installato nel computer locale, **GetPrinterDriver2** lo installa e visualizza qualsiasi interfaccia utente nella finestra specificata.

## <a name="syntax"></a>Sintassi


```C++
BOOL GetPrinterDriver2(
  _In_opt_ HWND    hWnd,
  _In_     HANDLE  hPrinter,
  _In_opt_ LPTSTR  pEnvironment,
  _In_     DWORD   Level,
  _Out_    LPBYTE  pDriverInfo,
  _In_     DWORD   cbBuf,
  _Out_    LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hWnd* \[ in, facoltativo\]
</dt> <dd>

Handle della finestra che verrà utilizzata come finestra padre di qualsiasi interfaccia utente, ad esempio una finestra di dialogo, visualizzata dal driver durante l'installazione. Se il valore di questo parametro è **NULL,** l'interfaccia utente del driver verrà comunque visualizzata all'utente durante l'installazione, ma non avrà una finestra padre.

</dd> <dt>

*hPrinter* \[ Pollici\]
</dt> <dd>

Handle per la stampante per cui devono essere recuperati i dati del driver. Usare la [**funzione OpenPrinter**](openprinter.md) [**o AddPrinter**](addprinter.md) per recuperare un handle della stampante.

</dd> <dt>

*pEnvironment* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica l'ambiente, ad esempio Windows x86, Windows IA64 o Windows x64). Se questo parametro è **NULL,** viene usato l'ambiente corrente dell'applicazione chiamante e del computer client (non dell'applicazione di destinazione e del server di stampa).

</dd> <dt>

*Livello* \[ Pollici\]
</dt> <dd>

Struttura del driver della stampante restituita nel buffer *pDriverInfo.* Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                | Significato                                             |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | [**INFORMAZIONI \_ SUL DRIVER \_ 1**](driver-info-1.md)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | [**INFORMAZIONI \_ SUL DRIVER \_ 2**](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | [**INFORMAZIONI \_ SUL DRIVER \_ 3**](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | [**INFORMAZIONI \_ SUL DRIVER \_ 4**](driver-info-4.md)<br/> |
| <span id="5"></span><dl> <dt>**5**</dt> </dl> | [**INFORMAZIONI \_ SUL DRIVER \_ 5**](driver-info-5.md)<br/> |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | [**INFORMAZIONI \_ SUL DRIVER \_ 6**](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <dt>**8**</dt> </dl> | [**INFORMAZIONI \_ SUL DRIVER \_ 8**](driver-info-8.md)<br/> |



 

</dd> <dt>

*pDriverInfo* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer che riceve una struttura contenente informazioni sul driver, come specificato da *Level*. Il buffer deve essere sufficientemente grande da archiviare le stringhe a cui puntano i membri della struttura.

Per determinare le dimensioni del buffer necessarie, chiamare **GetPrinterDriver2** con *cbBuf* impostato su zero. **GetPrinterDriver2** ha esito negativo, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce **ERROR INSUFFICIENT \_ \_ BUFFER** e il *parametro pcbNeeded* restituisce le dimensioni, in byte, del buffer necessario per contenere la matrice di strutture e i relativi dati.

</dd> <dt>

*cbBuf* \[ Pollici\]
</dt> <dd>

Dimensione, in byte, della matrice alla quale *punta pDriverInfo.*

</dd> <dt>

*pcbNeeded* \[ Cambio\]
</dt> <dd>

Puntatore a un valore che riceve il numero di byte copiati se la funzione ha esito positivo o il numero di byte necessari se *cbBuf* è troppo piccolo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero. Per ottenere lo stato restituito, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Commenti

Le strutture [**DRIVER \_ INFO \_ 2**](driver-info-2.md), [**DRIVER INFO \_ \_ 3**](driver-info-3.md), [**DRIVER INFO \_ \_ 4**](driver-info-4.md), [**DRIVER INFO \_ \_ 5**](driver-info-5.md), DRIVER INFO 6 e [**DRIVER INFO \_ \_**](driver-info-8.md) [**\_ \_ 8**](driver-info-6.md)contengono il nome file o il percorso completo e il nome file del driver della stampante nel membro **pDriverPath.** Un'applicazione può usare il percorso e il nome file per caricare un driver della stampante chiamando la [**funzione LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e fornendo il percorso e il nome file come singolo argomento.

La versione ANSI di questa funzione, **GetPrinterDriver2A,** non è supportata e restituisce **ERROR NOT \_ \_ SUPPORTED**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **GetPrinterDriver2W** (Unicode)<br/>                                                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Addprinterdriver**](addprinterdriver.md)
</dt> <dt>

[**INFORMAZIONI \_ SUL DRIVER \_ 1**](driver-info-1.md)
</dt> <dt>

[**INFORMAZIONI \_ SUL DRIVER \_ 2**](driver-info-2.md)
</dt> <dt>

[**INFORMAZIONI \_ SUL DRIVER \_ 3**](driver-info-3.md)
</dt> <dt>

[**INFORMAZIONI \_ SUL DRIVER \_ 4**](driver-info-4.md)
</dt> <dt>

[**INFORMAZIONI \_ SUL DRIVER \_ 5**](driver-info-5.md)
</dt> <dt>

[**INFORMAZIONI \_ SUL DRIVER \_ 6**](driver-info-6.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**Getprinterdriver**](getprinterdriver.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

