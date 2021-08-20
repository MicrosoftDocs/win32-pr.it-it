---
description: Specifica la modalità di controllo sezione. I valori validi sono 0, 1 e 2.
ms.assetid: 5269DB79-639C-4F67-B885-BF1274CDB635
title: CODECAPI_AVEncSliceControlMode proprietà (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8ed749419533e4c8c4cec1e6f977bcfa8586c20d43d27d56a2dd041ab5b0267
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118064772"
---
# <a name="codecapi_avencslicecontrolmode-property"></a>CODECAPI \_ AVEncSliceControlMode - proprietà

Specifica la modalità di controllo sezione. I valori validi sono 0, 1 e 2.

## <a name="data-type"></a>Tipo di dati

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncSliceControlMode**

## <a name="property-value"></a>Valore proprietà

Sezionare i valori della modalità di controllo:



| Valore                                                                        | Significato                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | L'impostazione di questo valore su 0 indica che la proprietà [CODECAPI \_ AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) specifica le dimensioni della sezione in unità di blocchi macro per sezione.<br/>     |
| <dl> <dt>1</dt> </dl> | L'impostazione di questo valore su 1 indica che la proprietà [CODECAPI \_ AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) specifica le dimensioni della sezione in unità di bit per sezione.<br/>            |
| <dl> <dt>2</dt> </dl> | L'impostazione di questo valore su 2 indica che la proprietà [CODECAPI \_ AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) specificherà le dimensioni della sezione in unità di righe del blocco macro per sezione.<br/> |



 

Il codificatore restituisce i valori supportati.

## <a name="remarks"></a>Commenti

**Codificatori H.264/AVC:**

È consigliabile che il codificatore [**supporti GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)e [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).

Se [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) non viene chiamato per CODECAPI \_ AVEncSliceControlMode, [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) per CODECAPI \_ AVEncSliceControlMode può restituire **VFW \_ E \_ CODECAPI \_ NO CURRENT \_ \_ VALUE**. [**GetDefaultValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getdefaultvalue) può restituire **VFW \_ E \_ CODECAPI \_ NO \_ DEFAULT** per CODECAPI \_ AVEncSliceControlMode.

Il valore predefinito consigliato è 2 (dimensioni in MB di riga per sezione).

Si tratta di un'API statica, il che significa che l'applicazione non modificherà questa impostazione mentre il codificatore è in esecuzione.

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
| Client minimo supportato<br/> | \[Windows 8.1 app desktop \| app UWP\]<br/>                                   |
| Server minimo supportato<br/> | Windows Server 2012 App desktop R2 \[ \| per app UWP\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

