---
description: La struttura ENTRYPOINTS definisce i punti di ingresso alle funzioni di esportazione utilizzate da Network Monitor per il funzionamento del parser.
ms.assetid: e2ac118d-e04b-489f-877f-84cc9888f8af
title: Struttura ENTRYPOINTS (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ENTRYPOINTS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3eebee878cd907ee20674224a969c82038f4ac6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966484"
---
# <a name="entrypoints-structure"></a>Struttura ENTRYPOINTS

La struttura **ENTRYPOINTS** definisce i punti di ingresso alle funzioni di esportazione utilizzate da Network Monitor per il funzionamento del parser.

## <a name="syntax"></a>Sintassi


```C++
typedef struct __ENTRYPOINTS {
  REGISTER         Register;
  DEREGISTER       Deregister;
  RECOGNIZEFRAME   RecognizeFrame;
  ATTACHPROPERTIES AttachProperties;
  FORMATPROPERTIES FormatProperties;
} ENTRYPOINTS, *LPENTRYPOINTS;
```



## <a name="members"></a>Members

<dl> <dt>

**Registra**
</dt> <dd>

Puntatore all'implementazione della funzione dell' [*esperto di registrazione*](register-expert.md) .

</dd> <dt>

**Annullamento registrazione**
</dt> <dd>

Puntatore all'implementazione della funzione di [**annullamento della registrazione**](deregister.md) .

</dd> <dt>

**RecognizeFrame**
</dt> <dd>

Puntatore all'implementazione della funzione di esportazione [**RecognizeFrame**](recognizeframe.md) .

</dd> <dt>

**AttachProperties**
</dt> <dd>

Puntatore all'implementazione della funzione di esportazione [**AttachProperties**](attachproperties.md) .

</dd> <dt>

**FormatProperties**
</dt> <dd>

Puntatore all'implementazione della funzione di esportazione [**FormatProperties**](formatproperties.md) .

</dd> </dl>

## <a name="remarks"></a>Commenti

La funzione **CreateProtocol** usa la struttura **ENTRYPOINTS** per fornire i puntatori a Network Monitor. I puntatori devono essere specificati nell'ordine identificato nella sezione membri precedenti.

Non è necessario implementare la funzione [**FormatProperties**](formatproperties.md) se Network Monitor non visualizza mai i dati del protocollo. Ad esempio, non è necessario implementare **FormatProperties** se un'applicazione di esportazione usa l'output del parser e Network Monitor non Visualizza l'output.



| Per informazioni su                                        | Vedere                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| Quali sono i parser e come funzionano con Network Monitor. | [Parser](parsers.md)                                  |
| Come implementare **DllMain**  include un esempio.        | [Implementazione di DllMain](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[AttachProperties](attachproperties.md)
</dt> <dt>

[CreateProtocol](createprotocol.md)
</dt> <dt>

[Annullamento registrazione](deregister.md)
</dt> <dt>

[FormatProperties](formatproperties.md)
</dt> <dt>

[RecognizeFrame](recognizeframe.md)
</dt> <dt>

[Registra](register-parser.md)
</dt> </dl>

 

 




