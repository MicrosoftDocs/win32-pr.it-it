---
description: Ottiene tutti gli ID proprietà disponibili in un profilo.
ms.assetid: 9ef2abdd-0b33-4be3-a124-7795f42d5e55
title: Metodo IScanProfile::GetAllPropIDs (Scanprofile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetAllPropIDs
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 7fd54e3e1cd45c3631df9b069ddf3c2e897037efb2870d00946f0a002e12f145
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965780"
---
# <a name="iscanprofilegetallpropids-method"></a>Metodo IScanProfile::GetAllPropIDs

Ottiene tutti gli ID proprietà disponibili in un profilo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetAllPropIDs(
  [in, out] ULONG  *num,
  [out]     PROPID *ppid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*num* \[ in, out\]
</dt> <dd>

Tipo: **ULONG \***

Numero di ID proprietà richiesti o restituiti.

</dd> <dt>

*ppid* \[ Cambio\]
</dt> <dd>

Tipo: **PROPID \***

Puntatore a una matrice di ID di proprietà.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Scanprofile.h</dt> </dl>    |
| Idl<br/>                      | <dl> <dt>Scanprofiles.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IScanProfile**](-wia-iscanprofile.md)
</dt> <dt>

[Schema del profilo di analisi](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




