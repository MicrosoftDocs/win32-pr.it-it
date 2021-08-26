---
description: Definisce i livelli di multicampionamento a scena intera che il dispositivo può applicare.
ms.assetid: 1a3c1efe-f5b1-47a1-a5f5-ac49d318f3b8
title: D3DMULTISAMPLE_TYPE enumerazione (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMULTISAMPLE_TYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e6173abf04f42b0632441b436706318796a5d0af758928e61dd3f19d30bda881
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027971"
---
# <a name="d3dmultisample_type-enumeration"></a>Enumerazione TYPE D3DMULTISAMPLE \_

Definisce i livelli di multicampionamento a scena intera che il dispositivo può applicare.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DMULTISAMPLE_TYPE { 
  D3DMULTISAMPLE_NONE          = 0,
  D3DMULTISAMPLE_NONMASKABLE   = 1,
  D3DMULTISAMPLE_2_SAMPLES     = 2,
  D3DMULTISAMPLE_3_SAMPLES     = 3,
  D3DMULTISAMPLE_4_SAMPLES     = 4,
  D3DMULTISAMPLE_5_SAMPLES     = 5,
  D3DMULTISAMPLE_6_SAMPLES     = 6,
  D3DMULTISAMPLE_7_SAMPLES     = 7,
  D3DMULTISAMPLE_8_SAMPLES     = 8,
  D3DMULTISAMPLE_9_SAMPLES     = 9,
  D3DMULTISAMPLE_10_SAMPLES    = 10,
  D3DMULTISAMPLE_11_SAMPLES    = 11,
  D3DMULTISAMPLE_12_SAMPLES    = 12,
  D3DMULTISAMPLE_13_SAMPLES    = 13,
  D3DMULTISAMPLE_14_SAMPLES    = 14,
  D3DMULTISAMPLE_15_SAMPLES    = 15,
  D3DMULTISAMPLE_16_SAMPLES    = 16,
  D3DMULTISAMPLE_FORCE_DWORD   = 0xffffffff
} D3DMULTISAMPLE_TYPE, *LPD3DMULTISAMPLE_TYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DMULTISAMPLE_NONE"></span><span id="d3dmultisample_none"></span>**D3DMULTISAMPLE \_ NONE**
</dt> <dd>

Non è disponibile alcun livello di multisampling a scena intera.

</dd> <dt>

<span id="D3DMULTISAMPLE_NONMASKABLE_"></span><span id="d3dmultisample_nonmaskable_"></span>**D3DMULTISAMPLE \_ NON MASCHERABILE** 
</dt> <dd>

Abilita il valore di qualità multicampionamento. Vedere la sezione Osservazioni.

</dd> <dt>

<span id="D3DMULTISAMPLE_2_SAMPLES"></span><span id="d3dmultisample_2_samples"></span>**ESEMPI DI D3DMULTISAMPLE \_ 2 \_**
</dt> <dd>

Livello di multicampionamento a scena intera disponibile.

</dd> <dt>

<span id="D3DMULTISAMPLE_3_SAMPLES"></span><span id="d3dmultisample_3_samples"></span>**ESEMPI DI D3DMULTISAMPLE \_ 3 \_**
</dt> <dd>

Livello di multicampionamento a scena intera disponibile.

</dd> <dt>

<span id="D3DMULTISAMPLE_4_SAMPLES"></span><span id="d3dmultisample_4_samples"></span>**ESEMPI DI D3DMULTISAMPLE \_ 4 \_**
</dt> <dd>

Livello di multicampionamento a scena intera disponibile.

</dd> <dt>

<span id="D3DMULTISAMPLE_5_SAMPLES"></span><span id="d3dmultisample_5_samples"></span>**ESEMPI DI D3DMULTISAMPLE \_ 5 \_**
</dt> <dd>

Livello di multicampionamento a scena intera disponibile.

</dd> <dt>

<span id="D3DMULTISAMPLE_6_SAMPLES"></span><span id="d3dmultisample_6_samples"></span>**ESEMPI DI D3DMULTISAMPLE \_ 6 \_**
</dt> <dd>

Livello di multicampionamento a scena intera disponibile.

</dd> <dt>

<span id="D3DMULTISAMPLE_7_SAMPLES"></span><span id="d3dmultisample_7_samples"></span>**ESEMPI DI D3DMULTISAMPLE \_ 7 \_**
</dt> <dd>

Livello di multicampionamento a scena intera disponibile.

</dd> <dt>

<span id="D3DMULTISAMPLE_8_SAMPLES"></span><span id="d3dmultisample_8_samples"></span>**ESEMPI DI D3DMULTISAMPLE \_ 8 \_**
</dt> <dd>

Livello di multicampionamento a scena intera disponibile.

</dd> <dt>

<span id="D3DMULTISAMPLE_9_SAMPLES"></span><span id="d3dmultisample_9_samples"></span>**ESEMPI DI D3DMULTISAMPLE \_ 9 \_**
</dt> <dd>

Livello di multicampionamento a scena intera disponibile.

</dd> <dt>

<span id="D3DMULTISAMPLE_10_SAMPLES"></span><span id="d3dmultisample_10_samples"></span>**ESEMPI D3DMULTISAMPLE \_ 10 \_**
</dt> <dd>

Livello di multicampionamento a scena intera disponibile.

</dd> <dt>

<span id="D3DMULTISAMPLE_11_SAMPLES"></span><span id="d3dmultisample_11_samples"></span>**ESEMPI DI D3DMULTISAMPLE \_ 11 \_**
</dt> <dd>

Livello di multicampionamento a scena intera disponibile.

</dd> <dt>

<span id="D3DMULTISAMPLE_12_SAMPLES"></span><span id="d3dmultisample_12_samples"></span>**ESEMPI D3DMULTISAMPLE \_ 12 \_**
</dt> <dd>

Livello di multicampionamento a scena intera disponibile.

</dd> <dt>

<span id="D3DMULTISAMPLE_13_SAMPLES"></span><span id="d3dmultisample_13_samples"></span>**ESEMPI D3DMULTISAMPLE \_ 13 \_**
</dt> <dd>

Livello di multicampionamento a scena intera disponibile.

</dd> <dt>

<span id="D3DMULTISAMPLE_14_SAMPLES"></span><span id="d3dmultisample_14_samples"></span>**ESEMPI D3DMULTISAMPLE \_ 14 \_**
</dt> <dd>

Livello di multicampionamento a scena intera disponibile.

</dd> <dt>

<span id="D3DMULTISAMPLE_15_SAMPLES"></span><span id="d3dmultisample_15_samples"></span>**ESEMPI D3DMULTISAMPLE \_ 15 \_**
</dt> <dd>

Livello di multicampionamento a scena intera disponibile.

</dd> <dt>

<span id="D3DMULTISAMPLE_16_SAMPLES"></span><span id="d3dmultisample_16_samples"></span>**ESEMPI DI D3DMULTISAMPLE \_ 16 \_**
</dt> <dd>

Livello di multicampionamento a scena intera disponibile.

</dd> <dt>

<span id="D3DMULTISAMPLE_FORCE_DWORD"></span><span id="d3dmultisample_force_dword"></span>**D3DMULTISAMPLE \_ FORCE \_ DWORD**
</dt> <dd>

Forza la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori consentirebbe a questa enumerazione di compilare a una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Oltre a abilitare il multisampling a scena completa in [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) time, saranno disponibili stati di rendering che attivano e disattivano vari aspetti a livelli con granularità fine.

Il multicampionamento è valido solo in una catena di scambio che viene creata o reimpostata con l'effetto di scambio DISCARD D3DSWAPEFFECT. \_

Il valore di antialiasing multisample può essere impostato con i parametri (o sotto-parametri) nei metodi seguenti.



| Metodo                                                                                             | Parametri                         | Sotto-parametri                     |
|----------------------------------------------------------------------------------------------------|------------------------------------|------------------------------------|
| [**IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype)           | MultiSampleType e pQualityLevels |                                    |
| [**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)                                       | pPresentationParameters            | MultiSampleType e pQualityLevels |
| [**IDirect3DDevice9::CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) | pPresentationParameters            | MultiSampleType e pQualityLevels |
| [**IDirect3DDevice9::CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) | MultiSampleType e pQualityLevels |                                    |
| [**IDirect3DDevice9::CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)               | MultiSampleType e pQualityLevels |                                    |
| [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)                                         | pPresentationParameters            | MultiSampleType e pQualityLevels |



 

Non è consigliabile passare da un tipo multicampionato a un altro per aumentare la qualità dell'antialiasing.

D3DMULTISAMPLE NONE abilita effetti di scambio diversi dall'eliminazione, \_ dal blocco e così via.

Se il dispositivo di visualizzazione supporta il multicampionamento mascherabile (più di un campione per un formato di destinazione di rendering a più campioni e supporto di antialias) o solo multisampling non mascherabile (supporto solo per antialias), il driver per il dispositivo fornisce il numero di livelli di qualità per il tipo di campionamento multiplo D3DMULTISAMPLE \_ NONMASKABLE. Le applicazioni che usano solo il multicampionamento per scopi di antialiasing devono solo eseguire query per il numero di livelli di qualità a più campioni non mascherabili supportati dal driver.

I livelli di qualità supportati dal dispositivo possono essere ottenuti con il parametro pQualityLevels [**di IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype). I livelli di qualità usati dall'applicazione vengono impostati con il parametro MultiSampleQuality [**di IDirect3DDevice9::CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) e [**IDirect3DDevice9::CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget).

Per informazioni sul multicampionamento mascherabile, vedere D3DRS \_ MULTISAMPLEMASK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**PARAMETRI \_ D3DPRESENT**](d3dpresent-parameters.md)
</dt> <dt>

[**D3DSURFACE \_ DESC**](d3dsurface-desc.md)
</dt> </dl>

 

 
