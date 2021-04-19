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
ms.openlocfilehash: bcf69653f03ccfbb52c8247c9ea459000db55e2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310942"
---
# <a name="certstoreprovgetcrlproperty-callback-function"></a>Funzione di callback CertStoreProvGetCRLProperty

La funzione di callback **CertStoreProvGetCRLProperty** recupera una proprietà specificata di un [*CRL*](../secgloss/c-gly.md).

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

*hStoreProv* \[ in\]
</dt> <dd>

Handle **HCERTSTOREPROV** per un [*archivio certificati*](../secgloss/c-gly.md).

</dd> <dt>

*pCrlContext* \[ in\]
</dt> <dd>

Puntatore a una struttura [**del \_ contesto CRL**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) .

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

Puntatore a un buffer che contiene il puntatore a una struttura [**del \_ contesto CRL**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) che deve essere restituita dalla funzione. Può essere impostato su **null** in una prima chiamata alla funzione per ottenere il valore di *pcbData* prima di allocare memoria per il buffer.

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

[**\_contesto CRL**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context)
</dt> </dl>

 

 
