---
description: Chiamato quando il certificato restituito dal callback CertStoreProvFindCTL non è stato usato e quindi rilasciato in una chiamata successiva a CertStoreProvFindCTL.
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
ms.openlocfilehash: 5f3f6d224ed19073408015b3b83b90a66e9402d9b838d50eb7a8381e312e0534
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877141"
---
# <a name="certstoreprovfreefindctl-callback-function"></a>Funzione di callback CertStoreProvFreeFindCTL

La funzione di callback **CertStoreProvFreeFindCTL** viene chiamata quando il certificato restituito dal callback [**CertStoreProvFindCTL**](certstoreprovfindctl.md) non è stato usato e quindi rilasciato in una chiamata successiva a **CertStoreProvFindCTL.** Prima che venga chiamato il callback CLOSE, tutti i certificati restituiti dal callback [**CertStoreProvFindCTL**](certstoreprovfindctl.md) devono essere rilasciati dal provider usando **CertStoreProvFindCTL** o **CertStoreProvFreeFindCTL.**

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

*hStoreProv* \[ Pollici\]
</dt> <dd>

**Handle HCERTSTOREPROV** per un [*archivio certificati.*](../secgloss/c-gly.md)

</dd> <dt>

*pCtlContext* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura CONTEXT \_ CTL.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)

</dd> <dt>

*pvStoreProvFindInfo* \[ Pollici\]
</dt> <dd>

Puntatore a un buffer contenente informazioni di ricerca.

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Tutti i valori di flag necessari.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** se la funzione ha esito positivo o **FALSE** in caso di esito negativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CertStoreProvFindCTL**](certstoreprovfindctl.md)
</dt> <dt>

[**CONTESTO \_ CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
