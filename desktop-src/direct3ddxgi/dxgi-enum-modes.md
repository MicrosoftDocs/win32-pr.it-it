---
description: Opzioni per l'enumerazione delle modalità di visualizzazione.
ms.assetid: 7e0f5629-f8e2-478b-b8eb-00780a3dcf1f
title: DXGI_ENUM_MODES (DXGI.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 568e3919955c2f5612cf88896a2cb6389ebc58fcb427e159824c1dc2feeebca6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025631"
---
# <a name="dxgi_enum_modes"></a>MODALITÀ DI ENUMERAZIONE DXGI \_ \_

Opzioni per l'enumerazione delle modalità di visualizzazione.



| Costante/valore                                                                                                                                                                                                                                                                  | Descrizione                                                                                                                                                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_ENUM_MODES_INTERLACED"></span><span id="dxgi_enum_modes_interlaced"></span><dl> <dt>**DXGI \_ MODALITÀ DI \_ \_ ENUMERAZIONE INTERLACCIATE**</dt> <dt>1UL</dt> </dl>                 | Includere le modalità interlacciate.<br/>                                                                                                                                                                                                                                                                                                            |
| <span id="DXGI_ENUM_MODES_SCALING"></span><span id="dxgi_enum_modes_scaling"></span><dl> <dt>**DXGI \_ ENUM \_ MODES \_ SCALING**</dt> <dt>2UL</dt> </dl>                          | Includere le modalità di scalabilità estesa.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="DXGI_ENUM_MODES_STEREO"></span><span id="dxgi_enum_modes_stereo"></span><dl> <dt>**DXGI \_ MODALITÀ ENUM \_ \_ STEREO**</dt> <dt>4UL</dt> </dl>                             | Includere le modalità stereo.<br/> **Direct3D 11:** Questo valore di enumerazione è supportato a partire da Windows 8.<br/>                                                                                                                                                                                                                       |
| <span id="DXGI_ENUM_MODES_DISABLED_STEREO"></span><span id="dxgi_enum_modes_disabled_stereo"></span><dl> <dt>**DXGI \_ MODALITÀ ENUMERAZIONE \_ \_ DISABILITATE \_ STEREO**</dt> <dt>8UL</dt> </dl> | Includere le modalità stereo nascoste perché l'utente ha disabilitato lo stereo. Le applicazioni del pannello di controllo possono usare questa opzione per visualizzare le funzionalità stereo che sono state disabilitate come parte di un'interfaccia utente che abilita e disabilita lo stereo.<br/> **Direct3D 11:** Questo valore di enumerazione è supportato a partire da Windows 8.<br/> |



## <a name="remarks"></a>Commenti

Queste opzioni flag vengono usate in [**IDXGIOutput::GetDisplayModeList**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-getdisplaymodelist) per enumerare le modalità di visualizzazione.

Queste opzioni flag vengono usate anche in [**IDXGIOutput1::GetDisplayModeList1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) per enumerare le modalità di visualizzazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>DXGI.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti DXGI](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




