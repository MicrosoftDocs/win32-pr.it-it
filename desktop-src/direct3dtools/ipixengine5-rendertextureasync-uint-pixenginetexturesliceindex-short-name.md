---
description: Esegue il rendering di una trama in un file e restituisce il risultato all'host in modo asincrono.
MS-HAID: vspixengine.IPixEngine5\_RenderTextureAsync\_UINT\_PixEngineTextureSliceIndex\_int\_float\_arr4\_float\_arr4\_BSTR\_UINT\_BSTR\_arr\_float\_arr\_UINT\_BSTR\_arr\_BOOL\_arr\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Metodo IPixEngine5::RenderTextureAsync
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 400ade8aa962a73234efbfb710d9ab6b178dfd4e
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626567"
---
# <a name="span-idvspixengineipixengine5_rendertextureasync_uint_pixenginetexturesliceindex_int_float_arr4_float_arr4_bstr_uint_bstr_arr_float_arr_uint_bstr_arr_bool_arr_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5rendertextureasync-method"></a><span id="vspixengine.ipixengine5_rendertextureasync_uint_pixenginetexturesliceindex_int_float_arr4_float_arr4_bstr_uint_bstr_arr_float_arr_uint_bstr_arr_bool_arr_bstr_ipixengine5callbacks_ptr_dword_dword"></span>Metodo IPixEngine5::RenderTextureAsync

Esegue il rendering di una trama in un file e restituisce il risultato all'host in modo asincrono.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RenderTextureAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        formatOverride,
   float [4]                  lower,
   float [4]                  upper,
   BSTR                       shaderFileName,
   UINT                       numFloatShaderVars,
   BSTR []                    count6_shaderFloatVarName,
   float []                   count6_shaderFloatVarValue,
   UINT                       numBoolShaderVars,
   BSTR []                    count9_shaderBoolVarName,
   BOOL []                    count9_shaderBoolVarValue,
   BSTR                       renderContentFileName,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a>Parametri

*textureId*   
ID della trama di cui eseguire il rendering.

*sliceIndex*   
Indice della sezione all'interno della trama di cui eseguire il rendering.

*formatOverride*   
Override del formato colore.

*Inferiore*   

*Superiore*   

*shaderFileName*   
Stringa COM contenente il percorso del file shader.

*numFloatShaderVars*   
Numero di variabili shader a virgola mobile

*count6 \_ shaderFloatVarName*   
Stringhe COM che contino i nomi delle variabili shader a virgola mobile.

*count6 \_ shaderFloatVarValue*   
Variabili di shader a virgola mobile.

*numBoolShaderVars*   
Numero di variabili shader booleane.

*count9 \_ shaderBoolVarName*   
Stringhe COM che contino i nomi delle variabili dello shader booleano.

*count9 \_ shaderBoolVarValue*   
Variabili di shader booleane.

*renderContentFileName*   
Stringa COM contenente il percorso del file in cui è stata scritta la trama sottoposta a rendering.

*Callback*   
Indirizzo di un oggetto che fornisce l'interfaccia di callback IPixEngine5.

*requestCookie*   
Cookie che identifica in modo univoco la richiesta e può essere usato per segnalare l'annullamento.

*progressIntervalMsecs*   
Non usato.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IPixEngine5**](/windows/desktop/direct3dtools/ipixengine5)

 

 
