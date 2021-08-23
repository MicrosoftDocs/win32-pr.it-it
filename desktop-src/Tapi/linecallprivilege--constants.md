---
description: Le costanti del flag di bit LINECALLPRIVILEGE descrivono i tipi di diritti di accesso o privilegi che un'applicazione con un handle di chiamata può \_ avere per la chiamata corrispondente.
ms.assetid: a58b7e9e-696e-4421-9b31-1ba8afe6e03b
title: LINECALLPRIVILEGE_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c00dd43442345c545bb5e0b1718131b6815fd236f9c7d770c0f3b47b10b47a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660051"
---
# <a name="linecallprivilege_-constants"></a>Costanti LINECALLPRIVILEGE \_

Le costanti del flag di bit **LINECALLPRIVILEGE \_** descrivono i tipi di diritti o privilegi di accesso che un'applicazione con un handle di chiamata può avere per la chiamata corrispondente.

<dl> <dt>

<span id="LINECALLPRIVILEGE_MONITOR"></span><span id="linecallprivilege_monitor"></span>**MONITORAGGIO LINECALLPRIVILEGE \_**
</dt> <dd> <dl> <dt>



L'applicazione ha privilegi di monitoraggio per la chiamata. Questi privilegi consentono all'applicazione di monitorare le modifiche dello stato e di eseguire query sulle informazioni e sullo stato della chiamata.


</dt> </dl> </dd> <dt>

<span id="LINECALLPRIVILEGE_NONE"></span><span id="linecallprivilege_none"></span>**LINECALLPRIVILEGE \_ NONE**
</dt> <dd> <dl> <dt>



L'applicazione non ha privilegi per la chiamata. L'handle dell'applicazione è void e non deve essere usato.


</dt> </dl> </dd> <dt>

<span id="LINECALLPRIVILEGE_OWNER"></span><span id="linecallprivilege_owner"></span>**LINECALLPRIVILEGE \_ OWNER**
</dt> <dd> <dl> <dt>



L'applicazione dispone dei privilegi di proprietario per la chiamata. Questi privilegi consentono all'applicazione di modificare la chiamata in modi che influiscono sullo stato della chiamata.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estendibilità. Tutti i 32 bit sono riservati.

Quando un handle di chiamata viene fornito per la prima volta a un'applicazione o ogni volta che vengono modificati i privilegi di chiamata dell'applicazione, il [**messaggio LINE \_ CALLSTATE**](line-callstate.md) viene inviato all'applicazione. Quando un'applicazione esegue una chiamata e se l'applicazione ricevente non dispone già di un handle con privilegi di proprietario, questo messaggio informa l'applicazione dei nuovi privilegi per la chiamata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




