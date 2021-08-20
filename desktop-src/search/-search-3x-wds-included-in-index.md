---
description: Questo argomento descrive gli elementi che Windows indici di ricerca.
ms.assetid: vs|search|~\search\wds3x\overviews\misc_items_in_index.htm
title: Elementi inclusi nell'indice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cbffec8aba8a985faca112eac434b669d22eff82d94d6b4eaf5588585ced771
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118463324"
---
# <a name="what-is-included-in-the-index"></a>Elementi inclusi nell'indice

Questo argomento descrive gli elementi che Windows indici di ricerca.

Questo argomento è organizzato come segue:

-   [Indicizzato per impostazione predefinita](#indexed-by-default)
-   [Formati di file supportati](#file-formats-supported)
-   [Esclusioni di file](#file-exclusions)
-   [Esclusioni di cartelle](#folder-exclusions)
-   [Esclusioni di unità](#drive-exclusions)
-   [Argomenti correlati](#related-topics)

 

## <a name="indexed-by-default"></a>Indicizzato per impostazione predefinita

I gestori di protocollo e i filtri sono inclusi in Windows ricerca per indicizzare i tipi di contenuto seguenti:

-   In Windows Vista e versioni successive, gli elementi di posta elettronica Microsoft Outlook e Microsoft Outlook Express di un utente vengono indicizzati mentre l'applicazione di posta è in esecuzione.
-   I file offline nella cache lato client (CSC) vengono indicizzati Windows ricerca locale.
-   Windows La ricerca supporta la raccolta di indirizzi iniziali dei file nei volumi NTFS e FAT32. NTFS supporta l'indicizzazione basata sulle notifiche e FAT32 supporta una ricerca per indicizzazione incrementale all'avvio e quindi risponde alle notifiche.
-   Windows Vista e versioni successive continuano a esporre una proprietà per cartella/per file per abilitare l'indicizzazione: l'opzione  " Per la ricerca **rapida,** consentendo al Servizio di indicizzazione di indicizzare questa cartella " nella finestra di dialogo Proprietà . L'impostazione del flag di bit FANCI garantisce che le proprietà di base del protocollo, ad esempio URL, nome file e dimensioni, siano indicizzate, ma che non vengono eseguiti né gestori di filtri né gestori di proprietà.
-   Il contenuto di testo è indicizzato, ma la punteggiatura non lo è.

## <a name="file-formats-supported"></a>Formati di file supportati

Windows La ricerca include gestori di protocollo, gestori di proprietà e gestori di filtri per indicizzare automaticamente i formati seguenti:

-   File multimediali: tutti i tipi di file multimediali
-   **HTML** (nlhtml.dll): .ascx, .asp, .aspx, .css, .hhc, .htm, .html, .htt, .htw, .htx, .odc, .stm
-   **HTML MIME** (mimefilt.dll): .mht, .mhtml
-   **Office** (offfilt.dll): .doc, dot, pot, pps, .ppt, xlb, xlc, .xls, xlt
-   **Text** (query.dll): .asm, .asx, .bat, .c, .cmd, .cpp, .cxx, .def, .dic, .h, .hpp, .hxx, .idl, .idq, .inf, .ini, .inx, .js, .log, .m3u, .rc, .reg, .rtf, .txt, .url, .vbs, .wtx
-   **XML** (xmlfilt.dll): .xml, xsl
-   **OneNote**: .one
-   **Tablet Journal** (jntfiltr.dll): .jnt

Le proprietà vengono indicizzate per tutti i file, ad eccezione dell'archiviazione strutturata. In Windows Vista e versioni successive, molte proprietà dei file multimediali vengono indicizzate; Tuttavia, il contenuto non viene indicizzato se i file sono protetti da DRM (Digital Rights Management).

> [!Note]  
> Il filtro HTML non indicizza i commenti HTML.

 

## <a name="file-exclusions"></a>Esclusioni di file

Quando a un tipo di file non è associato un filtro o a un file non è associata un'estensione, le proprietà di sistema per i file di tale tipo vengono indicizzate, ma il contenuto del file non viene indicizzato.

Inoltre, Windows ricerca non indicizza il contenuto dei file in Information Rights Management (IRM) o Digital Rights Management (DRM).

In Windows Vista (solo), i file seguenti sono esclusi dall'indicizzazione per impostazione predefinita:

-   File contrassegnati come Hidden o System.
-   File con le estensioni seguenti:

    .386, .aps, . AudioCD, .bin, .bk1, .bk2, .bkf, .bsc, .btr, .chk, .ci, .crwl, .dbg, .dct, . DeskLink, .dir, .dl, \_ .dll, .drv, .dvd, .evt, .ex \_ , .exe, .exp, .eyb, .fnd, .fnt, . Folder, .fon, .ghi, .gthr, .hqx, .icm, .idb, .idx, .ilk, .imc, .in \_ , .ini, .inv, .jbf, .latex, .lib, .local, .m14, .mac, .manifest, .map, . MAPIMail, .mmf, .movie, .mv, .mydocs, .ncb, .obj, .oc, \_ .ocx, .pch, .pdb, .pf, .pma, .pmc, .pml, .pmr, .res, .rmp, .rpc, .rsp, .sbr, .sc2, .sit, \_ .sr, \_ .sy, .sym, .sys, .tlb, .trc, .ttc, .ttf, .vbx, .vxd, .wll, .wlt, .la, .z96, . ZFSendToTarget.

## <a name="folder-exclusions"></a>Esclusioni di cartelle

> [!TIP]
> Per i nomi di cartella non viene fatto distinzione tra maiuscole e minuscole.

 

Le cartelle seguenti sono escluse dall'indicizzazione per impostazione predefinita:



| Modello di esclusione cartelle                                                              | Effetto in Windows 7 | Effetto in Windows Vista | Descrizione                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------|---------------------|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *%System%* \\ ProgramData \\ Microsoft \\ Search \\ Data\\                                    | **Esclusione**        | Nessun effetto               | Dati dell'indicizzatore nell'unità di sistema.                                                                                                                                                                                          |
| *%System%* \\ Users \\ *UserName* \\ AppData\\                                              | **Esclusione**        | Nessun effetto               | Dati dell'applicazione dell'utente (inclusi i dati temporanei) nell'unità di sistema.<br/> Per ogni utente che accede al sistema, viene aggiunto un modello di esclusione specifico che esclude i dati dell'applicazione dall'indice.<br/> |
| *%System%* \\ Utenti \\ \* \\ AppData \\ Local Microsoft Windows Temporary Internet \\ \\ \\ Files\\ | **Esclusione**        | Nessun effetto               | Percorso predefinito Windows Internet Explorer file Internet temporanei nell'unità di sistema.<br/> Se il percorso Internet Explorer file Temporanei Internet viene modificato, è possibile indicizzare tali file.<br/>    |
| *%System%* \\ \\Windows Csc\\                                                            | **Esclusione**        | Nessun effetto               | Se l'indicizzazione è attivata per la directory Windows di sistema, la cartella CSC (nell'unità di sistema) è ancora esclusa dall'indicizzazione.                                                                                           |
| *%System%* \\ \\ \* Windows \\ Temp\\                                                       | **Esclusione**        | Nessun effetto               | Windows dati temporanei nell'unità di sistema.                                                                                                                                                                                     |
| *%System%* \\ Windows.\*\\                                                              | **Esclusione**        | Nessun effetto               | Le Windows le installazioni nell'unità di sistema.                                                                                                                                                                             |
| *%System%* \\ Programdata\\                                                             | **Esclusione**        | **Esclusione**            | Si noti che la sottocartella del menu Start condiviso è indicizzata.                                                                                                                                                                     |
| *%System%* \\ Utenti \\ \* \\ AppData\\                                                      | **Esclusione**        | **Esclusione**            | Dati dell'applicazione degli utenti (inclusi i dati temporanei).                                                                                                                                                                              |
| *%System%* \\ Utenti \\ \* \\ AppData \\ Local \\ Temp\\                                         | **Esclusione**        | **Esclusione**            | Dati temporanei degli utenti. Se l'indicizzazione è attivata per i dati dell'applicazione utente, i dati temporanei utente vengono comunque esclusi dall'indicizzazione per impostazione predefinita.                                                                                           |
| *%System%* \\ Windows\\                                                                 | **Esclusione**        | **Esclusione**            | File del sistema operativo nell'unità di sistema.                                                                                                                                                                                |
| *%System%* \\ $Cestino\\                                                            | **Esclusione**        | **Esclusione**            | Percorso dei file nel Cestino.                                                                                                                                                                                      |
| *%System%* \\ Costruire\\                                                                   | Nessun effetto           | **Esclusione**            | Nell'unità di sistema.                                                                                                                                                                                                       |
| *%System%* \\ Repository installato\\                                                    | Nessun effetto           | **Esclusione**            | Nell'unità di sistema.                                                                                                                                                                                                       |
| *%System%* \\ Programmi\\                                                           | Nessun effetto           | **Esclusione**            | Nell'unità di sistema.                                                                                                                                                                                                       |
| *%System%* \\ Programmi (x86)\\                                                     | Nessun effetto           | **Esclusione**            | Nell'unità di sistema.                                                                                                                                                                                                       |
| \*\\Temp\\\*                                                                          | Nessun effetto           | **Esclusione**            | Windows dati temporanei e altre cartelle con il nome "temp".                                                                                                                                                                  |
| *%System%* \\ Impostazioni \\ predefinite degli utenti\\                                                          | Nessun effetto           | **Esclusione**            | Percorso dei dati del profilo utente predefiniti nell'unità di sistema.                                                                                                                                                             |
| \*\\finestre.\*\\                                                                      | Nessun effetto           | **Esclusione**            | Le Windows e altre cartelle con nomi che iniziano con "windows".                                                                                                                                         |



 

## <a name="drive-exclusions"></a>Esclusioni di unità

In Windows 7 e Windows Vista, le unità rimovibili non vengono indicizzate per impostazione predefinita.

> [!Note]  
> Se le unità rimovibili vengono segnalate come unità fisse, è possibile aggiungerle per l'indicizzazione anche se sono effettivamente rimovibili. Le informazioni rimarranno nell'indice e Windows ricerca eseguirà una ricerca per indicizzazione incrementale per riconciliare i risultati dell'indicizzazione quando il disco rimovibile viene collegato nuovamente. Poiché le unità flash USB vengono segnalate come rimovibili, non possono essere indicizzate.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Indicizzazione, query e notifiche nella ricerca Windows ricerca](-search-3x-wds-included-in-index.md)
</dt> <dt>

[Processo di indicizzazione nella Windows ricerca](-search-indexing-process-overview.md)
</dt> <dt>

[Processo di query nella Windows ricerca](querying-process--windows-search-.md)
</dt> <dt>

[Processo di notifica nella Windows ricerca](-search-3x-wds-support.md)
</dt> <dt>

[Requisiti di formattazione url](url-formatting-requirements.md)
</dt> </dl>

 

 




