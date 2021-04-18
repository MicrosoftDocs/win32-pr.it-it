---
description: La struttura EXPERTCONFIG contiene i dati di configurazione dell'esperto. L'esperto sovrappone il membro RawConfigData con una struttura specifica dell'esperto.
ms.assetid: 6167e846-d58c-40a8-94f7-c6d6185ae724
title: Struttura EXPERTCONFIG (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTCONFIG
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 293bdf4c792c10232564a7ba6386df430e81ecb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305952"
---
# <a name="expertconfig-structure"></a>Struttura EXPERTCONFIG

La struttura **EXPERTCONFIG** contiene i dati di configurazione dell'esperto. L'esperto sovrappone il membro **RawConfigData** con una struttura specifica dell'esperto.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  DWORD RawConfigLength;
  BYTE  RawConfigData[];
} EXPERTCONFIG, *PEXPERTCONFIG;
```



## <a name="members"></a>Members

<dl> <dt>

**RawConfigLength**
</dt> <dd>

Lunghezza totale della struttura, inclusi i quattro byte utilizzati per il membro. Network Monitor usa il valore quando la struttura viene salvata e letta da un'unità disco.

</dd> <dt>

**RawConfigData**
</dt> <dd>

Dati di configurazione. L'esperto deve aggiungere i dati di configurazione. Si supponga, ad esempio, di disporre di una struttura di dati simile alla seguente.

``` syntax
typedef struct
{
    DWORD       RawConfigLength;   // Overlay of structure
    DWORD       PickNumEvents;
    DWORD       NumEventsSpecific;
    DWORD       PickSpeedThroughCapture;
    DWORD       PickStartup;
    DWORD       PickAttachProperties;
} TESTEXPERTCONFIG;
typedef TESTEXPERTCONFIG* LPTESTEXPERTCONFIG;
```

Si noti che **RawConfigLength** garantisce che la sovrapposizione funzioni correttamente. Quando si usano i dati, il codice potrebbe essere simile al seguente:

``` syntax
BOOL WINAPI Configure( 
    HEXPERTKEY ExpertKey,
    PEXPERTCONFIG * ppConfig,
    PEXPERTSTARTUPINFO pStartupInfo,
    DWORD StartupFlags,
    HWND hWnd
)
{
    LPTESTEXPERTCONFIG  lpConfig;

    //...
    lpConfig = (LPTESTEXPERTCONFIG)(*ppConfig);
    //...
}
```

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




