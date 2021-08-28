---
description: Converte un print ticket in una struttura DEVMODE.
ms.assetid: 3b0a6afd-fa9d-434e-a95f-b051296d4567
title: Funzione ConvertPrintTicketToDevModeThunk2
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
ms.openlocfilehash: e6325ca61d18d571a3a3b346b18f6191b53e43d2ce96799c34a643477123f20c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112681"
---
# <a name="convertprinttickettodevmodethunk2-function"></a>Funzione ConvertPrintTicketToDevModeThunk2

\[Questa funzione non è supportata e potrebbe essere disabilitata o eliminata nelle versioni future di Windows. [**PTConvertPrintTicketToDevMode fornisce**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode) funzionalità equivalenti e deve essere usato.\]

Converte un print ticket in una [**struttura DEVMODE.**](/windows/win32/api/wingdi/ns-wingdi-devmodea)

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

*hProvider* \[ Pollici\]
</dt> <dd>

Handle per un provider di ticket di stampa aperto. Questo handle viene restituito dalla [**funzione BindPTProviderThunk.**](bindptproviderthunk.md)

</dd> <dt>

*pPrintTicket* \[ Pollici\]
</dt> <dd>

Buffer che contiene il print ticket da convertire.

</dd> <dt>

*cbSize* \[ Pollici\]
</dt> <dd>

Dimensione, in byte, del buffer passato in *pPrintTicket.*

</dd> <dt>

*baseType* \[ Pollici\]
</dt> <dd>

Valore che indica se il [**valore DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) predefinito dell'utente o il **valore DEVMODE** predefinito della coda di stampa viene usato per fornire valori all'output **DEVMODE** quando *pPrintTicket* non specifica tutte le possibili impostazioni per **devMODE.** Il valore di questo parametro deve essere un membro [**dell'enumerazione EDefaultDevmodeType,**](/windows/win32/api/prntvpt/ne-prntvpt-edefaultdevmodetype) di cui è stato eseguito il cast come **INT.**

</dd> <dt>

*ambito* \[ Pollici\]
</dt> <dd>

Valore che specifica l'ambito di *pPrintTicket.* Questo valore può specificare una singola pagina, un intero documento o tutti i documenti nel processo di stampa. Il valore di questo parametro deve essere un membro [**dell'enumerazione EPrintTicketScope,**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) di cui viene eseguito il cast come **valore DWORD.**

</dd> <dt>

*ppDevmode* \[ Cambio\]
</dt> <dd>

Indirizzo dell'oggetto [**DEVMODE appena creato.**](/windows/win32/api/wingdi/ns-wingdi-devmodea) Questa funzione chiama [**CoTaskMemAlloc per**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) allocare questo buffer. Quando il buffer non è più necessario, il chiamante deve liberarlo chiamando [**CoTaskMemFree.**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)

</dd> <dt>

*pcbDevModeLength* \[ Cambio\]
</dt> <dd>

Dimensione, in byte, [**dell'oggetto DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) restituito in *ppDevmode.*

</dd> <dt>

*errMsg* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una stringa che specifica quale elemento non è valido per il print ticket in *pPrintTicket.* Se è valido, è **NULL.** Se *errMsg* non è **NULL quando** la funzione restituisce un risultato, il chiamante deve liberare la stringa con [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).

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

[**PTConvertPrintTicketToDevMode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode)
</dt> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> </dl>

 

