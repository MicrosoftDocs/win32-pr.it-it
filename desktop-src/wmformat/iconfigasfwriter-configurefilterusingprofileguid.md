---
title: Metodo IConfigAsfWriter ConfigureFilterUsingProfileGuid
description: Il metodo ConfigureFilterUsingProfileGuid configura il filtro per la scrittura di un file ASF basato sul profilo predefinito specificato. (Deprecato).
ms.assetid: 94161ee7-1b74-47af-9d77-568abe6237c3
keywords:
- Metodo ConfigureFilterUsingProfileGuid Windows Media Format
- Metodo ConfigureFilterUsingProfileGuid Windows Media Format, interfaccia IConfigAsfWriter
- Interfaccia IConfigAsfWriter-formato Windows Media, metodo ConfigureFilterUsingProfileGuid
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfileGuid
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a1521738af4411baa2c11f3d20722e09e2d22a83
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104517025"
---
# <a name="iconfigasfwriterconfigurefilterusingprofileguid-method"></a>Metodo IConfigAsfWriter:: ConfigureFilterUsingProfileGuid

Il metodo **ConfigureFilterUsingProfileGuid** configura il filtro per la scrittura di un file ASF basato sul profilo predefinito specificato. (Deprecata)

## <a name="syntax"></a>Sintassi


```C++
HRESULT ConfigureFilterUsingProfileGuid(
  [in] REFGUID guidProfile
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*guidProfile* \[ in\]
</dt> <dd>

**GUID** che identifica un profilo come definito nel file di intestazione Wmsysprf. h di Windows Media Format SDK.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei seguenti valori **HRESULT** .



| Codice restituito                                                                                         | Descrizione                             |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                | Il metodo è riuscito.<br/>        |
| <dl> <dt>**E \_ non riescono**</dt> </dl>              | Profilo non valido.<br/>    |
| <dl> <dt>**\_ \_ stato non corretto di VFW E \_**</dt> </dl> | Il grafico del filtro è stato arrestato.<br/> |



 

## <a name="remarks"></a>Commenti

A partire da Windows Media Format 9 Series SDK, non sono stati definiti nuovi profili di sistema. Con questo metodo è possibile utilizzare solo i GUID del profilo di sistema versione 8 (o versioni precedenti).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

