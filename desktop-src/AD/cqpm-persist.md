---
title: Messaggio CQPM_PERSIST (cmnquery. h)
description: Inviato alla funzione di callback CQPageProc di una pagina di estensione del modulo di query per consentire alla pagina di leggere o scrivere dati di query dalla memoria persistente.
ms.assetid: f01586dd-4ed3-45af-9e25-a596a693313d
ms.tgt_platform: multiple
keywords:
- Messaggio CQPM_PERSIST Active Directory
topic_type:
- apiref
api_name:
- CQPM_PERSIST
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70aaaae3b4fcc6788a16d59477d5f8158b43b892
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048307"
---
# <a name="cqpm_persist-message"></a>CQPM \_ messaggio permanente

Il messaggio di **\_ persistenza CQPM** viene inviato alla funzione di callback [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) di una pagina di estensione del modulo di query per consentire alla pagina di leggere o scrivere dati di query dalla memoria persistente.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Contiene un valore diverso da zero per leggere i dati della query o zero per scrivere i dati della query.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a un'interfaccia [**IPersistQuery**](/windows/win32/api/cmnquery/nn-cmnquery-ipersistquery) da cui devono essere letti o scritti i dati della query.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **\_ OK** se l'esito è positivo o un codice di errore **HRESULT** standard.

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

[**IPersistQuery**](/windows/win32/api/cmnquery/nn-cmnquery-ipersistquery)
</dt> </dl>

 

