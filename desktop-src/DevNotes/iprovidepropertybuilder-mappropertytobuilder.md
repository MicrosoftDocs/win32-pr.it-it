---
description: Controlla se un generatore deve essere associato a una determinata proprietà.
ms.assetid: 8fab2dc2-3549-4559-b704-6783d929274e
title: Metodo IProvidePropertyBuilder::MapPropertyToBuilder
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
ms.openlocfilehash: 35ff9e82164251c4490355bbf0499b7fa690415d388b95f7f9c7fd0e6bd7dd3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001691"
---
# <a name="iprovidepropertybuildermappropertytobuilder-method"></a>Metodo IProvidePropertyBuilder::MapPropertyToBuilder

Controlla se un generatore deve essere associato a una determinata proprietà.

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

*dispid* \[ Pollici\]
</dt> <dd>

DISPID della proprietà in questione.

</dd> <dt>

*pdwCtlBldType* \[ Cambio\]
</dt> <dd>

Generatore di cui eseguire il mapping. Questo parametro può essere una combinazione dei valori seguenti.



| Valore                                                                                                                                                                                                                                                          | Significato                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span id="CTLBLDTYPE_FSTDPROPBUILDER"></span><span id="ctlbldtype_fstdpropbuilder"></span><dl> <dt>**CTLBLDTYPE \_ FSTDPROPBUILDER**</dt> <dt>1</dt> </dl>    | Richiamare un'system builder standard (non supportata in Visual Studio).<br/> |
| <span id="CTLBLDTYPE_FINTERNALBUILDER"></span><span id="ctlbldtype_finternalbuilder"></span><dl> <dt>**CTLBLDTYPE \_ FINTERNALBUILDER**</dt> <dt>2</dt> </dl> | Richiamare un generatore personalizzato.<br/>                                           |
| <span id="CTLBLDTYPE_EDITSOBJDIRECTLY"></span><span id="ctlbldtype_editsobjdirectly"></span><dl> <dt>**CTLBLDTYPE \_ EDITSOBJDIRECTLY**</dt> <dt>4</dt> </dl> | Il compilatore modifica l'oggetto. Si tratta di un comportamento comune.<br/>              |



 

</dd> <dt>

*pbstrGuidBldr* \[ Cambio\]
</dt> <dd>

GUID che identifica il generatore per questa proprietà.

</dd> <dt>

*builderAvailable* \[ out, retval\]
</dt> <dd>

Questo parametro è **TRUE** se questa proprietà supporta attualmente un generatore.

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

 

 




