---
description: Ignora il numero specificato di elementi durante un'enumerazione degli oggetti IWiaItem2 disponibili.
ms.assetid: 7a5e9e1c-1e6e-4de0-9499-bf89e35c19aa
title: 'Metodo IEnumWiaItem2:: Skip (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Skip
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 7618aad923136a9a32d8b7fb935050fefe07bff1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966844"
---
# <a name="ienumwiaitem2skip-method"></a>Metodo IEnumWiaItem2:: Skip

Ignora il numero specificato di elementi durante un'enumerazione degli oggetti [**IWiaItem2**](-wia-iwiaitem2.md) disponibili.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Skip(
  [in] ULONG cElt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*cElt* \[ in\]
</dt> <dd>

Tipo: **ULONG**

Specifica il numero di elementi da ignorare.

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



 

 




