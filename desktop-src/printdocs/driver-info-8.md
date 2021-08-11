---
description: Contiene informazioni sul driver della stampante.
ms.assetid: 6237def2-ffd4-4d93-b3a4-56f225793457
title: DRIVER_INFO_8 struttura (Winspool.h)
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
ms.openlocfilehash: 753b05b9d59bb98742d5c49102b604cc0a499a4dcdc6c624489d261400279297
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118234840"
---
# <a name="driver_info_8-structure"></a>Struttura DRIVER \_ INFO \_ 8

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

**Pname**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome del driver, ad esempio QMS 810.

</dd> <dt>

**pEnvironment**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica l'ambiente per cui è stato scritto il driver, ad esempio Windows x86, Windows IA64 e Windows x64.

</dd> <dt>

**pDriverPath**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica un nome di file o un percorso completo e un nome file per il file che contiene il driver di dispositivo (ad esempio, C: \\ DRIVERS \\Pscript.dll).

</dd> <dt>

**pDataFile**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica un nome file o un percorso completo e un nome file per il file che contiene i dati del driver (ad esempio, C: \\ DRIVERS \\ Qms810.ppd).

</dd> <dt>

**pConfigFile**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica un nome file o un percorso completo e un nome file per la libreria a collegamento dinamico di configurazione del driver di dispositivo (ad esempio, C: \\ DRIVERS \\Pscrptui.dll).

</dd> <dt>

**pHelpFile**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica un nome di file o un percorso completo e un nome file per il file della Guida del driver di dispositivo (ad esempio, C: \\ DRIVERS \\ Pscrptui.hlp).

</dd> <dt>

**pDependentFiles**
</dt> <dd>

Puntatore a un buffer MultiSZ che contiene una sequenza di stringhe con terminazione Null. Ogni stringa con terminazione Null nel buffer contiene il nome di un file da cui dipende il driver. La sequenza di stringhe viene terminata da una stringa vuota di lunghezza zero. Se **pDependentFiles** non è **NULL** e non contiene nomi di file, punta a un buffer che contiene due stringhe vuote.

</dd> <dt>

**pMonitorName**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica un monitoraggio della lingua, ad esempio "monitoraggio PJL". Questo membro può essere **NULL** e deve essere specificato solo per le stampanti in grado di comunicare bidirezionale.

</dd> <dt>

**pDefaultDataType**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il tipo di dati predefinito del processo di stampa, ad esempio "EMF".

</dd> <dt>

**pszzPreviousNames**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica i nomi dei driver della stampante precedenti compatibili con questo driver. Ad esempio, OldName1 \\ 0OldName2 \\ 0 \\ 0.

</dd> <dt>

**ftDriverDate**
</dt> <dd>

Data del pacchetto driver, come codificato nei file del driver.

</dd> <dt>

**dwlDriverVersion**
</dt> <dd>

Numero di versione del driver. Questo deriva dalla struttura della versione del driver.

</dd> <dt>

**pszMfgName**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome del produttore.

</dd> <dt>

**pszOEMUrl**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica l'URL del produttore.

</dd> <dt>

**pszHardwareID**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica l'ID hardware per il driver della stampante.

</dd> <dt>

**pszProvider**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il provider del driver della stampante, ad esempio "Microsoft Windows 2000".

</dd> <dt>

**pszPrintProcessor**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il processore di stampa, ad esempio "WinPrint".

</dd> <dt>

**pszVendorSetup**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica la DLL di installazione del driver del fornitore e il punto di ingresso.

</dd> <dt>

**pszzColorProfiles**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica i profili colori associati al driver.

</dd> <dt>

**pszInfPath**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il percorso del file inf del driver nell'archivio driver. Vedere la sezione Osservazioni. Deve essere **NULL se** DRIVER INFO \_ \_ 8 viene passato ad [**AddPrinterDriver**](addprinterdriver.md) o [**AddPrinterDriverEx.**](addprinterdriverex.md)

</dd> <dt>

**dwPrinterDriverAttributes**
</dt> <dd>

Flag di attributo per i driver della stampante. Deve essere 0 se DRIVER INFO 8 viene \_ passato ad \_ [**AddPrinterDriver**](addprinterdriver.md) o [**AddPrinterDriverEx.**](addprinterdriverex.md) In caso contrario, può essere qualsiasi combinazione dei flag seguenti:



