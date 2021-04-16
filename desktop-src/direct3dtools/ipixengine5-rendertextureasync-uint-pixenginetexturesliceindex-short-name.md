---
description: Esegue il rendering di una trama in un file e restituisce il risultato al asynchrnously host.
MS-HAID: vspixengine.IPixEngine5\_RenderTextureAsync\_UINT\_PixEngineTextureSliceIndex\_int\_float\_arr4\_float\_arr4\_BSTR\_UINT\_BSTR\_arr\_float\_arr\_UINT\_BSTR\_arr\_BOOL\_arr\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPixEngine5:: RenderTextureAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd16214887514fa348a672c45d5eb85c2df6bca5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521522"
---
# <a name="span-idvspixengineipixengine5_rendertextureasync_uint_pixenginetexturesliceindex_int_float_arr4_float_arr4_bstr_uint_bstr_arr_float_arr_uint_bstr_arr_bool_arr_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5rendertextureasync-method"></a><span id="vspixengine.ipixengine5_rendertextureasync_uint_pixenginetexturesliceindex_int_float_arr4_float_arr4_bstr_uint_bstr_arr_float_arr_uint_bstr_arr_bool_arr_bstr_ipixengine5callbacks_ptr_dword_dword"></span>Metodo IPixEngine5:: RenderTextureAsync

Esegue il rendering di una trama in un file e restituisce il risultato al asynchrnously host.

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
Sostituzione del formato colori.

*inferiore*   

*superiore*   

*shaderFileName*   
Stringa COM contenente il percorso del file shader.

*numFloatShaderVars*   
Numero di variabili shader a virgola mobile

*\_shaderFloatVarName count6*   
Stringhe COM che consono i nomi delle variabili shader a virgola mobile.

*\_shaderFloatVarValue count6*   
Variabili shader a virgola mobile.

*numBoolShaderVars*   
Numero di variabili di shader booleane.

*\_shaderBoolVarName count9*   
Stringhe COM che denominano i nomi delle variabili shader booleane.

*\_shaderBoolVarValue count9*   
Variabili shader booleane.

*renderContentFileName*   
Stringa COM contenente il percorso del file in cui è stata scritta la trama di cui è stato eseguito il rendering.

*callback*   
Indirizzo di un oggetto che fornisce l'interfaccia di callback IPixEngine5.

*requestCookie*   
Un cookie che identifica in modo univoco la richiesta e può essere usato per segnalare l'annullamento.

*progressIntervalMsecs*   
Non usato.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IPixEngine5**](/windows/desktop/direct3dtools/ipixengine5)

 

 
