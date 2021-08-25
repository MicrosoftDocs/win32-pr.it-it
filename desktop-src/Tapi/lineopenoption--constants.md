---
description: Le costanti LINEOPENOPTION \_ elencano le opzioni disponibili per l'apertura di una riga.
ms.assetid: 361ae90c-a2cf-4107-a2da-80f561a82c56
title: LINEOPENOPTION_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0dc6a4780b366b2dce08110ecce40c7140ab1d0956d788dce5a67d5d0501b6d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739251"
---
# <a name="lineopenoption_-constants"></a>Costanti LINEOPENOPTION \_

Le **costanti LINEOPENOPTION \_** elencano le opzioni disponibili per l'apertura di una riga.

<dl> <dt>

<span id="LINEOPENOPTION_PROXY"></span><span id="lineopenoption_proxy"></span>**LINEOPENOPTION \_ PROXY**
</dt> <dd> <dl> <dt>



L'applicazione è disposta a gestire le richieste provenienti da altre applicazioni con la riga aperta.


</dt> </dl> </dd> <dt>

<span id="LINEOPENOPTION_SINGLEADDRESS"></span><span id="lineopenoption_singleaddress"></span>**LINEOPENOPTION \_ SINGLEADDRESS**
</dt> <dd> <dl> <dt>



L'applicazione deve essere informata delle nuove chiamate create nel dispositivo line solo se tali chiamate vengono visualizzate sull'indirizzo specificato nel membro **dwAddressID** nella struttura [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) a cui punta il *parametro lpCallParams.*


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Per altri dettagli sul funzionamento di queste opzioni, vedere [**lineOpen.**](/windows/desktop/api/Tapi/nf-tapi-lineopen)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




