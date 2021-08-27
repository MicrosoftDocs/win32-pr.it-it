---
description: Carica un elenco di stringhe nell'elenco MRU (Most Recently Used) dal Registro di sistema.
title: Metodo IACLCustomMRU::Initialize
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IACLCustomMRU.Initialize
api_type:
- COM
api_location: ''
ms.assetid: 358921b0-46c4-4428-b0b5-57a44fc3247b
ms.openlocfilehash: 0e0cad5f144a4ce97c648463cfdf31bf1c2ee7da0fb89b5508ce9386dba0f14f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111761"
---
# <a name="iaclcustommruinitialize-method"></a>Metodo IACLCustomMRU::Initialize

Carica un elenco di stringhe nell'elenco MRU (Most Recently Used) dal Registro di sistema.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Initialize(
  [in] LPCWSTR pwszMRURegKey,
  [in] DWORD   dwMax
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pwszMRURegKey* \[ Pollici\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntatore a un buffer contenente la chiave del Registro di sistema contenente le stringhe per l'elenco MRU.

</dd> <dt>

*dwMax* \[ Pollici\]
</dt> <dd>

Tipo: **DWORD**

Numero massimo di voci che possono essere prese da *pwszMRURegKey*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/> |



 

 




