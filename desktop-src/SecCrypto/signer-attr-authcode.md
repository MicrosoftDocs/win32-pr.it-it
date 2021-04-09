---
description: Specifica gli attributi per una firma Authenticode.
ms.assetid: 1c1052c3-c5c5-48ae-8266-0b367800a84a
title: Struttura SIGNER_ATTR_AUTHCODE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_ATTR_AUTHCODE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 952ed0f55a185d9a7ef9eeed3366f64c84423ddd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968650"
---
# <a name="signer_attr_authcode-structure"></a>Struttura del FIRMATARIo \_ attr \_ AUTHCODE

La struttura del **firmatario \_ attr \_ AUTHCODE** specifica gli attributi per una firma [*Authenticode*](../secgloss/a-gly.md) .

> [!Note]  
> Questa struttura non è definita in alcun file di intestazione. Per usare questa struttura, è necessario definirla come illustrato in questo argomento.

 

## <a name="syntax"></a>Sintassi


```C++
typedef struct _SIGNER_ATTR_AUTHCODE {
  DWORD   cbSize;
  BOOL    fCommercial;
  BOOL    fIndividual;
  LPCWSTR pwszName;
  LPCWSTR pwszInfo;
} SIGNER_ATTR_AUTHCODE, *PSIGNER_ATTR_AUTHCODE;
```



## <a name="members"></a>Members

<dl> <dt>

**cbSize**
</dt> <dd>

Dimensione, in byte, della struttura.

</dd> <dt>

**fCommercial**
</dt> <dd>

**True** per firmare l'oggetto come server di pubblicazione commerciale; in caso contrario, **false**.

</dd> <dt>

**fIndividual**
</dt> <dd>

**True** per firmare l'oggetto come singolo editore; in caso contrario, **false**.

</dd> <dt>

**pwszName**
</dt> <dd>

Nome visualizzato del file dopo il download.

</dd> <dt>

**pwszInfo**
</dt> <dd>

Nome visualizzato dell'URL del file durante il download.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**informazioni sulla firma del FIRMATARIo \_ \_**](signer-signature-info.md)
</dt> </dl>

 

 
