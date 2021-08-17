---
description: Unisce due print ticket e restituisce un ticket di stampa valido e valido.
ms.assetid: 4aa7b9de-abf2-4781-942e-0b992a6bffed
title: Funzione MergeAndValidatePrintTicketThunk2
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
ms.openlocfilehash: 156a242d9aa017cc67106a39db6d86809e0ac6f464566205ead09f69fe1b3b7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118471674"
---
# <a name="mergeandvalidateprintticketthunk2-function"></a>Funzione MergeAndValidatePrintTicketThunk2

\[Questa funzione non è supportata e potrebbe essere disabilitata o eliminata nelle versioni future di Windows. [**PTMergeAndValidatePrintTicket fornisce**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket) funzionalità equivalenti e deve essere usato.\]

Unisce due print ticket e restituisce un ticket di stampa valido e valido.

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

*hProvider* \[ Pollici\]
</dt> <dd>

Handle per un provider di ticket di stampa aperto. Questo handle viene restituito dalla [**funzione BindPTProviderThunk.**](bindptproviderthunk.md)

</dd> <dt>

*pBasePrintTicket* \[ Pollici\]
</dt> <dd>

Buffer che contiene i dati del print ticket di base, espressi in XML come descritto in [Schema di stampa.](./printschema.md)

</dd> <dt>

*basePrintTicketLength* \[ Pollici\]
</dt> <dd>

Dimensione, in byte, del buffer a cui fa riferimento *pBasePrintTicket.*

</dd> <dt>

*pDeltaPrintTicket* \[ in, facoltativo\]
</dt> <dd>

Buffer che contiene il print ticket da unire. I dati del print ticket sono espressi in XML come descritto in [Schema di stampa](./printschema.md). Il valore di questo parametro può essere **NULL.**

</dd> <dt>

*deltaPrintTicketLength* \[ Pollici\]
</dt> <dd>

Dimensione, in byte, del buffer a cui fa riferimento *pDeltaPrintTicket.*

</dd> <dt>

*ambito* \[ Pollici\]
</dt> <dd>

Valore che specifica se l'ambito di *pDeltaPrintTicket* e *ppValidatedPrintTicket* è una singola pagina, un intero documento o tutti i documenti nel processo di stampa. Il valore di questo parametro deve essere un membro [**dell'enumerazione EPrintTicketScope,**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) di cui viene eseguito il cast come **valore DWORD.**

</dd> <dt>

*ppValidatedPrintTicket* \[ Cambio\]
</dt> <dd>

Indirizzo del buffer che contiene il print ticket unito e convalidato. Questa funzione chiama [**CoTaskMemAlloc per**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) allocare questo buffer. Quando il buffer non è più necessario, il chiamante deve liberarlo chiamando [**CoTaskMemFree.**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)

</dd> <dt>

*pValidatedPrintTicketLength* \[ Cambio\]
</dt> <dd>

Dimensione, in byte, del buffer a cui fa riferimento *ppValidatedPrintTicket.*

</dd> <dt>

*pbstrErrorMessage* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una stringa che specifica quale elemento non è valido per il print ticket in *pBasePrintTicket* *o pDeltaPrintTicket.* Se sono entrambi validi, questo valore è **NULL.** Se *pbstrErrorMessage non* è **NULL** quando la funzione viene restituita, il chiamante deve liberare la stringa [**con SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).

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

[**PTMergeAndValidatePrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket)
</dt> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> </dl>

 

