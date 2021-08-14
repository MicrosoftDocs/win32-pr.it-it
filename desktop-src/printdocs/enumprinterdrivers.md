---
description: La funzione EnumPrinterDrivers enumera i driver della stampante installati in un server di stampa specificato.
ms.assetid: fa3d8cf4-70bc-4362-833e-e4217ed5d43b
title: Funzione EnumPrinterDrivers (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterDrivers
- EnumPrinterDriversA
- EnumPrinterDriversW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 7be4efb1de46a960508972b00d113c5a27ab57187c1a89475eebcde69f14d978
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117686733"
---
# <a name="enumprinterdrivers-function"></a>Funzione EnumPrinterDrivers

La **funzione EnumPrinterDrivers** enumera i driver della stampante installati in un server di stampa specificato.

## <a name="syntax"></a>Sintassi


```C++
BOOL EnumPrinterDrivers(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDriverInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome del server in cui vengono enumerati i driver della stampante.

Se *pName* è **NULL,** la funzione enumera i driver della stampante locale.

</dd> <dt>

*pEnvironment* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica l'ambiente, ad esempio Windows x86, Windows IA64, Windows x64 o Windows NT R4000. Se questo parametro è **NULL,** la funzione usa l'ambiente corrente del chiamante/client (non del server/destinazione).

Se la *stringa pEnvironment* specifica "all", **EnumPrinterDrivers** enumera i driver della stampante per tutte le piattaforme installate nel server specificato.

</dd> <dt>

*Livello* \[ Pollici\]
</dt> <dd>

Tipo di struttura di informazioni restituito nel buffer *pDriverInfo.* Può essere uno dei seguenti.



| Valore                                                                                                | Significato                                             |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | [**DRIVER \_ INFO \_ 1**](driver-info-1.md)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | [**DRIVER \_ INFO \_ 2**](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | [**INFORMAZIONI \_ DRIVER \_ 3**](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | [**INFORMAZIONI \_ DRIVER \_ 4**](driver-info-4.md)<br/> |
| <span id="5"></span><dl> <dt>**5**</dt> </dl> | [**INFORMAZIONI \_ DRIVER \_ 5**](driver-info-5.md)<br/> |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | [**INFORMAZIONI \_ DRIVER \_ 6**](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <dt>**8**</dt> </dl> | [**INFORMAZIONI \_ DRIVER \_ 8**](driver-info-8.md)<br/> |



 

</dd> <dt>

*pDriverInfo* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer che riceve una matrice di strutture DRIVER \_ \_ \* INFO, come specificato da *Level.* Ogni struttura contiene dati che descrivono un driver della stampante disponibile. Il buffer deve essere sufficientemente grande da ricevere la matrice di strutture e qualsiasi stringa o altri dati a cui puntano i membri della struttura.

Per determinare le dimensioni del buffer necessarie, chiamare **EnumPrinterDrivers** con *cbBuf* impostato su zero. **EnumPrinterDrivers** ha esito negativo, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce ERROR INSUFFICIENT BUFFER e il parametro \_ \_ *pcbNeeded* restituisce le dimensioni, in byte, del buffer necessario per contenere la matrice di strutture e i relativi dati.

</dd> <dt>

*cbBuf* \[ Pollici\]
</dt> <dd>

Dimensione, in byte, del buffer a cui punta *pDriverInfo*

</dd> <dt>

*pcbNeeded* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve il numero di byte copiati nel buffer *pDriverInfo* se la funzione ha esito positivo. Se il buffer è troppo piccolo, la funzione ha esito negativo e la variabile riceve il numero di byte necessari.

</dd> <dt>

*pcReturned* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve il numero di strutture restituite nel buffer *pDriverInfo.* Numero di driver della stampante installati nel server di stampa specificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona che potrebbe non essere restituita immediatamente. La velocità di ritorno di questa funzione dipende da fattori di run-time, ad esempio lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante, difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **EnumPrinterDriversW** (Unicode) ed **EnumPrinterDriversA** (ANSI)<br/>                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Addprinterdriver**](addprinterdriver.md)
</dt> <dt>

[**DRIVER \_ INFO \_ 1**](driver-info-1.md)
</dt> <dt>

[**DRIVER \_ INFO \_ 2**](driver-info-2.md)
</dt> <dt>

[**INFORMAZIONI \_ DRIVER \_ 3**](driver-info-3.md)
</dt> <dt>

[**INFORMAZIONI \_ DRIVER \_ 4**](driver-info-4.md)
</dt> <dt>

[**INFORMAZIONI \_ DRIVER \_ 5**](driver-info-5.md)
</dt> <dt>

[**INFORMAZIONI \_ DRIVER \_ 6**](driver-info-6.md)
</dt> <dt>

[**Getprinterdriver**](getprinterdriver.md)
</dt> </dl>

 

