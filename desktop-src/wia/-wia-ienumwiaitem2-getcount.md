---
description: Restituisce il numero di elementi archiviati da questo enumeratore.
ms.assetid: d374ec81-0bd5-4b5d-8002-e3b53476421a
title: 'Metodo IEnumWiaItem2:: GetCount (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.GetCount
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 23c067b8e4da93d678f641890a85e2535b3ca50d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049595"
---
# <a name="ienumwiaitem2getcount-method"></a>Metodo IEnumWiaItem2:: GetCount

Restituisce il numero di elementi archiviati da questo enumeratore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCount(
  [out] ULONG *cElt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*cElt* \[ out\]
</dt> <dd>

Tipo: **ULONG \** _

Riceve un puntatore a un _ *ULONG** che riceve il numero di elementi nell'enumerazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




