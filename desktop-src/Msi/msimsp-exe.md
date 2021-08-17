---
description: Il metodo consigliato per la generazione di un pacchetto di patch è l'uso di strumenti di creazione delle patch, ad esempio Msimsp.exe e Patchwiz.dll. Lo Msimsp.exe è disponibile solo nei componenti dell'SDK Windows per Windows programma di installazione.
ms.assetid: fa8e9d68-3db1-4d17-aa99-2ca0ed421c7a
title: Msimsp.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa82f2fbefc9046877f4f98cf4a3c126d94e6542b60076f0491bd0f311ee00a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118627798"
---
# <a name="msimspexe"></a>Msimsp.exe

Il metodo consigliato per la generazione di un pacchetto di patch è usare strumenti di creazione delle patch, ad esempio Msimsp.exe e [Patchwiz.dll](patchwiz-dll.md). Lo Msimsp.exe è disponibile solo nei componenti dell'SDK Windows [per Windows programma di installazione.](platform-sdk-components-for-windows-installer-developers.md)

Msimsp.exe è un file eseguibile che chiama [Patchwiz.dll](patchwiz-dll.md). Lo strumento può essere usato per creare un pacchetto di patch passando il percorso di un file delle proprietà di creazione patch (file con estensione pcp) e il percorso del pacchetto di patch da creare. Msimsp.ex può essere usato anche per creare un file di log e per specificare una cartella temporanea in cui vengono salvate le trasformazioni, i file cab e i file usati per creare il pacchetto patch.

La sintassi della riga di comando per Msimsp.exe è:

**Msimsp.exe -s** *\[ percorso del file \] con estensione pcp* **-p** percorso del file *\[ \] msp* **{options}**

Le opzioni della riga di comando non supportano la distinzione tra maiuscole e minuscole e i delimitatori di barra possono essere usati al posto di un trattino. Se non viene specificata alcuna opzione, Msimsp.exe i valori correnti delle proprietà delle informazioni di riepilogo.

<dl> <dt>

<span id="-s_path_to_.pcp_file_"></span><span id="-S_PATH_TO_.PCP_FILE_"></span>**-s**_\[ percorso del file \] con estensione pcp_
</dt> <dd>

Questa operazione è obbligatoria e deve essere seguita dal percorso del file delle proprietà di creazione della patch (estensione pcp). Per altre informazioni, [ vedere ](patchwiz-dll.md)PatchWiz.dll.

</dd> <dt>

<span id="-ppath_to_.msp_file"></span><span id="-PPATH_TO_.MSP_FILE"></span>**-p**_percorso del file con estensione msp_
</dt> <dd>

Questa operazione è obbligatoria e seguita dal percorso del pacchetto patch che viene creato (estensione msp).

</dd> <dt>

<span id="-fpath_to_temporary_folder"></span><span id="-FPATH_TO_TEMPORARY_FOLDER"></span>**-f**_percorso della cartella temporanea_
</dt> <dd>

facoltativo. Seguito dal percorso della cartella temporanea. Il percorso predefinito è %TMP% \\ ~pcw \_ tmp.tmp. \\

</dd> <dt>

<span id="-k"></span><span id="-K"></span>**-k**
</dt> <dd>

facoltativo. Ha esito negativo se la cartella temporanea esiste già.

</dd> <dt>

<span id="-lpath_to_log_file"></span><span id="-LPATH_TO_LOG_FILE"></span>**-l**_percorso del file di log_
</dt> <dd>

facoltativo. Seguito dal percorso del file di log che descrive il processo di creazione della patch e gli errori. Per altre informazioni, vedere [Valori restituiti per UiCreatePatchPackage.](return-values-for-uicreatepatchpackage.md)

</dd> <dt>

<span id="-lppath_to_log_file_with_performance_data"></span><span id="-LPPATH_TO_LOG_FILE_WITH_PERFORMANCE_DATA"></span>**-lp**_percorso del file di log con dati sulle prestazioni_
</dt> <dd>

facoltativo. Seguito dal percorso del file di log che descrive il processo di creazione della patch e gli errori. Questa opzione scrive i dati sulle prestazioni nel file di log. Questa opzione richiede la versione 4.0 Patchwiz.dll.

</dd> <dt>

<span id="-d"></span><span id="-D"></span>**-d**
</dt> <dd>

facoltativo. Visualizza una finestra di dialogo se la creazione della patch viene completata correttamente.

</dd> <dt>

<span id="-_"></span>**-?**
</dt> <dd>

Visualizza la Guida della riga di comando.

</dd> </dl>

> [!Note]
> Msimsp.exe può avere esito negativo quando chiama Makecab.exe se sono presenti valori nella colonna File della tabella [File](file-table.md) del pacchetto di installazione che differiscono solo in base alla distinzione tra maiuscole e minuscole. Windows Il programma di installazione fa distinzione tra maiuscole e minuscole e consente un pacchetto di installazione come nella tabella seguente solo quando Comp1 e Comp2 vengono installati in directory diverse. Tuttavia, in questo scenario non è possibile usare Msimsp.exe o [Patchwiz.dll](patchwiz-dll.md) per generare una patch per il pacchetto, perché Msimsp.exe e Patchwiz.dll chiamano Makecab.exe, senza distinzione tra maiuscole e minuscole.
> 
> Evitare di creare un pacchetto di installazione, ad esempio la tabella [file parziale seguente.](file-table.md)
> 
> | File       | Componente\_ | FileName   |
> |------------|-------------|------------|
> | readme.txt | Comp1       | readme.txt |
> | ReadMe.txt | Comp2       | readme.txt |


## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un pacchetto di patch](creating-a-patch-package.md)
</dt> <dt>

[Esempio di applicazione di patch per gli aggiornamenti di piccole dimensioni](a-small-update-patching-example.md)
</dt> <dt>

[Windows Strumenti di sviluppo del programma di installazione](windows-installer-development-tools.md)
</dt> <dt>

[Versioni rilasciate, strumenti e ridistribuibili](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



