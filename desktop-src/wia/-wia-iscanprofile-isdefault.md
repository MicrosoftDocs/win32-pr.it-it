---
description: Ottiene un valore che indica se il profilo è il profilo di analisi predefinito di un dispositivo IWiaItem2 associato.
ms.assetid: 32ca3b9f-6235-4eec-aa94-bf20f15a9a16
title: Metodo IScanProfile::IsDefault (Scanprofile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.IsDefault
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 3f763286a6db8430514cd70bc05eb160935e0fdc7ae8b5c452e8c09a113c0af5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882411"
---
# <a name="iscanprofileisdefault-method"></a>Metodo IScanProfile::IsDefault

Ottiene un valore che indica se il profilo è il profilo di analisi predefinito di un [**dispositivo IWiaItem2**](-wia-iwiaitem2.md) associato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsDefault(
  [out] BOOL *pbDefault
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbDefault* \[ Cambio\]
</dt> <dd>

Tipo: **BOOL \***

Puntatore a un **oggetto BOOL.**

<dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**Vero**


</dt> <dd>

Il profilo è l'impostazione predefinita.

</dd> <dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False**


</dt> <dd>

Il profilo non è quello predefinito.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

*pbDefault* è **TRUE** se il profilo contiene un `<Default>` elemento . È **FALSE se** tale elemento non è presente. L'elemento non ha alcun valore.

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

 

 




