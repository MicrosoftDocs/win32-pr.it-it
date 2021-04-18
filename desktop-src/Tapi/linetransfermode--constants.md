---
description: Le \_ costanti del flag di bit LINETRANSFERMODE descrivono diverse modalità di risoluzione delle richieste di trasferimento delle chiamate.
ms.assetid: 0a01131f-b63c-45ef-a0a9-17d69a0dacf9
title: Costanti LINETRANSFERMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fff01f68ab4c43cf15a532639ade9d357a269ba6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325281"
---
# <a name="linetransfermode_-constants"></a>\_Costanti LINETRANSFERMODE

Le costanti del flag di bit **LINETRANSFERMODE \_** descrivono diverse modalità di risoluzione delle richieste di trasferimento delle chiamate.

<dl> <dt>

<span id="LINETRANSFERMODE_CONFERENCE"></span><span id="linetransfermode_conference"></span>**\_conferenza LINETRANSFERMODE**
</dt> <dd> <dl> <dt>



Il trasferimento viene risolto stabilendo una conferenza a tre vie tra l'applicazione, l'entità connessa alla chiamata iniziale e l'entità connessa alla chiamata di consultazione. Quando questa opzione è selezionata, viene creata una chiamata di conferenza.


</dt> </dl> </dd> <dt>

<span id="LINETRANSFERMODE_TRANSFER"></span><span id="linetransfermode_transfer"></span>**\_trasferimento LINETRANSFERMODE**
</dt> <dd> <dl> <dt>



Il trasferimento viene risolto trasferendo la chiamata iniziale alla chiamata di consultazione. Entrambe le chiamate diventeranno inattive per l'applicazione.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estensibilità. Tutti i 32 bit sono riservati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




