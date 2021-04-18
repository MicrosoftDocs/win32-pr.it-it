---
description: Il metodo seprops imposta le proprietà dell'oggetto di destinazione sullo stato appropriato per l'ora specificata.
ms.assetid: 65e701c9-d3a1-4396-9cba-a7830757701f
title: 'Metodo IPropertySetter:: seprops (qedit. h)'
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
ms.openlocfilehash: 6a36b1735ea5b8261c37bee66ac90b9a186a55f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329621"
---
# <a name="ipropertysettersetprops-method"></a>Metodo IPropertySetter:: seprops

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

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

*PTarget* \[ in\]
</dt> <dd>

Puntatore all'oggetto di destinazione per il quale impostare le proprietà.

</dd> <dt>

*rtNow* \[ in\]
</dt> <dd>

Ora in cui impostare le proprietà, in unità 100-nanosecondi, oppure-1 per impostare le proprietà statiche (quelle che non variano nel tempo).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato da DES per impostare le proprietà su una transizione o un effetto. In genere, un'applicazione non chiamerà questo metodo.

L'oggetto specificato da *PTarget* deve implementare l'interfaccia **IDispatch** .

> [!Note]  
> Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




