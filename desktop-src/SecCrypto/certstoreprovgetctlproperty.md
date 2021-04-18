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
ms.openlocfilehash: e30a9e735d44fc5681d5cd3932baaf3cc90aa30d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315804"
---
# <a name="certstoreprovgetctlproperty-callback-function"></a>Funzione di callback CertStoreProvGetCTLProperty

La funzione di callback **CertStoreProvGetCTLProperty** recupera una proprietà specificata di un [*elenco di certificati attendibili*](../secgloss/c-gly.md) (CTL).

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

*hStoreProv* \[ in\]
</dt> <dd>

Handle **HCERTSTOREPROV** per un [*archivio certificati*](../secgloss/c-gly.md).

</dd> <dt>

*pCtlContext* \[ in\]
</dt> <dd>

Puntatore a una struttura [**di \_ contesto CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) .

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

Puntatore a un buffer che contiene il puntatore a una struttura [**del \_ contesto CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) che deve essere restituita dalla funzione. Per ottenere il valore di *pcbData* prima di allocare memoria per il buffer, questo parametro può essere impostato su **null** in una prima chiamata alla funzione.

</dd> <dt>

*pcbData* \[ in uscita\]
</dt> <dd>

Puntatore a un **valore DWORD** che indica la lunghezza del buffer *pvData* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce un valore diverso da zero.

Se la funzione ha esito negativo, viene restituito zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_contesto CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)
</dt> </dl>

 

 
