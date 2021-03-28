---
description: Aggiunge una voce all'elenco degli ultimi elementi usati (MRU).
title: 'Metodo IACLCustomMRU:: AddMRUString'
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
ms.openlocfilehash: d2f444041f466b367f3d4532f65029bcc69c3683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994637"
---
# <a name="iaclcustommruaddmrustring-method"></a>Metodo IACLCustomMRU:: AddMRUString

Aggiunge una voce all'elenco degli ultimi elementi usati (MRU).

## <a name="syntax"></a>Sintassi


```C++
HRESULT AddMRUString(
  [in] LPCWSTR pwszEntry
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pwszEntry* \[ in\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntatore a un buffer contenente la nuova voce.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |



 

 




