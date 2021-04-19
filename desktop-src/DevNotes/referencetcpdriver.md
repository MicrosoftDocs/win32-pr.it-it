---
description: Ottiene un riferimento a un oggetto driver TCP V4.
ms.assetid: 8f12fa58-1622-40d0-9a99-e7c8ede08b38
title: ReferenceTcpDriver (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReferenceTcpDriver
api_type:
- LibDef
api_location:
- Drvref.lib
ms.openlocfilehash: 4a9068739517cceedee72a675739b2d8b067b2ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332658"
---
# <a name="referencetcpdriver-function"></a>ReferenceTcpDriver (funzione)

Ottiene un riferimento a un oggetto driver TCP V4.

## <a name="syntax"></a>Sintassi


```C++
NTSTATUS WINAPI ReferenceTcpDriver(
  _Out_ PDRIVER_OBJECT *ppDriverObject
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppDriverObject* \[ out\]
</dt> <dd>

Puntatore a una struttura **di \_ oggetti driver** . Per ulteriori informazioni, vedere la documentazione relativa a WDK.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, viene restituito **lo stato \_ Success**. Se ha esito negativo, verrà restituito il codice di stato appropriato.

## <a name="remarks"></a>Commenti

Questa funzione può essere chiamata solo dalla modalità kernel. Il chiamante deve decrementare il conteggio dei riferimenti chiamando la funzione **ObDereferenceObject** al termine dell'oggetto.

Questa funzione è implementata in Drvref. lib, disponibile per il download. Vedere [libreria API di riferimento per il driver di rete Windows](https://www.microsoft.com/downloads/details.aspx?FamilyID=85037e05-f8f8-46b4-a013-3aa6248396c0).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Libreria<br/> | <dl> <dt>Drvref. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ReferenceTcpDriverV6**](referencetcpdriverv6.md)
</dt> </dl>

 

 




