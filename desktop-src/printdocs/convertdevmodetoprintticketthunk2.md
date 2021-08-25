---
description: Converte una struttura DEVMODE in un print ticket.
ms.assetid: c03371f8-a978-4fb7-82cc-f76a65f3904c
title: Funzione ConvertDevModeToPrintTicketThunk2
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
ms.openlocfilehash: d5aea99e54a43eb35f76c719da885f8d7ae0352d47ecff62b7df38de30410025
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950391"
---
# <a name="convertdevmodetoprintticketthunk2-function"></a>Funzione ConvertDevModeToPrintTicketThunk2

\[Questa funzione non è supportata e potrebbe essere disabilitata o eliminata nelle versioni future di Windows. [**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket) fornisce funzionalità equivalenti e deve essere usato.\]

Converte una [**struttura DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) in un print ticket.

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

*hProvider* \[ Pollici\]
</dt> <dd>

Handle per un provider di ticket di stampa aperto. Questo handle viene restituito dalla [**funzione BindPTProviderThunk.**](bindptproviderthunk.md)

</dd> <dt>

*pDevmode* \[ Pollici\]
</dt> <dd>

Puntatore [**all'oggetto DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) da convertire.

</dd> <dt>

*cbSize* \[ Pollici\]
</dt> <dd>

Dimensione, in byte, [**dell'oggetto DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) passato in *pDevmode.*

</dd> <dt>

*ambito* \[ Pollici\]
</dt> <dd>

Valore che specifica l'ambito di *ppPrintTicket.* Questo valore può specificare una singola pagina, un intero documento o tutti i documenti nel processo di stampa. Il valore di questo parametro deve essere un membro [**dell'enumerazione EPrintTicketScope,**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) di cui viene eseguito il cast come **valore DWORD.**

</dd> <dt>

*ppPrintTicket* \[ Cambio\]
</dt> <dd>

Indirizzo del buffer che contiene un print ticket che rappresenta il [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) passato in *pDevmode.* Questa funzione chiama [**CoTaskMemAlloc per**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) allocare questo buffer. Quando il buffer non è più necessario, il chiamante deve liberarlo chiamando [**CoTaskMemFree.**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)

</dd> <dt>

*pcbPrintTicketLength* \[ Cambio\]
</dt> <dd>

Dimensione, in byte, del ticket di stampa restituito in *ppPrintTicket.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce **S \_ OK;** in caso contrario, restituisce un **codice di errore HRESULT.** Per altre informazioni sui codici di errore COM, vedere [Gestione degli errori.](../com/error-handling-in-com.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                            |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Prntvpt.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Schema di stampa](./printschema.md)
</dt> <dt>

[**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket)
</dt> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> </dl>

 

