---
description: Le \_ costanti del flag di bit PHONEPRIVILEGE descrivono i vari modi in cui è possibile aprire un dispositivo telefonico.
ms.assetid: 1dc2fab9-b044-4ae3-8c16-fa450f9ef714
title: Costanti PHONEPRIVILEGE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6d04c074e03d6f0b7f7a6c58e4268e0bd5057a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333938"
---
# <a name="phoneprivilege_-constants"></a>\_Costanti PHONEPRIVILEGE

Le costanti del flag di bit **PHONEPRIVILEGE \_** descrivono i vari modi in cui è possibile aprire un dispositivo telefonico.

<dl> <dt>

<span id="PHONEPRIVILEGE_MONITOR"></span><span id="phoneprivilege_monitor"></span>**\_monitoraggio PHONEPRIVILEGE**
</dt> <dd> <dl> <dt>



Un'applicazione che apre un dispositivo telefonico con il privilegio di monitoraggio viene aggiornata sugli eventi e sulle modifiche di stato che si verificano sul telefono. L'applicazione non è in grado di richiamare alcuna operazione sul dispositivo telefonico che cambierebbe lo stato, quindi possono essere richiamate solo le operazioni di stato. Più applicazioni possono monitorare un dispositivo telefonico in un determinato momento.


</dt> </dl> </dd> <dt>

<span id="PHONEPRIVILEGE_OWNER"></span><span id="phoneprivilege_owner"></span>**\_proprietario PHONEPRIVILEGE**
</dt> <dd> <dl> <dt>



Un'applicazione che apre un dispositivo telefonico con il privilegio proprietario è autorizzata a modificare lo stato dei blocchi di lampade, suoneria, schermo, hookswitch e dati del telefono. L'apertura di un dispositivo telefonico in modalità proprietario fornisce anche il monitoraggio del dispositivo telefonico. Una sola applicazione può essere il proprietario di un dispositivo telefonico in un determinato momento.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estensibilità. Tutti i 32 bit sono riservati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




