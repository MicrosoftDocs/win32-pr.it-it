---
description: Ottiene il GUID della categoria dell'elemento Windows Image Acquisition (WIA) 2.0 a cui è associato il profilo.
ms.assetid: 2c816789-ad66-4b06-9160-7a86289ff373
title: Metodo IScanProfile::GetItem (Scanprofile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetItem
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 5a7f52a2d89bbd35b59febb25528fe493c4b5646afc70251fc19978d6d6265db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451041"
---
# <a name="iscanprofilegetitem-method"></a>Metodo IScanProfile::GetItem

Ottiene il GUID della categoria dell'elemento Windows Image Acquisition (WIA) 2.0 a cui è associato il profilo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetItem(
  [out] GUID *pguidCategory
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pguidCategory* \[ Cambio\]
</dt> <dd>

Tipo: **\* GUID**

Puntatore al GUID della categoria dell'elemento WIA 2.0. Si tratta sempre di una delle costanti ITEM \_ CATEGORY di WIA IPA. \_ \_

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                              |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Scanprofile.h</dt> </dl>    |
| Idl<br/>                      | <dl> <dt>Scanprofiles.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IScanProfile**](-wia-iscanprofile.md)
</dt> <dt>

[Schema del profilo di analisi](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




