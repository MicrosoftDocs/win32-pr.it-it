---
title: Messaggio CQPM_ENABLE (cmnquery. h)
description: Inviato alla funzione di callback CQPageProc di una pagina di estensione del modulo di query per abilitare o disabilitare la pagina.
ms.assetid: dc75fab7-6de7-4138-86df-84d44e774120
ms.tgt_platform: multiple
keywords:
- Messaggio CQPM_ENABLE Active Directory
topic_type:
- apiref
api_name:
- CQPM_ENABLE
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0252c5e1ec7fd9633241416fbf01bb4ead52c45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048003"
---
# <a name="cqpm_enable-message"></a>\_Messaggio di abilitazione CQPM

Il messaggio di **\_ Abilitazione di CQPM** viene inviato alla funzione di callback [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) di una pagina di estensione del modulo di query per abilitare o disabilitare la pagina.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Contiene zero per disabilitare la pagina o un valore diverso da zero per abilitare la pagina.

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato.

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
</dt> </dl>

 

 





