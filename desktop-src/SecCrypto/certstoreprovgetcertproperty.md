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
ms.openlocfilehash: c7d338c94c4e9655c125b0f70e3f2e8dfa732316a970c74c26e4a7fbced22671
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769926"
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

*hStoreProv* \[ Pollici\]
</dt> <dd>

**Handle HCERTSTOREPROV** per un [*archivio certificati*](../secgloss/c-gly.md).

</dd> <dt>

*pCertContext* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura CERT \_ CONTEXT.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)

</dd> <dt>

*dwPropId* \[ Pollici\]
</dt> <dd>

Indica un identificatore di proprietà.

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Tutti i valori di flag necessari.

</dd> <dt>

*pvData* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer per contenere il puntatore a una [**struttura CERT \_ CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) che deve essere restituita dalla funzione. Può essere impostato su **NULL** in una prima chiamata alla funzione per ottenere il valore *di pcbData* prima di allocare memoria per il buffer.

</dd> <dt>

*pcbData* \[ in, out\]
</dt> <dd>

Puntatore a **un valore DWORD** che indica la lunghezza del buffer *pvData.*

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
</dt> </dl>

 

 
