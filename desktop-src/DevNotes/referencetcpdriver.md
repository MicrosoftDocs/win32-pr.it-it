---
description: Ottiene un riferimento a un oggetto driver TCP v4.
ms.assetid: 8f12fa58-1622-40d0-9a99-e7c8ede08b38
title: Funzione ReferenceTcpDriver
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
ms.openlocfilehash: 36329ecb695c6fcc011f7e1fe4f44a149fbeac48b0125c34330b9bde51342f5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690841"
---
# <a name="referencetcpdriver-function"></a>Funzione ReferenceTcpDriver

Ottiene un riferimento a un oggetto driver TCP v4.

## <a name="syntax"></a>Sintassi


```C++
NTSTATUS WINAPI ReferenceTcpDriver(
  _Out_ PDRIVER_OBJECT *ppDriverObject
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppDriverObject* \[ Cambio\]
</dt> <dd>

Puntatore a una **struttura DRIVER \_ OBJECT.** Per altre informazioni, vedere la documentazione relativa a WDK.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce **STATUS \_ SUCCESS**. Se ha esito negativo, restituirà il codice di stato appropriato.

## <a name="remarks"></a>Commenti

Questa funzione può essere chiamata solo dalla modalità kernel. Il chiamante deve decrementare il conteggio dei riferimenti chiamando la **funzione ObDereferenceObject** quando termina con l'oggetto .

Questa funzione viene implementata in Drvref.lib, disponibile per il download. Vedere [Windows libreria API di riferimento ai driver di rete.](https://www.microsoft.com/downloads/details.aspx?FamilyID=85037e05-f8f8-46b4-a013-3aa6248396c0)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Libreria<br/> | <dl> <dt>Drvref.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RiferimentoTcpDriverV6**](referencetcpdriverv6.md)
</dt> </dl>

 

 




