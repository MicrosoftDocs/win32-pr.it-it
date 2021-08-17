---
description: Recupera una proprietà specificata di un elenco di certificati attendibili (CTL).
ms.assetid: 65309715-65b4-4608-960d-3404e68800a2
title: Funzione di callback CertStoreProvGetCTLProperty
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCTLProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 1677c2cccbdf0b422696437736380bd0bb57542220a898332d72ec7a0562fd1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769760"
---
# <a name="certstoreprovgetctlproperty-callback-function"></a>Funzione di callback CertStoreProvGetCTLProperty

La funzione di callback **CertStoreProvGetCTLProperty** recupera una proprietà specificata di un elenco di [*certificati*](../secgloss/c-gly.md) attendibili (CTL).

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI CertStoreProvGetCTLProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCTL_CONTEXT  pCtlContext,
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

Handle **HCERTSTOREPROV per** un [*archivio certificati.*](../secgloss/c-gly.md)

</dd> <dt>

*pCtlContext* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura CONTEXT \_ CTL.**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)

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

Puntatore a un buffer per contenere il puntatore a una [**struttura CONTEXT CTL \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) che deve essere restituita dalla funzione. Per ottenere il valore di *pcbData* prima di allocare memoria per il buffer, questo parametro può essere impostato su **NULL** in una prima chiamata alla funzione.

</dd> <dt>

*pcbData* \[ in, out\]
</dt> <dd>

Puntatore a **un valore DWORD** che indica la lunghezza del buffer *pvData.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce un valore diverso da zero.

Se la funzione ha esito negativo, restituisce zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CONTESTO \_ CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)
</dt> </dl>

 

 
