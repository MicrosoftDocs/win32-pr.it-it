---
description: Imposta il valore delle proprietà figlio specificate nell'oggetto <Properties> elemento di un profilo di analisi.
ms.assetid: 3cf7b723-4004-49e5-b3bd-49a84432ede3
title: 'Metodo IScanProfile:: SetProperty (scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: f8f21891ae0cc5fa8e64fafd4acb9e61334a7279
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752855"
---
# <a name="iscanprofilesetproperty-method"></a>Metodo IScanProfile:: SetProperty

Imposta il valore delle proprietà figlio specificate nell' `<Properties>` elemento di un profilo di analisi.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetProperty(
  [in] ULONG       num,
  [in] PROPID      *pid,
  [in] PROPVARIANT *pvar
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

Puntatore a una matrice di numeri di identificazione delle proprietà da impostare. Ogni valore nella matrice è una [costante di proprietà WIA](-wia-wia-property-constants.md).

</dd> <dt>

_pvar * \[ in\]
</dt> <dd>

Tipo: **[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \** _

Puntatore a una matrice di valori da assegnare alle proprietà.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: _ *HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Ogni valore nella matrice a cui punta il *PID* è una delle [costanti della proprietà WIA](-wia-wia-property-constants.md). È possibile estendere questo sistema di identificazione. Vedere [definizione delle proprietà personalizzate](-wia-defining-custom-properties.md).

Le modifiche apportate a un profilo non vengono salvate su disco fino a quando l'applicazione non chiama il metodo [**IScanProfile:: Save**](-wia-iscanprofile-save.md) .

Se due applicazioni creano oggetti del profilo di analisi dallo stesso file XML e ogni applicazione scrive le modifiche nel relativo oggetto, solo le modifiche apportate dall'applicazione che chiama [**IScanProfile:: Save**](-wia-iscanprofile-save.md) Last vengono salvate su disco.

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

 

 
