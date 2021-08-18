---
description: Apre un'istanza di un provider di ticket di stampa.
ms.assetid: 815cc360-8dcd-4c58-a64d-5d77436a8623
title: Funzione BindPTProviderThunk
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
ms.openlocfilehash: 460728eac742fb96ca122981a5874408e12e6c8eddd36fc901e70874e5e040c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119720231"
---
# <a name="bindptproviderthunk-function"></a>Funzione BindPTProviderThunk

\[Questa funzione non è supportata e potrebbe essere disabilitata o eliminata nelle versioni future di Windows. [**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex) fornisce funzionalità equivalenti e deve essere usato.\]

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

*pszPrinterName* \[ Pollici\]
</dt> <dd>

Nome completo di una coda di stampa.

</dd> <dt>

*maxVersion* \[ Pollici\]
</dt> <dd>

Versione più recente dello [schema di stampa](./printschema.md) supportata dal chiamante.

</dd> <dt>

*prefVersion* \[ Pollici\]
</dt> <dd>

Versione dello schema [di stampa richiesta](./printschema.md) dal chiamante.

</dd> <dt>

*phProvider* \[ Cambio\]
</dt> <dd>

Puntatore a un handle al provider del ticket di stampa.

</dd> <dt>

*usedVersion* \[ Cambio\]
</dt> <dd>

Versione dello schema [di stampa che](./printschema.md) verrà utilizzata dal provider di print ticket.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce **S \_ OK;** in caso contrario, restituisce un **codice di errore HRESULT.** Per altre informazioni sui codici di errore COM, vedere [Gestione degli errori.](../com/error-handling-in-com.md)

## <a name="remarks"></a>Commenti

Prima di chiamare questa funzione, il thread chiamante deve inizializzare COM chiamando [**CoInitializeEx.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)

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

[**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex)
</dt> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> </dl>

 

