---
description: La struttura DRIVER INFO 2 identifica un driver della stampante, il numero di versione del driver, l'ambiente per cui è stato scritto il driver, il nome del file in cui è archiviato il driver e \_ \_ così via.
ms.assetid: cca1227d-69b9-44df-8dac-384c2f8843ae
title: DRIVER_INFO_2 struttura (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_2
- _DRIVER_INFO_2A
- _DRIVER_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: dcb65f066286b5f5cd2fec935fb2223c25cf87fcc64d17de274b9b182a372440
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118732859"
---
# <a name="driver_info_2-structure"></a>Struttura DRIVER \_ INFO \_ 2

La **struttura DRIVER INFO \_ \_ 2** identifica un driver della stampante, il numero di versione del driver, l'ambiente per cui è stato scritto il driver, il nome del file in cui è archiviato il driver e così via.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _DRIVER_INFO_2 {
  DWORD  cVersion;
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDriverPath;
  LPTSTR pDataFile;
  LPTSTR pConfigFile;
} DRIVER_INFO_2, *PDRIVER_INFO_2;
```



## <a name="members"></a>Members

<dl> <dt>

**cVersion**
</dt> <dd>

Versione del sistema operativo per cui è stato scritto il driver. Il valore supportato è 3.

</dd> <dt>

**Pname**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome del driver, ad esempio "QMS 810".

</dd> <dt>

**pEnvironment**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica l'ambiente per cui è stato scritto il driver,ad esempio Windows x86, Windows IA64 e Windows x64).

</dd> <dt>

**pDriverPath**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica un nome file o un percorso completo e un nome file per il file che contiene il driver di dispositivo (ad esempio, "c: \\ drivers \\pscript.dll").

</dd> <dt>

**pDataFile**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica un nome di file o un percorso completo e un nome file per il file che contiene i dati del driver(ad esempio, "c: \\ drivers \\ Qms810.ppd").

</dd> <dt>

**pConfigFile**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica un nome di file o un percorso completo e un nome file per il .dll di configurazione del driver di dispositivo (ad esempio, "c: \\ drivers \\Pscrptui.dll").

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ DRIVER \_ INFO \_ 2W** (Unicode) e **\_ DRIVER INFO \_ \_ 2A** (ANSI)<br/>                             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API Spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Addprinterdriver**](addprinterdriver.md)
</dt> <dt>

[**Getprinterdriver**](getprinterdriver.md)
</dt> </dl>

 

 




