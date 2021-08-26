---
description: Recupera un handle di oggetto per l'oggetto specificato associato al processo specificato.
ms.assetid: c7b371c3-02c0-4137-ad9d-dd07a74fe2a5
title: Funzione ObFindHandleForObject (Ntosp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObFindHandleForObject
api_type:
- LibDef
api_location:
- Ntoskrnl.lib
- Ntoskrnl.dll
ms.openlocfilehash: 481def34e3e8656205eefe96058fe3c7558d2c898c7e05ddc78f9a67435c507e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984151"
---
# <a name="obfindhandleforobject-function"></a>Funzione ObFindHandleForObject

\[Questa funzione è obsoleta e può essere modificata o non disponibile nelle versioni future di Windows. Evitare di usare questa funzione.\]

Recupera un handle di oggetto per l'oggetto specificato associato al processo specificato.

## <a name="syntax"></a>Sintassi


```C++
BOOLEAN WINAPI ObFindHandleForObject(
  _In_     PEPROCESS Process,
  _In_     PVOID     Object,
  _In_opt_ PVOID     Reserved1,
  _In_opt_ PVOID     Reserved2,
  _Out_    PHANDLE   Handle
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Processo* \[ Pollici\]
</dt> <dd>

Processo. Questo handle viene restituito dalla **funzione IoGetCurrentProcess** **o PsGetCurrentProcess.**

</dd> <dt>

*Oggetto* \[ Pollici\]
</dt> <dd>

Puntatore all'oggetto .

</dd> <dt>

*Riservato1* \[ in, facoltativo\]
</dt> <dd>

Riservato.

</dd> <dt>

*Riservato2* \[ in, facoltativo\]
</dt> <dd>

Riservato.

</dd> <dt>

*Handle* \[ Cambio\]
</dt> <dd>

Handle dell'oggetto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce **TRUE se** viene trovata una corrispondenza e FALSE in **caso contrario.**

## <a name="remarks"></a>Commenti

Questa funzione è disponibile in Ntoskrnl.exe e può essere chiamata solo dalla modalità kernel. La libreria di importazione corrispondente è disponibile tramite Windows Driver Kit (WDK).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Ntosp.h</dt> </dl>      |
| Libreria<br/>                  | <dl> <dt>Ntoskrnl.lib</dt> </dl> |



 

 




