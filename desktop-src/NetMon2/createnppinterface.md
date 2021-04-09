---
description: La funzione CreateNPPInterface usa il BLOB restituito dal Finder per creare un oggetto NPP che può essere usato dall'applicazione.
ms.assetid: 41f48c72-3284-4ebc-baff-63553c8971e6
title: Funzione CreateNPPInterface (Netmon. h)
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
ms.openlocfilehash: d0efa1c33dd5e0778f13ddd59290de324c92e813
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967779"
---
# <a name="createnppinterface-function"></a>CreateNPPInterface (funzione)

La funzione **CreateNPPInterface** usa il BLOB restituito dal Finder per creare un oggetto NPP che può essere usato dall'applicazione.

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

*hBlob* \[ in\]
</dt> <dd>

Handle per il BLOB restituito dal Finder.

</dd> <dt>

*IID* \[ in\]
</dt> <dd>

Identificatore dell'interfaccia chiamata dall'oggetto NPP (ad esempio,**IRTC** o **IDelaydC**).

</dd> <dt>

*ppvObject* \[ out\]
</dt> <dd>

Puntatore al puntatore restituito all'interfaccia richiesta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.

Se la funzione ha esito negativo, il valore restituito è un valore NMERR che descrive l'errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




