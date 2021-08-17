---
description: Flag per le opzioni di creazione di superfici e risorse.
ms.assetid: b5026566-89b5-458e-b36d-a55e5f8c10c1
title: DXGI_USAGE (DXGI.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d7bc0773794c6c2243d8a3171cbd6ffdafbe1cdd558e1198c2c8cc0b1a3440d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117909932"
---
# <a name="dxgi_usage"></a>UTILIZZO \_ DXGI

Flag per le opzioni di creazione di superfici e risorse.



| Costante/valore                                                                                                                                                                                                                                                                                  | Descrizione                                                                                                                                                                                                                                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_USAGE_BACK_BUFFER"></span><span id="dxgi_usage_back_buffer"></span><dl> <dt>**DXGI \_ UTILIZZO \_ BACK \_ BUFFER**</dt> <dt>1L << (2 + 4)</dt> </dl>                             | La superficie o la risorsa viene usata come buffer nascosto. Non è necessario passare **DXGI \_ USAGE BACK \_ \_ BUFFER** quando si crea una catena di scambio. È tuttavia possibile determinare se una risorsa appartiene a una catena di scambio quando si chiama [**IDXGIResource::GetUsage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) e si ottiene **DXGI \_ USAGE BACK \_ \_ BUFFER**.<br/> |
| <span id="DXGI_USAGE_DISCARD_ON_PRESENT"></span><span id="dxgi_usage_discard_on_present"></span><dl> <dt>**DXGI \_ USAGE \_ DISCARD \_ ON \_ PRESENT**</dt> <dt>1L << (5 + 4)</dt> </dl>       | Questo flag è solo per uso interno.<br/>                                                                                                                                                                                                                                                                                  |
| <span id="DXGI_USAGE_READ_ONLY"></span><span id="dxgi_usage_read_only"></span><dl> <dt>**DXGI \_ USAGE \_ READ \_ ONLY**</dt> <dt>1L << (4 + 4)</dt> </dl>                                   | Usare la superficie o la risorsa per la sola lettura.<br/>                                                                                                                                                                                                                                                                        |
| <span id="DXGI_USAGE_RENDER_TARGET_OUTPUT"></span><span id="dxgi_usage_render_target_output"></span><dl> <dt>**DXGI \_ OUTPUT \_ \_ DESTINAZIONE RENDERING \_ UTILIZZO**</dt> <dt>1L << (1 + 4)</dt> </dl> | Usare la superficie o la risorsa come destinazione di rendering di output.<br/>                                                                                                                                                                                                                                                              |
| <span id="DXGI_USAGE_SHADER_INPUT"></span><span id="dxgi_usage_shader_input"></span><dl> <dt>**DXGI \_ INPUT \_ SHADER \_ DI**</dt> UTILIZZO <dt>1L << (0 + 4)</dt> </dl>                          | Usare la superficie o la risorsa come input per uno shader.<br/>                                                                                                                                                                                                                                                                 |
| <span id="DXGI_USAGE_SHARED"></span><span id="dxgi_usage_shared"></span><dl> <dt>**DXGI \_ USAGE \_ SHARED**</dt> <dt>1L << (3 + 4)</dt> </dl>                                             | Condividere la superficie o la risorsa.<br/>                                                                                                                                                                                                                                                                                       |
| <span id="DXGI_USAGE_UNORDERED_ACCESS"></span><span id="dxgi_usage_unordered_access"></span><dl> <dt>**DXGI \_ UTILIZZO \_ ACCESSO NON \_ ORDINATO**</dt> <dt>1L << (6 + 4)</dt> </dl>              | Usare la superficie o la risorsa per l'accesso non ordinato.<br/>                                                                                                                                                                                                                                                                    |



## <a name="remarks"></a>Commenti

Ogni flag è definito come intero senza segno.

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

Queste opzioni flag vengono usate in una chiamata al metodo [**IDXGIFactory::CreateSwapChain,**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory-createswapchain) [**IDXGIFactory2::CreateSwapChainForHwnd,**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd) [**IDXGIFactory2::CreateSwapChainForCoreWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)o [**IDXGIFactory2::CreateSwapChainForComposition**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) per descrivere l'utilizzo della superficie e le opzioni di accesso alla CPU per il buffer nascosto di una catena di scambio. Non è possibile usare i valori **DXGI \_ USAGE \_ SHARED,** **DXGI \_ USAGE DISCARD ON \_ \_ \_ PRESENT** e **DXGI \_ USAGE READ \_ \_ ONLY** come input per creare una catena di scambio. Tuttavia, DXGI può impostare **DXGI \_ USAGE DISCARD ON \_ \_ \_ PRESENT** e **DXGI \_ USAGE READ \_ \_ ONLY** per alcuni buffer back della catena di scambio per conto dell'applicazione. È possibile chiamare il [**metodo IDXGIResource::GetUsage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) per recuperare l'utilizzo di questi buffer nascosto. La catena di scambio supporta solo il valore **DXGI \_ CPU \_ ACCESS \_ NONE** nella parte **DXGI \_ CPU ACCESS \_ \_ FIELD** di **DXGI \_ USAGE**.

Queste opzioni di flag vengono usate anche dal [**metodo IDXGIDevice::CreateSurface.**](/windows/desktop/api/DXGI/nf-dxgi-idxgidevice-createsurface)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>DXGI.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti DXGI](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




