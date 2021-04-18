---
description: Enumera o trova il primo o il CTL successivo in un archivio esterno che corrisponde ai criteri specificati.
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
ms.openlocfilehash: 9454f918c9cbc5b6f90642d46fbb33573b70457f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315806"
---
# <a name="certstoreprovfindctl-callback-function"></a>Funzione di callback CertStoreProvFindCTL

La funzione di callback **CertStoreProvFindCTL** enumera o trova il primo o il successivo [*CTL*](../secgloss/c-gly.md) in un [*archivio esterno*](../secgloss/e-gly.md) che corrisponde ai criteri specificati.

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

*hStoreProv* \[ in\]
</dt> <dd>

Handle **HCERTSTOREPROV** per un [*archivio certificati*](../secgloss/c-gly.md).

</dd> <dt>

*pFindInfo* \[ in\]
</dt> <dd>

Un puntatore a un [**\_ archivio certificati \_ prova a \_ trovare \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) la struttura di informazioni contenente tutti i parametri passati a [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore). CHANGETABLE(CHANGES …).

</dd> <dt>

*pPrevCtlContext* \[ in\]
</dt> <dd>

Puntatore a una struttura [**di \_ contesto CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) dell'ultimo CTL trovato. Alla prima chiamata alla funzione, questo parametro deve essere impostato su **null**. Nelle chiamate successive deve essere impostato sul puntatore restituito nel parametro *ppProvCTLContext* nell'ultima chiamata. Un puntatore non **null** passato in questo parametro viene liberato dalla funzione di callback.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Tutti i valori di flag necessari.

</dd> <dt>

*ppvStoreProvFindInfo* \[ in uscita\]
</dt> <dd>

Puntatore a un puntatore al buffer per restituire le informazioni sul provider dell'archivio. Facoltativamente, il callback può restituire un puntatore alle informazioni di ricerca interne in questo parametro. Dopo la prima chiamata, questo parametro viene impostato sul puntatore restituito dalla chiamata precedente alla funzione.

</dd> <dt>

*ppProvCtlContext* \[ out\]
</dt> <dd>

In una ricerca riuscita viene restituito un puntatore al CTL trovato in questo parametro.

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

[**\_informazioni su \_ prova \_ archivio \_ certificati**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore)
</dt> <dt>

[**\_contesto CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)
</dt> </dl>

 

 
