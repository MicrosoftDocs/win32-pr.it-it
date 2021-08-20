---
description: I flag seguenti specificano il livello di riconnessione dinamica da usare durante il rendering.
ms.assetid: 5e9d5f11-6716-4539-96fd-a0b37036555b
title: Flag di riconnessione dinamica (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CONNECTF_DYNAMIC_NONE
- CONNECTF_DYNAMIC_SOURCES
- CONNECTF_DYNAMIC_EFFECTS
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: f7bd2ff28c0928c59c632df501e6545b50707cfd948dd57e4ff1bd1cf01d1721
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966241"
---
# <a name="dynamic-reconnection-flags"></a>Flag di riconnessione dinamica

\[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

I flag seguenti specificano il livello di riconnessione dinamica da usare durante il rendering.



| Costante/valore                                                                                                                                                                                                                                            | Descrizione                                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| <span id="CONNECTF_DYNAMIC_NONE"></span><span id="connectf_dynamic_none"></span><dl> <dt>**CONNECTF \_ DYNAMIC \_ NONE**</dt> <dt>0x00</dt> </dl>          | Nessuna riconnessione dinamica. Caricare tutti gli elementi prima di eseguire il rendering del progetto.<br/> |
| <span id="CONNECTF_DYNAMIC_SOURCES"></span><span id="connectf_dynamic_sources"></span><dl> <dt>**CONNECTF \_ ORIGINI \_ DINAMICHE**</dt> <dt>0x01</dt> </dl> | Caricare le origini solo in base alle esigenze.<br/>                                           |
| <span id="CONNECTF_DYNAMIC_EFFECTS"></span><span id="connectf_dynamic_effects"></span><dl> <dt>**CONNECTF \_ EFFETTI \_ DINAMICI**</dt> <dt>0x02</dt> </dl> | Riservato. Non usare.<br/>                                                  |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Qedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IRenderEngine::SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md)
</dt> </dl>

 

 




