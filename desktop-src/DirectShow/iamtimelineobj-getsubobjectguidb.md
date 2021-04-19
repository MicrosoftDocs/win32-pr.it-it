---
description: "Il metodo GetSubObjectGUIDB Recupera il GUID dell'oggetto SubObject associato a questo oggetto sequenza temporale. Questo metodo è equivalente a IAMTimelineObj:: GetSubObjectGUID, ma riceve un valore BSTR."
ms.assetid: 693cafda-78c8-4ba4-90d7-23fedcd1fc52
title: 'Metodo IAMTimelineObj:: GetSubObjectGUIDB (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetSubObjectGUIDB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 903c6638eececd635af2facd964adabe26f0c106
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326555"
---
# <a name="iamtimelineobjgetsubobjectguidb-method"></a>Metodo IAMTimelineObj:: GetSubObjectGUIDB

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `GetSubObjectGUIDB` metodo recupera il GUID dell'oggetto SubObject associato a questo oggetto sequenza temporale. Questo metodo è equivalente a [**IAMTimelineObj:: GetSubObjectGUID**](iamtimelineobj-getsubobjectguid.md), ma riceve un valore **BSTR** .

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSubObjectGUIDB(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pval* \[ out, retval\]
</dt> <dd>

Riceve una stringa che rappresenta il GUID dell'oggetto SubObject.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Il metodo alloca memoria per la stringa. Per liberare la memoria, l'applicazione deve chiamare **SysFreeString** .

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

[**Interfaccia IAMTimelineObj**](iamtimelineobj.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




