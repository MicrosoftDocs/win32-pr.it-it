---
title: Funzione CopyRootCauseInfo (Ndattributils.h)
description: Crea una copia di una struttura RootCauseInfo.
ms.assetid: 6bcd1341-657a-40c1-bebd-1c0f780ae337
keywords:
- Funzione CopyRootCauseInfo NDF
topic_type:
- apiref
api_name:
- CopyRootCauseInfo
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98bb09fd9a61da536ddd17a4067838b33d4f86ffb8ee29fb404dc861220a5166
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685831"
---
# <a name="copyrootcauseinfo-function"></a>Funzione CopyRootCauseInfo

La **funzione CopyRootCauseInfo** crea una copia di [**una struttura RootCauseInfo.**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)

## <a name="syntax"></a>Sintassi


```C++
HRESULT CopyRootCauseInfo(
  _Out_       RootCauseInfo *Dest,
  _In_  const RootCauseInfo *Source
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Dest* \[ Cambio\]
</dt> <dd>

Tipo: **[ **RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)\***

Struttura da aggiornare.

</dd> <dt>

*Origine* \[ Pollici\]
</dt> <dd>

Tipo: **const [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) \***

Struttura esistente da copiare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

I possibili valori restituiti includono, ma non solo, quanto segue.



| Codice restituito                                                                                   | Descrizione                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata.<br/>                                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Uno o più parametri non sono stati forniti correttamente.<br/>          |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | La memoria disponibile non è sufficiente per completare questa operazione.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                 |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Ndattributils.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)
</dt> </dl>

 

 





