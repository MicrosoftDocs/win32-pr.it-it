---
description: Le costanti LINELOCATIONOPTION definiscono i valori usati nel membro dwOptions della struttura LINELOCATIONENTRY restituito come parte della struttura LINETRANSLATECAPS restituita da \_ lineGetTranslateCaps.
ms.assetid: 3b185c16-2535-4a90-855b-29e52828ea4c
title: LINELOCATIONOPTION_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c45de77a6d887b6fb0c5fa0e45e7005a621aa10ca44cc3218078eea74d00a2fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003049"
---
# <a name="linelocationoption_-constants"></a>Costanti \_ LINELOCATIONOPTION

Le **costanti \_ LINELOCATIONOPTION** definiscono i valori usati nel membro **dwOptions** della struttura [**LINELOCATIONENTRY**](/windows/desktop/api/Tapi/ns-tapi-linelocationentry) restituita come parte della struttura [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) restituita da [**lineGetTranslateCaps.**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)

<dl> <dt>

<span id="LINELOCATIONOPTION_PULSEDIAL"></span><span id="linelocationoption_pulsedial"></span>**LINELOCATIONOPTION \_ PULSEDIAL**
</dt> <dd> <dl> <dt>



La modalità di composizione predefinita in questa posizione è la composizione a pulsazione. Se questo bit è impostato, [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) inserirà un modificatore di composizione "P" all'inizio della stringa dialable restituita quando viene selezionata questa posizione. Se questo bit non è impostato, **lineTranslateAddress** inserirà un modificatore di composizione "T" all'inizio della stringa dialable.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Non estendibile. Tutti i 32 bit sono riservati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




