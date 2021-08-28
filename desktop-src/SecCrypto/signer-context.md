---
description: Contiene un BLOB firmato.
ms.assetid: c12d9007-c779-4363-8e28-6387a665a0d6
title: SIGNER_CONTEXT struttura
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_CONTEXT
api_type:
- NA
api_location: ''
ms.openlocfilehash: c1c67733886aa44a9a4f2179b16fee36a95f4462876ebe5d873b5e9b0ff2d2a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117973584"
---
# <a name="signer_context-structure"></a>Struttura SIGNER \_ CONTEXT

La **struttura SIGNER \_ CONTEXT** contiene un OGGETTO [*BLOB firmato.*](../secgloss/b-gly.md)

> [!Note]  
> Questa struttura non è definita in alcun file di intestazione. Per usare questa struttura, è necessario definirla manualmente come illustrato in questo argomento.

 

## <a name="syntax"></a>Sintassi


```C++
typedef struct _SIGNER_CONTEXT {
  DWORD cbSize;
  DWORD cbBlob;
  BYTE  *pbBlob;
} SIGNER_CONTEXT, *PSIGNER_CONTEXT;
```



## <a name="members"></a>Members

<dl> <dt>

**cbSize**
</dt> <dd>

Dimensione, in byte, della struttura .

</dd> <dt>

**cbBlob**
</dt> <dd>

Dimensione, in byte, del **membro pbBlob.**

</dd> <dt>

**pbBlob**
</dt> <dd>

Puntatore al BLOB firmato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Firma del firmatario**](signersign.md)
</dt> <dt>

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 
