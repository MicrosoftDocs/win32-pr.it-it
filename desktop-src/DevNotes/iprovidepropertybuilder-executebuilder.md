---
description: Notifica a un oggetto che deve visualizzare il relativo generatore per la proprietà specificata.
ms.assetid: 4d855aed-aaa1-4cc8-be9d-1175c254a813
title: 'Metodo IProvidePropertyBuilder:: ExecuteBuilder'
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
ms.openlocfilehash: c37c2a4ca1003bd701ea141f1723f4ca16aa69c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325215"
---
# <a name="iprovidepropertybuilderexecutebuilder-method"></a>Metodo IProvidePropertyBuilder:: ExecuteBuilder

Notifica a un oggetto che deve visualizzare il relativo generatore per la proprietà specificata.

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

*DISPID* \[ in\]
</dt> <dd>

DISPID della proprietà per la quale viene visualizzato il generatore.

</dd> <dt>

*bstrGuidBldr* \[ in\]
</dt> <dd>

**BSTR** del GUID del generatore da richiamare. Questa operazione viene restituita da [**MapToPropertyBuilder**](iprovidepropertybuilder-mappropertytobuilder.md).

</dd> <dt>

*pdispApp* \[ in\]
</dt> <dd>

Impostare su **null**.

</dd> <dt>

*hwndBldrOwner* \[ in\]
</dt> <dd>

Handle per la finestra del generatore popup padre.

</dd> <dt>

*pvarValue* \[ in uscita\]
</dt> <dd>

Valore corrente della proprietà. Questo valore può essere modificato dall'oggetto e modificato nel nuovo valore se *pbActionCommitted* è **true**.

</dd> <dt>

*pbActionCommitted* \[ out, retval\]
</dt> <dd>

Valore che indica se il generatore ha eseguito un'azione sull'oggetto. Può essere usato quando un utente modifica qualcosa, quindi preme OK nella finestra di dialogo Generatore popup.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Vsp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IProvidePropertyBuilder**](iprovidepropertybuilder.md)
</dt> </dl>

 

 




