---
description: Converte una struttura DEVMODE in un Print Ticket.
ms.assetid: c03371f8-a978-4fb7-82cc-f76a65f3904c
title: ConvertDevModeToPrintTicketThunk2 (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertDevModeToPrintTicketThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: f13d597a11a4d6cfd1ad6f5d70b3a386560f5106
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311556"
---
# <a name="convertdevmodetoprintticketthunk2-function"></a>ConvertDevModeToPrintTicketThunk2 (funzione)

\[Questa funzione non è supportata e potrebbe essere disabilitata o eliminata nelle versioni future di Windows. [**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket) fornisce funzionalità equivalenti e deve essere usato in alternativa.\]

Converte una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) in un Print Ticket.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ConvertDevModeToPrintTicketThunk2(
  _In_  HPTPROVIDER hProvider,
  _In_  BYTE        *pDevmode,
  _In_  ULONG       cbSize,
  _In_  DWORD       scope,
  _Out_ BYTE        **ppPrintTicket,
  _Out_ INT         *pcbPrintTicketLength
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hProvider* \[ in\]
</dt> <dd>

Handle per un provider di ticket di stampa aperto. Questo handle viene restituito dalla funzione [**BindPTProviderThunk**](bindptproviderthunk.md) .

</dd> <dt>

*pDevmode* \[ in\]
</dt> <dd>

Puntatore alla [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) da convertire.

</dd> <dt>

*cbSize* \[ in\]
</dt> <dd>

Dimensione, in byte, del [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) passato in *pDevmode*.

</dd> <dt>

*ambito* \[ in\]
</dt> <dd>

Valore che specifica l'ambito di *ppPrintTicket*. Questo valore può specificare una singola pagina, un intero documento o tutti i documenti nel processo di stampa. Il valore di questo parametro deve essere un membro dell'enumerazione [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) , di cui è stato eseguito il cast come **DWORD**.

</dd> <dt>

*ppPrintTicket* \[ out\]
</dt> <dd>

Indirizzo del buffer contenente un ticket di stampa che rappresenta l'oggetto [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) passato in *pDevmode*. Questa funzione chiama [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) per allocare il buffer. Quando il buffer non è più necessario, il chiamante deve liberarlo chiamando [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

</dd> <dt>

*pcbPrintTicketLength* \[ out\]
</dt> <dd>

Dimensione, in byte, del ticket di stampa restituito in *ppPrintTicket*.

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

[**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket)
</dt> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> </dl>

 

