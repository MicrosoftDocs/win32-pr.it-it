---
description: Le \_ costanti LINECARDOPTION definiscono i valori usati nel membro dwOptions della struttura LINECARDENTRY restituita come parte della struttura LINETRANSLATECAPS restituita da lineGetTranslateCaps.
ms.assetid: 36c67fbf-e5ca-4ec4-a03a-0b828667abcc
title: Costanti LINECARDOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91dd9948d4a8963e8a9c860f68f0067c601f602c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333651"
---
# <a name="linecardoption_-constants"></a>\_Costanti LINECARDOPTION

Le **\_ costanti LINECARDOPTION** definiscono i valori usati nel membro **dwOptions** della struttura [**LINECARDENTRY**](/windows/desktop/api/Tapi/ns-tapi-linecardentry) restituita come parte della struttura [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) restituita da [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps). Le **\_ costanti LINECARDOPTION** t hanno i valori seguenti:

<dl> <dt>

<span id="LINECARDOPTION_HIDDEN"></span><span id="linecardoption_hidden"></span>**LINECARDOPTION \_ nascosto**
</dt> <dd> <dl> <dt>



Questa scheda chiamante è stata nascosta dall'utente. Non viene visualizzato da dial Helper nell'elenco principale delle schede di chiamata disponibili, ma verrà visualizzato nell'elenco di schede da cui è possibile copiare le regole di composizione.


</dt> </dl> </dd> <dt>

<span id="LINECARDOPTION_PREDEFINED"></span><span id="linecardoption_predefined"></span>**LINECARDOPTION \_ predefinito**
</dt> <dd> <dl> <dt>



Questa scheda chiamante è una delle definizioni delle schede di chiamata predefinite incluse in telefonia da Microsoft. Non è possibile rimuoverlo completamente utilizzando l'helper di connessione. Se l'utente tenta di rimuoverlo, viene nascosto. Continua quindi a essere accessibile per la copia delle regole di composizione.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Non estendibile. Tutti i 32 bit sono riservati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




