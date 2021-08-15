---
description: Enumera o trova il primo CTL o successivo in un archivio esterno che corrisponde ai criteri specificati.
ms.assetid: 0b465e6e-fb5c-4621-a968-c2cdcab0ea15
title: Funzione di callback CertStoreProvFindCTL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFindCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: f3064b42961196a7522fba6d08ac684aa4421b26727cdf229854351c777a4b56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770008"
---
# <a name="certstoreprovfindctl-callback-function"></a>Funzione di callback CertStoreProvFindCTL

La funzione di callback **CertStoreProvFindCTL** enumera o trova il primo O successivo [*CTL*](../secgloss/c-gly.md) in un archivio esterno [*che*](../secgloss/e-gly.md) corrisponde ai criteri specificati.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI CertStoreProvFindCTL(
  _In_    HCERTSTOREPROV              hStoreProv,
  _In_    PCCERT_STORE_PROV_FIND_INFO pFindInfo,
  _In_    PCCTL_CONTEXT               pPrevCtlContext,
  _In_    DWORD                       dwFlags,
  _Inout_ void                        **ppvStoreProvFindInfo,
  _Out_   PCCTL_CONTEXT               *ppProvCtlContext
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hStoreProv* \[ Pollici\]
</dt> <dd>

**Handle HCERTSTOREPROV** per un [*archivio certificati.*](../secgloss/c-gly.md)

</dd> <dt>

*pFindInfo* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura \_ \_ PROV \_ FIND \_ INFO CERT STORE**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) contenente tutti i parametri passati a [**CertFindCTLInStore.**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore) CHANGETABLE(CHANGES …).

</dd> <dt>

*pPrevCtlContext* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura CONTEXT CTL \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) dell'ultimo CTL trovato. Alla prima chiamata alla funzione, questo parametro deve essere impostato su **NULL.** Nelle chiamate successive, deve essere impostato sul puntatore restituito nel *parametro ppProvCTLContext* nell'ultima chiamata. Un **puntatore non NULL** passato in questo parametro viene liberato dalla funzione di callback.

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Tutti i valori di flag necessari.

</dd> <dt>

*ppvStoreProvFindInfo* \[ in, out\]
</dt> <dd>

Puntatore a un puntatore al buffer per restituire le informazioni del provider dell'archivio. Facoltativamente, il callback può restituire un puntatore alle informazioni di ricerca interne in questo parametro. Dopo la prima chiamata, questo parametro viene impostato sul puntatore restituito dalla chiamata precedente alla funzione .

</dd> <dt>

*ppProvCtlContext* \[ Cambio\]
</dt> <dd>

In caso di esito positivo della ricerca, in questo parametro viene restituito un puntatore all'elenco CTL trovato.

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

[**CERT \_ STORE \_ PROV \_ FIND \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore)
</dt> <dt>

[**CONTESTO \_ CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)
</dt> </dl>

 

 
