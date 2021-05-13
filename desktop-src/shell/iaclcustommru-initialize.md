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
ms.openlocfilehash: 715c6991021070dd132942de0bb18c8b77684860
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841232"
---
# <a name="iaclcustommruinitialize-method"></a>Metodo IACLCustomMRU::Initialize

Carica un elenco di stringhe nell'elenco degli ultimi caratteri usati dal Registro di sistema.

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
| Client minimo supportato<br/> | Solo app desktop di Windows XP \[\]<br/>          |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/> |



 

 




