---
description: La funzione ExpertGetStartupInfo recupera le informazioni di configurazione di avvio per l'esperto.
ms.assetid: 15f080ed-50b7-40c6-b283-dbe416a2b0e9
title: Funzione ExpertGetStartupInfo (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertGetStartupInfo
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7e4327965dce1c4bca07846a818609e555c16a3a27b0a19204a9971eaf9d642e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366883"
---
# <a name="expertgetstartupinfo-function"></a>Funzione ExpertGetStartupInfo

La **funzione ExpertGetStartupInfo** recupera le informazioni di configurazione di avvio per l'esperto.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI ExpertGetStartupInfo(
  _In_  HEXPERTKEY         hExpertKey,
  _Out_ PEXPERTSTARTUPINFO pExpertStartupInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hExpertKey* \[ Pollici\]
</dt> <dd>

Identificatore univoco dell'esperto. Network Monitor passa *hExpertKey* all'esperto quando chiama la [funzione](run.md) Run.

</dd> <dt>

*pExpertStartupInfo* \[ Cambio\]
</dt> <dd>

Puntatore a una [struttura EXPERTSTARTUPINFO](expertstartupinfo.md) che contiene informazioni di avvio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito è NMERR.

## <a name="remarks"></a>Commenti

La **funzione ExpertGetStartupInfo** viene usata se l'esperto deve determinare le informazioni di avvio usate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




