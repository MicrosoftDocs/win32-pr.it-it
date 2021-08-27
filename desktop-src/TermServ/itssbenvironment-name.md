---
title: Proprietà ITsSbEnvironment Name
description: Recupera un valore che indica il nome dell'ambiente che ospita il computer di destinazione.
ms.assetid: 8104bdae-f445-425b-b326-cc3333839d29
ms.tgt_platform: multiple
keywords:
- Proprietà Name Servizi Desktop remoto
- Proprietà Name Servizi Desktop remoto, interfaccia ITsSbEnvironment
- Interfaccia ITsSbEnvironment Servizi Desktop remoto proprietà , Name
topic_type:
- apiref
api_name:
- ITsSbEnvironment.Name
- ITsSbEnvironment.get_Name
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d60f64cf8bc350ca80072b2c7a43ecabf2fbe5d4650188b7d5a5e5c05a4fbc7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072201"
---
# <a name="itssbenvironmentname-property"></a>Proprietà ITsSbEnvironment::Name

Recupera un valore che indica il nome dell'ambiente che ospita il computer di destinazione.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Name(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Valore proprietà

Puntatore a una **variabile BSTR** che contiene il nome dell'ambiente.

## <a name="remarks"></a>Commenti

Questo metodo restituisce una stringa che non viene usata direttamente da Connessione Desktop remoto Broker (Gestore connessione Desktop remoto). Gestore connessione Desktop remoto passa questa stringa ai plug-in delle risorse.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                            |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                       |
| Idl<br/>                      | <dl> <dt>Sbtsv.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITsSbEnvironment**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment)
</dt> </dl>

 

 





