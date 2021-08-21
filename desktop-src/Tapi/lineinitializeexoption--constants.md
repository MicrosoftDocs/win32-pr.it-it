---
description: Le costanti LINEINITIALIZEEXOPTION \_ specificano il meccanismo di notifica degli eventi da usare durante l'inizializzazione di una sessione.
ms.assetid: 77674a45-7133-4518-af47-a9d58392b80b
title: LINEINITIALIZEEXOPTION_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e92a1df7c4ea88cad126dcf5b542dbbdc33704814518dbc79cdf5d6bff5da402
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073041"
---
# <a name="lineinitializeexoption_-constants"></a>Costanti LINEINITIALIZEEXOPTION \_

Le **costanti LINEINITIALIZEEXOPTION \_** specificano il meccanismo di notifica degli eventi da usare durante l'inizializzazione di una sessione.

<dl> <dt>

<span id="LINEINITIALIZEEXOPTION_CALLHUBTRACKING"></span><span id="lineinitializeexoption_callhubtracking"></span>**LINEINITIALIZEEXOPTION \_ CALLHUBTRACKING**
</dt> <dd> <dl> <dt>



L'applicazione desidera usare il meccanismo di notifica degli eventi di rilevamento dell'hub chiamate. Questa costante viene esposta solo alle applicazioni che negoziano una versione TAPI 3.0 o successiva.


</dt> </dl> </dd> <dt>

<span id="LINEINITIALIZEEXOPTION_USECOMPLETIONPORT"></span><span id="lineinitializeexoption_usecompletionport"></span>**LINEINITIALIZEEXOPTION \_ USECOMPLETIONPORT**
</dt> <dd> <dl> <dt>



L'applicazione vuole usare il meccanismo di notifica degli eventi Porta di completamento. Questo flag viene esposto solo alle applicazioni che negoziano una versione TAPI 2.0 o successiva.


</dt> </dl> </dd> <dt>

<span id="LINEINITIALIZEEXOPTION_USEEVENT"></span><span id="lineinitializeexoption_useevent"></span>**LINEINITIALIZEEXOPTION \_ USEEVENT**
</dt> <dd> <dl> <dt>



L'applicazione desidera usare il meccanismo di notifica degli eventi di Gestione eventi. Questo flag viene esposto solo alle applicazioni che negoziano una versione TAPI 2.0 o successiva.


</dt> </dl> </dd> <dt>

<span id="LINEINITIALIZEEXOPTION_USEHIDDENWINDOW"></span><span id="lineinitializeexoption_usehiddenwindow"></span>**LINEINITIALIZEEXOPTION \_ USEHIDDENWINDOW**
</dt> <dd> <dl> <dt>



L'applicazione desidera usare il meccanismo di notifica degli eventi Finestra nascosta. Questo flag viene esposto solo alle applicazioni che negoziano una versione TAPI 2.0 o successiva.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Per altri dettagli sul funzionamento di queste opzioni, vedere [**lineInitializeEx.**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




