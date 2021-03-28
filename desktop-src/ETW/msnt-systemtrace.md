---
description: Classe padre dalla quale vengono derivate tutte le classi di traccia degli eventi di sistema. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 27979d9c-eca7-426f-8f8e-99443e5a0188
title: Classe MSNT_SystemTrace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSNT_SystemTrace
- MSNT_SystemTrace.Flags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2eb0044029761a93a353a08a955d39d76c267f9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977818"
---
# <a name="msnt_systemtrace-class"></a>\_Classe MSNT SystemTrace

Classe padre dalla quale vengono derivate tutte le classi di traccia degli eventi di sistema.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Guid("{9e814aad-3204-11d2-9a82-006008a86939}")]
class MSNT_SystemTrace : EventTrace
{
  uint32 Flags;
};
```

## <a name="members"></a>Members

La **classe \_ SystemTrace di MSNT** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ SystemTrace di MSNT** dispone di queste proprietà.

<dl> <dt>

**Flag**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **DefineValues {" \_ \_ processo flag di traccia eventi \_ ", " \_ \_ thread flag \_ di traccia eventi", \_ " \_ \_ caricamento immagine flag di traccia eventi \_ ", " \_ \_ \_ contatori processo flag di traccia eventi \_ ", " \_ flag di traccia evento \_ \_ CSWITCH", " \_ flag di traccia evento \_ \_ DPC", " \_ \_ interrupt flag di traccia evento \_ ", " \_ flag di traccia eventi \_ \_ SYSTEMCALL", "flag di traccia eventi i/o \_ \_ \_ disco \_ ", "flag di traccia eventi i/o \_ \_ \_ \_ file disco \_ ", " \_ flag di traccia evento \_ \_ disco \_ io \_ init", "Event \_ trace \_ flag \_ dispatcher", "EVENT \_ trace \_ flag \_ Memory \_ Page \_ fault", "Event \_ trace flag memoria hardware", \_ \_ \_ \_ "EVENT \_ trace \_ flag \_ virtual \_ Alloc", "Event \_ trace \_ flag \_ Network \_ tcpip" \_ Registro di traccia eventi registro di \_ \_ sistema "," \_ flag di traccia evento \_ \_ ALPC "," \_ flag di traccia evento \_ \_ split \_ io "," \_ \_ driver di traccia di traccia eventi \_ "," \_ profilo contrassegno di traccia eventi "," i/o file flag di traccia eventi " \_ \_ \_ \_ \_ \_ ," \_ traccia eventi \_ flag \_ file \_ io \_ init "}**, **ValueMap {" 0x00000001 "," 0x00000002 "," 0x00000004 "," 0x00000008 "," 0x00000010 "," 0x00000020 "," 0x00000040 "," 0x00000080 "," 0x00000100 " , "0x00000200", "0x00000400", "0x00000800", "0x00001000", "0x00002000", "0x00004000", "0x00010000", "** 0x00020000", "0x00100000", "0x00200000", "0x00800000", "0x01000000", "0x02000000", "0x04000000"}
</dt> </dl>

Abilita flag che indica i provider di kernel abilitati.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



 

 




