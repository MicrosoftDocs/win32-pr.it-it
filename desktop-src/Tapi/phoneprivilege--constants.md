---
description: Le costanti del flag di bit PHONEPRIVILEGE descrivono i vari modi in cui è possibile aprire \_ un dispositivo telefonico.
ms.assetid: 1dc2fab9-b044-4ae3-8c16-fa450f9ef714
title: PHONEPRIVILEGE_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae9b3f3848af8c9858522bd924ccb77d7bf1682f09b66c0cfdcb5527b93416dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761293"
---
# <a name="phoneprivilege_-constants"></a>Costanti PHONEPRIVILEGE \_

Le costanti del flag di bit **PHONEPRIVILEGE \_** descrivono i vari modi in cui è possibile aprire un dispositivo telefonico.

<dl> <dt>

<span id="PHONEPRIVILEGE_MONITOR"></span><span id="phoneprivilege_monitor"></span>**MONITORAGGIO PHONEPRIVILEGE \_**
</dt> <dd> <dl> <dt>



Un'applicazione che apre un dispositivo telefono con il privilegio monitor viene informata degli eventi e delle modifiche dello stato che si verificano nel telefono. L'applicazione non può richiamare operazioni sul dispositivo telefonico che ne modificano lo stato, pertanto è possibile richiamare solo le operazioni di stato. Più applicazioni possono monitorare un dispositivo telefonico in un determinato momento.


</dt> </dl> </dd> <dt>

<span id="PHONEPRIVILEGE_OWNER"></span><span id="phoneprivilege_owner"></span>**PROPRIETARIO PHONEPRIVILEGE \_**
</dt> <dd> <dl> <dt>



Un'applicazione che apre un dispositivo telefono con il privilegio proprietario può modificare lo stato delle lampadine, della suoneria, dello schermo, del hookswitch e dei blocchi di dati del telefono. L'apertura di un dispositivo telefono in modalità proprietario offre anche il monitoraggio del dispositivo telefonico. Solo un'applicazione può essere proprietaria di un dispositivo telefonico in un determinato momento.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estendibilità. Tutti i 32 bit sono riservati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




