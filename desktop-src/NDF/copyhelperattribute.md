---
title: Funzione CopyHelperAttribute (Ndattributils. h)
description: Crea una copia di una struttura dell' \_ attributo helper.
ms.assetid: ff49be29-4cd8-4730-929f-c66a7325704f
keywords:
- CopyHelperAttribute funzione NDF
topic_type:
- apiref
api_name:
- CopyHelperAttribute
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59fac3449ee48659980681c836d24406c4db7e2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301362"
---
# <a name="copyhelperattribute-function"></a>CopyHelperAttribute (funzione)

La funzione **CopyHelperAttribute** crea una copia di una struttura dell' [**\_ attributo Helper**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT CopyHelperAttribute(
  _Out_       HELPER_ATTRIBUTE *Dest,
  _In_  const HELPER_ATTRIBUTE *Source
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Dest* \[ out\]
</dt> <dd>

Tipo: **\* [**\_ attributo Helper**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)* _

Struttura da aggiornare.

</dd> <dt>

_Source * \[ in\]
</dt> <dd>

Tipo: **\* [**\_ attributo Helper**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)const* _

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

[**Helper ( \_ attributo)**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)
</dt> </dl>

 

 





