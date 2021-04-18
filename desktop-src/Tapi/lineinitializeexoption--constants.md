---
description: Le \_ costanti LINEINITIALIZEEXOPTION specificano il meccanismo di notifica degli eventi da usare per l'inizializzazione di una sessione.
ms.assetid: 77674a45-7133-4518-af47-a9d58392b80b
title: Costanti LINEINITIALIZEEXOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86543c367877d74562cc0af13261881b7df19982
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331029"
---
# <a name="lineinitializeexoption_-constants"></a>\_Costanti LINEINITIALIZEEXOPTION

Le **costanti \_ LINEINITIALIZEEXOPTION** specificano il meccanismo di notifica degli eventi da usare per l'inizializzazione di una sessione.

<dl> <dt>

<span id="LINEINITIALIZEEXOPTION_CALLHUBTRACKING"></span><span id="lineinitializeexoption_callhubtracking"></span>**\_CALLHUBTRACKING LINEINITIALIZEEXOPTION**
</dt> <dd> <dl> <dt>



L'applicazione desidera usare il meccanismo di notifica degli eventi di rilevamento dell'hub chiamate. Questa costante viene esposta solo alle applicazioni che negoziano una versione di TAPI 3,0 o successiva.


</dt> </dl> </dd> <dt>

<span id="LINEINITIALIZEEXOPTION_USECOMPLETIONPORT"></span><span id="lineinitializeexoption_usecompletionport"></span>**\_USECOMPLETIONPORT LINEINITIALIZEEXOPTION**
</dt> <dd> <dl> <dt>



L'applicazione desidera utilizzare il meccanismo di notifica degli eventi della porta di completamento. Questo flag viene esposto solo alle applicazioni che negoziano una versione di TAPI 2,0 o successiva.


</dt> </dl> </dd> <dt>

<span id="LINEINITIALIZEEXOPTION_USEEVENT"></span><span id="lineinitializeexoption_useevent"></span>**\_USEEVENT LINEINITIALIZEEXOPTION**
</dt> <dd> <dl> <dt>



L'applicazione desidera utilizzare il meccanismo di notifica degli eventi del gestore eventi. Questo flag viene esposto solo alle applicazioni che negoziano una versione di TAPI 2,0 o successiva.


</dt> </dl> </dd> <dt>

<span id="LINEINITIALIZEEXOPTION_USEHIDDENWINDOW"></span><span id="lineinitializeexoption_usehiddenwindow"></span>**\_USEHIDDENWINDOW LINEINITIALIZEEXOPTION**
</dt> <dd> <dl> <dt>



L'applicazione desidera utilizzare il meccanismo di notifica degli eventi della finestra nascosta. Questo flag viene esposto solo alle applicazioni che negoziano una versione di TAPI 2,0 o successiva.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Per ulteriori informazioni sul funzionamento di queste opzioni, vedere [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




