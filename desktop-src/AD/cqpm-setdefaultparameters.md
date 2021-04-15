---
title: Messaggio CQPM_SETDEFAULTPARAMETERS (cmnquery. h)
description: Inviato alla funzione di callback CQPageProc di una pagina di estensione del modulo di query per impostare parametri predefiniti alternativi per la pagina.
ms.assetid: 4d7f1c03-5c67-4f4c-b381-034a142251fe
ms.tgt_platform: multiple
keywords:
- Messaggio CQPM_SETDEFAULTPARAMETERS Active Directory
topic_type:
- apiref
api_name:
- CQPM_SETDEFAULTPARAMETERS
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c4df77b9068c23a0eeac30181d131cb8469dc53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476492"
---
# <a name="cqpm_setdefaultparameters-message"></a>\_Messaggio CQPM SETDEFAULTPARAMETERS

Il messaggio **CQPM \_ SETDEFAULTPARAMETERS** viene inviato alla funzione di callback [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) di una pagina di estensione del modulo di query per impostare parametri predefiniti alternativi per la pagina.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Contiene un valore diverso da zero se la pagina è la pagina predefinita o zero in caso contrario.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**openQueryWindow**](/windows/desktop/api/Cmnquery/ns-cmnquery-openquerywindow) che contiene i dati sulla finestra di dialogo query del servizio directory.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questo messaggio viene ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                              |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                        |
| Intestazione<br/>                   | <dl> <dt>Cmnquery. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[**OPENQUERYWINDOW**](/windows/desktop/api/Cmnquery/ns-cmnquery-openquerywindow)
</dt> </dl>

 

 





