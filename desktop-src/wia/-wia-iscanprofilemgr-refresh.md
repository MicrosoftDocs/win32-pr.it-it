---
description: Enumera nuovamente tutti i profili di analisi nel sistema.
ms.assetid: f5e49645-e81a-4750-8ea5-f0c698a61752
title: Metodo IScanProfileMgr::Refresh (Scanprofilemgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.Refresh
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 5bb343d310be3aa352c4777275c231f6264d6d25fe5ad88cde559995da915aa9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208944"
---
# <a name="iscanprofilemgrrefresh-method"></a>Metodo IScanProfileMgr::Refresh

Enumera nuovamente tutti i profili di analisi nel sistema.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Refresh();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Usare questo metodo quando più oggetti [**IScanProfileMgr**](-wia-iscanprofilemgr.md) potrebbero creare o eliminare profili contemporaneamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                              |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Scanprofilemgr.h</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Scanprofiles.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IScanProfileMgr**](-wia-iscanprofilemgr.md)
</dt> <dt>

[Schema del profilo di analisi](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




