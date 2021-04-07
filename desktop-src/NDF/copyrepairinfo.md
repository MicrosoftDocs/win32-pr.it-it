---
title: Funzione CopyRepairInfo (Ndattributils. h)
description: Crea una copia di una struttura RepairInfo.
ms.assetid: a1147ce6-9a90-4a46-8fe4-da3353391a13
keywords:
- CopyRepairInfo funzione NDF
topic_type:
- apiref
api_name:
- CopyRepairInfo
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a24d15ec5a8a69b3c8c40700273ebcb6f32bcfd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964001"
---
# <a name="copyrepairinfo-function"></a>CopyRepairInfo (funzione)

La funzione **CopyRepairInfo** crea una copia di una struttura [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT CopyRepairInfo(
  _Out_       RepairInfo *Dest,
  _In_  const RepairInfo *Source
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Dest* \[ out\]
</dt> <dd>

Tipo: **[**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) \** _

Struttura da aggiornare.

</dd> <dt>

_Source * \[ in\]
</dt> <dd>

Tipo: **const [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) \** _

Struttura esistente da copiare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: _ *HRESULT**

I valori restituiti possibili includono, ma non sono limitati a, quanto segue.



| Codice restituito                                                                                   | Descrizione                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Operazione completata.<br/>                                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Uno o più parametri non sono stati specificati correttamente.<br/>          |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria disponibile insufficiente per completare questa operazione.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                 |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Ndattributils. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)
</dt> </dl>

 

 





