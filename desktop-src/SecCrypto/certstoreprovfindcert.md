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
ms.openlocfilehash: 09701991d6b192d27f921642bfc960df819f9140
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347076"
---
# <a name="certstoreprovfindcert-callback-function"></a>Funzione di callback CertStoreProvFindCert

La funzione di callback **CertStoreProvFindCert** enumera o trova il primo o il certificato successivo in un [*archivio esterno*](../secgloss/e-gly.md) che corrisponde ai criteri specificati.

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

*hStoreProv* \[ in\]
</dt> <dd>

Handle **HCERTSTOREPROV** per un [*archivio certificati*](../secgloss/c-gly.md).

</dd> <dt>

*pFindInfo* \[ in\]
</dt> <dd>

Un puntatore a un [**\_ archivio certificati \_ prova a \_ trovare \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) la struttura di informazioni contenente tutti i parametri passati alla funzione [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) .

</dd> <dt>

*pPrevCertContext* \[ in\]
</dt> <dd>

Puntatore a un [**\_ contesto CERT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) del certificato trovato. Alla prima chiamata alla funzione, questo parametro deve essere impostato su **null**. Nelle chiamate successive deve essere impostato sul puntatore restituito nel parametro *ppProvCertContext* nell'ultima chiamata. Un puntatore non **null** passato in questo parametro viene liberato dalla funzione di callback.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Tutti i valori di flag necessari.

</dd> <dt>

*ppvStoreProvFindInfo* \[ in uscita\]
</dt> <dd>

Puntatore a un puntatore a un buffer per restituire le informazioni sul provider dell'archivio. Facoltativamente, il callback può restituire un puntatore alle informazioni di ricerca interne in questo parametro. Dopo la prima chiamata, questo parametro viene impostato sul puntatore restituito dalla chiamata precedente alla funzione.

</dd> <dt>

*ppProvCertContext* \[ out\]
</dt> <dd>

In una ricerca corretta viene restituito un puntatore al certificato trovato in questo parametro.

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

[**contesto del certificato \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**\_informazioni su \_ prova \_ archivio \_ certificati**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)
</dt> </dl>

 

 
