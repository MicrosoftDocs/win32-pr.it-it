---
description: Ottiene il valore delle proprietà figlio specificate nell'oggetto <Properties> elemento di un profilo di analisi.
ms.assetid: 528b51f5-51e0-4639-965d-ee318eb2187b
title: 'Metodo IScanProfile:: GetProperty (scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 48137e61d88d580ac556220b4e47b949d9e2c242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308261"
---
# <a name="iscanprofilegetproperty-method"></a>Metodo IScanProfile:: GetProperty

Ottiene il valore delle proprietà figlio specificate nell' `<Properties>` elemento di un profilo di analisi.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetProperty(
  [in]  ULONG       num,
  [in]  PROPID      *pid,
  [out] PROPVARIANT *pvar
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

numero di  \[ in\]
</dt> <dd>

Tipo: **ULONG**

Numero di voci nelle matrici a cui punta *PID* e *pvar*.

</dd> <dt>

*PID* \[ in\]
</dt> <dd>

Tipo: **propid \** _

Puntatore a una matrice dei numeri di identificazione delle proprietà da impostare. Ogni valore nella matrice è una [costante di proprietà WIA](-wia-wia-property-constants.md).

</dd> <dt>

_pvar * \[ out\]
</dt> <dd>

Tipo: **[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \** _

Puntatore a una matrice di valori.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: _ *HRESULT**

Restituisce \_ false se uno dei valori di proprietà non è disponibile; in caso contrario, restituisce \_ un codice di errore standard com.

## <a name="remarks"></a>Commenti

Il tipo di ogni valore deve essere dello stesso tipo impostato con la chiamata a [**IScanProfile:: SetProperty**](-wia-iscanprofile-setproperty.md).

Ogni valore nella matrice a cui punta il *PID* è una delle [costanti della proprietà WIA](-wia-wia-property-constants.md). È possibile estendere questo sistema di identificazione. Vedere [definizione delle proprietà personalizzate](-wia-defining-custom-properties.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Scanprofile. h</dt> </dl>    |
| IDL<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IScanProfile**](-wia-iscanprofile.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Schema del profilo di analisi](-wia-scan-profile-schema.md)
</dt> <dt>

[Costanti della proprietà WIA](-wia-wia-property-constants.md)
</dt> <dt>

[Definizione di proprietà personalizzate](-wia-defining-custom-properties.md)
</dt> </dl>

 

 
