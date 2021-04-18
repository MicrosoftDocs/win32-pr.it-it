---
description: Carica un elenco di stringhe nell'elenco degli ultimi elementi usati (MRU) dal registro di sistema.
title: 'Metodo IACLCustomMRU:: Initialize'
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
ms.openlocfilehash: 768df625cb66c888ddccc85f72de5b8676c20b10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994632"
---
# <a name="iaclcustommruinitialize-method"></a>Metodo IACLCustomMRU:: Initialize

Carica un elenco di stringhe nell'elenco degli ultimi elementi usati (MRU) dal registro di sistema.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Initialize(
  [in] LPCWSTR pwszMRURegKey,
  [in] DWORD   dwMax
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pwszMRURegKey* \[ in\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntatore a un buffer contenente la chiave del registro di sistema contenente le stringhe per l'elenco MRU.

</dd> <dt>

*dwMax* \[ in\]
</dt> <dd>

Tipo: **DWORD**

Numero massimo di voci che possono essere ricavate da *pwszMRURegKey*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |



 

 




