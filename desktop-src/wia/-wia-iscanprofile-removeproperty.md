---
description: Rimuove un elenco specificato di proprietà figlio nell'oggetto <Properties> elemento di un profilo di analisi.
ms.assetid: 512ccfec-0c95-4abb-98b6-d309e432151b
title: 'Metodo IScanProfile:: RemoveProperty (scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.RemoveProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 1ac1d713ab36da5c35ea7a0d7c523699e7c85b34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130026"
---
# <a name="iscanprofileremoveproperty-method"></a>Metodo IScanProfile:: RemoveProperty

Rimuove un elenco specificato di proprietà figlio nell' `<Properties>` elemento di un profilo di analisi.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RemoveProperty(
  [in] ULONG  num,
  [in] PROPID *pid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

numero di  \[ in\]
</dt> <dd>

Tipo: **ULONG**

Numero di voci nella matrice a cui punta il *PID* .

</dd> <dt>

*PID* \[ in\]
</dt> <dd>

Tipo: **propid \** _

Puntatore a una matrice di numeri di identificazione delle proprietà da eliminare. Ogni è una [costante di proprietà WIA](-wia-wia-property-constants.md).

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

 

 




