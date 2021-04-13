---
description: Contiene informazioni sul driver della stampante.
ms.assetid: 6237def2-ffd4-4d93-b3a4-56f225793457
title: Struttura DRIVER_INFO_8 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_8
- _DRIVER_INFO_8A
- _DRIVER_INFO_8W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 3cc174fdc8617a8ff59afc5a12740eaba715114f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349091"
---
# <a name="driver_info_8-structure"></a>\_Struttura informazioni driver \_ 8

Contiene informazioni sul driver della stampante.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _DRIVER_INFO_8 {
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
  LPTSTR    pszPrintProcessor;
  LPTSTR    pszVendorSetup;
  LPTSTR    pszzColorProfiles;
  LPTSTR    pszInfPath;
  DWORD     dwPrinterDriverAttributes;
  LPTSTR    pszzCoreDriverDependencies;
  FILETIME  ftMinInboxDriverVerDate;
  DWORDLONG dwlMinInboxDriverVerVersion;
} DRIVER_INFO_8, *PDRIVER_INFO_8, *LPDRIVER_INFO_8;
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

Puntatore a una stringa con terminazione null che specifica l'ambiente per il quale è stato scritto il driver, ad esempio Windows x86, Windows IA64 e Windows x64.

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

Puntatore a una stringa con terminazione null che specifica il provider del driver della stampante (ad esempio, "Microsoft Windows 2000").

</dd> <dt>

**pszPrintProcessor**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il processore di stampa, ad esempio "WinPrint".

</dd> <dt>

**pszVendorSetup**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica la DLL di installazione del driver del fornitore e il punto di ingresso.

</dd> <dt>

**pszzColorProfiles**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica i profili colori associati al driver.

</dd> <dt>

**pszInfPath**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il percorso del file. inf del driver nell'archivio driver. (Vedere la sezione Osservazioni). Deve essere **null** se il driver \_ info \_ 8 viene passato a [**AddPrinterDriver**](addprinterdriver.md) o [**AddPrinterDriverEx**](addprinterdriverex.md).

</dd> <dt>

**dwPrinterDriverAttributes**
</dt> <dd>

Flag di attributo per i driver della stampante. Deve essere 0 se il DRIVER \_ info \_ 8 viene passato a [**AddPrinterDriver**](addprinterdriver.md) o [**AddPrinterDriverEx**](addprinterdriverex.md). In caso contrario, può essere una qualsiasi combinazione dei flag seguenti:



| Nome/valore del flag                                                         | Significato                                                                                                                                                                                                                                                                                                                                             | Sistema operativo minimo                                             |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| compatibile con il \_ pacchetto driver della stampante \_ \_<br/> 0x00000001<br/>        | Il driver della stampante fa parte di un pacchetto driver.                                                                                                                                                                                                                                                                                                     | Windows Vista                                          |
| DRIVER della stampante \_ \_ XPS<br/> 0x00000002<br/>                   | Il driver della stampante supporta il formato XPS Microsoft descritto in [XML Paper Specification: Panoramica](/previous-versions/windows/hardware/design/dn641615(v=vs.85))e anche in [comportamento del prodotto, sezione <27>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43).                        | Windows 8<br/> Windows Server 2012<br/>    |
| \_sandbox driver della stampante \_ \_ abilitato<br/> 0x00000004<br/>      | Il driver della stampante è compatibile con l' [isolamento dei driver della stampante](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24). Per ulteriori informazioni, vedere il [comportamento del prodotto, sezione <28>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43). | Windows 7<br/> Windows Server 2008 R2<br/> |
| \_classe driver della stampante \_<br/> 0x00000008<br/>                 | Il driver della stampante è un [driver della stampante di classe](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).                                                                                                                                                                                       | Windows 8<br/> Windows Server 2012<br/>    |
| DRIVER della stampante \_ \_ derivato<br/> 0x00000010<br/>               | Il driver della stampante è un [driver della stampante derivato](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).                                                                                                                                                                                   | Windows 8<br/> Windows Server 2012<br/>    |
| DRIVER della stampante \_ \_ non \_ condivisibile<br/> 0x00000020<br/>        | Le stampanti che utilizzano questo driver della stampante non possono essere condivise.                                                                                                                                                                                                                                                                                                | Windows 8<br/> Windows Server 2012<br/>    |
| \_ \_ Fax categoria driver della stampante \_<br/> 0x00000040<br/>         | Il driver della stampante è destinato all'utilizzo con [stampanti fax](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).                                                                                                                                                                                    | Windows 8<br/> Windows Server 2012<br/>    |
| \_file di \_ categoria del driver della stampante \_<br/> 0x00000080<br/>        | Il driver della stampante è destinato all'uso con [stampanti di file](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).                                                                                                                                                                                  | Windows 8<br/> Windows Server 2012<br/>    |
| \_categoria driver della stampante \_ \_ virtuale<br/> 0x00000100<br/>     | Il driver della stampante è destinato all'uso con le [stampanti virtuali](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).                                                                                                                                                                            | Windows 8<br/> Windows Server 2012<br/>    |
| \_ \_ servizio categoria driver \_ stampanti<br/> 0x00000200<br/>     | Il driver della stampante è destinato all'uso con le [stampanti del servizio](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).                                                                                                                                                                            | Windows 8<br/> Windows Server 2012<br/>    |
| reimpostazione soft del driver della stampante \_ \_ \_ \_ obbligatoria<br/> 0x00000400<br/> | Le stampanti che utilizzano questo driver della stampante devono seguire le linee guida descritte nella definizione della classe dispositivo USB. Per ulteriori informazioni, vedere il [comportamento del prodotto, sezione <36>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43)                                                                      | Windows 8<br/> Windows Server 2012<br/>    |



 

</dd> <dt>

**pszzCoreDriverDependencies**
</dt> <dd>

Puntatore a una stringa multistringa con terminazione null che specifica tutti i driver della stampante di base da cui dipende il driver. Deve essere **null** se il **driver \_ info \_ 8** viene passato a [**AddPrinterDriver**](addprinterdriver.md) o [**AddPrinterDriverEx**](addprinterdriverex.md).

</dd> <dt>

**ftMinInboxDriverVerDate**
</dt> <dd>

Data più recente consentita di tutti i driver forniti con Windows e da cui dipende questo driver.

</dd> <dt>

**dwlMinInboxDriverVerVersion**
</dt> <dd>

La versione più recente consentita di tutti i driver forniti con Windows e da cui dipende questo driver.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le stringhe per questi membri sono contenute nel file con estensione inf utilizzato per aggiungere il driver.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ \_ Informazioni driver \_ 8W** (Unicode) e **\_ driver \_ info \_ 8a** (ANSI)<br/>                             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**AddPrinterDriverEx**](addprinterdriverex.md)
</dt> </dl>

 

