---
description: Recupera una proprietà specificata di un certificato.
ms.assetid: 827e0331-1f87-4891-8cc1-de1bcbad2963
title: Funzione di callback CertStoreProvGetCertProperty
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCertProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 50de9a73438e2755e002570f921d15e6086a4b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310943"
---
# <a name="certstoreprovgetcertproperty-callback-function"></a>Funzione di callback CertStoreProvGetCertProperty

La funzione di callback **CertStoreProvGetCertProperty** recupera una proprietà specificata di un certificato.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI CertStoreProvGetCertProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCERT_CONTEXT pCertContext,
  _In_    DWORD          dwPropId,
  _In_    DWORD          dwFlags,
  _Out_   void           *pvData,
  _Inout_ DWORD          *pcbData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hStoreProv* \[ in\]
</dt> <dd>

Handle **HCERTSTOREPROV** per un [*archivio certificati*](../secgloss/c-gly.md).

</dd> <dt>

*pCertContext* \[ in\]
</dt> <dd>

Puntatore a una struttura [**del \_ contesto del certificato**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) .

</dd> <dt>

*dwPropId* \[ in\]
</dt> <dd>

Indica un identificatore di proprietà.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Tutti i valori di flag necessari.

</dd> <dt>

*pvData* \[ out\]
</dt> <dd>

Puntatore a un buffer che contiene il puntatore a una struttura [**del \_ contesto del certificato**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) che deve essere restituita dalla funzione. Può essere impostato su **null** in una prima chiamata alla funzione per ottenere il valore di *pcbData* prima di allocare memoria per il buffer.

</dd> <dt>

*pcbData* \[ in uscita\]
</dt> <dd>

Puntatore a un **valore DWORD** che indica la lunghezza del buffer *pvData* .

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
</dt> </dl>

 

 