| Nome/valore del flag                                                         | Significato                                                                                                                                                                                                                                                                                                                                             | Sistema operativo minimo                                             |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| IN GRADO DI \_ RICONOSCERE IL PACCHETTO DRIVER DELLA \_ \_ STAMPANTE<br/> 0x00000001<br/>        | Il driver della stampante fa parte di un pacchetto driver.                                                                                                                                                                                                                                                                                                     | Windows Vista                                          |
| XPS \_ DRIVER \_ DELLA STAMPANTE<br/> 0x00000002<br/>                   | Il driver della stampante supporta il formato Microsoft XPS descritto nella sezione [XML Paper Specification: Panoramica](/previous-versions/windows/hardware/design/dn641615(v=vs.85))e anche in Comportamento prodotto, sezione [<27>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43).                        | Windows 8<br/> Windows Server 2012<br/>    |
| SANDBOX \_ DRIVER DELLA STAMPANTE \_ \_ ABILITATA<br/> 0x00000004<br/>      | Il driver della stampante è compatibile con [l'isolamento del driver della stampante](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24). Per altre informazioni, vedere [la sezione Comportamento del prodotto <28>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43). | Windows 7<br/> Windows Server 2008 R2<br/> |
| CLASSE \_ DRIVER \_ STAMPANTE<br/> 0x00000008<br/>                 | Il driver della stampante è un [driver della stampante di classe](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).                                                                                                                                                                                       | Windows 8<br/> Windows Server 2012<br/>    |
| DRIVER \_ DELLA \_ STAMPANTE DERIVATO<br/> 0x00000010<br/>               | Il driver della stampante è un [driver della stampante derivato.](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24)                                                                                                                                                                                   | Windows 8<br/> Windows Server 2012<br/>    |
| DRIVER \_ DELLA STAMPANTE NON \_ \_ CONDIVISIBILE<br/> 0x00000020<br/>        | Le stampanti che utilizzano questo driver della stampante non possono essere condivise.                                                                                                                                                                                                                                                                                                | Windows 8<br/> Windows Server 2012<br/>    |
| PRINTER \_ DRIVER \_ CATEGORY \_ FAX<br/> 0x00000040<br/>         | Il driver della stampante è destinato all'utilizzo con [le stampanti fax](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).                                                                                                                                                                                    | Windows 8<br/> Windows Server 2012<br/>    |
| FILE DI \_ CATEGORIA DEL DRIVER DELLA \_ \_ STAMPANTE<br/> 0x00000080<br/>        | Il driver della stampante è destinato all'uso con [le stampanti di file](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).                                                                                                                                                                                  | Windows 8<br/> Windows Server 2012<br/>    |
| CATEGORIA \_ DI DRIVER DELLA STAMPANTE \_ \_ VIRTUALE<br/> 0x00000100<br/>     | Il driver della stampante è destinato all'uso con [le stampanti virtuali.](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24)                                                                                                                                                                            | Windows 8<br/> Windows Server 2012<br/>    |
| SERVIZIO CATEGORIA \_ \_ DRIVER \_ STAMPANTE<br/> 0x00000200<br/>     | Il driver della stampante è destinato all'uso con [le stampanti di servizio.](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24)                                                                                                                                                                            | Windows 8<br/> Windows Server 2012<br/>    |
| REIMPOSTAZIONE \_ DEL SOFT RESET DEL DRIVER DELLA STAMPANTE \_ \_ \_ NECESSARIA<br/> 0x00000400<br/> | Le stampanti che usano questo driver della stampante devono seguire le linee guida descritte nella definizione della classe di dispositivo USB. Per altre informazioni, vedere [La sezione Comportamento del prodotto <36>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43)                                                                      | Windows 8<br/> Windows Server 2012<br/>    |



 

</dd> <dt>

**pszzCoreDriverDependencies**
</dt> <dd>

Puntatore a una stringa multipla con terminazione Null che specifica tutti i driver principali della stampante da cui dipende il driver. Deve essere **NULL se** driver INFO **\_ \_ 8** viene passato ad [**AddPrinterDriver**](addprinterdriver.md) o [**AddPrinterDriverEx.**](addprinterdriverex.md)

</dd> <dt>

**ftMinInboxDriverVerDate**
</dt> <dd>

La data meno recente consentita di tutti i driver forniti con Windows e da cui dipende questo driver.

</dd> <dt>

**dwlMinInboxDriverVerVersion**
</dt> <dd>

La versione meno recente consentita di tutti i driver forniti con Windows e da cui dipende questo driver.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le stringhe per questi membri sono contenute nel file inf usato per aggiungere il driver.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ DRIVER \_ INFO \_ 8W** (Unicode) e **\_ DRIVER INFO \_ \_ 8A** (ANSI)<br/>                             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API Spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Addprinterdriver**](addprinterdriver.md)
</dt> <dt>

[**AddPrinterDriverEx**](addprinterdriverex.md)
</dt> </dl>

 

