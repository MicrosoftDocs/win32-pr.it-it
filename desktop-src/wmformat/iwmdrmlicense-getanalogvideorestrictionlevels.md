---
title: Metodo IWMDRMLicense GetAnalogVideoRestrictionLevels (wmdrmsdk. h)
description: Il metodo GetAnalogVideoRestrictionLevels recupera tutte le restrizioni video analogiche impostate per la licenza corrente.
ms.assetid: cf0ac7c0-236d-4d60-8850-81dc6754cf01
keywords:
- Metodo GetAnalogVideoRestrictionLevels Windows Media Format
- Metodo GetAnalogVideoRestrictionLevels Windows Media Format, interfaccia IWMDRMLicense
- Interfaccia IWMDRMLicense-formato Windows Media, metodo GetAnalogVideoRestrictionLevels
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetAnalogVideoRestrictionLevels
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a168f25381b807cc8c0cd17f7ba6764c3591513
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328529"
---
# <a name="iwmdrmlicensegetanalogvideorestrictionlevels-method"></a>Metodo IWMDRMLicense:: GetAnalogVideoRestrictionLevels

Il metodo **GetAnalogVideoRestrictionLevels** recupera tutte le restrizioni video analogiche impostate per la licenza corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetAnalogVideoRestrictionLevels(
  [out]     WMDRM_ANALOG_VIDEO_RESTRICTIONS rgAnalogVideoRestrictions[],
  [in, out] DWORD                           *pcRestrictions
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*\[ rgAnalogVideoRestrictions \]* in \[ uscita\]
</dt> <dd>

Riceve una matrice di strutture di [**\_ \_ \_ restrizioni video analogiche WMDRM**](wmdrm-analog-video-restrictions.md) . Impostare su **null** per ottenere il numero di elementi nella matrice in *pcResctrictions*.

</dd> <dt>

*pcRestrictions* \[ in uscita\]
</dt> <dd>

Numero di elementi nella matrice di restrizioni. Se *rgAnalogVideoRestrictions* è impostato su **null**, questo valore viene impostato sul numero di elementi necessari nella matrice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

È necessario allocare memoria per la matrice di restrizioni. A tale scopo, chiamare prima il metodo con *rgAnalogVideoRestrictions* impostato su **null**, impostando il valore su *pcRestrictions* sul numero di elementi necessari.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





