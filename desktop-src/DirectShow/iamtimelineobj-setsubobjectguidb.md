---
description: Il metodo SetSubObjectGUIDB specifica il GUID del sottooggetto associato a questo oggetto. Questo metodo equivale a IAMTimelineObj::SetSubObjectGUID, ma accetta un valore BSTR.
ms.assetid: b2523b17-1df3-4be5-8bbb-6b67815f9349
title: Metodo IAMTimelineObj::SetSubObjectGUIDB (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetSubObjectGUIDB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a9bb2f88e1312a3a8640147d9ced7ebc1c2157a0633aeed969f36c43236b6052
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154967"
---
# <a name="iamtimelineobjsetsubobjectguidb-method"></a>Metodo IAMTimelineObj::SetSubObjectGUIDB

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il `SetSubObjectGUIDB` metodo specifica il GUID del sottooggetto associato a questo oggetto. Questo metodo equivale a [**IAMTimelineObj::SetSubObjectGUID,**](iamtimelineobj-setsubobjectguid.md) ma accetta un **valore BSTR.**

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetSubObjectGUIDB(
   BSTR newVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*newVal* 
</dt> <dd>

**BSTR** che rappresenta il GUID del sottooggetto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S OK in caso di esito positivo o un \_ **valore HRESULT** che indica la causa dell'errore.

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare l'aggiornamento di Microsoft Windows SDK per Windows [Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IAMTimelineObj**](iamtimelineobj.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




