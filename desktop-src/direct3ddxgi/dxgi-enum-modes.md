---
description: Opzioni per l'enumerazione delle modalità di visualizzazione.
ms.assetid: 7e0f5629-f8e2-478b-b8eb-00780a3dcf1f
title: DXGI_ENUM_MODES (DXGI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056ad959f0b86fb6f357d690f2daab908275e038
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322524"
---
# <a name="dxgi_enum_modes"></a>\_modalità di enumerazione DXGI \_

Opzioni per l'enumerazione delle modalità di visualizzazione.



| Costante/valore                                                                                                                                                                                                                                                                  | Descrizione                                                                                                                                                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_ENUM_MODES_INTERLACED"></span><span id="dxgi_enum_modes_interlaced"></span><dl> <dt>**DXGI \_ Modalità di enumerazione 1UL \_ \_ interlacciato**</dt> <dt></dt> </dl>                 | Includere le modalità interlacciate.<br/>                                                                                                                                                                                                                                                                                                            |
| <span id="DXGI_ENUM_MODES_SCALING"></span><span id="dxgi_enum_modes_scaling"></span><dl> <dt>**DXGI \_ Modalità di enumerazione con \_ \_ scalabilità**</dt> <dt>2UL</dt> </dl>                          | Includere le modalità di scalabilità estesa.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="DXGI_ENUM_MODES_STEREO"></span><span id="dxgi_enum_modes_stereo"></span><dl> <dt>**DXGI \_ Modalità di enumerazione \_ \_ stereo**</dt> <dt>4UL</dt> </dl>                             | Includere le modalità stereo.<br/> **Direct3D 11:** Questo valore di enumerazione è supportato a partire da Windows 8.<br/>                                                                                                                                                                                                                       |
| <span id="DXGI_ENUM_MODES_DISABLED_STEREO"></span><span id="dxgi_enum_modes_disabled_stereo"></span><dl> <dt>**DXGI \_ \_Modalità enum \_ disabilitate 8UL \_ stereo**</dt> <dt></dt> </dl> | Includere le modalità stereo nascoste perché l'utente ha disattivato lo stereo. Le applicazioni del pannello di controllo possono usare questa opzione per mostrare le funzionalità stereo che sono state disabilitate come parte di un'interfaccia utente che Abilita e Disabilita lo stereo.<br/> **Direct3D 11:** Questo valore di enumerazione è supportato a partire da Windows 8.<br/> |



## <a name="remarks"></a>Commenti

Queste opzioni dei flag vengono usate in [**IDXGIOutput:: GetDisplayModeList**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-getdisplaymodelist) per enumerare le modalità di visualizzazione.

Queste opzioni dei flag vengono usate anche in [**IDXGIOutput1:: GetDisplayModeList1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) per enumerare le modalità di visualizzazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>DXGI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti DXGI](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




