---
description: Chiamato quando il certificato restituito dal callback CertStoreProvFindCRL non è stato usato e quindi rilasciato, in una chiamata successiva a CertStoreProvFindCRL.
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
ms.openlocfilehash: b5f5443d58a86c8bab979d17d64dc693d94ae373
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883813"
---
# <a name="certstoreprovfreefindcrl-callback-function"></a>Funzione di callback CertStoreProvFreeFindCRL

La funzione di callback **CertStoreProvFreeFindCRL** viene chiamata quando il certificato restituito dal callback [**CertStoreProvFindCRL**](certstoreprovfindcrl.md) non è stato usato e quindi rilasciato in una chiamata successiva a **CertStoreProvFindCRL**. Prima che venga chiamato il callback di chiusura, tutti i certificati restituiti dal callback [**CertStoreProvFindCRL**](certstoreprovfindcrl.md) devono essere rilasciati dal provider utilizzando **CertStoreProvFindCRL** o **CertStoreProvFreeFindCRL**.

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

*hStoreProv* \[ in\]
</dt> <dd>

Handle **HCERTSTOREPROV** per un [*archivio certificati*](../secgloss/c-gly.md).

</dd> <dt>

*pCrlContext* \[ in\]
</dt> <dd>

Puntatore a un [**\_ contesto CRL**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).

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

[**CertStoreProvFindCRL**](certstoreprovfindcrl.md)
</dt> <dt>

[**\_contesto CRL**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
