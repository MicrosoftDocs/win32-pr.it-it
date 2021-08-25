---
description: Recupera una proprietà specificata di un CRL.
ms.assetid: b02f4f92-952a-4625-a7d4-6e78e542774e
title: Funzione di callback CertStoreProvGetCRLProperty
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCRLProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 2662c29ede9feec90b10869a4dc21277a8c6bdc6243e60ce894819e4b27dce5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877051"
---
# <a name="certstoreprovgetcrlproperty-callback-function"></a>Funzione di callback CertStoreProvGetCRLProperty

La funzione di callback **CertStoreProvGetCRLProperty** recupera una proprietà specificata di un [*CRL.*](../secgloss/c-gly.md)

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI CertStoreProvGetCRLProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCRL_CONTEXT  pCrlContext,
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

**Handle HCERTSTOREPROV** per un [*archivio certificati.*](../secgloss/c-gly.md)

</dd> <dt>

*pCrlContext* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura CONTEXT \_ CRL.**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context)

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

Puntatore a un buffer per contenere il puntatore a una [**struttura CRL \_ CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) che deve essere restituita dalla funzione. Può essere impostato su **NULL** in una prima chiamata alla funzione per ottenere il valore di *pcbData* prima di allocare memoria per il buffer.

</dd> <dt>

*pcbData* \[ in, out\]
</dt> <dd>

Puntatore a **un valore DWORD** che indica la lunghezza del buffer *pvData.*

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

[**CONTESTO \_ CRL**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context)
</dt> </dl>

 

 
