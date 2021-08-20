---
description: Specifica gli attributi per una firma Authenticode.
ms.assetid: 1c1052c3-c5c5-48ae-8266-0b367800a84a
title: SIGNER_ATTR_AUTHCODE struttura
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
ms.openlocfilehash: 2cce522403e4b4e416bd3d1ecb9d6c4a551ef3bb67407f853f586bd061f3d8e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898948"
---
# <a name="signer_attr_authcode-structure"></a>Struttura \_ SIGNER ATTR \_ AUTHCODE

La **struttura \_ SIGNER ATTR \_ AUTHCODE** specifica gli attributi per una [*firma Authenticode.*](../secgloss/a-gly.md)

> [!Note]  
> Questa struttura non è definita in alcun file di intestazione. Per usare questa struttura, è necessario definirla manualmente come illustrato in questo argomento.

 

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

Dimensione, in byte, della struttura .

</dd> <dt>

**fCommercial**
</dt> <dd>

**TRUE** per firmare l'oggetto come editore commerciale; in caso contrario, **FALSE.**

</dd> <dt>

**fIndividual**
</dt> <dd>

**TRUE** per firmare l'oggetto come singolo autore. in caso contrario, **FALSE.**

</dd> <dt>

**pwszName**
</dt> <dd>

Nome visualizzato del file al momento del download.

</dd> <dt>

**pwszInfo**
</dt> <dd>

Nome visualizzato dell'URL del file al momento del download.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INFORMAZIONI SULLA \_ FIRMA DEL \_ FIRMATARIO**](signer-signature-info.md)
</dt> </dl>

 

 
