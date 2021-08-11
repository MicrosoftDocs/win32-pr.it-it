---
description: La struttura DRIVER \_ INFO \_ 3 contiene informazioni sul driver della stampante.
ms.assetid: ccf87319-0bcf-4f71-8de3-0190459d2b0e
title: DRIVER_INFO_3 struttura (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_3
- _DRIVER_INFO_3A
- _DRIVER_INFO_3W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 8187b90ee9cc423051b8b57d942fa026cca6f8c3d3bbfabd7721ed204484cb71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118234913"
---
# <a name="driver_info_3-structure"></a>Struttura DRIVER \_ INFO \_ 3

La **struttura DRIVER INFO \_ \_ 3** contiene informazioni sul driver della stampante.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _DRIVER_INFO_3 {
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
} DRIVER_INFO_3, *PDRIVER_INFO_3;
```



## <a name="members"></a>Members

<dl> <dt>

**cVersion**
</dt> <dd>

Versione del sistema operativo per cui è stato scritto il driver. I valori supportati sono 3 e 4, che rappresentano rispettivamente i driver V3 e V4.

</dd> <dt>

**Pname**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome del driver, ad esempio "QMS 810".

</dd> <dt>

**pEnvironment**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica l'ambiente per cui è stato scritto il driver, ad esempio Windows x86, Windows IA64 e Windows x64.

</dd> <dt>

**pDriverPath**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica un nome di file o un percorso completo e un nome file per il file che contiene il driver di dispositivo, ad esempio "C: \\ DRIVERS \\Pscript.dll").

</dd> <dt>

**pDataFile**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica un nome di file o un percorso completo e un nome di file per il file che contiene i dati del driver, ad esempio "C: \\ DRIVERS \\ Qms810.ppd".

</dd> <dt>

**pConfigFile**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica un nome di file o un percorso completo e un nome file per la libreria a collegamento dinamico di configurazione del driver di dispositivo , ad esempio "C: \\ DRIVERS \\Pscrptui.dll").

</dd> <dt>

**pHelpFile**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica un nome di file o un percorso completo e un nome file per il file della Guida del driver di dispositivo.

</dd> <dt>

**pDependentFiles**
</dt> <dd>

Puntatore a un buffer MultiSZ che contiene una sequenza di stringhe con terminazione Null. Ogni stringa con terminazione Null nel buffer contiene il nome di un file da cui dipende il driver. La sequenza di stringhe viene terminata da una stringa vuota di lunghezza zero. Se **pDependentFiles** non è **NULL** e non contiene nomi di file, punta a un buffer che contiene due stringhe vuote.

</dd> <dt>

**pMonitorName**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica un monitoraggio del linguaggio, ad esempio "monitoraggio PJL". Questo membro può essere **NULL** e deve essere specificato solo per le stampanti in grado di comunicare bidirezionale.

</dd> <dt>

**pDefaultDataType**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il tipo di dati predefinito del processo di stampa, ad esempio "EMF".

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ DRIVER \_ INFO \_ 3W** (Unicode) e **\_ DRIVER INFO \_ \_ 3A** (ANSI)<br/>                             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API Spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Addprinterdriver**](addprinterdriver.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**Getprinterdriver**](getprinterdriver.md)
</dt> </dl>

 

 




