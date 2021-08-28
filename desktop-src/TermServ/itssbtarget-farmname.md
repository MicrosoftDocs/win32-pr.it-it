---
title: Proprietà ITsSbTarget FarmName
description: Recupera o specifica il nome della farm a cui è unita questa destinazione.
ms.assetid: 83e168ae-f985-40f9-912b-496c0695f82a
ms.tgt_platform: multiple
keywords:
- Proprietà FarmName Servizi Desktop remoto
- Proprietà FarmName Servizi Desktop remoto, interfaccia ITsSbTarget
- Interfaccia ITsSbTarget Servizi Desktop remoto proprietà , FarmName
- Proprietà FarmName Servizi Desktop remoto, interfaccia ITsSbTargetEx
- Interfaccia ITsSbTargetEx Servizi Desktop remoto proprietà , FarmName
topic_type:
- apiref
api_name:
- ITsSbTarget.FarmName
- ITsSbTarget.get_FarmName
- ITsSbTarget.put_FarmName
- ITsSbTargetEx.FarmName
- ITsSbTargetEx.get_FarmName
- ITsSbTargetEx.put_FarmName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0b1c36a1a44f38dac11a7e474d7fefb80a09948
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988294"
---
# <a name="itssbtargetfarmname-property"></a>Proprietà ITsSbTarget::FarmName

Recupera o specifica il nome della farm a cui è unita questa destinazione.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_FarmName(
  [in]          BSTR Val
);

HRESULT get_FarmName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Valore proprietà

Variabile **BSTR** che contiene il nome della farm.

## <a name="requirements"></a>Requisiti




| Requisito | Valore |
|--------|-------|
| Client minimo supportato<br /> | Nessuno supportato<br /> | 
| Server minimo supportato<br /> | Windows Server 2012<br /> | 
| IDL<br /> | <dl><dt>Sbtsv.idl</dt></dl> | 
| IID<br /> | IID_ITsSbTarget è definito come:<ul><li>16616ECC-272D-411D-B324-126893033856</li><li>e85e10ea-db0b-4752-b456-5fd5840901c0 in Windows Server 2008 R2</li></ul> | 




## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITsSbTargetEx**](itssbtargetex.md)
</dt> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





