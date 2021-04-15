---
description: Enumera o trova il primo o il CRL successivo in un archivio esterno che corrisponde ai criteri specificati.
ms.assetid: caf218f5-f379-4cb6-bb4b-4767b846d45c
title: Funzione di callback CertStoreProvFindCRL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFindCRL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: b20b7a4b677356e59be9f2f6df47b260c12d2f64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529712"
---
# <a name="certstoreprovfindcrl-callback-function"></a>Funzione di callback CertStoreProvFindCRL

La funzione di callback **CertStoreProvFindCRL** enumera o trova il primo o il [*CRL*](../secgloss/c-gly.md) successivo in un [*Archivio*](../secgloss/e-gly.md) esterno che corrisponde ai criteri specificati.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI CertStoreProvFindCRL(
  _In_    HCERTSTOREPROV              hStoreProv,
  _In_    PCCERT_STORE_PROV_FIND_INFO pFindInfo,
  _In_    PCCRL_CONTEXT               pPrevCrlContext,
  _In_    DWORD                       dwFlags,
  _Inout_ void                        **ppvStoreProvFindInfo,
  _Out_   PCCRL_CONTEXT               *ppProvCrlContext
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

Un puntatore a un [**\_ archivio certificati \_ prova a \_ trovare \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) la struttura di informazioni contenente tutti i parametri passati alla funzione [**CertFindCRLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore) .

</dd> <dt>

*pPrevCrlContext* \[ in\]
</dt> <dd>

Puntatore a una struttura [**del \_ contesto CRL**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) dell'ultimo CRL trovato. Alla prima chiamata alla funzione, questo parametro deve essere impostato su **null**. Nelle chiamate successive deve essere impostato sul puntatore restituito nel parametro *ppProvCRLContext* nell'ultima chiamata. Un puntatore non **null** passato in questo parametro viene liberato dalla funzione di callback.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Tutti i valori di flag necessari.

</dd> <dt>

*ppvStoreProvFindInfo* \[ in uscita\]
</dt> <dd>

Puntatore a un puntatore a un buffer per restituire le informazioni sul provider dell'archivio. Facoltativamente, il callback può restituire un puntatore alle informazioni di ricerca interne in questo parametro. Dopo la prima chiamata, questo parametro viene impostato sul puntatore restituito dalla chiamata precedente alla funzione.

</dd> <dt>

*ppProvCrlContext* \[ out\]
</dt> <dd>

In una ricerca corretta viene restituito un puntatore al CRL trovato in questo parametro.

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

[**CertFindCRLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore)
</dt> <dt>

[**\_contesto CRL**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context)
</dt> </dl>

 

 
