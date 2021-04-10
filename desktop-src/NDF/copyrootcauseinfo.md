---
title: Funzione CopyRootCauseInfo (Ndattributils. h)
description: Crea una copia di una struttura RootCauseInfo.
ms.assetid: 6bcd1341-657a-40c1-bebd-1c0f780ae337
keywords:
- CopyRootCauseInfo funzione NDF
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
ms.openlocfilehash: 5093d7af6458668a763aa206cacd22a0526aa521
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964002"
---
# <a name="copyrootcauseinfo-function"></a>CopyRootCauseInfo (funzione)

La funzione **CopyRootCauseInfo** crea una copia di una struttura [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT CopyRootCauseInfo(
  _Out_       RootCauseInfo *Dest,
  _In_  const RootCauseInfo *Source
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Dest* \[ out\]
</dt> <dd>

Tipo: **[**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) \** _

Struttura da aggiornare.

</dd> <dt>

_Source * \[ in\]
</dt> <dd>

Tipo: **const [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) \** _

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

[**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)
</dt> </dl>

 

 





