---
description: Chiamato quando il certificato restituito dal callback CertStoreProvFindCert non è stato usato e quindi rilasciato in una chiamata successiva a CertStoreProvFindCert.
ms.assetid: be882b56-027c-4540-9426-27d3c2b262e9
title: Funzione di callback CertStoreProvFreeFindCert
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCert
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: ab2a6ae1bd8199e7bed97626c83241223fc3943b94fcb387868331329d8740a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877301"
---
# <a name="certstoreprovfreefindcert-callback-function"></a>Funzione di callback CertStoreProvFreeFindCert

La funzione di callback **CertStoreProvFreeFindCert** viene chiamata quando il certificato restituito dal callback [**CertStoreProvFindCert**](certstoreprovfindcert.md) non è stato usato e quindi rilasciato in una chiamata successiva a **CertStoreProvFindCert.** Prima che venga chiamato il callback CLOSE, tutti i certificati restituiti dal callback [**CertStoreProvFindCert**](certstoreprovfindcert.md) devono essere rilasciati dal provider usando **CertStoreProvFindCert** o **CertStoreProvFreeFindCert.**

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI CertStoreProvFreeFindCert(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCERT_CONTEXT pCertContext,
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

*pCertContext* \[ Pollici\]
</dt> <dd>

Puntatore a [**CERT \_ CONTEXT.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)

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

[**CONTESTO DEL \_ CERTIFICATO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**CertStoreProvFindCert**](certstoreprovfindcert.md)
</dt> </dl>

 

 
