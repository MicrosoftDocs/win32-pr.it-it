---
title: Struttura MPCOMPONENT_VERSION (MpClient. h)
description: Tempo di aggiornamento e versione per un singolo componente.
ms.assetid: 43468230-EE13-4630-8C09-F8DF983EF748
keywords:
- Struttura MPCOMPONENT_VERSION le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPCOMPONENT_VERSION
topic_type:
- apiref
api_name:
- MPCOMPONENT_VERSION
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a1d4b5011bb185dc8ca0892e0a0e65bc4a7d8b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964166"
---
# <a name="mpcomponent_version-structure"></a>Struttura della versione di MPCOMPONENT \_

Tempo di aggiornamento e versione per un singolo componente.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMPCOMPONENT_VERSION {
  ULONGLONG      Version;
  ULARGE_INTEGER UpdateTime;
} MPCOMPONENT_VERSION, *PMPCOMPONENT_VERSION;
```



## <a name="members"></a>Members

<dl> <dt>

**Versione**
</dt> <dd>

Tipo: **ULONGLONG**

</dd> <dd>

Campo della versione. Ogni **parola** rappresenta Major, minor, Build e Revision.

</dd> <dt>

**UpdateTime**
</dt> <dd>

Tipo: **ULARGE \_ Integer**

</dd> <dd>

Ora dell'ultimo aggiornamento del componente, nel formato **FILETIME** .

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





