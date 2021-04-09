---
title: Proprietà Name di ITsSbEnvironment
description: Recupera un valore che indica il nome dell'ambiente che ospita il computer di destinazione.
ms.assetid: 8104bdae-f445-425b-b326-cc3333839d29
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà nome
- Nome Servizi Desktop remoto proprietà, interfaccia ITsSbEnvironment
- Interfaccia ITsSbEnvironment Servizi Desktop remoto, proprietà Name
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
ms.openlocfilehash: 2b5ac2fd725ec07102c08e93b2bfb39dabe701ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963962"
---
# <a name="itssbenvironmentname-property"></a>Proprietà ITsSbEnvironment:: Name

Recupera un valore che indica il nome dell'ambiente che ospita il computer di destinazione.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Name(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Valore proprietà

Puntatore a una variabile **BSTR** che contiene il nome dell'ambiente.

## <a name="remarks"></a>Commenti

Questo metodo restituisce una stringa non utilizzata direttamente da Connessione Desktop remoto broker (gestore connessione Desktop remoto). Gestore connessione Desktop remoto passa questa stringa ai plug-in delle risorse.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                            |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                       |
| IDL<br/>                      | <dl> <dt>Sbtsv. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITsSbEnvironment**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment)
</dt> </dl>

 

 





