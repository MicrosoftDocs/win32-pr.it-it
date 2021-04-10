---
description: Recupera un handle di oggetto per l'oggetto specificato associato al processo specificato.
ms.assetid: c7b371c3-02c0-4137-ad9d-dd07a74fe2a5
title: Funzione ObFindHandleForObject (Ntosp. h)
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
ms.openlocfilehash: 7ba87d05d4264f3bb160bae16053a338e38e2145
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877433"
---
# <a name="obfindhandleforobject-function"></a>ObFindHandleForObject (funzione)

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

*Processo* \[ di in\]
</dt> <dd>

Processo. Questo handle viene restituito dalla funzione **IoGetCurrentProcess** o **PsGetCurrentProcess** .

</dd> <dt>

*Oggetto* \[ di in\]
</dt> <dd>

Puntatore all'oggetto.

</dd> <dt>

*Reserved1* \[ in, facoltativo\]
</dt> <dd>

Riservato.

</dd> <dt>

*Reserved2* \[ in, facoltativo\]
</dt> <dd>

Riservato.

</dd> <dt>

*Gestisci* \[ out\]
</dt> <dd>

Handle dell'oggetto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce **true** se viene trovata una corrispondenza e **false** in caso contrario.

## <a name="remarks"></a>Commenti

Questa funzione è disponibile in Ntoskrnl.exe e può essere chiamata solo dalla modalità kernel. La libreria di importazione corrispondente è disponibile tramite Windows Driver Kit (WDK).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Ntosp. h</dt> </dl>      |
| Libreria<br/>                  | <dl> <dt>Ntoskrnl. lib</dt> </dl> |



 

 




