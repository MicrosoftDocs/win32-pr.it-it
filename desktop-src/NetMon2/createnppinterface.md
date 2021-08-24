---
description: La funzione CreateNPPInterface usa il BLOB restituito dal finder per creare un NPP che l'applicazione può usare.
ms.assetid: 41f48c72-3284-4ebc-baff-63553c8971e6
title: Funzione CreateNPPInterface (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateNPPInterface
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 03c2bb7fae0f68e6d38016df353266cfc9ec11757eeb98f6a5e41ab4316e63c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744541"
---
# <a name="createnppinterface-function"></a>Funzione CreateNPPInterface

La **funzione CreateNPPInterface usa** il BLOB restituito dal finder per creare un NPP che l'applicazione può usare.

## <a name="syntax"></a>Sintassi


```C++
DWORD CreateNPPInterface(
  _In_  HBLOB  hBlob,
  _In_  REFIID iid,
  _Out_ void   **ppvObject
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hBlob* \[ Pollici\]
</dt> <dd>

Handle per il BLOB restituito dal Finder.

</dd> <dt>

*iid* \[ in\]
</dt> <dd>

Identificatore dell'interfaccia chiamata dall'NPP , ad esempio **IRTC** o **IDelaydC.**

</dd> <dt>

*ppvObject* \[ Cambio\]
</dt> <dd>

Puntatore al puntatore restituito all'interfaccia richiesta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito è un valore NMERR che descrive l'errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Npptools.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




