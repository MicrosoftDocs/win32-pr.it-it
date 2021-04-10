---
description: La \_ struttura informazioni driver \_ 4 contiene informazioni sul driver della stampante.
ms.assetid: 63000de6-74e7-4427-98d7-7bbd2dd61080
title: Struttura DRIVER_INFO_4 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_4
- _DRIVER_INFO_4A
- _DRIVER_INFO_4W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: b737947b19e93a6b8de0563128a0f1be412101ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227350"
---
# <a name="driver_info_4-structure"></a>\_Struttura informazioni driver \_ 4

La **struttura \_ informazioni driver \_ 4** contiene informazioni sul driver della stampante.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _DRIVER_INFO_4 {
  DWORD  cVersion;
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDriverPath;
  LPTSTR pDataFile;
  LPTSTR pConfigFile;
  LPTSTR pHelpFile;
  LPTSTR pDependentFiles;
  LPTSTR pMonitorName;
  LPTSTR pDefaultDataType;
  LPTSTR pszzPreviousNames;
} DRIVER_INFO_4, *PDRIVER_INFO_4;
```



## <a name="members"></a>Members

<dl> <dt>

**cVersion**
</dt> <dd>

Versione del sistema operativo per cui è stato scritto il driver. Il valore supportato è 3.

</dd> <dt>

**pName**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome del driver (ad esempio, "QMS 810").

</dd> <dt>

**pEnvironment**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica l'ambiente per il quale è stato scritto il driver (ad esempio, Windows x86, Windows IA64 e Windows x64).

</dd> <dt>

**pDriverPath**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica un nome file o un percorso completo e un nome file per il file contenente il driver di dispositivo (ad esempio, C: \\ drivers \\Pscript.dll).

</dd> <dt>

**pDataFile**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica un nome file o un percorso completo e un nome file per il file che contiene i dati del driver (ad esempio, C: \\ drivers \\ Qms810. PPD).

</dd> <dt>

**pConfigFile**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica un nome file o un percorso completo e un nome file per la libreria a collegamento dinamico della configurazione del driver di dispositivo (ad esempio, C: \\ drivers \\Pscrptui.dll).

</dd> <dt>

**pHelpFile**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica un nome file o un percorso completo e un nome file per il file della guida del driver di dispositivo.

</dd> <dt>

**pDependentFiles**
</dt> <dd>

Puntatore a un buffer MultiSZ che contiene una sequenza di stringhe con terminazione null. Ogni stringa con terminazione null nel buffer contiene il nome di un file da cui dipende il driver. La sequenza di stringhe termina con una stringa vuota di lunghezza zero. Se **pDependentFiles** non è **null** e non contiene nomi di file, punterà a un buffer contenente due stringhe vuote.

</dd> <dt>

**pMonitorName**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica un monitor del linguaggio (ad esempio, il monitoraggio di PJL). Questo membro può essere **null** e deve essere specificato solo per le stampanti in grado di comunicare bidirezionale.

</dd> <dt>

**pDefaultDataType**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il tipo di dati predefinito del processo di stampa, ad esempio EMF.

</dd> <dt>

**pszzPreviousNames**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica i nomi dei driver della stampante precedenti compatibili con questo driver. Ad esempio, OldName1 \\ 0OldName2 \\ 0 \\ 0.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ \_ Informazioni driver \_ 4W** (Unicode) e **\_ driver \_ info \_ 4a** (ANSI)<br/>                             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**GetPrinterDriver**](getprinterdriver.md)
</dt> </dl>

 

 




