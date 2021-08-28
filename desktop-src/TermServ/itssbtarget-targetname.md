---
title: Proprietà ITsSbTarget TargetName
description: Specifica o recupera il nome della destinazione.
ms.assetid: ba5c3158-b4bc-457f-94ea-adb2e0852129
ms.tgt_platform: multiple
keywords:
- Proprietà TargetName Servizi Desktop remoto
- Proprietà TargetName Servizi Desktop remoto, interfaccia ITsSbTarget
- Interfaccia ITsSbTarget Servizi Desktop remoto proprietà , TargetName
- Proprietà TargetName Servizi Desktop remoto, interfaccia ITsSbTargetEx
- Interfaccia ITsSbTargetEx Servizi Desktop remoto , proprietà TargetName
topic_type:
- apiref
api_name:
- ITsSbTarget.TargetName
- ITsSbTarget.get_TargetName
- ITsSbTarget.put_TargetName
- ITsSbTargetEx.TargetName
- ITsSbTargetEx.get_TargetName
- ITsSbTargetEx.put_TargetName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7da653b581c512e0397bb4c486d7c21d6844d41b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982594"
---
# <a name="itssbtargettargetname-property"></a>Proprietà ITsSbTarget::TargetName

Specifica o recupera il nome della destinazione.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_TargetName(
  [in]          BSTR Val
);

HRESULT get_TargetName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Valore proprietà

Variabile **BSTR** che specifica il nome di destinazione.

## <a name="remarks"></a>Commenti

Questa proprietà era di sola lettura prima di Windows Server 2012.

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

 

 





