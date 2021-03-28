---
description: Questi tipi di dati possono essere utilizzati per specificare il tipo di un valore del registro di sistema.
title: Tipi di dati del registro di sistema (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4185e7af-e1f0-40af-91c7-0ff7e27896ae
api_name:
- REG_BINARY
- REG_DWORD
- REG_QWORD
- REG_DWORD_LITTLE_ENDIAN
- REG_QWORD_LITTLE_ENDIAN
- REG_DWORD_BIG_ENDIAN
- REG_EXPAND_SZ
- REG_LINK
- REG_MULTI_SZ
- REG_NONE
- REG_RESOURCE_LIST
- REG_SZ
api_type:
- HeaderDef
api_location:
- Winnt.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4de4595b55716d58df04a598dd6ba298f22829d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "104996593"
---
# <a name="registry-data-types"></a>Tipi di dati del registro di sistema

Questi tipi di dati possono essere utilizzati per specificare il tipo di un valore del registro di sistema.



| Costante                                                                                                                                                                                      | Descrizione                                                                                                                                                                                                                                                                                                                  |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_BINARY"></span><span id="reg_binary"></span><dl> <dt>**REG \_ binario**</dt> </dl>                                          | Dati binari in qualsiasi forma.<br/>                                                                                                                                                                                                                                                                                          |
| <span id="REG_DWORD"></span><span id="reg_dword"></span><dl> <dt>**REG \_ DWORD**</dt> </dl>                                             | numero a 32 bit.<br/>                                                                                                                                                                                                                                                                                                    |
| <span id="REG_QWORD"></span><span id="reg_qword"></span><dl> <dt>**REG \_ QWORD**</dt> </dl>                                             | numero a 64 bit.<br/>                                                                                                                                                                                                                                                                                                    |
| <span id="REG_DWORD_LITTLE_ENDIAN"></span><span id="reg_dword_little_endian"></span><dl> <dt>**\_ \_ Little Endian reg \_ DWORD**</dt> </dl> | numero a 32 bit in formato little-endian. Equivale a **reg \_ DWORD**.<br/> In formato little-endian, un valore multibyte viene archiviato in memoria dal byte più basso, ovvero "estremità minima", al byte più alto. Il valore 0x12345678., ad esempio, viene archiviato come (0x78 0x56 0x34 0x12) in formato little-endian.<br/> |
| <span id="REG_QWORD_LITTLE_ENDIAN"></span><span id="reg_qword_little_endian"></span><dl> <dt>**REG \_ QWORD \_ Little \_ endian**</dt> </dl> | Numero a 64 bit in formato little-endian. Equivale a **reg \_ QWORD**. <br/>                                                                                                                                                                                                                                   |
| <span id="REG_DWORD_BIG_ENDIAN"></span><span id="reg_dword_big_endian"></span><dl> <dt>**REG \_ DWORD \_ Big \_ endian**</dt> </dl>          | numero a 32 bit nel formato big-endian.<br/> Nel formato big-endian, un valore multibyte viene archiviato in memoria dal byte più alto ("Big end") al byte più basso. Il valore 0x12345678., ad esempio, viene archiviato come (0x12 0x34 0x56 0x78) nel formato big-endian.<br/>                                                   |
| <span id="REG_EXPAND_SZ"></span><span id="reg_expand_sz"></span><dl> <dt>**REG \_ Espandi \_ SZ**</dt> </dl>                                | Stringa con terminazione null che contiene riferimenti non espansi a variabili di ambiente (ad esempio, "% PATH%"). Si tratta di una stringa Unicode o ANSI, a seconda che si usino le funzioni Unicode o ANSI.<br/>                                                                                                     |
| <span id="REG_LINK"></span><span id="reg_link"></span><dl> <dt>**\_collegamento reg**</dt> </dl>                                                | Collegamento simbolico Unicode.<br/>                                                                                                                                                                                                                                                                                            |
| <span id="REG_MULTI_SZ"></span><span id="reg_multi_sz"></span><dl> <dt>**REG \_ - \_ SZ**</dt> </dl>                                   | Matrice di stringhe con terminazione null che terminano con due caratteri null.<br/>                                                                                                                                                                                                                                      |
| <span id="REG_NONE"></span><span id="reg_none"></span><dl> <dt>**REG \_ None**</dt> </dl>                                                | Nessun tipo di valore definito.<br/>                                                                                                                                                                                                                                                                                            |
| <span id="REG_RESOURCE_LIST"></span><span id="reg_resource_list"></span><dl> <dt>**\_elenco delle risorse reg \_**</dt> </dl>                    | Elenco delle risorse del driver del dispositivo.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="REG_SZ"></span><span id="reg_sz"></span><dl> <dt>**REG \_ SZ**</dt> </dl>                                                      | Stringa con terminazione Null. Si tratta di una stringa Unicode o ANSI, a seconda che si usino le funzioni Unicode o ANSI.<br/>                                                                                                                                                                                          |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Winnt. h</dt> </dl> |



 

 




