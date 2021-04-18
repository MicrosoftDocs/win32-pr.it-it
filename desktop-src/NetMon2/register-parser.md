---
description: La funzione Register Export deve essere implementata in tutte le dll del parser. L'implementazione di Register crea e compila un database delle proprietà per un protocollo. Network Monitor utilizza il database per determinare le proprietà supportate dal protocollo.
ms.assetid: b8a2752d-30a6-48f2-90b3-b1430ae983d2
title: Funzione Register parser callback (Netmon. h)
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
ms.openlocfilehash: bc49cc083cf6ba46594473a041d9a1ad138efa22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310495"
---
# <a name="register-parser-callback-function"></a>Funzione di callback Register parser

La funzione **Register** Export deve essere implementata in tutte le dll del parser. L'implementazione di **Register** crea e compila un [*database delle proprietà*](p.md) per un protocollo. Network Monitor utilizza il database per determinare le proprietà supportate dal protocollo.

## <a name="syntax"></a>Sintassi


```C++
VOID Register(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hProtocol* \[ in\]
</dt> <dd>

Handle del protocollo fornito da Network Monitor quando si chiama **Register**. L'handle *hProtocol* è necessario quando si chiamano le funzioni di supporto di esportazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

No.

## <a name="remarks"></a>Osservazioni

Network Monitor inizia a chiamare la funzione **Register** non appena viene caricata un'acquisizione. Network Monitor chiama la funzione **Register** per ogni protocollo che può identificare. La funzione [CreateProtocol](createprotocol.md) passa un puntatore alla funzione **Register** .

L'implementazione del **Registro** include le chiamate alle funzioni seguenti.

-   Una chiamata alle funzioni [CreatePropertyDatabase](createpropertydatabase.md) e [AddProperty](/previous-versions/bb251873(v=msdn.10)) per creare un database di tutte le proprietà supportate dal protocollo.
-   Una chiamata alla funzione [CreateHandoffTable](createhandofftable.md) è obbligatoria se il protocollo usa un [*set di continuità*](h.md).

Se la DLL del parser contiene più parser e il parser è in grado di rilevare più di un protocollo, è necessario implementare una funzione **Register** per ogni protocollo.



| Per informazioni su                                        | Vedere                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| Quali sono i parser e come funzionano con Network Monitor. | [Parser](parsers.md)                                 |
| I punti di ingresso inclusi nella DLL del parser.        | [Architettura DLL parser](parser-dll-architecture.md) |
| Come implementare il **Registro**  è incluso un esempio.       | [Implementazione del registro](implementing-register.md)     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



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

 

