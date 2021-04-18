---
description: La classe del dispositivo comm/DataModel è costituita da dispositivi DataModel.
ms.assetid: 6bc314c6-30ec-4318-856a-3ab2fa6aadfb
title: comunicazione/datamode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89210bcf14931e3905f71cdbb8678f5519cc4c3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308313"
---
# <a name="commdatamodem"></a>comunicazione/datamode

La classe del dispositivo comm/DataModel è costituita da dispositivi DataModel. Per accedere a questi dispositivi, è possibile usare le funzioni [file](/windows/desktop/FileIO/file-management-functions) e [comunicazioni](/windows/desktop/DevIO/communications-functions). I dispositivi in questa classe sono associati a dispositivi line che supportano il \_ tipo di supporto LINEMEDIAMODE DATAmodel, specificato nel membro **dwMediaModes** della struttura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) per il dispositivo linea.

La funzione [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) compila una struttura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , impostando **dwStringFormat** sul \_ valore binario STRINGFORMAT e aggiungendo questi membri aggiuntivi:

``` syntax
HANDLE hComm;            // file handle to data modem
CHAR   szDeviceName[1];  // name of data modem
```

Il membro **hComm** è l'handle della porta di comunicazione aperta. Questo membro è **null** se la porta non è ancora aperta o se il parametro *dwSelect* di [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) non è il \_ valore della chiamata LINECALLSELECT. Se una chiamata è attiva, il provider di servizi di solito apre la porta stessa per ottenere il controllo diretto dell'hardware di comunicazione, ma è necessario solo per restituire un handle valido se la linea è connessa. Il provider di servizi apre la porta usando il \_ valore Overlapped del flag file \_ e quindi configura la porta usando le impostazioni specificate dalla funzione [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) . È possibile impostare altre opzioni di configurazione per il dispositivo usando le funzioni di comunicazione con l'handle restituito.

Il membro **szDeviceName** è una stringa con terminazione **null** che specifica il nome della porta di comunicazione associata alla riga, all'indirizzo o alla chiamata.

Se **hComm** è un handle valido, è possibile usarlo nelle chiamate successive alle funzioni di file, ad esempio [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) e [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), per inviare e ricevere dati sulla chiamata. Al termine dell'utilizzo della porta di comunicazione e preferibilmente prima di utilizzare la funzione [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) per deallocare la chiamata, è necessario chiudere la porta utilizzando la funzione [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .

Quando si usano le funzioni [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) e [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) , alcuni provider di servizi richiedono che i dati di configurazione per questa classe di dispositivo abbiano il formato seguente:

``` syntax
typedef struct  tagDEVCFG  {
  DEVCFGHDR   dfgHdr;
  COMMCONFIG  commconfig;
} DEVCFG, *PDEVCFG, FAR* LPDEVCFG;

// Device setting information
typedef struct  tagDEVCFGDR  {
  DWORD       dwSize;
  DWORD       dwVersion;
  WORD        fwOptions;
  WORD        wWaitBong;
} DEVCFGHDR;
```

Di seguito sono riportate le informazioni di configurazione del dispositivo da usare con le funzioni [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) e [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) .

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Somma delle dimensioni della struttura **DEVCFGHDR** e delle dimensioni effettive della struttura [**COMMCONFIG**](/windows/desktop/api/winbase/ns-winbase-commconfig) .

</dd> <dt>

<span id="dwVersion"></span><span id="dwversion"></span><span id="DWVERSION"></span>**dwVersion**
</dt> <dd>

Numero di versione della struttura **DEVCONFIG** UniModel. Questo membro può essere MDMCFG \_ Version (0x00010003).

</dd> <dt>

<span id="fwOptions"></span><span id="fwoptions"></span><span id="FWOPTIONS"></span>**fwOptions**
</dt> <dd>

Flag di opzione visualizzati nella pagina di opzioni UniModel. Questo membro può essere una combinazione di questi valori:

<dl> <dt>

<span id="TERMINAL_PRE__1_"></span><span id="terminal_pre__1_"></span>PRE-terminale \_ (1)
</dt> <dd>

Visualizza la schermata pre-terminale.

</dd> <dt>

<span id="TERMINAL_POST__2_"></span><span id="terminal_post__2_"></span>POST del terminale \_ (2)
</dt> <dd>

Visualizza la schermata post-terminale.

</dd> <dt>

<span id="MANUAL_DIAL__4_"></span><span id="manual_dial__4_"></span>\_Composizione manuale (4)
</dt> <dd>

Consente di comporre il telefono manualmente, se è in grado di eseguire questa operazione.

</dd> <dt>

<span id="LAUNCH_LIGHTS__8_"></span><span id="launch_lights__8_"></span>Luci di avvio \_ (8)
</dt> <dd>

Visualizza l'icona del modem nell'area stato della barra delle applicazioni.

\_Per impostazione predefinita viene impostato solo il valore luci di avvio

</dd> </dl> </dd> <dt>

<span id="wWaitBong"></span><span id="wwaitbong"></span><span id="WWAITBONG"></span>**wWaitBong**
</dt> <dd>

Numero di secondi (in granularità di due secondi) per sostituire l'attesa del tono di credito ($).

</dd> <dt>

<span id="Commconfig"></span><span id="commconfig"></span><span id="COMMCONFIG"></span>**Commconfig**
</dt> <dd>

Struttura [**COMMCONFIG**](/windows/desktop/api/winbase/ns-winbase-commconfig) che può essere utilizzata con le funzioni di configurazione delle comunicazioni e del modem.

</dd> </dl>

 

 
