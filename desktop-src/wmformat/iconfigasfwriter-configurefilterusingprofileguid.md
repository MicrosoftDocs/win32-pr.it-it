---
title: Metodo IConfigAsfWriter ConfigureFilterUsingProfileGuid
description: Il metodo ConfigureFilterUsingProfileGuid configura il filtro per scrivere un file ASF in base al profilo predefinito specificato. (Deprecato).
ms.assetid: 94161ee7-1b74-47af-9d77-568abe6237c3
keywords:
- Metodo ConfigureFilterUsingProfileGuid windows Media Format
- Metodo ConfigureFilterUsingProfileGuid windows Media Format , interfaccia IConfigAsfWriter
- Metodo ConfigureFilterUsingProfileGuid dell'interfaccia IConfigAsfWriter di Windows Media Format
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfileGuid
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f427dc67695ebaca3e3e7502f2f1961b738a8f775ace394948ef445f3ad9a64e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118703087"
---
# <a name="iconfigasfwriterconfigurefilterusingprofileguid-method"></a>Metodo IConfigAsfWriter::ConfigureFilterUsingProfileGuid

Il **metodo ConfigureFilterUsingProfileGuid** configura il filtro per scrivere un file ASF in base al profilo predefinito specificato. (Deprecata)

## <a name="syntax"></a>Sintassi


```C++
HRESULT ConfigureFilterUsingProfileGuid(
  [in] REFGUID guidProfile
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*guidProfile* \[ Pollici\]
</dt> <dd>

**GUID** che identifica un profilo come definito nel file di intestazione Windows Media Format SDK Wmsysprf.h.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** seguenti.



| Codice restituito                                                                                         | Descrizione                             |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Il metodo è riuscito.<br/>        |
| <dl> <dt>**E \_ FAIL**</dt> </dl>              | Il profilo non è valido.<br/>    |
| <dl> <dt>**VFW \_ E \_ STATO \_ ERRATO**</dt> </dl> | Il grafico dei filtri viene arrestato.<br/> |



 

## <a name="remarks"></a>Commenti

A partire dall'SDK Windows Media Format 9 Series, non sono stati definiti nuovi profili di sistema. Con questo metodo è possibile usare solo i GUID del profilo di sistema versione 8 (o precedenti).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

