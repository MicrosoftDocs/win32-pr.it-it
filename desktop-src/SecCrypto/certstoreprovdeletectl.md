---
description: Chiamato da CertDeleteCTLFromStore prima di eliminare un elenco di scopi consentiti dall'archivio.
ms.assetid: 6cda772f-7e94-414d-99fc-a90451ac0ccf
title: Funzione di callback CertStoreProvDeleteCTL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvDeleteCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: abeea0fdc3b6d77974b2c057d0e2ea98fe11e63a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880997"
---
# <a name="certstoreprovdeletectl-callback-function"></a>Funzione di callback CertStoreProvDeleteCTL

La funzione di callback **CertStoreProvDeleteCTL** viene chiamata da [**CertDeleteCTLFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletectlfromstore) prima di eliminare un elenco di scopi consentiti dall'archivio. Questa funzione determina se è possibile eliminare un elenco di scopi consentiti.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI CertStoreProvDeleteCTL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCTL_CONTEXT  pCtlContext,
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

Puntatore a una struttura [**di \_ contesto CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) .

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Tutti i valori di flag necessari.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se è possibile eliminare un CTL dall'archivio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |



 

 
