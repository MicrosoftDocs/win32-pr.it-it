---
description: Chiamato quando il certificato restituito dal callback CertStoreProvFindCRL non è stato usato e quindi rilasciato in una chiamata successiva a CertStoreProvFindCRL.
ms.assetid: e90609f6-63cd-40eb-bd5a-289473daa5bb
title: Funzione di callback CertStoreProvFreeFindCRL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCRL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 1bf7e3b2518789bdf3755cefec0dcc27c88642c376cafca039ce5cc20533a068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769936"
---
# <a name="certstoreprovfreefindcrl-callback-function"></a>Funzione di callback CertStoreProvFreeFindCRL

La funzione di callback **CertStoreProvFreeFindCRL** viene chiamata quando il certificato restituito dal callback [**CertStoreProvFindCRL**](certstoreprovfindcrl.md) non è stato usato e quindi rilasciato in una chiamata successiva a **CertStoreProvFindCRL.** Prima che venga chiamato il callback CLOSE, tutti i certificati restituiti dal callback [**CertStoreProvFindCRL**](certstoreprovfindcrl.md) devono essere rilasciati dal provider **usando CertStoreProvFindCRL** o **CertStoreProvFreeFindCRL.**

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI CertStoreProvFreeFindCRL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCRL_CONTEXT  pCrlContext,
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

*pCrlContext* \[ Pollici\]
</dt> <dd>

Puntatore a un [**oggetto CONTEXT \_ CRL.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)

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

[**CertStoreProvFindCRL**](certstoreprovfindcrl.md)
</dt> <dt>

[**CONTESTO \_ CRL**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
