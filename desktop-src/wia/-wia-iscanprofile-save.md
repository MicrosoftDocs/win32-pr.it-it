---
description: Salva le modifiche apportate a un profilo su disco.
ms.assetid: e844bd4c-93c3-44a3-b7d5-0beb71c9fa17
title: Metodo IScanProfile::Save (Scanprofile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.Save
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 7cf4201a0d149c7b529e595d7f2c2ea92a6010f6cffd3e6c5c74fb3cdc040651
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450921"
---
# <a name="iscanprofilesave-method"></a>Metodo IScanProfile::Save

Salva le modifiche apportate a un profilo su disco.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Save();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Un profilo di analisi salvato è un file XML archiviato in %USERPROFILE% \\ Application Data Microsoft Document Center \\ \\ \\ UserScanProfiles.

Se più di un processo scrive nell'oggetto [**IScanProfile,**](-wia-iscanprofile.md) quello che chiama **IScanProfile::Save** last è l'unico processo le cui modifiche vengono salvate.

Il **metodo IScanProfile::Save** convalida il profilo prima del salvataggio. Il profilo viene sempre considerato valido a meno che la categoria dell'elemento Windows wia (WIA) 2.0 associato al profilo non sia WIA CATEGORY FLATBED o \_ \_ WIA \_ CATEGORY \_ FEEDER. Se la categoria è WIA CATEGORY FLATBED o WIA CATEGORY FEEDER, le proprietà seguenti devono essere valide per l'elemento, se le proprietà sono \_ \_ \_ \_ contenute nel profilo:

LUMINOSITÀ \_ DI WIA IPS \_

CONTRASTO \_ DI IP WIA \_

TIPO \_ DI DATI IPA DI WIA \_

WIA \_ IPS \_ XRES

FORMATO \_ IPA WIA \_

Inoltre, se la categoria è WIA CATEGORY FEEDER, la proprietà WIA IPS PAGE SIZE deve essere valida, se presente \_ \_ nel \_ \_ \_ profilo. Per altre informazioni su queste proprietà, vedere Costanti delle proprietà [**degli elementi WIA dello scanner.**](-wia-wiaitempropscanneritem.md)

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

 

 




