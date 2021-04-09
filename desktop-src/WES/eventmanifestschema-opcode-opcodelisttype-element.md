---
title: Elemento Opcode (OpcodeListType)
description: Contiene un valore numerico che identifica l'attività o un punto all'interno di un'attività che l'applicazione stava eseguendo durante la generazione dell'evento (ad esempio, l'inizializzazione o la chiusura).
ms.assetid: 8c5cfbd3-6a74-452c-a12f-41d663426e2c
keywords:
- opcode element EventLog
topic_type:
- apiref
api_name:
- opcode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e9d02b77b4a36bac26d52d7bf8d849eab8731d27
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121335"
---
# <a name="opcode-opcodelisttype-element"></a>Elemento Opcode (OpcodeListType)

Contiene un valore numerico che identifica l'attività o un punto all'interno di un'attività che l'applicazione stava eseguendo durante la generazione dell'evento (ad esempio, l'inizializzazione o la chiusura).

``` syntax
<xs:element name="opcode"
    type="OpcodeType"
 />
```

L'elemento **OpCode** è definito dal tipo complesso [**OpcodeListType**](eventmanifestschema-opcodelisttype-complextype.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Elementi padre**
</dt> <dt>

[**OpCodes (TaskType)**](eventmanifestschema-opcodes-tasktype-element.md)
</dt> <dt>

[**OpCodes (ProviderType)**](eventmanifestschema-opcodes-providertype-element.md)
</dt> <dt>

[**OpCodes (MetadataType)**](eventmanifestschema-opcodes-metadatatype-element.md)
</dt> </dl>

 

 





