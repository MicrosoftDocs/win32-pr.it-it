---
description: Enumera o trova il primo o il certificato successivo in un archivio esterno che corrisponde ai criteri specificati.
ms.assetid: 1129a372-4d7c-454e-969b-26a1d6037bc0
title: Funzione di callback CertStoreProvFindCert
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFindCert
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: a50a53e819fcfd12ff490b4e6642536c01d9a49b4e9345e7713bf0eb08a0fac6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770020"
---
# <a name="certstoreprovfindcert-callback-function"></a>Funzione di callback CertStoreProvFindCert

La funzione di callback **CertStoreProvFindCert** enumera o trova il primo o il certificato successivo in un archivio [*esterno*](../secgloss/e-gly.md) che corrisponde ai criteri specificati.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI CertStoreProvFindCert(
  _In_    HCERTSTOREPROV              hStoreProv,
  _In_    PCCERT_STORE_PROV_FIND_INFO pFindInfo,
  _In_    PCCERT_CONTEXT              pPrevCertContext,
  _In_    DWORD                       dwFlags,
  _Inout_ void                        **ppvStoreProvFindInfo,
  _Out_   PCCERT_CONTEXT              *ppProvCertContext
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

Puntatore a una [**struttura CERT \_ STORE \_ PROV FIND \_ \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) contenente tutti i parametri passati alla funzione [**CertFindCertificateInStore.**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)

</dd> <dt>

*pPrevCertContext* \[ Pollici\]
</dt> <dd>

Puntatore a un [**CERT \_ CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) del certificato trovato. Alla prima chiamata alla funzione, questo parametro deve essere impostato su **NULL.** Nelle chiamate successive, deve essere impostato sul puntatore restituito nel *parametro ppProvCertContext* nell'ultima chiamata. Un **puntatore** non NULL passato in questo parametro viene liberato dalla funzione di callback.

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Tutti i valori di flag necessari.

</dd> <dt>

*ppvStoreProvFindInfo* \[ in, out\]
</dt> <dd>

Puntatore a un puntatore a un buffer per restituire le informazioni sul provider dell'archivio. Facoltativamente, il callback può restituire un puntatore alle informazioni di ricerca interne in questo parametro. Dopo la prima chiamata, questo parametro viene impostato sul puntatore restituito dalla chiamata precedente alla funzione.

</dd> <dt>

*ppProvCertContext* \[ Cambio\]
</dt> <dd>

In caso di esito positivo della ricerca, in questo parametro viene restituito un puntatore al certificato trovato.

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

[**CONTESTO \_ CERT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**CERT \_ STORE \_ PROV \_ FIND \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)
</dt> </dl>

 

 
