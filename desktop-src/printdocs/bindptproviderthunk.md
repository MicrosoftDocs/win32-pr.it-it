---
description: Apre un'istanza di un provider di ticket di stampa.
ms.assetid: 815cc360-8dcd-4c58-a64d-5d77436a8623
title: BindPTProviderThunk (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BindPTProviderThunk
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: bf63fc6faf9d47993fafb97c8d3a1c18d6d6c985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227358"
---
# <a name="bindptproviderthunk-function"></a>BindPTProviderThunk (funzione)

\[Questa funzione non è supportata e potrebbe essere disabilitata o eliminata nelle versioni future di Windows. [**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex) fornisce funzionalità equivalenti e deve essere usato in alternativa.\]

Apre un'istanza di un provider di ticket di stampa.

## <a name="syntax"></a>Sintassi


```C++
HRESULT BindPTProviderThunk(
  _In_  LPTSTR      pszPrinterName,
  _In_  INT         maxVersion,
  _In_  INT         prefVersion,
  _Out_ HPTPROVIDER *phProvider,
  _Out_ INT         *usedVersion
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pszPrinterName* \[ in\]
</dt> <dd>

Nome completo di una coda di stampa.

</dd> <dt>

*MaxVersion* \[ in\]
</dt> <dd>

Versione più recente dello [schema di stampa](./printschema.md) supportato dal chiamante.

</dd> <dt>

*prefVersion* \[ in\]
</dt> <dd>

Versione dello schema di [stampa](./printschema.md) richiesta dal chiamante.

</dd> <dt>

*phProvider* \[ out\]
</dt> <dd>

Puntatore a un handle per il provider del ticket di stampa.

</dd> <dt>

*usedVersion* \[ out\]
</dt> <dd>

Versione dello schema di [stampa](./printschema.md) che userà il provider del ticket di stampa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce **S \_ OK**. in caso contrario, restituisce un codice di errore **HRESULT** . Per ulteriori informazioni sui codici di errore COM, vedere [gestione degli errori](../com/error-handling-in-com.md).

## <a name="remarks"></a>Commenti

Prima di chiamare questa funzione, il thread chiamante deve inizializzare COM chiamando [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex).

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

[**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex)
</dt> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> </dl>

 

