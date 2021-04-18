---
description: Unisce due ticket di stampa e restituisce un ticket di stampa valido ed valido.
ms.assetid: 4aa7b9de-abf2-4781-942e-0b992a6bffed
title: MergeAndValidatePrintTicketThunk2 (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MergeAndValidatePrintTicketThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: 4a21b9e505e39d64e8e0c696a3b8a6432a012d76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318363"
---
# <a name="mergeandvalidateprintticketthunk2-function"></a>MergeAndValidatePrintTicketThunk2 (funzione)

\[Questa funzione non è supportata e potrebbe essere disabilitata o eliminata nelle versioni future di Windows. [**PTMergeAndValidatePrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket) fornisce funzionalità equivalenti e deve essere usato in alternativa.\]

Unisce due ticket di stampa e restituisce un ticket di stampa valido ed valido.

## <a name="syntax"></a>Sintassi


```C++
HRESULT MergeAndValidatePrintTicketThunk2(
  _In_      HPTPROVIDER hProvider,
  _In_      BYTE        *pBasePrintTicket,
  _In_      INT         basePrintTicketLength,
  _In_opt_  BYTE        *pDeltaPrintTicket,
  _In_      INT         deltaPrintTicketLength,
  _In_      DWORD       scope,
  _Out_     BYTE        **ppValidatedPrintTicket,
  _Out_     INT         *pValidatedPrintTicketLength,
  _Out_opt_ BSTR        *pbstrErrorMessage
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hProvider* \[ in\]
</dt> <dd>

Handle per un provider di ticket di stampa aperto. Questo handle viene restituito dalla funzione [**BindPTProviderThunk**](bindptproviderthunk.md) .

</dd> <dt>

*pBasePrintTicket* \[ in\]
</dt> <dd>

Buffer che contiene i dati del ticket di stampa di base, espressi in XML come descritto nello [schema di stampa](./printschema.md).

</dd> <dt>

*basePrintTicketLength* \[ in\]
</dt> <dd>

Dimensione, in byte, del buffer a cui fa riferimento *pBasePrintTicket*.

</dd> <dt>

*pDeltaPrintTicket* \[ in, facoltativo\]
</dt> <dd>

Buffer che contiene il ticket di stampa da unire. I dati del ticket di stampa sono espressi in XML come descritto nello [schema di stampa](./printschema.md). Il valore di questo parametro può essere **null**.

</dd> <dt>

*deltaPrintTicketLength* \[ in\]
</dt> <dd>

Dimensione, in byte, del buffer a cui fa riferimento *pDeltaPrintTicket*.

</dd> <dt>

*ambito* \[ in\]
</dt> <dd>

Valore che specifica se l'ambito di *pDeltaPrintTicket* e *ppValidatedPrintTicket* è una singola pagina, un intero documento o tutti i documenti nel processo di stampa. Il valore di questo parametro deve essere un membro dell'enumerazione [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) , di cui è stato eseguito il cast come **DWORD**.

</dd> <dt>

*ppValidatedPrintTicket* \[ out\]
</dt> <dd>

Indirizzo del buffer che contiene il Print Ticket Unito e convalidato. Questa funzione chiama [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) per allocare il buffer. Quando il buffer non è più necessario, il chiamante deve liberarlo chiamando [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

</dd> <dt>

*pValidatedPrintTicketLength* \[ out\]
</dt> <dd>

Dimensione, in byte, del buffer a cui fa riferimento *ppValidatedPrintTicket*.

</dd> <dt>

*pbstrErrorMessage* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una stringa che specifica l'elemento, se presente, non valido sul ticket di stampa in *pBasePrintTicket* o *pDeltaPrintTicket*. Se sono entrambi validi, questo valore è **null**. Se *pbstrErrorMessage* è diverso da **null** quando la funzione restituisce, il chiamante deve liberare la stringa con [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).

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

[**PTMergeAndValidatePrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket)
</dt> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> </dl>

 

