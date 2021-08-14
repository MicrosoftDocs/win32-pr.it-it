---
description: Aggiunge una voce all'elenco degli elementi usati più di recente.
title: Metodo IACLCustomMRU::AddMRUString
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IACLCustomMRU.AddMRUString
api_type:
- COM
api_location: ''
ms.assetid: d8fb8fa5-452b-45fd-b015-d9bf3d0c642e
ms.openlocfilehash: e5acd71a56ef0dd569315ee924313b10e27e6a4ba7ca75d1dbfa0d1e50932cdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118223595"
---
# <a name="iaclcustommruaddmrustring-method"></a>Metodo IACLCustomMRU::AddMRUString

Aggiunge una voce all'elenco degli elementi usati più di recente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AddMRUString(
  [in] LPCWSTR pwszEntry
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pwszEntry* \[ Pollici\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntatore a un buffer contenente la nuova voce.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/> |



 

 




