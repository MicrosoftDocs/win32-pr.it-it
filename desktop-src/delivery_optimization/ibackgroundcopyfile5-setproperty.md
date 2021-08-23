---
title: Metodo SetProperty IBackgroundCopyFile5 (Deliveryoptimization.h)
description: Imposta una proprietà generica di un Ottimizzazione recapito trasferimento di file di tipo do.
ms.assetid: 63B6806E-47D6-49B0-9867-628C110540D0
keywords:
- Metodo SetProperty
- Metodo SetProperty, interfaccia IBackgroundCopyFile5
- Interfaccia IBackgroundCopyFile5, metodo SetProperty
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 10da7fff9066ccefe7c356e3577ffffe7b0fc2e89d5fdb3f74611f5621d5b757
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755601"
---
# <a name="ibackgroundcopyfile5setproperty-method"></a>Metodo IBackgroundCopyFile5::SetProperty

Imposta una proprietà generica di un Ottimizzazione recapito trasferimento di file di tipo do.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetProperty(
  [in]  BITS_FILE_PROPERTY_ID    PropertyId,
  [out] BITS_FILE_PROPERTY_VALUE *ProertyValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PropertyId* \[ Pollici\]
</dt> <dd>

Specifica la proprietà da impostare.

</dd> <dt>

*ProertyValue* \[ Cambio\]
</dt> <dd>

Puntatore a un'unione che specifica il valore da impostare. Viene utilizzato il membro di unione appropriato per l'ID proprietà.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, solo app desktop versione 1709 \[\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile5 è definito come 85C1657F-DAFC-40E8-8834-DF18EA25717E<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBackgroundCopyFile5**](ibackgroundcopyfile5.md)
</dt> <dt>

[**IBackgroundCopyFile5.GetProperty**](ibackgroundcopyfile5-getproperty.md)
</dt> </dl>

 

 





