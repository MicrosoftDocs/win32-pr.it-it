---
description: Flag per le opzioni di creazione di superfici e risorse.
ms.assetid: b5026566-89b5-458e-b36d-a55e5f8c10c1
title: DXGI_USAGE (DXGI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e55e99d86201c76fbe2ec229b13b5831d767ff34
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322511"
---
# <a name="dxgi_usage"></a>utilizzo di DXGI \_

Flag per le opzioni di creazione di superfici e risorse.



| Costante/valore                                                                                                                                                                                                                                                                                  | Descrizione                                                                                                                                                                                                                                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_USAGE_BACK_BUFFER"></span><span id="dxgi_usage_back_buffer"></span><dl> <dt>**DXGI \_ \_ \_ Buffer back di utilizzo**</dt> <dt> <<  1L (2 + 4)</dt> </dl>                             | La superficie o la risorsa viene utilizzata come buffer nascosto. Non è necessario passare il **\_ \_ \_ buffer di utilizzo di DXGI** quando si crea una catena di scambio. È tuttavia possibile determinare se una risorsa appartiene a una catena di scambio quando si chiama [**IDXGIResource:: getusage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) e si ottiene il **\_ \_ \_ buffer di utilizzo di DXGI**.<br/> |
| <span id="DXGI_USAGE_DISCARD_ON_PRESENT"></span><span id="dxgi_usage_discard_on_present"></span><dl> <dt>**DXGI \_ Eliminazione dell'utilizzo \_ \_ nel \_**</dt> <dt> <<  1L corrente (5 + 4)</dt> </dl>       | Questo flag è solo per uso interno.<br/>                                                                                                                                                                                                                                                                                  |
| <span id="DXGI_USAGE_READ_ONLY"></span><span id="dxgi_usage_read_only"></span><dl> <dt>**DXGI \_ UTILIZZO \_ di \_ sola lettura**</dt> <dt>1L <<  (4 + 4)</dt> </dl>                                   | Utilizzare la superficie o la risorsa solo per la lettura.<br/>                                                                                                                                                                                                                                                                        |
| <span id="DXGI_USAGE_RENDER_TARGET_OUTPUT"></span><span id="dxgi_usage_render_target_output"></span><dl> <dt>**DXGI \_ \_Output della \_ destinazione \_ di rendering di utilizzo**</dt> <dt> <<  1L (1 + 4)</dt> </dl> | Usare la superficie o la risorsa come destinazione di rendering dell'output.<br/>                                                                                                                                                                                                                                                              |
| <span id="DXGI_USAGE_SHADER_INPUT"></span><span id="dxgi_usage_shader_input"></span><dl> <dt>**DXGI \_ <<  \_ \_ input shader di utilizzo**</dt> <dt>(0 + 4)</dt> </dl>                          | Utilizzare la superficie o la risorsa come input per uno shader.<br/>                                                                                                                                                                                                                                                                 |
| <span id="DXGI_USAGE_SHARED"></span><span id="dxgi_usage_shared"></span><dl> <dt>**DXGI \_ UTILIZZO \_**</dt> <dt> <<  1L condiviso (3 + 4)</dt> </dl>                                             | Condividere la superficie o la risorsa.<br/>                                                                                                                                                                                                                                                                                       |
| <span id="DXGI_USAGE_UNORDERED_ACCESS"></span><span id="dxgi_usage_unordered_access"></span><dl> <dt>**DXGI \_ UTILIZZO di \_ \_ accesso non ordinato**</dt> <dt>1L <<  (6 + 4)</dt> </dl>              | Utilizzare la superficie o la risorsa per l'accesso non ordinato.<br/>                                                                                                                                                                                                                                                                    |



## <a name="remarks"></a>Commenti

Ogni flag viene definito come Unsigned Integer.

``` syntax
#define DXGI_CPU_ACCESS_NONE    ( 0 )
#define DXGI_CPU_ACCESS_DYNAMIC    ( 1 )
#define DXGI_CPU_ACCESS_READ_WRITE    ( 2 )
#define DXGI_CPU_ACCESS_SCRATCH    ( 3 )
#define DXGI_CPU_ACCESS_FIELD        15
#define DXGI_USAGE_SHADER_INPUT             ( 1L << (0 + 4) )
#define DXGI_USAGE_RENDER_TARGET_OUTPUT     ( 1L << (1 + 4) )
#define DXGI_USAGE_BACK_BUFFER              ( 1L << (2 + 4) )
#define DXGI_USAGE_SHARED                   ( 1L << (3 + 4) )
#define DXGI_USAGE_READ_ONLY                ( 1L << (4 + 4) )
#define DXGI_USAGE_DISCARD_ON_PRESENT       ( 1L << (5 + 4) )
#define DXGI_USAGE_UNORDERED_ACCESS         ( 1L << (6 + 4) )
typedef UINT DXGI_USAGE;
```

Queste opzioni dei flag vengono usate in una chiamata al metodo [**IDXGIFactory:: CreateSwapChain**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory-createswapchain), [**IDXGIFactory2:: CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), [**IDXGIFactory2:: CreateSwapChainForCoreWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)o [**IDXGIFactory2:: CreateSwapChainForComposition**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) per descrivere le opzioni di utilizzo della superficie e di accesso alla CPU per il buffer nascosto di una catena di scambio. Non è possibile usare **la \_ \_ condivisione di utilizzo di DXGI**, l' **\_ utilizzo di DXGI \_ scartare \_ sul \_ presente** e i valori di **\_ \_ sola lettura \_** per l'utilizzo di DXGI come input per creare una catena di scambio. Tuttavia, DXGI può impostare **gli \_ \_ scarti di utilizzo di DXGI \_ in \_** caso di utilizzo di DXGI e in **\_ \_ sola lettura \_** per alcuni dei buffer back della catena di scambio per conto dell'applicazione. È possibile chiamare il metodo [**IDXGIResource:: getusage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) per recuperare l'utilizzo di questi buffer back. La catena di scambio supporta solo il valore **\_ None di \_ accesso \_ alla CPU DXGI** nel **campo di \_ accesso alla CPU \_ \_ DXGI** parte di **DXGI \_ Usage**.

Queste opzioni dei flag vengono usate anche dal metodo [**IDXGIDevice:: CreateSurface**](/windows/desktop/api/DXGI/nf-dxgi-idxgidevice-createsurface) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>DXGI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti DXGI](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




