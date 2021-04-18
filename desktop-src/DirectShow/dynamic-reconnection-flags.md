---
description: I flag seguenti specificano il livello di riconnessione dinamica da usare durante il rendering.
ms.assetid: 5e9d5f11-6716-4539-96fd-a0b37036555b
title: Flag di riconnessione dinamica (qedit. h)
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
ms.openlocfilehash: 322c7d88cd84857ba0ebc1d19ed76a24e11cc3fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326927"
---
# <a name="dynamic-reconnection-flags"></a>Flag di riconnessione dinamica

\[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

I flag seguenti specificano il livello di riconnessione dinamica da usare durante il rendering.



| Costante/valore                                                                                                                                                                                                                                            | Descrizione                                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| <span id="CONNECTF_DYNAMIC_NONE"></span><span id="connectf_dynamic_none"></span><dl> <dt>**CONNECTF \_ \_Nessuno dinamico**</dt> <dt>0x00</dt> </dl>          | Nessuna riconnessione dinamica. Caricare tutti gli elementi prima di eseguire il rendering del progetto.<br/> |
| <span id="CONNECTF_DYNAMIC_SOURCES"></span><span id="connectf_dynamic_sources"></span><dl> <dt>**CONNECTF \_ \_Origini dinamiche**</dt> <dt>0x01</dt> </dl> | Caricare le origini solo se necessario.<br/>                                           |
| <span id="CONNECTF_DYNAMIC_EFFECTS"></span><span id="connectf_dynamic_effects"></span><dl> <dt>**CONNECTF \_ \_Effetti dinamici**</dt> <dt>0x02</dt> </dl> | Riservato. Non usare.<br/>                                                  |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Qedit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IRenderEngine::SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md)
</dt> </dl>

 

 




