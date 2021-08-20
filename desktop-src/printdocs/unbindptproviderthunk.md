---
description: Chiude un handle a un provider di ticket di stampa.
ms.assetid: ce979c89-9f9d-4e89-b142-beed414caa3f
title: Funzione UnbindPTProviderThunk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UnbindPTProviderThunk
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: e9091360a34a00b7598e50c1b3226d8cc82c82f124602b0308836c61dc8f27ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117685997"
---
# <a name="unbindptproviderthunk-function"></a>Funzione UnbindPTProviderThunk

\[Questa funzione non è supportata e potrebbe essere disabilitata o eliminata nelle versioni future Windows. [**PTCloseProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider) fornisce funzionalità equivalenti e deve essere usato.\]

Chiude un handle a un provider di ticket di stampa.

## <a name="syntax"></a>Sintassi


```C++
HRESULT UnbindPTProviderThunk(
  _In_ HPTPROVIDER hProvider
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hProvider* \[ Pollici\]
</dt> <dd>

Handle per un provider di ticket di stampa aperto. Questo handle viene restituito dalla [**funzione BindPTProviderThunk.**](bindptproviderthunk.md)

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

[Stampare lo schema](./printschema.md)
</dt> <dt>

[**PTCloseProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider)
</dt> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> </dl>

 

