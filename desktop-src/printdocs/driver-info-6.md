---
description: La \_ struttura informazioni driver \_ 6 contiene informazioni sul driver della stampante.
ms.assetid: 9771cbb5-caaa-4b7d-9a96-d24234440bac
title: Struttura DRIVER_INFO_6 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_6
- _DRIVER_INFO_6A
- _DRIVER_INFO_6W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 20edef2aca2c6948984f5195b16711b78112354a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311539"
---
# <a name="driver_info_6-structure"></a>\_Struttura informazioni driver \_ 6

La **struttura \_ informazioni driver \_ 6** contiene informazioni sul driver della stampante.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _DRIVER_INFO_6 {
  DWORD     cVersion;
  LPTSTR    pName;
  LPTSTR    pEnvironment;
  LPTSTR    pDriverPath;
  LPTSTR    pDataFile;
  LPTSTR    pConfigFile;
  LPTSTR    pHelpFile;
  LPTSTR    pDependentFiles;
  LPTSTR    pMonitorName;
  LPTSTR    pDefaultDataType;
  LPTSTR    pszzPreviousNames;
  FILETIME  ftDriverDate;
  DWORDLONG dwlDriverVersion;
  LPTSTR    pszMfgName;
  LPTSTR    pszOEMUrl;
  LPTSTR    pszHardwareID;
  LPTSTR    pszProvider;
} DRIVER_INFO_6, *PDRIVER_INFO_6, *LPDRIVER_INFO_6;
```



## <a name="members"></a>Members

<dl> <dt>

**cVersion**
</dt> <dd>

Versione del sistema operativo per cui è stato scritto il driver. Il valore supportato è 3.

</dd> <dt>

**pName**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome del driver (ad esempio, QMS 810).

</dd> <dt>

**pEnvironment**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica l'ambiente per il quale è stato scritto il driver, ad esempio Windows NT x86, Windows IA64 e Windows x64.

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

Puntatore a una stringa con terminazione null che specifica un nome file o un percorso completo e un nome file per il file della guida del driver di dispositivo (ad esempio, C: \\ drivers \\ PSCRPTUI. hlp).

</dd> <dt>

**pDependentFiles**
</dt> <dd>

Puntatore a un buffer MultiSZ che contiene una sequenza di stringhe con terminazione null. Ogni stringa con terminazione null nel buffer contiene il nome di un file da cui dipende il driver. La sequenza di stringhe termina con una stringa vuota di lunghezza zero. Se **pDependentFiles** non è **null** e non contiene nomi di file, punterà a un buffer contenente due stringhe vuote.

</dd> <dt>

**pMonitorName**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica un monitor del linguaggio (ad esempio, "monitoraggio PJL"). Questo membro può essere **null** e deve essere specificato solo per le stampanti in grado di comunicare bidirezionale.

</dd> <dt>

**pDefaultDataType**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il tipo di dati predefinito del processo di stampa, ad esempio "EMF".

</dd> <dt>

**pszzPreviousNames**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica i nomi dei driver della stampante precedenti compatibili con questo driver. Ad esempio, OldName1 \\ 0OldName2 \\ 0 \\ 0.

</dd> <dt>

**ftDriverDate**
</dt> <dd>

Data del pacchetto di driver, come codificato nei file del driver.

</dd> <dt>

**dwlDriverVersion**
</dt> <dd>

Numero di versione del driver. Questo deriva dalla struttura della versione del driver.

</dd> <dt>

**pszMfgName**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome del produttore.

</dd> <dt>

**pszOEMUrl**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica l'URL per il produttore.

</dd> <dt>

**pszHardwareID**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica l'ID hardware per il driver della stampante.

</dd> <dt>

**pszProvider**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il provider del driver della stampante (ad esempio, "Microsoft Windows 2000")

</dd> </dl>

## <a name="remarks"></a>Commenti

Le stringhe per questi membri sono contenute nel file con estensione inf utilizzato per aggiungere il driver.

Se si chiama [**AddPrinterDriver**](addprinterdriver.md) o [**AddPrinterDriverEx**](addprinterdriverex.md) con un *livello* diverso da 6 e quindi si chiama [**GetPrinterDriver**](getprinterdriver.md) o [**EnumPrinterDrivers**](enumprinterdrivers.md) con *Level* uguale a 6, viene restituita la struttura **info del driver \_ \_ 6** con **pszMfgName**, **pszOEMUrl**, **pszHardwareID** e **pszProvider** impostati su **null**, **dwlDriverVersion** impostato su 0 e **ftDriverDate** impostato su (0, 0).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ Informazioni sul driver \_ \_ 6W** (Unicode) e **\_ informazioni sul driver \_ \_ 6a** (ANSI)<br/>                             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**AddPrinterDriverEx**](addprinterdriverex.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**GetPrinterDriver**](getprinterdriver.md)
</dt> </dl>

 

 




