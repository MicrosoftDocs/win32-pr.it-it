---
description: Imposta il profilo di analisi specificato come profilo predefinito.
ms.assetid: c680be8b-88f0-4f7f-b1a3-e12711dba870
title: Metodo IScanProfileMgr::SetDefault (Scanprofilemgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.SetDefault
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: fd7b46241e967e02083c344aa7f3f77a773c72b02ff74b225910788d498fe252
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965790"
---
# <a name="iscanprofilemgrsetdefault-method"></a>Metodo IScanProfileMgr::SetDefault

Imposta il profilo di analisi specificato come profilo predefinito.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetDefault(
  [in] IScanProfile *pScanProfile
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pScanProfile* \[ Pollici\]
</dt> <dd>

Tipo: **[ **IScanProfile**](-wia-iscanprofile.md)\***

Puntatore al profilo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Usare il **metodo IScanProfileMgr::SetDefault** per aggiungere un elemento al profilo o per rimuovere tale elemento dal profilo predefinito `<Default>` precedente del dispositivo.

Usare il [**metodo ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) per modificare il profilo predefinito.

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

 

 




