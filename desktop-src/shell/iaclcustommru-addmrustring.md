---
description: Aggiunge una voce all'elenco MRU (Most Recently Used).
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
ms.openlocfilehash: 300474dde82274c668e52d9fe9910634d0ac904c
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842002"
---
# <a name="iaclcustommruaddmrustring-method"></a>Metodo IACLCustomMRU::AddMRUString

Aggiunge una voce all'elenco MRU (Most Recently Used).

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
| Client minimo supportato<br/> | Solo app desktop di Windows XP \[\]<br/>          |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/> |



 

 




