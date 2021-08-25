---
description: La funzione Deregister export libera le risorse usate per creare il database delle proprietà del protocollo. La DLL del parser deve implementare La registrazione.
ms.assetid: 80852aed-07aa-440f-a537-f6cce461292e
title: Funzione di callback Deregister (Netmon.h)
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
ms.openlocfilehash: cb06ab6e08a674a186bcdb260140915c378db9affc13b17db33d9132109cec78
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911221"
---
# <a name="deregister-callback-function"></a>Funzione di callback di annullamento della registrazione

La **funzione Deregister** export libera le risorse usate per creare il database delle [*proprietà del protocollo*](p.md). La DLL del parser deve implementare **Deregister**.

## <a name="syntax"></a>Sintassi


```C++
VOID Deregister(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hProtocol* \[ Pollici\]
</dt> <dd>

Handle del protocollo per un database specifico.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

No.

## <a name="remarks"></a>Osservazioni

Network Monitor chiama **Deregister dopo** aver passato tutte le informazioni di acquisizione alla DLL del parser. La DLL del parser deve implementare una **funzione Deregister** per ogni protocollo supportato dal parser.

Quando si implementa **Deregister**, la DLL del parser deve chiamare la [funzione DestroyPropertyDatabase](destroypropertydatabase.md) per rilasciare le risorse [*del database delle*](p.md) proprietà.



| Per informazioni su                                        | Vedere                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| Che cosa sono i parser e come funzionano con Network Monitor. | [Parser](parsers.md)                                 |
| Punti di ingresso inclusi nella DLL del parser.        | [Architettura della DLL del parser](parser-dll-architecture.md) |
| Come implementare **La registrazione include**  un esempio.     | [Implementazione dell'annullamento della registrazione](implementing-deregister.md) |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[DestroyPropertyDatabase](destroypropertydatabase.md)
</dt> </dl>

 

 




