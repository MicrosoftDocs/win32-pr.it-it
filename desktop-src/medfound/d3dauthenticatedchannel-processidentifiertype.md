---
description: Specifica il tipo di processo identificato nella \_ struttura di output QUERYRESTRICTEDSHAREDRESOURCEPROCESS di D3DAUTHENTICATEDCHANNEL \_ .
ms.assetid: 8878905e-f55b-4dbc-9608-da0082daf673
title: Enumerazione D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 1b2fdb7384ff868b02f54650de9662b297ce39db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127938"
---
# <a name="d3dauthenticatedchannel_processidentifiertype-enumeration"></a>\_Enumerazione D3DAUTHENTICATEDCHANNEL PROCESSIDENTIFIERTYPE

Specifica il tipo di processo identificato nella struttura di [**\_ \_ output QUERYRESTRICTEDSHAREDRESOURCEPROCESS di D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-output.md) .

## <a name="syntax"></a>Sintassi


```C++
typedef enum  { 
  PROCESSIDTYPE_UNKNOWN  = 0,
  PROCESSIDTYPE_DWM      = 1,
  PROCESSIDTYPE_HANDLE   = 2
} D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="PROCESSIDTYPE_UNKNOWN"></span><span id="processidtype_unknown"></span>**PROCESSIDTYPE \_ sconosciuto**
</dt> <dd>

Tipo di processo sconosciuto.

</dd> <dt>

<span id="PROCESSIDTYPE_DWM"></span><span id="processidtype_dwm"></span>**PROCESSIDTYPE \_ DWM**
</dt> <dd>

Processo di Gestione finestre desktop (DWM).

</dd> <dt>

<span id="PROCESSIDTYPE_HANDLE"></span><span id="processidtype_handle"></span>**\_handle PROCESSIDTYPE**
</dt> <dd>

Handle per un processo.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                 |
| Intestazione<br/>                   | <dl> <dt>D3d9types. h (include d3d9. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni video Direct3D](direct3d-video-enumerations.md)
</dt> </dl>

 

 




