---
description: Ottiene un riferimento a un oggetto driver TCP v6.
ms.assetid: 9f57ea0b-0ab4-4ef9-9bf1-1f41f72dfbe9
title: Funzione ReferenceTcpDriverV6
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
ms.openlocfilehash: 7c8fc1a24b812608db74fa16b8dafc323fe48442d61d7d7b35c0d371c0828ad3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571771"
---
# <a name="referencetcpdriverv6-function"></a>Funzione ReferenceTcpDriverV6

Ottiene un riferimento a un oggetto driver TCP v6.

## <a name="syntax"></a>Sintassi


```C++
NTSTATUS WINAPI ReferenceTcpDriverV6(
  _Out_ PDRIVER_OBJECT *ppDriverObject
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppDriverObject* \[ Cambio\]
</dt> <dd>

Puntatore a una **struttura DRIVER \_ OBJECT.** Per altre informazioni, vedere la documentazione di WDK.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce **STATUS \_ SUCCESS**. Se non riesce, restituirà il codice di stato appropriato.

## <a name="remarks"></a>Commenti

Questa funzione può essere chiamata solo dalla modalità kernel. Il chiamante deve decrementare il conteggio dei riferimenti chiamando la **funzione ObDereferenceObject** al termine dell'oggetto.

Questa funzione viene implementata in Drvref.lib, disponibile per il download. Vedere [Windows libreria API di riferimento del driver di rete](https://www.microsoft.com/downloads/details.aspx?FamilyID=85037e05-f8f8-46b4-a013-3aa6248396c0).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Libreria<br/> | <dl> <dt>Drvref.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ReferenceTcpDriver**](referencetcpdriver.md)
</dt> </dl>

 

 




