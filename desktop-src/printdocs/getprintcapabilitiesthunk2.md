---
description: Recupera le funzionalità delle stampanti formattate in conformità con XML Print Schema.
ms.assetid: 15219c19-b64c-4c51-9357-15a797557693
title: Funzione GetPrintCapabilitiesThunk2
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
ms.openlocfilehash: 55127d15eae41380fd5376ca54589488e255a740a7881042f54bc203873701f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971390"
---
# <a name="getprintcapabilitiesthunk2-function"></a>Funzione GetPrintCapabilitiesThunk2

\[Questa funzione non è supportata e potrebbe essere disabilitata o eliminata nelle versioni future Windows. [**PTGetPrintCapabilities**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities) fornisce funzionalità equivalenti e deve essere usato.\]

Recupera le funzionalità della stampante formattate in conformità con XML [Print Schema.](./printschema.md)

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

*hProvider* \[ Pollici\]
</dt> <dd>

Handle per un provider di ticket di stampa aperto. Questo handle viene restituito dalla [**funzione BindPTProviderThunk.**](bindptproviderthunk.md)

</dd> <dt>

*pPrintTicket* \[ Pollici\]
</dt> <dd>

Buffer che contiene i dati del ticket di stampa, espresso in XML come descritto in [Schema di stampa](./printschema.md).

</dd> <dt>

*cbPrintTicket* \[ Pollici\]
</dt> <dd>

Dimensione, in byte, del buffer a cui fa riferimento *pPrintTicket*.

</dd> <dt>

*ppbPrintCapabilities* \[ Cambio\]
</dt> <dd>

Indirizzo del buffer allocato da questa funzione e contenente le informazioni valide sulle funzionalità di stampa, codificate come XML. Questa funzione chiama [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) per allocare questo buffer. Quando il buffer non è più necessario, il chiamante deve liberarlo chiamando [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

</dd> <dt>

*pcbPrintCapabilitiesLength* \[ Cambio\]
</dt> <dd>

Dimensione, in byte, del buffer a cui fa riferimento *ppbPrintCapabilities.*

</dd> <dt>

*pbstrErrorMessage* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una stringa che specifica l'elemento che, se necessario, non è valido *per pPrintTicket.* Se è valido, questo valore è **NULL.** Se *pbstrErrorMessage* non è **NULL quando** la funzione restituisce , il chiamante deve liberare la stringa con [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce **S \_ OK;** in caso contrario, restituisce un **codice di errore HRESULT.** Per altre informazioni sui codici di errore COM, vedere [Gestione degli errori](../com/error-handling-in-com.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                            |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Prntvpt.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PTGetPrintCapabilities**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities)
</dt> <dt>

[Stampare lo schema](./printschema.md)
</dt> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> </dl>

 

