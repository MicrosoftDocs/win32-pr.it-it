---
description: Recupera il tipo MAC dalla categoria NetworkInfo della sezione NPP del BLOB e converte i dati del tipo in un numero di tipo MAC.
ms.assetid: 53aa538c-69ee-4b34-93fb-9e61c6baadea
title: Funzione GetNPPMacTypeAsNumber (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPMacTypeAsNumber
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 9174b1deeb04d8d9665509daeff56d832d447892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525134"
---
# <a name="getnppmactypeasnumber-function"></a>GetNPPMacTypeAsNumber (funzione)

La funzione **GetNPPMacTypeAsNumber** Recupera il tipo Mac dalla categoria networkInfo della sezione NPP del BLOB e converte i dati del tipo in un numero di tipo Mac.

## <a name="syntax"></a>Sintassi


```C++
DWORD GetNPPMacTypeAsNumber(
  _In_  HBLOB   hBlob,
  _Out_ LPDWORD lpMacType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hBlob* \[ in\]
</dt> <dd>

Handle per il BLOB specificato.

</dd> <dt>

*lpMacType* \[ out\]
</dt> <dd>

Puntatore al tipo MAC.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.

Se il tag non è disponibile, il valore restituito è il \_ tipo Mac \_ Unknown.

## <a name="remarks"></a>Commenti

Questa funzione esegue il mapping del tag, **NPP: networkInfo: MacType** al **\_ tipo \_ \* Mac** come definito nel file Npptypes. h.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




