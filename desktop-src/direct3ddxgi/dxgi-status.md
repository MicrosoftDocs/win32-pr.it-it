---
description: Codici di stato che possono essere restituiti dalle funzioni DXGI.
ms.assetid: dd7480b4-8218-4716-ab9f-74a9955b8aa7
title: DXGI_STATUS (DXGI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39c402880ccdcbda009402d56127e70a61543d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322513"
---
# <a name="dxgi_status"></a>\_stato DXGI

Codici di stato che possono essere restituiti dalle funzioni DXGI.



| Costante/valore                                                                                                                                                                                                                                                                                      | Descrizione                                                                                                                                                                                                                                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_STATUS_OCCLUDED"></span><span id="dxgi_status_occluded"></span><dl> <dt>**DXGI \_ STATO \_**</dt> bloccato <dt>0x087A0001</dt> </dl>                                                 | Il contenuto della finestra non è visibile. Quando si riceve questo stato, un'applicazione può arrestare il rendering e utilizzare il \_ \_ test di DXGI presente per determinare quando riprendere il rendering. \_ \_ Se si usa una catena di scambio Flip Model, non verrà visualizzato lo stato dxgi.<br/>                                                                                                                           |
| <span id="DXGI_STATUS_MODE_CHANGED"></span><span id="dxgi_status_mode_changed"></span><dl> <dt>**DXGI \_ Modalità di stato \_ \_ modificata**</dt> <dt>0x087A0007</dt> </dl>                                    | La modalità di visualizzazione del desktop è stata modificata. è possibile che si verifichino la conversione o l'allungamento dei colori. L'applicazione deve chiamare [**IDXGISwapChain:: ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) per trovare la corrispondenza con la nuova modalità di visualizzazione.<br/>                                                                       |
| <span id="DXGI_STATUS_MODE_CHANGE_IN_PROGRESS"></span><span id="dxgi_status_mode_change_in_progress"></span><dl> <dt>**DXGI \_ \_ \_ Modifica della modalità \_ di stato in \_ corso**</dt> <dt>0x087A0008</dt> </dl> | [**IDXGISwapChain:: ResizeTarget**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizetarget) e [**IDXGISwapChain:: SetFullscreenState**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate) restituiranno \_ \_ \_ una modifica della modalità \_ di stato DXGI in \_ corso se si verifica una transizione in modalità a schermo intero/con finestra quando viene chiamata una delle API.<br/> |



## <a name="remarks"></a>Commenti

Il valore **HRESULT** per ogni valore di **\_ stato DXGI** è determinato da questa macro definita in DXGItype. h:


```
#define _FACDXGI    0x87a
#define MAKE_DXGI_STATUS(code)  MAKE_HRESULT(0, _FACDXGI, code)
```



**\_ Lo stato DXGI \_** , ad esempio, viene definito come **0x087A0001**:


```
#define DXGI_STATUS_OCCLUDED                    MAKE_DXGI_STATUS(1)
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>DXGI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti DXGI](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




