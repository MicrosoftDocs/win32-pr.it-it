---
description: Ottiene un riferimento a un oggetto driver TCP V6.
ms.assetid: 9f57ea0b-0ab4-4ef9-9bf1-1f41f72dfbe9
title: ReferenceTcpDriverV6 (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReferenceTcpDriverV6
api_type:
- LibDef
api_location:
- Drvref.lib
ms.openlocfilehash: d0a3f56ea59eb753dc7a49d6f6b1d0c48be8abca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332367"
---
# <a name="referencetcpdriverv6-function"></a>ReferenceTcpDriverV6 (funzione)

Ottiene un riferimento a un oggetto driver TCP V6.

## <a name="syntax"></a>Sintassi


```C++
NTSTATUS WINAPI ReferenceTcpDriverV6(
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

[**ReferenceTcpDriver**](referencetcpdriver.md)
</dt> </dl>

 

 




