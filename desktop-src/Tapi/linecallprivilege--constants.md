---
description: Le \_ costanti del flag di bit LINECALLPRIVILEGE descrivono i tipi di diritti di accesso o i privilegi che un'applicazione con un handle di chiamata potrebbe avere per la chiamata corrispondente.
ms.assetid: a58b7e9e-696e-4421-9b31-1ba8afe6e03b
title: Costanti LINECALLPRIVILEGE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac2569ec255d2da3ad384292eb87afaa285f54b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332895"
---
# <a name="linecallprivilege_-constants"></a>\_Costanti LINECALLPRIVILEGE

Le costanti del flag di bit **LINECALLPRIVILEGE \_** descrivono i tipi di diritti di accesso o i privilegi che un'applicazione con un handle di chiamata potrebbe avere per la chiamata corrispondente.

<dl> <dt>

<span id="LINECALLPRIVILEGE_MONITOR"></span><span id="linecallprivilege_monitor"></span>**\_monitoraggio LINECALLPRIVILEGE**
</dt> <dd> <dl> <dt>



L'applicazione dispone di privilegi di monitoraggio per la chiamata. Questi privilegi consentono all'applicazione di monitorare le modifiche di stato e le informazioni di query e lo stato della chiamata.


</dt> </dl> </dd> <dt>

<span id="LINECALLPRIVILEGE_NONE"></span><span id="linecallprivilege_none"></span>**LINECALLPRIVILEGE \_ None**
</dt> <dd> <dl> <dt>



L'applicazione non dispone di privilegi per la chiamata. L'handle dell'applicazione non è valido e non deve essere usato.


</dt> </dl> </dd> <dt>

<span id="LINECALLPRIVILEGE_OWNER"></span><span id="linecallprivilege_owner"></span>**\_proprietario LINECALLPRIVILEGE**
</dt> <dd> <dl> <dt>



L'applicazione dispone dei privilegi di proprietario per la chiamata. Questi privilegi consentono all'applicazione di modificare la chiamata in modi che influiscono sullo stato della chiamata.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estensibilità. Tutti i 32 bit sono riservati.

Quando un handle di chiamata viene fornito per la prima volta a un'applicazione o ogni volta che vengono modificati i privilegi di chiamata di tale applicazione, il messaggio di [**riga \_ CALLSTATE**](line-callstate.md) viene inviato all'applicazione. Quando un'applicazione passa una chiamata e se l'applicazione ricevente non dispone già di un handle con privilegi di proprietario, questo messaggio informa l'applicazione sui nuovi privilegi della chiamata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




