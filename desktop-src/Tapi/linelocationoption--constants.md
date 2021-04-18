---
description: Le \_ costanti LINELOCATIONOPTION definiscono i valori usati nel membro dwOptions della struttura LINELOCATIONENTRY restituita come parte della struttura LINETRANSLATECAPS restituita da lineGetTranslateCaps.
ms.assetid: 3b185c16-2535-4a90-855b-29e52828ea4c
title: Costanti LINELOCATIONOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f60398953d2f809e29a78323e3b1dedfcac7a1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331027"
---
# <a name="linelocationoption_-constants"></a>\_Costanti LINELOCATIONOPTION

Le **costanti \_ LINELOCATIONOPTION** definiscono i valori usati nel membro **dwOptions** della struttura [**LINELOCATIONENTRY**](/windows/desktop/api/Tapi/ns-tapi-linelocationentry) restituita come parte della struttura [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) restituita da [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps).

<dl> <dt>

<span id="LINELOCATIONOPTION_PULSEDIAL"></span><span id="linelocationoption_pulsedial"></span>**\_PULSEDIAL LINELOCATIONOPTION**
</dt> <dd> <dl> <dt>



La modalità di composizione predefinita in questa posizione è la composizione a impulsi. Se questo bit è impostato, [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) inserirà un modificatore di composizione "P" all'inizio della stringa di connessione remota restituita quando si seleziona questa posizione. Se questo bit non è impostato, **lineTranslateAddress** inserirà un modificatore di composizione "T" all'inizio della stringa di connessione.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Non estendibile. Tutti i 32 bit sono riservati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




