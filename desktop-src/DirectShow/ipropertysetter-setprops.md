---
description: Il metodo SetProps imposta le proprietà dell'oggetto di destinazione sullo stato appropriato per l'ora specificata.
ms.assetid: 65e701c9-d3a1-4396-9cba-a7830757701f
title: Metodo IPropertySetter::SetProps (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.SetProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b3b5a1832897b52d21c57e26595b7d66c4fc9a53f2bcbee0090c53d00f8fe832
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767211"
---
# <a name="ipropertysettersetprops-method"></a>Metodo IPropertySetter::SetProps

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `SetProps` metodo imposta le proprietà dell'oggetto di destinazione sullo stato appropriato per l'ora specificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetProps(
  [in] IUnknown       *pTarget,
  [in] REFERENCE_TIME rtNow
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTarget* \[ Pollici\]
</dt> <dd>

Puntatore all'oggetto di destinazione per il quale impostare le proprietà.

</dd> <dt>

*rtNow* \[ Pollici\]
</dt> <dd>

Ora in cui impostare le proprietà, in unità di 100 nanosecondi, oppure -1 per impostare le proprietà statiche (quelle che non variano nel tempo).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato da DES per impostare le proprietà su una transizione o un effetto. In genere un'applicazione non chiama questo metodo.

L'oggetto specificato da *pTarget* deve implementare **l'interfaccia IDispatch.**

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare [Microsoft Windows SDK Update per Windows Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




