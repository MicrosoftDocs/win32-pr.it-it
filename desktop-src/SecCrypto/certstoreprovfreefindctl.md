---
description: Chiamato quando il certificato restituito dal callback CertStoreProvFindCTL non è stato usato e quindi rilasciato, in una chiamata successiva a CertStoreProvFindCTL.
ms.assetid: 04e62a4e-4542-4225-8750-fabbda5adf0d
title: Funzione di callback CertStoreProvFreeFindCTL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: ff0c9c3b7be6b8a4cafd759c3411f5096ee8640b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310944"
---
# <a name="certstoreprovfreefindctl-callback-function"></a>Funzione di callback CertStoreProvFreeFindCTL

La funzione di callback **CertStoreProvFreeFindCTL** viene chiamata quando il certificato restituito dal callback [**CertStoreProvFindCTL**](certstoreprovfindctl.md) non è stato usato e quindi rilasciato in una chiamata successiva a **CertStoreProvFindCTL**. Prima che venga chiamato il callback di chiusura, tutti i certificati restituiti dal callback [**CertStoreProvFindCTL**](certstoreprovfindctl.md) devono essere rilasciati dal provider utilizzando **CertStoreProvFindCTL** o **CertStoreProvFreeFindCTL**.

## <a name="syntax"></a>Sintassi


```C++
BOOL CertStoreProvFreeFindCTL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCTL_CONTEXT  pCtlContext,
  _In_ void           *pvStoreProvFindInfo,
  _In_ DWORD          dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hStoreProv* \[ in\]
</dt> <dd>

Handle **HCERTSTOREPROV** per un [*archivio certificati*](../secgloss/c-gly.md).

</dd> <dt>

*pCtlContext* \[ in\]
</dt> <dd>

Puntatore a una struttura [**di \_ contesto CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) .

</dd> <dt>

*pvStoreProvFindInfo* \[ in\]
</dt> <dd>

Puntatore a un buffer contenente le informazioni di ricerca.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Tutti i valori di flag necessari.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se la funzione ha esito positivo o **false** se l'operazione ha esito negativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CertStoreProvFindCTL**](certstoreprovfindctl.md)
</dt> <dt>

[**\_contesto CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
