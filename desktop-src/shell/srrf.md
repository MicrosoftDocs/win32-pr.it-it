---
description: Flag che limitano l'impostazione o la restituzione dei dati.
title: SRRF (Shlwapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: c9dbffd1-3b3e-4a25-89ee-1666e2812a62
api_name:
- SRRF_RT_REG_NONE
- SRRF_RT_REG_SZ
- SRRF_RT_REG_EXPAND_SZ
- SRRF_RT_REG_BINARY
- SRRF_RT_REG_DWORD
- SRRF_RT_REG_MULTI_SZ
- SRRF_RT_REG_QWORD
- SRRF_RT_DWORD
- SRRF_RT_QWORD
- SRRF_RT_ANY
- SRRF_RM_ANY
- SRRF_RM_NORMAL
- SRRF_RM_SAFE
- SRRF_RM_SAFENETWORK
- SRRF_NOEXPAND
- SRRF_ZEROONFAILURE
- SRRF_NOVIRT
api_type:
- HeaderDef
api_location:
- Shlwapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3ba36b64496413a54e6d8b8b96c16c265367d05c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050172"
---
# <a name="srrf"></a>SRRF

Flag che limitano l'impostazione o la restituzione dei dati.



| Costante/valore                                                                                                                                                                                                                                           | Descrizione                                                                                                                                                                                                            |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SRRF_RT_REG_NONE"></span><span id="srrf_rt_reg_none"></span><dl> <dt>**SRRF \_ RT \_ reg \_ None**</dt> <dt>0x00000001</dt> </dl>                 | Digitare REG \_ None.<br/>                                                                                                                                                                                             |
| <span id="SRRF_RT_REG_SZ"></span><span id="srrf_rt_reg_sz"></span><dl> <dt>**SRRF \_ RT \_ reg \_ SZ**</dt> <dt>0x00000002</dt> </dl>                       | Digitare REG \_ SZ. \_ \_ I tipi reg Expand SZ vengono convertiti automaticamente in reg \_ SZ a meno che non \_ sia specificato il flag SRRF NOEXPAND.<br/>                                                                                     |
| <span id="SRRF_RT_REG_EXPAND_SZ"></span><span id="srrf_rt_reg_expand_sz"></span><dl> <dt>**SRRF \_ RT \_ reg \_ expand \_ SZ**</dt> <dt>0x00000004</dt> </dl> | Digitare REG \_ expand \_ SZ. Se si recupera un valore, è necessario ottenere anche il \_ flag SRRF NOEXPAND oppure [**SHRegGetValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetvaluea) ha esito negativo con un \_ parametro error non valido \_ .<br/>                                     |
| <span id="SRRF_RT_REG_BINARY"></span><span id="srrf_rt_reg_binary"></span><dl> <dt>**SRRF \_ RT \_ reg \_ binario**</dt> <dt>0x00000008</dt> </dl>           | Digitare REG \_ Binary.<br/>                                                                                                                                                                                           |
| <span id="SRRF_RT_REG_DWORD"></span><span id="srrf_rt_reg_dword"></span><dl> <dt>**SRRF \_ RT \_ reg \_ DWORD**</dt> <dt>0x00000010</dt> </dl>              | Digitare REG \_ DWORD.<br/>                                                                                                                                                                                            |
| <span id="SRRF_RT_REG_MULTI_SZ"></span><span id="srrf_rt_reg_multi_sz"></span><dl> <dt>**SRRF \_ RT \_ reg \_ \_ multisz**</dt> <dt>0x00000020</dt> </dl>    | Digitare REG \_ \_ multisz.<br/>                                                                                                                                                                                        |
| <span id="SRRF_RT_REG_QWORD"></span><span id="srrf_rt_reg_qword"></span><dl> <dt>**SRRF \_ RT \_ reg \_ QWORD**</dt> <dt>0x00000040</dt> </dl>              | Digitare REG \_ QWORD.<br/>                                                                                                                                                                                            |
| <span id="SRRF_RT_DWORD"></span><span id="srrf_rt_dword"></span><dl> <dt>**SRRF \_ RT \_ DWORD**</dt> <dt>0x00000018</dt> </dl>                           | REG \_ DWORD e i tipi binari reg a 32 bit \_ . Equivale a SRRF \_ RT \_ reg \_ Binary \| SRRF \_ RT \_ reg reg \_ DWORD. Se si recupera un valore, se i dati binari del valore sono maggiori di 32 bit, non vengono restituiti.<br/> |
| <span id="SRRF_RT_QWORD"></span><span id="srrf_rt_qword"></span><dl> <dt>**SRRF \_ RT \_ QWORD**</dt> <dt>0x00000048</dt> </dl>                           | REG \_ QWORD e i tipi binari reg a 64 bit \_ . Equivale a SRRF \_ RT \_ reg \_ Binary \| SRRF \_ RT \_ reg \_ QWORD. Se si recupera un valore, se i dati binari del valore sono maggiori di 64 bit, non vengono restituiti.<br/> |
| <span id="SRRF_RT_ANY"></span><span id="srrf_rt_any"></span><dl> <dt>**SRRF \_ RT \_ qualsiasi**</dt> <dt>0x0000FFFF</dt> </dl>                                 | Tutti i tipi. Impostare questo flag se non \_ è impostato alcun altro valore RT SRRF.<br/>                                                                                                                                                 |
| <span id="SRRF_RM_ANY"></span><span id="srrf_rm_any"></span><dl> <dt>**SRRF \_ RM \_ any**</dt> <dt>0x00000000</dt> </dl>                                 | Nessuna restrizione in modalità. Si tratta del valore predefinito.<br/>                                                                                                                                                             |
| <span id="SRRF_RM_NORMAL"></span><span id="srrf_rm_normal"></span><dl> <dt>**SRRF \_ 0x00010000 \_ normale RM**</dt> <dt></dt> </dl>                        | Limitare la modalità di avvio del sistema a "avvio normale".<br/>                                                                                                                                                              |
| <span id="SRRF_RM_SAFE"></span><span id="srrf_rm_safe"></span><dl> <dt>**SRRF \_ 0x00020000 \_ Safe RM**</dt> <dt></dt> </dl>                              | Limitare la modalità di avvio del sistema alla "modalità provvisoria".<br/>                                                                                                                                                                |
| <span id="SRRF_RM_SAFENETWORK"></span><span id="srrf_rm_safenetwork"></span><dl> <dt>**SRRF \_ 0x00040000 \_ SAFENETWORK RM**</dt> <dt></dt> </dl>         | Limitare la modalità di avvio del sistema alla "modalità provvisoria con rete".<br/>                                                                                                                                                |
| <span id="SRRF_NOEXPAND"></span><span id="srrf_noexpand"></span><dl> <dt>**SRRF \_ NOEXPAND**</dt> <dt>0x10000000</dt> </dl>                            | Non espandere automaticamente le \_ stringhe di ambiente reg Expand \_ SZ.<br/>                                                                                                                                            |
| <span id="SRRF_ZEROONFAILURE"></span><span id="srrf_zeroonfailure"></span><dl> <dt>**SRRF \_**</dt> <dt>0x20000000</dt> ZEROONFAILURE </dl>             | Se si recupera un valore, se *pvData* non è **null**, impostare il contenuto del buffer *pvData* su tutti gli zeri in caso di errore.<br/>                                                                                        |
| <span id="SRRF_NOVIRT"></span><span id="srrf_novirt"></span><dl> <dt>**SRRF \_**</dt> <dt>0x40000000</dt> NOVIRT </dl>                                  | Quando si recupera un valore, se la chiave richiesta è virtualizzata, non riesce e il file di errore non è stato \_ \_ \_ trovato.<br/>                                                                                                            |



## <a name="remarks"></a>Commenti

Questi valori sono definiti in Shlwapi. h.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Shlwapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SHRegSetValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregsetvalue)
</dt> <dt>

[**SHRegGetValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetvaluea)
</dt> </dl>

 

 




