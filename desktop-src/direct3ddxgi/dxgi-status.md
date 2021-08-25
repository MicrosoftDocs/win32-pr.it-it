---
description: Codici di stato che possono essere restituiti dalle funzioni DXGI.
ms.assetid: dd7480b4-8218-4716-ab9f-74a9955b8aa7
title: DXGI_STATUS (DXGI.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2151c2c209feb630dfe445af2f5afc9d20048c08872fc73f9f5388abc5abb4b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951231"
---
# <a name="dxgi_status"></a>STATO \_ DXGI

Codici di stato che possono essere restituiti dalle funzioni DXGI.



| Costante/valore                                                                                                                                                                                                                                                                                      | Descrizione                                                                                                                                                                                                                                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_STATUS_OCCLUDED"></span><span id="dxgi_status_occluded"></span><dl> <dt>**DXGI \_ STATO \_ OCCLUDED**</dt> <dt>0x087A0001</dt> </dl>                                                 | Il contenuto della finestra non è visibile. Quando si riceve questo stato, un'applicazione può arrestare il rendering e usare DXGI \_ PRESENT \_ TEST per determinare quando riprendere il rendering. Se si usa una catena di scambio di modelli di inversione, non si riceverà LO \_ \_ STATO DXGI OCCLUDED.<br/>                                                                                                                           |
| <span id="DXGI_STATUS_MODE_CHANGED"></span><span id="dxgi_status_mode_changed"></span><dl> <dt>**DXGI \_ MODALITÀ \_ DI STATO MODIFICATA \_ 0x087A0007**</dt> <dt></dt> </dl>                                    | La modalità di visualizzazione del desktop è stata modificata e potrebbe essere presente una conversione/estensione del colore. L'applicazione deve chiamare [**IDXGISwapChain::ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) in modo che corrisponda alla nuova modalità di visualizzazione.<br/>                                                                       |
| <span id="DXGI_STATUS_MODE_CHANGE_IN_PROGRESS"></span><span id="dxgi_status_mode_change_in_progress"></span><dl> <dt>**DXGI \_ MODIFICA \_ DELLA MODALITÀ DI STATO \_ \_ \_ IN**</dt> CORSO <dt>0X087A0008</dt> </dl> | [**IDXGISwapChain::ResizeTarget**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizetarget) e [**IDXGISwapChain::SetFullscreenState**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate) restituiranno DXGI STATUS MODE CHANGE IN PROGRESS se si verifica una transizione in modalità schermo \_ \_ \_ \_ intero/finestra quando viene chiamata una delle \_ DUE API.<br/> |



## <a name="remarks"></a>Commenti

Il **valore HRESULT** per ogni **valore DXGI \_ STATUS** è determinato da questa macro definita in DXGItype.h:


```
#define _FACDXGI    0x87a
#define MAKE_DXGI_STATUS(code)  MAKE_HRESULT(0, _FACDXGI, code)
```



Ad esempio, **DXGI \_ STATUS \_ OCCLUDED** è definito **come 0x087A0001**:


```
#define DXGI_STATUS_OCCLUDED                    MAKE_DXGI_STATUS(1)
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>DXGI.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti DXGI](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




