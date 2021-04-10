---
description: La funzione Deregister Export libera le risorse utilizzate per creare il database delle proprietà del protocollo. La DLL del parser deve implementare l'annullamento della registrazione.
ms.assetid: 80852aed-07aa-440f-a537-f6cce461292e
title: Annullare la registrazione della funzione di callback (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Deregister
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 9458ff74f29cd8eb7a75da0a3628a2dd1519ba43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227383"
---
# <a name="deregister-callback-function"></a>Annullare la registrazione della funzione di callback

La funzione **deregister** Export libera le risorse utilizzate per creare il database delle [*Proprietà*](p.md)del protocollo. La DLL del parser deve implementare l' **annullamento della registrazione**.

## <a name="syntax"></a>Sintassi


```C++
VOID Deregister(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hProtocol* \[ in\]
</dt> <dd>

Handle del protocollo per un database specifico.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

No.

## <a name="remarks"></a>Osservazioni

Network Monitor chiama la funzionalità di **annullamento della registrazione** dopo il passaggio di tutte le informazioni di acquisizione alla DLL del parser. La DLL del parser deve implementare una funzione di **annullamento della registrazione** per ogni protocollo supportato dal parser.

Quando si implementa la funzione di **annullamento della registrazione**, è necessario che la dll del parser chiami la funzione [DestroyPropertyDatabase](destroypropertydatabase.md) per rilasciare le risorse del [*database della proprietà*](p.md) .



| Per informazioni su                                        | Vedere                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| Quali sono i parser e come funzionano con Network Monitor. | [Parser](parsers.md)                                 |
| I punti di ingresso inclusi nella DLL del parser.        | [Architettura DLL parser](parser-dll-architecture.md) |
| Come implementare la **Deregistrazione**  è incluso un esempio.     | [Implementazione della deregistrazione](implementing-deregister.md) |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[DestroyPropertyDatabase](destroypropertydatabase.md)
</dt> </dl>

 

 




