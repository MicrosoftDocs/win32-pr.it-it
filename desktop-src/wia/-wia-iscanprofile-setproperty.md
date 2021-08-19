---
description: Imposta il valore delle proprietà figlio specificate nell'oggetto . <Properties> elemento di un profilo di analisi.
ms.assetid: 3cf7b723-4004-49e5-b3bd-49a84432ede3
title: Metodo IScanProfile::SetProperty (Scanprofile.h)
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
ms.openlocfilehash: ba4c7aff5139f1230179299d80065f1b933a6cf2d01d4ca03c045ccbe142c3cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118441427"
---
# <a name="iscanprofilesetproperty-method"></a>Metodo IScanProfile::SetProperty

Imposta il valore delle proprietà figlio specificate `<Properties>` nell'elemento di un profilo di analisi.

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

*num* \[ Pollici\]
</dt> <dd>

Tipo: **ULONG**

Numero di voci nelle matrici a cui *puntano pid* e *pvar*.

</dd> <dt>

*pid* \[ Pollici\]
</dt> <dd>

Tipo: **PROPID \***

Puntatore a una matrice di numeri di identificazione delle proprietà da impostare. Ogni valore nella matrice è una costante [di proprietà WIA](-wia-wia-property-constants.md).

</dd> <dt>

*pvar* \[ Pollici\]
</dt> <dd>

Tipo: **[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)\***

Puntatore a una matrice di valori da assegnare alle proprietà.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Ogni valore nella matrice a cui *punta pid* è una delle costanti [di proprietà WIA](-wia-wia-property-constants.md). È possibile estendere questo sistema di identificazione. Vedere [Definizione di proprietà personalizzate.](-wia-defining-custom-properties.md)

Le modifiche apportate a un profilo non vengono salvate su disco finché l'applicazione non chiama il [**metodo IScanProfile::Save.**](-wia-iscanprofile-save.md)

Se due applicazioni creano oggetti profilo di analisi dallo stesso file XML e ogni applicazione scrive le modifiche nel relativo oggetto , solo le modifiche apportate dall'applicazione che chiama [**IScanProfile::Save**](-wia-iscanprofile-save.md) per ultimo vengono salvate su disco.

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

**Informazioni concettuali**
</dt> <dt>

[Schema del profilo di analisi](-wia-scan-profile-schema.md)
</dt> <dt>

[Costanti delle proprietà WIA](-wia-wia-property-constants.md)
</dt> <dt>

[Definizione di proprietà personalizzate](-wia-defining-custom-properties.md)
</dt> </dl>

 

 
