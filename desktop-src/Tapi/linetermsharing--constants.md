---
description: Le \_ costanti del flag di bit LINETERMSHARING descrivono i diversi modi in cui un terminale può essere condiviso tra dispositivi linea, indirizzi o chiamate.
ms.assetid: 50a52a50-4d94-4068-9ea4-bea862400036
title: Costanti LINETERMSHARING_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2587621b6362195a610339ba5620b32f1d4f761
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326878"
---
# <a name="linetermsharing_-constants"></a>\_Costanti LINETERMSHARING

Le costanti del flag di bit **LINETERMSHARING \_** descrivono i diversi modi in cui un terminale può essere condiviso tra dispositivi linea, indirizzi o chiamate.

<dl> <dt>

<span id="LINETERMSHARING_PRIVATE"></span><span id="linetermsharing_private"></span>**LINETERMSHARING \_ privato**
</dt> <dd> <dl> <dt>



Il dispositivo terminal è privato per un dispositivo a riga singola.


</dt> </dl> </dd> <dt>

<span id="LINETERMSHARING_SHAREDCONF"></span><span id="linetermsharing_sharedconf"></span>**\_SHAREDCONF LINETERMSHARING**
</dt> <dd> <dl> <dt>



Il dispositivo terminal può essere utilizzato da più righe. Il [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) delle richieste dei diversi terminali viene unito o sottoposto a conferenza nel terminale.


</dt> </dl> </dd> <dt>

<span id="LINETERMSHARING_SHAREDEXCL"></span><span id="linetermsharing_sharedexcl"></span>**\_SHAREDEXCL LINETERMSHARING**
</dt> <dd> <dl> <dt>



Il dispositivo terminal può essere utilizzato da più righe. L'ultimo dispositivo a linee per eseguire un [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) o [**TSPI \_ lineSetTerminal**](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal) nel terminale per una determinata modalità terminale avrà una connessione esclusiva al terminale per tale modalità.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estensibilità. Tutti i 32 bit sono riservati.

Queste costanti descrivono le classi di flussi di controllo e di informazioni che possono essere indirizzate direttamente tra un dispositivo a linee e un dispositivo Terminal (ad esempio un set di telefono).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

