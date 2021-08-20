---
description: Enumera o trova il primo O successivo CRL in un archivio esterno che corrisponde ai criteri specificati.
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
ms.openlocfilehash: eebcc990da0cd2d866325200223e9e654e45e055299a8b384a613dc9841c2799
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126681"
---
# <a name="certstoreprovfindcrl-callback-function"></a>Funzione di callback CertStoreProvFindCRL

La funzione di callback **CertStoreProvFindCRL** enumera o trova il primo O successivo [*CRL*](../secgloss/c-gly.md) in un archivio esterno [*che*](../secgloss/e-gly.md) corrisponde ai criteri specificati.

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

*hStoreProv* \[ Pollici\]
</dt> <dd>

**Handle HCERTSTOREPROV** per un [*archivio certificati*](../secgloss/c-gly.md).

</dd> <dt>

*pFindInfo* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura CERT \_ STORE \_ PROV FIND \_ \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) contenente tutti i parametri passati alla funzione [**CertFindCRLInStore.**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore)

</dd> <dt>

*pPrevCrlContext* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura CRL \_ CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) dell'ultimo CRL trovato. Alla prima chiamata alla funzione, questo parametro deve essere impostato su **NULL.** Nelle chiamate successive, deve essere impostato sul puntatore restituito nel *parametro ppProvCRLContext* nell'ultima chiamata. Un **puntatore** non NULL passato in questo parametro viene liberato dalla funzione di callback.

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Tutti i valori di flag necessari.

</dd> <dt>

*ppvStoreProvFindInfo* \[ in, out\]
</dt> <dd>

Puntatore a un puntatore a un buffer per restituire le informazioni sul provider dell'archivio. Facoltativamente, il callback può restituire un puntatore alle informazioni di ricerca interne in questo parametro. Dopo la prima chiamata, questo parametro viene impostato sul puntatore restituito dalla chiamata precedente alla funzione.

</dd> <dt>

*ppProvCrlContext* \[ Cambio\]
</dt> <dd>

In caso di esito positivo della ricerca, in questo parametro viene restituito un puntatore all'elenco CRL trovato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** se la funzione ha esito positivo o **FALSE** se ha esito negativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CERT \_ STORE \_ PROV \_ FIND \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[**CertFindCRLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore)
</dt> <dt>

[**CONTESTO \_ CRL**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context)
</dt> </dl>

 

 
