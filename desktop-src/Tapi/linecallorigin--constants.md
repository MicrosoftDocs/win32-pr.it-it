---
description: Le \_ costanti LINECALLORIGIN descrivono l'origine di una chiamata.
ms.assetid: b830a40e-62d9-4a6c-b43f-8318f30a7cd4
title: Costanti LINECALLORIGIN_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f00495d67dcff56ef7ee34cd85600a281e006ec3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326615"
---
# <a name="linecallorigin_-constants"></a>\_Costanti LINECALLORIGIN

Le **costanti \_ LINECALLORIGIN** descrivono l'origine di una chiamata.

<dl> <dt>

<span id="LINECALLORIGIN_CONFERENCE"></span><span id="linecallorigin_conference"></span>**\_conferenza LINECALLORIGIN**
</dt> <dd> <dl> <dt>



L'handle di chiamata è per una chiamata di conferenza, ovvero è la connessione dell'applicazione al Bridge di conferenza nel Commuter.


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_EXTERNAL"></span><span id="linecallorigin_external"></span>**LINECALLORIGIN \_ esterno**
</dt> <dd> <dl> <dt>



La chiamata ha avuto origine come una chiamata in ingresso su una riga esterna.


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_INBOUND"></span><span id="linecallorigin_inbound"></span>**LINECALLORIGIN in \_ ingresso**
</dt> <dd> <dl> <dt>



La chiamata ha avuto origine come chiamata in ingresso, ma il provider di servizi non è in grado di determinare se proviene da un'altra stazione nello stesso Commuter o da una riga esterna. I provider di servizi possono usare questa costante solo quando è stata negoziata la versione 1,4 o successiva di TAPI. In caso contrario, il provider di servizi può sostituire LINECALLORIGIN \_ undisp.


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_INTERNAL"></span><span id="linecallorigin_internal"></span>**LINECALLORIGIN \_ interno**
</dt> <dd> <dl> <dt>



La chiamata ha avuto origine come chiamata in ingresso in una stazione interna allo stesso ambiente di cambio.


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_OUTBOUND"></span><span id="linecallorigin_outbound"></span>**LINECALLORIGIN in \_ uscita**
</dt> <dd> <dl> <dt>



La chiamata ha avuto origine da questa stazione come chiamata in uscita.


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_UNAVAIL"></span><span id="linecallorigin_unavail"></span>**LINECALLORIGIN non \_ disponibile**
</dt> <dd> <dl> <dt>



L'origine della chiamata non è disponibile e non verrà mai conosciuta per questa chiamata.


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_UNKNOWN"></span><span id="linecallorigin_unknown"></span>**LINECALLORIGIN \_ sconosciuto**
</dt> <dd> <dl> <dt>



L'origine della chiamata è attualmente sconosciuta, ma potrebbe essere nota in seguito.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estensibilità. Tutti i 32 bit sono riservati.

L'origine di una chiamata viene archiviata nel membro **dwOrigin** della struttura [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) della chiamata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




