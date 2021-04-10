---
description: Contiene informazioni su una firma digitale.
ms.assetid: 0b86fdf9-533f-4640-8c70-c3c8f4ef2c68
title: Struttura SIGNER_SIGNATURE_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_SIGNATURE_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8e2b1fa68da51a649a01d4356ebfb1519ceeffb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231707"
---
# <a name="signer_signature_info-structure"></a>Struttura delle \_ informazioni sulla firma del firmatario \_

La struttura delle **\_ \_ informazioni sulla firma del firmatario** contiene informazioni su una firma digitale.

> [!Note]  
> Questa struttura non è definita in alcun file di intestazione. Per usare questa struttura, è necessario definirla come illustrato in questo argomento.

 

## <a name="syntax"></a>Sintassi


```C++
typedef struct _SIGNER_SIGNATURE_INFO {
  DWORD             cbSize;
  ALG_ID            algidHash;
  DWORD             dwAttrChoice;
  union {
    SIGNER_ATTR_AUTHCODE *pAttrAuthcode;
  };
  PCRYPT_ATTRIBUTES psAuthenticated;
  PCRYPT_ATTRIBUTES psUnauthenticated;
} SIGNER_SIGNATURE_INFO, *PSIGNER_SIGNATURE_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**cbSize**
</dt> <dd>

Dimensione, in byte, della struttura.

</dd> <dt>

**algidHash**
</dt> <dd>

Algoritmo hash utilizzato per la firma digitale.

</dd> <dt>

**dwAttrChoice**
</dt> <dd>

Specifica se la firma ha attributi [*Authenticode*](../secgloss/a-gly.md) . Il membro può essere costituito da uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                                                      | Significato                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_AUTHCODE_ATTR"></span><span id="signer_authcode_attr"></span><dl> <dt>**\_ Firmatario AUTHCODE \_ attr**</dt> <dt>1</dt> </dl> | Firma con attributi [*Authenticode*](../secgloss/a-gly.md) .<br/>           |
| <span id="SIGNER_NO_ATTR"></span><span id="signer_no_attr"></span><dl> <dt>**\_ Firmatario Nessun \_ attr**</dt> <dt>0</dt> </dl>                   | La firma non ha attributi [*Authenticode*](../secgloss/a-gly.md) .<br/> |



 

</dd> <dt>

**pAttrAuthcode**
</dt> <dd>

Specifica gli attributi per una firma [*Authenticode*](../secgloss/a-gly.md) . Questo membro è obbligatorio se il valore del membro **dwAttrChoice** è **Signer \_ AUTHCODE \_ attr**.

</dd> <dt>

**psAuthenticated**
</dt> <dd>

Attributi specificati dall'utente autenticati aggiunti alla firma digitale.

</dd> <dt>

**psUnauthenticated**
</dt> <dd>

Attributi non autenticati specificati dall'utente aggiunti alla firma digitale.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SignerSign**](signersign.md)
</dt> <dt>

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 
