---
description: Converte un ticket di stampa in una struttura DEVMODE.
ms.assetid: 3b0a6afd-fa9d-434e-a95f-b051296d4567
title: ConvertPrintTicketToDevModeThunk2 (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertPrintTicketToDevModeThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: cf05ab6739dad09332ebc6746a05f3c40ef32de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057907"
---
# <a name="convertprinttickettodevmodethunk2-function"></a>ConvertPrintTicketToDevModeThunk2 (funzione)

\[Questa funzione non è supportata e potrebbe essere disabilitata o eliminata nelle versioni future di Windows. [**PTConvertPrintTicketToDevMode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode) fornisce funzionalità equivalenti e deve essere usato in alternativa.\]

Converte un ticket di stampa in una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT ConvertPrintTicketToDevModeThunk2(
  _In_      HPTPROVIDER hProvider,
  _In_      BYTE        *pPrintTicket,
  _In_      ULONG       cbSize,
  _In_      INT         baseType,
  _In_      DWORD       scope,
  _Out_     BYTE        **ppDevmode,
  _Out_     ULONG       *pcbDevModeLength,
  _Out_opt_ BSTR        *errMsg
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hProvider* \[ in\]
</dt> <dd>

Handle per un provider di ticket di stampa aperto. Questo handle viene restituito dalla funzione [**BindPTProviderThunk**](bindptproviderthunk.md) .

</dd> <dt>

*pPrintTicket* \[ in\]
</dt> <dd>

Buffer che contiene il ticket di stampa da convertire.

</dd> <dt>

*cbSize* \[ in\]
</dt> <dd>

Dimensione, in byte, del buffer passato in *pPrintTicket*.

</dd> <dt>

*baseType* \[ in\]
</dt> <dd>

Valore che indica se l'oggetto [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) predefinito dell'utente o l'oggetto **DEVMODE** della coda di stampa viene utilizzato per fornire i valori alla **DEVMODE** di output quando *pPrintTicket* non specifica tutte le impostazioni possibili per un oggetto **DEVMODE**. Il valore di questo parametro deve essere un membro dell'enumerazione [**EDefaultDevmodeType**](/windows/win32/api/prntvpt/ne-prntvpt-edefaultdevmodetype) , di cui è stato eseguito il cast come **int**.

</dd> <dt>

*ambito* \[ in\]
</dt> <dd>

Valore che specifica l'ambito di *pPrintTicket*. Questo valore può specificare una singola pagina, un intero documento o tutti i documenti nel processo di stampa. Il valore di questo parametro deve essere un membro dell'enumerazione [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) , di cui è stato eseguito il cast come **DWORD**.

</dd> <dt>

*ppDevmode* \[ out\]
</dt> <dd>

Indirizzo dell'oggetto [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)appena creato. Questa funzione chiama [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) per allocare il buffer. Quando il buffer non è più necessario, il chiamante deve liberarlo chiamando [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

</dd> <dt>

*pcbDevModeLength* \[ out\]
</dt> <dd>

Dimensione, in byte, dell'oggetto [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) restituito in *ppDevmode*.

</dd> <dt>

*errmsg* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una stringa che specifica il valore che, se presente, non è valido per il ticket di stampa in *pPrintTicket*. Se è valido, questo valore è **null**. Se *errmsg* è diverso da **null** quando la funzione restituisce, il chiamante deve liberare la stringa con [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce **S \_ OK**. in caso contrario, restituisce un codice di errore **HRESULT** . Per ulteriori informazioni sui codici di errore COM, vedere [gestione degli errori](../com/error-handling-in-com.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Prntvpt.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa schema](./printschema.md)
</dt> <dt>

[**PTConvertPrintTicketToDevMode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode)
</dt> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> </dl>

 

