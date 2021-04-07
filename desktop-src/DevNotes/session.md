---
description: La struttura della sessione contiene informazioni sulla sessione corrente.
ms.assetid: e04571f9-eeb7-4612-8cb2-05aca7b5df06
title: Struttura della sessione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SESSION
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9e1f356020df681e00f43c7a47ac16048764c0ab
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747671"
---
# <a name="session-structure"></a>Struttura della sessione

\[Questa struttura contiene le informazioni necessarie solo quando si usano le funzioni **DeleteExtractedFiles** ed **Extract** , che non sono supportate. Questa documentazione viene fornita solo a scopo informativo.\]

La struttura della **sessione** contiene informazioni sulla sessione corrente.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  ACTION    act;
  HFILELIST hflist;
  BOOL      fAllCabinets;
  BOOL      fOverwrite;
  BOOL      fNoLineFeed;
  BOOL      fSelfExtract;
  long      cbSelfExtractSize;
  long      cbSelfExtractSize;
  int       ahfSelf[cMAX_CAB_FILE_OPEN];
  int       cErrors;
  HFDI      hfdi;
  ERF       erf;
  long      cFiles;
  long      cbTotalBytes;
  PERROR    perr;
  SPILLERR  se;
  long      cbSpill;
  char      achSelf[cbFILE_NAME_MAX];
  char      achMsg[cbMAX_LINE*2];
  char      achLine;
  char      achLocation;
  char      achFile;
  char      achDest;
  char      achCabPath;
  BOOL      fContinuationCabinet;
  BOOL      fShowReserveInfo;
  BOOL      fNextCabCalled;
  CABINET   acab[2];
  char      achZap[cbFILE_NAME_MAX];
  char      achCabinetFile[cbFILE_NAME_MAX];
  int       cArgv;
  char      **pArgv;
  int       fDestructive;
  USHORT    iCurrentFolder;
} SESSION, *PSESSION;
```



## <a name="members"></a>Members

<dl> <dt>

**atto**
</dt> <dd>

l'azione da eseguire. Questo membro può essere uno dei valori del tipo enumerato seguente.

``` syntax
typedef enum {
    actBAD,         // Invalid action
    actHELP,        // Show help
    actDEFAULT,     // Perform default action based on command line arguments
    actDIRECTORY,   // Force display of cabinet directory
    actEXTRACT,     // Force file extraction
    actCOPY,        // Do single file-to-file copy
} ACTION;  
```

</dd> <dt>

**hflist**
</dt> <dd>

Handle per un elenco di file specificati nella riga di comando. Questo tipo di dati viene dichiarato nel modo seguente:

`typedef void *HFILELIST;`

</dd> <dt>

**fAllCabinets**
</dt> <dd>

Flag che indica se deve essere elaborato più di un file CAB. Se questo valore è **true**, vengono elaborati i file CAB di continuazione.

</dd> <dt>

**fOverwrite**
</dt> <dd>

Flag che indica se i file esistenti devono essere sovrascritti. Se questo valore è **true**, i file esistenti vengono sovrascritti.

</dd> <dt>

**fNoLineFeed**
</dt> <dd>

Flag che indica se l'ultima `printf` chiamata presenta i caratteri di nuova riga ( `\n` ). Se questo valore è **true**, l'ultima `printf` chiamata non include i caratteri di nuova riga.

</dd> <dt>

**fSelfExtract**
</dt> <dd>

Flag che indica se un file CAB è autoestraente. Se questo valore è **true**, l'archivio è autoestraente.

</dd> <dt>

**cbSelfExtractSize**
</dt> <dd>

Lunghezza della parte eseguibile (con estensione exe) di un cabinet autoestraente.

</dd> <dt>

**cbSelfExtractSize**
</dt> <dd>

Lunghezza della parte CAB di un cabinet autoestraente.

</dd> <dt>

**ahfSelf**
</dt> <dd>

Il file viene gestito nel file CAB.

`#define cMAX_CAB_FILE_OPEN    2 `

</dd> <dt>

**cErrors**
</dt> <dd>

