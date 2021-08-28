---
description: La funzione Register export deve essere implementata in tutte le DLL del parser. L'implementazione di Register crea e compila un database delle proprietà per un protocollo. Network Monitor usa il database per determinare le proprietà supportate dal protocollo.
ms.assetid: b8a2752d-30a6-48f2-90b3-b1430ae983d2
title: Funzione di callback Register Parser (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Register
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 4c24f719018f155fab26df4673b7dc3be18546675532657cb8fb3a0271763af2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128921"
---
# <a name="register-parser-callback-function"></a>Funzione di callback Register Parser

La **funzione register** export deve essere implementata in tutte le DLL del parser. L'implementazione **di Register** crea e compila un database [*delle proprietà*](p.md) per un protocollo. Network Monitor usa il database per determinare le proprietà supportate dal protocollo.

## <a name="syntax"></a>Sintassi


```C++
VOID Register(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hProtocol* \[ Pollici\]
</dt> <dd>

Handle del protocollo fornito Network Monitor quando si chiama **Register**. *L'handle hProtocol* è necessario quando si chiamano le funzioni helper di esportazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

No.

## <a name="remarks"></a>Osservazioni

Network Monitor inizia a chiamare la **funzione Register** non appena viene caricata un'acquisizione. Network Monitor chiama la **funzione Register** per ogni protocollo che può identificare. La [funzione CreateProtocol](createprotocol.md) passa un puntatore alla **funzione Register.**

L'implementazione **di Register** include chiamate alle funzioni seguenti.

-   Chiamata alle funzioni [CreatePropertyDatabase](createpropertydatabase.md) e [AddProperty](/previous-versions/bb251873(v=msdn.10)) per creare un database di tutte le proprietà supportate dal protocollo.
-   Una chiamata alla [funzione CreateHandoffTable](createhandofftable.md) è necessaria se il protocollo usa un [*set handoff*](h.md).

Se la DLL del parser contiene più parser e il parser può rilevare più di un protocollo, è necessario implementare una funzione **Register** per ogni protocollo.



| Per informazioni su                                        | Vedere                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| Che cosa sono i parser e come funzionano con Network Monitor. | [Parser](parsers.md)                                 |
| Punti di ingresso inclusi nella DLL del parser.        | [Architettura della DLL del parser](parser-dll-architecture.md) |
| Come implementare **Register include**  un esempio.       | [Implementazione del registro](implementing-register.md)     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[AddProperty](/previous-versions/bb251873(v=msdn.10))
</dt> <dt>

[CreateHandoffTable](createhandofftable.md)
</dt> <dt>

[CreatePropertyDatabase](createpropertydatabase.md)
</dt> <dt>

[CreateProtocol](createprotocol.md)
</dt> </dl>

 

