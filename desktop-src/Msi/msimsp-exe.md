---
description: Il metodo consigliato per la generazione di un pacchetto di patch consiste nell'usare strumenti per la creazione di patch, ad esempio Msimsp.exe e Patchwiz.dll. Lo strumento Msimsp.exe è disponibile solo nei componenti Windows SDK per Windows Installer sviluppatori.
ms.assetid: fa8e9d68-3db1-4d17-aa99-2ca0ed421c7a
title: Msimsp.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1810fd0c544695742273bbb0e63b22138529c129
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320937"
---
# <a name="msimspexe"></a>Msimsp.exe

Il metodo consigliato per la generazione di un pacchetto di patch consiste nell'usare strumenti per la creazione di patch, ad esempio Msimsp.exe e [Patchwiz.dll](patchwiz-dll.md). Lo strumento Msimsp.exe è disponibile solo nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).

Msimsp.exe è un file eseguibile che chiama [Patchwiz.dll](patchwiz-dll.md). Lo strumento può essere usato per creare un pacchetto di patch passando il percorso di un file delle proprietà di creazione della patch (file con estensione PCP) e il percorso del pacchetto di patch in fase di creazione. Msimsp. es può inoltre essere utilizzato per creare un file di log e per specificare una cartella temporanea in cui vengono salvati le trasformazioni, i file CAB e i file utilizzati per creare il pacchetto di patch.

La sintassi della riga di comando per Msimsp.exe è:

Percorso **Msimsp.exe-s del** *\[ file \] . PCP* **-p** *\[ percorso del file \] con estensione msp* **{options}**

Le opzioni della riga di comando non fanno distinzione tra maiuscole e minuscole e i delimitatori barra possono essere utilizzati al posto di un trattino. Se non viene specificata alcuna opzione, Msimsp.exe Visualizza i valori correnti delle proprietà delle informazioni di riepilogo.

<dl> <dt>

<span id="-s_path_to_.pcp_file_"></span><span id="-S_PATH_TO_.PCP_FILE_"></span>**-s**_\[ percorso del file \] . PCP_
</dt> <dd>

Questa operazione è obbligatoria e deve essere seguita dal percorso del file delle proprietà di creazione della patch (estensione PCP). Per ulteriori informazioni, vedere [PatchWiz.dll](patchwiz-dll.md).

</dd> <dt>

<span id="-ppath_to_.msp_file"></span><span id="-PPATH_TO_.MSP_FILE"></span>**-p**_percorso del file con estensione msp_
</dt> <dd>

Questa operazione è obbligatoria e seguita dal percorso del pacchetto di patch creato (estensione msp).

</dd> <dt>

<span id="-fpath_to_temporary_folder"></span><span id="-FPATH_TO_TEMPORARY_FOLDER"></span>**-f**_percorso alla cartella temporanea_
</dt> <dd>

facoltativo. Seguito dal percorso alla cartella temporanea. Il percorso predefinito è% TMP% \\ ~ PCW \_ tmp. tmp \\ .

</dd> <dt>

<span id="-k"></span><span id="-K"></span>**-k**
</dt> <dd>

facoltativo. Esito negativo se la cartella temporanea esiste già.

</dd> <dt>

<span id="-lpath_to_log_file"></span><span id="-LPATH_TO_LOG_FILE"></span>**-l**_percorso del file di log_
</dt> <dd>

facoltativo. Seguito dal percorso del file di log che descrive il processo di creazione della patch ed errori. Per ulteriori informazioni, vedere [valori restituiti per UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).

</dd> <dt>

<span id="-lppath_to_log_file_with_performance_data"></span><span id="-LPPATH_TO_LOG_FILE_WITH_PERFORMANCE_DATA"></span>**-LP**_percorso del file di log con dati sulle prestazioni_
</dt> <dd>

facoltativo. Seguito dal percorso del file di log che descrive il processo di creazione della patch ed errori. Questa opzione scrive i dati sulle prestazioni in un file di log. Questa opzione richiede la versione 4,0 di Patchwiz.dll.

</dd> <dt>

<span id="-d"></span><span id="-D"></span>**-d**
</dt> <dd>

facoltativo. Visualizza una finestra di dialogo se la creazione della patch viene completata correttamente.

</dd> <dt>

<span id="-_"></span>**-?**
</dt> <dd>

Visualizza la guida della riga di comando.

</dd> </dl>

> [!Note]
> Msimsp.exe possono avere esito negativo quando chiama Makecab.exe se nella colonna file della [tabella di file](file-table.md) del pacchetto di installazione sono presenti valori che differiscono solo per le maiuscole/minuscole. Windows Installer fa distinzione tra maiuscole e minuscole e consente un pacchetto di installazione, ad esempio nella tabella seguente, solo quando comp1 e comp2 sono installati in directory diverse. Tuttavia, in questo scenario non è possibile utilizzare Msimsp.exe o [Patchwiz.dll](patchwiz-dll.md) per generare una patch per il pacchetto, poiché Msimsp.exe e Patchwiz.dll chiamare Makecab.exe, che non fa distinzione tra maiuscole e minuscole.
> 
> Evitare di creare un pacchetto di installazione come la seguente [tabella file](file-table.md)parziale.
> 
> | File       | Componente\_ | FileName   |
> |------------|-------------|------------|
> | readme.txt | Comp1       | readme.txt |
> | ReadMe.txt | Comp2       | readme.txt |


## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un pacchetto di patch](creating-a-patch-package.md)
</dt> <dt>

[Un piccolo esempio di patch di aggiornamento](a-small-update-patching-example.md)
</dt> <dt>

[Strumenti di sviluppo Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Versioni rilasciate, strumenti e ridistribuibili](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



