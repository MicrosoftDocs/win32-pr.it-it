---
description: Specifica la modalità di controllo sezionamento. I valori validi sono 0, 1 e 2.
ms.assetid: 5269DB79-639C-4F67-B885-BF1274CDB635
title: Proprietà CODECAPI_AVEncSliceControlMode (codecapit. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0aef928a3938b2f0756d2e84b6836da194823dab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966407"
---
# <a name="codecapi_avencslicecontrolmode-property"></a>Proprietà AVEncSliceControlMode di codecapi \_

Specifica la modalità di controllo sezionamento. I valori validi sono 0, 1 e 2.

## <a name="data-type"></a>Tipo di dati

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncSliceControlMode**

## <a name="property-value"></a>Valore proprietà

Valori della modalità di controllo Slice:



| Valore                                                                        | Significato                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | L'impostazione di questo valore su 0 indica che la proprietà [ \_ AVEncSliceControlSize di codecapis](codecapi-avencslicecontrolsize.md) specificherà le dimensioni delle sezioni in unità di macroblocchi per sezione.<br/>     |
| <dl> <dt>1</dt> </dl> | Impostando questo valore su 1 si indica che la proprietà [ \_ AVEncSliceControlSize di codecapis](codecapi-avencslicecontrolsize.md) specificherà le dimensioni delle sezioni in unità di bit per sezione.<br/>            |
| <dl> <dt>2</dt> </dl> | Impostando questo valore su 2 si indica che la proprietà [ \_ AVEncSliceControlSize di codecapis](codecapi-avencslicecontrolsize.md) specificherà le dimensioni delle sezioni in unità di macroblocco righe per sezione.<br/> |



 

Il codificatore restituisce i valori supportati.

## <a name="remarks"></a>Commenti

**Codificatori H. 264/AVC:**

È consigliabile che il codificatore supporti [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)e [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).

Se [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) non viene chiamato per codecapis \_ AVEncSliceControlMode, [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) per codecapis \_ AVENCSLICECONTROLMODE può restituire **VFW \_ E \_ codecapi \_ senza \_ \_ valore corrente**. [**GetDefaultValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getdefaultvalue) può restituire **VFW \_ E \_ codecapi \_ non per \_ impostazione predefinita** per codecapis \_ AVEncSliceControlMode.

Il valore predefinito consigliato è 2 (dimensione in MB di riga per sezione).

Si tratta di un'API statica, che significa che l'applicazione ha vinto la modifica quando il codificatore è in esecuzione.

## <a name="examples"></a>Esempio


```C++
if (pCodecAPI->IsSupported(&CODECAPI_AVEncSliceControlMode) == S_OK) {                
     VARIANT var;
     var.vt = VT_UI4;
     var.ulVal =ulSliceMode;
     pCodecAPI->SetValue(&CODECAPI_AVEncSliceControlMode, &var);
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App \[ desktop di Windows 8.1 app \| UWP\]<br/>                                   |
| Server minimo supportato<br/> | App desktop di Windows Server 2012 R2 \[ \| UWP\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Codecapis. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

