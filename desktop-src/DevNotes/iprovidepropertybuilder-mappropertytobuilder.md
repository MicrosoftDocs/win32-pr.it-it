---
description: Verifica se un generatore deve essere associato a una particolare proprietà.
ms.assetid: 8fab2dc2-3549-4559-b704-6783d929274e
title: 'Metodo IProvidePropertyBuilder:: MapPropertyToBuilder'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IProvidePropertyBuilder.MapPropertyToBuilder
api_type:
- COM
api_location:
- Vsp.dll
ms.openlocfilehash: 5fa755449bfb97940235fe45f9e299aa828e6faa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325214"
---
# <a name="iprovidepropertybuildermappropertytobuilder-method"></a>Metodo IProvidePropertyBuilder:: MapPropertyToBuilder

Verifica se un generatore deve essere associato a una particolare proprietà.

## <a name="syntax"></a>Sintassi


```C++
void MapPropertyToBuilder(
  [in]          LONG   dispid,
  [out]         DWORD  *pdwCtlBldType,
  [out]         LPBSTR pbstrGuidBldr,
  [out, retval] LPBOOL builderAvailable
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DISPID* \[ in\]
</dt> <dd>

DISPID della proprietà in questione.

</dd> <dt>

*pdwCtlBldType* \[ out\]
</dt> <dd>

Generatore di cui eseguire il mapping. Questo parametro può essere una combinazione dei valori seguenti.



| Valore                                                                                                                                                                                                                                                          | Significato                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span id="CTLBLDTYPE_FSTDPROPBUILDER"></span><span id="ctlbldtype_fstdpropbuilder"></span><dl> <dt>**CTLBLDTYPE \_ FSTDPROPBUILDER**</dt> <dt>1</dt> </dl>    | Richiama un generatore di sistema standard (non supportato in Visual Studio).<br/> |
| <span id="CTLBLDTYPE_FINTERNALBUILDER"></span><span id="ctlbldtype_finternalbuilder"></span><dl> <dt>**CTLBLDTYPE \_ FINTERNALBUILDER**</dt> <dt>2</dt> </dl> | Richiamare un generatore personalizzato.<br/>                                           |
| <span id="CTLBLDTYPE_EDITSOBJDIRECTLY"></span><span id="ctlbldtype_editsobjdirectly"></span><dl> <dt>**CTLBLDTYPE \_ EDITSOBJDIRECTLY**</dt> <dt>4</dt> </dl> | Il compilatore modifica l'oggetto. Si tratta di un comportamento comune.<br/>              |



 

</dd> <dt>

*pbstrGuidBldr* \[ out\]
</dt> <dd>

GUID che identifica il generatore per questa proprietà.

</dd> <dt>

*builderAvailable* \[ out, retval\]
</dt> <dd>

Questo parametro è **true** se questa proprietà supporta attualmente un generatore.

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

 

 




