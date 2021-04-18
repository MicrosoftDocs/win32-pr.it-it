---
description: Le \_ costanti LINEOPENOPTION elencano le opzioni disponibili per l'apertura di una riga.
ms.assetid: 361ae90c-a2cf-4107-a2da-80f561a82c56
title: Costanti LINEOPENOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dee9182ff7a28627eebd695ce5d9c0877460b15e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331256"
---
# <a name="lineopenoption_-constants"></a>\_Costanti LINEOPENOPTION

Le **\_ costanti LINEOPENOPTION** elencano le opzioni disponibili per l'apertura di una riga.

<dl> <dt>

<span id="LINEOPENOPTION_PROXY"></span><span id="lineopenoption_proxy"></span>**\_proxy LINEOPENOPTION**
</dt> <dd> <dl> <dt>



L'applicazione è pronta a gestire le richieste provenienti da altre applicazioni con la riga aperta.


</dt> </dl> </dd> <dt>

<span id="LINEOPENOPTION_SINGLEADDRESS"></span><span id="lineopenoption_singleaddress"></span>**\_SINGLEADDRESS LINEOPENOPTION**
</dt> <dd> <dl> <dt>



L'applicazione deve essere informata sulle nuove chiamate create sul dispositivo di linea solo se tali chiamate vengono visualizzate nell'indirizzo specificato nel membro **dwAddressID** della struttura [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) a cui punta il parametro *lpCallParams* .


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Per ulteriori informazioni sul funzionamento di queste opzioni, vedere [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




