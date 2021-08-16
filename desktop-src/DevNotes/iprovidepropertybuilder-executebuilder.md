---
description: Notifica a un oggetto che deve visualizzare il generatore per la proprietà specificata.
ms.assetid: 4d855aed-aaa1-4cc8-be9d-1175c254a813
title: Metodo IProvidePropertyBuilder::ExecuteBuilder
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IProvidePropertyBuilder.ExecuteBuilder
api_type:
- COM
api_location:
- Vsp.dll
ms.openlocfilehash: 9aef31629cac755d5689de929c02fbc8d9b816bf868a48bd59df3d08c911d9b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117827256"
---
# <a name="iprovidepropertybuilderexecutebuilder-method"></a>Metodo IProvidePropertyBuilder::ExecuteBuilder

Notifica a un oggetto che deve visualizzare il generatore per la proprietà specificata.

## <a name="syntax"></a>Sintassi


```C++
void ExecuteBuilder(
  [in]          LONG      dispid,
  [in]          BSTR      bstrGuidBldr,
  [in]          IDispatch *pdispApp,
  [in]          LONG_PTR  hwndBldrOwner,
  [in, out]     LPVARIANT pvarValue,
  [out, retval] LPBOOL    pbActionCommitted
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dispid* \[ Pollici\]
</dt> <dd>

DISPID della proprietà per cui viene visualizzato il generatore.

</dd> <dt>

*bstrGuidBldr* \[ Pollici\]
</dt> <dd>

Valore **BSTR** del GUID del generatore da richiamare. Viene restituito da [**MapToPropertyBuilder.**](iprovidepropertybuilder-mappropertytobuilder.md)

</dd> <dt>

*pdispApp* \[ Pollici\]
</dt> <dd>

Impostare su **NULL.**

</dd> <dt>

*hwndBldrOwner* \[ Pollici\]
</dt> <dd>

Handle per la finestra padre del generatore popup.

</dd> <dt>

*pvarValue* \[ in, out\]
</dt> <dd>

Valore corrente della proprietà. Questo valore può essere modificato dall'oggetto e viene modificato nel nuovo valore se *pbActionCommitted* è **TRUE.**

</dd> <dt>

*pbActionCommitted* \[ out, retval\]
</dt> <dd>

Valore che indica se il generatore ha eseguito un'azione sull'oggetto . Può essere usato quando un utente modifica un elemento e quindi preme OK nella finestra di dialogo generatore popup.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Vsp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IProvidePropertyBuilder**](iprovidepropertybuilder.md)
</dt> </dl>

 

 