Numero di errori rilevati durante la sessione di estrazione.

</dd> <dt>

**hfdi**
</dt> <dd>

Handle per il contesto IDE. Questo tipo di dati viene dichiarato nel modo seguente:

`typedef void FAR *HFDI; `

</dd> <dt>

**erf**
</dt> <dd>

Struttura degli errori di IDE. Vedere [**ERF**](/windows/win32/api/fdi_fci_types/ns-fdi_fci_types-erf).

</dd> <dt>

**cFiles**
</dt> <dd>

Numero di file elaborati.

</dd> <dt>

**cbTotalBytes**
</dt> <dd>

Numero totale di byte estratti.

</dd> <dt>

**perr**
</dt> <dd>

Il pass-through IDE.

</dd> <dt>

**Se**
</dt> <dd>

Errore di file. Questo membro può essere uno dei valori del tipo enumerato seguente.

``` syntax
typedef enum {
    seNONE,                     // No error
    seNOT_ENOUGH_MEMORY,        // Not enough RAM
    seCANNOT_CREATE,            // Cannot create spill file
    seNOT_ENOUGH_SPACE,         // Not enough space for spill file
} SPILLERR;
```

</dd> <dt>

**cbSpill**
</dt> <dd>

Dimensioni del file di fuoriuscita richiesto.

</dd> <dt>

**achSelf**
</dt> <dd>

Nome del file eseguibile (exe).

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

**achMsg**
</dt> <dd>

Buffer di formattazione del messaggio.

`#define cbMAX_LINE          256`

</dd> <dt>

**achLine**
</dt> <dd>

Buffer di formattazione della linea.

</dd> <dt>

**achLocation**
</dt> <dd>

La directory di output.

</dd> <dt>

**achFile**
</dt> <dd>

Nome file corrente da estrarre.

</dd> <dt>

**achDest**
</dt> <dd>

Nome del file di destinazione forzata.

</dd> <dt>

**achCabPath**
</dt> <dd>

Percorso da esaminare per un file CAB.

</dd> <dt>

**fContinuationCabinet**
</dt> <dd>

Flag che indica se il file CAB corrente è il primo elaborato. Se impostato su **true**, non è il primo file CAB elaborato.

</dd> <dt>

**fShowReserveInfo**
</dt> <dd>

Flag che indica se devono essere fornite informazioni riservate. Se impostato su **true**, le informazioni vengono rese disponibili.

</dd> <dt>

**fNextCabCalled**
</dt> <dd>

Questo membro fornisce un modo per determinare quali voci **Acab** usare se si elaborano tutti i file in un set di file CAB (**fAllCabinet** è impostato su **true**).

</dd> <dt>

**ACAB**
</dt> <dd>

Ultime due voci nel set di file CAB. Questa struttura viene definita nel modo seguente:

``` syntax
typedef struct {
    char    achCabPath[cbFILE_NAME_MAX];     // Cabinet file path
    char    achCabFilename[cbFILE_NAME_MAX]; // Cabinet file name.ext
    char    achDiskName[cbFILE_NAME_MAX];    // User readable disk label
    USHORT  setID;
    USHORT  iCabinet;
} CABINET;
typedef CABINET *PCABINET;
```

</dd> <dt>

**achZap**
</dt> <dd>

Prefisso da rimuovere dal nome del file.

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

**achCabinetFile**
</dt> <dd>

File CAB corrente.

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

**cArgv**
</dt> <dd>

Argc autoestraente predefinito.

</dd> <dt>

**pArgv**
</dt> <dd>

Puntatore a un puntatore al valore predefinito argv autoestraente \[ \] .

</dd> <dt>

**fDestructive**
</dt> <dd>

Flag che riduce al minimo lo spazio su disco necessario quando è impostato su **true**.

</dd> <dt>

**iCurrentFolder**
</dt> <dd>

Se **fDestructive** è impostato su **true**, estrarre solo la cartella corrente.

</dd> </dl>

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DeleteExtractedFiles**](deleteextractedfiles.md)
</dt> <dt>

[**Estrarre**](extract.md)
</dt> </dl>

 

 
