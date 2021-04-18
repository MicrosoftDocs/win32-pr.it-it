---
description: Nell'elenco seguente vengono descritte le costanti dei criteri di dismissione.
ms.assetid: a085709e-1c61-4ae2-832e-fda59479cef6
title: Costanti dei criteri di scaricamento (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 052d07a5fe538543b66ec8d48c940f63fe82a682
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312057"
---
# <a name="discharge-policy-constants"></a>Costanti dei criteri di scaricamento

Nell'elenco seguente vengono descritte le costanti dei criteri di dismissione.



| Costante/valore                                                                                                                                                                                                                                            | Descrizione                                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DISCHARGE_POLICY_CRITICAL"></span><span id="discharge_policy_critical"></span><dl> <dt>**Scarica \_ CRITERIO \_ critico**</dt> <dt>0</dt> </dl> | Quale delle impostazioni dei criteri di scaricamento della batteria (strutture a [**\_ \_ livello di energia del sistema**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) ) viene usato quando la batteria viene scaricata sotto la soglia critica.<br/> |
| <span id="DISCHARGE_POLICY_LOW"></span><span id="discharge_policy_low"></span><dl> <dt>**Scarica \_ CRITERIO \_ basso**</dt> <dt>1</dt> </dl>                | Quale delle impostazioni dei criteri di scaricamento della batteria (strutture a [**\_ \_ livello di energia del sistema**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) ) viene usato quando la batteria viene scaricata al di sotto della soglia inferiore.<br/>      |
| <span id="NUM_DISCHARGE_POLICIES"></span><span id="num_discharge_policies"></span><dl> Numero di <dt>**\_ \_Criteri di dismissione**</dt> <dt>4</dt> </dl>          | Numero di impostazioni dei criteri di scaricamento della batteria (strutture a [**\_ \_ livello di alimentazione del sistema**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) ) specificate.<br/>                                                           |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>WinNT. h (include Windows. h)</dt> </dl> |



 

 




