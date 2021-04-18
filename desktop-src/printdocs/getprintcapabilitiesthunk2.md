---
description: Recupera le funzionalità di stampanti formattate in conformità con lo schema di stampa XML.
ms.assetid: 15219c19-b64c-4c51-9357-15a797557693
title: GetPrintCapabilitiesThunk2 (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrintCapabilitiesThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: eb60f1cdabad6287e236fc099fc304e9e7de83ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313022"
---
# <a name="getprintcapabilitiesthunk2-function"></a>GetPrintCapabilitiesThunk2 (funzione)

\[Questa funzione non è supportata e potrebbe essere disabilitata o eliminata nelle versioni future di Windows. [**PTGetPrintCapabilities**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities) fornisce funzionalità equivalenti e deve essere usato in alternativa.\]

Recupera le funzionalità della stampante formattate in conformità con lo [schema di stampa](./printschema.md)XML.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetPrintCapabilitiesThunk2(
  _In_      HPTPROVIDER hProvider,
  _In_      BYTE        *pPrintTicket,
  _In_      INT         cbPrintTicket,
  _Out_     BYTE        **ppbPrintCapabilities,
  _Out_     INT         *pcbPrintCapabilitiesLength,
  _Out_opt_ BSTR        *pbstrErrorMessage
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

Buffer che contiene i dati del ticket di stampa, espressi in XML come descritto nello [schema di stampa](./printschema.md).

</dd> <dt>

*cbPrintTicket* \[ in\]
</dt> <dd>

Dimensione, in byte, del buffer a cui fa riferimento *pPrintTicket*.

</dd> <dt>

*ppbPrintCapabilities* \[ out\]
</dt> <dd>

Indirizzo del buffer allocato da questa funzione e contenente le informazioni sulle funzionalità di stampa valide, codificate in formato XML. Questa funzione chiama [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) per allocare il buffer. Quando il buffer non è più necessario, il chiamante deve liberarlo chiamando [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

</dd> <dt>

*pcbPrintCapabilitiesLength* \[ out\]
</dt> <dd>

Dimensione, in byte, del buffer a cui fa riferimento *ppbPrintCapabilities*.

</dd> <dt>

*pbstrErrorMessage* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una stringa che specifica l'elemento, se presente, non valido per *pPrintTicket*. Se è valido, questo valore è **null**. Se *pbstrErrorMessage* è diverso da **null** quando la funzione restituisce, il chiamante deve liberare la stringa con [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).

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

[**PTGetPrintCapabilities**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities)
</dt> <dt>

[Stampa schema](./printschema.md)
</dt> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> </dl>

 

