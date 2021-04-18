---
description: In questo argomento vengono descritti gli elementi indici di ricerca di Windows.
ms.assetid: vs|search|~\search\wds3x\overviews\misc_items_in_index.htm
title: Contenuto dell'indice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5560a14e3537c8e3ac8c7544aa7ffc9a0bc1bc64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306186"
---
# <a name="what-is-included-in-the-index"></a>Contenuto dell'indice

In questo argomento vengono descritti gli elementi indici di ricerca di Windows.

Questo argomento è organizzato nel modo seguente:

-   [Indicizzate per impostazione predefinita](#indexed-by-default)
-   [Formati di file supportati](#file-formats-supported)
-   [Esclusioni di file](#file-exclusions)
-   [Esclusioni di cartelle](#folder-exclusions)
-   [Esclusioni delle unità](#drive-exclusions)
-   [Argomenti correlati](#related-topics)

 

## <a name="indexed-by-default"></a>Indicizzate per impostazione predefinita

I gestori di protocollo e i filtri sono inclusi in Windows Search per indicizzare i tipi di contenuto seguenti:

-   In Windows Vista e versioni successive, gli elementi Microsoft Outlook e Microsoft Outlook Express mail di un utente vengono indicizzati durante l'esecuzione dell'applicazione di posta elettronica.
-   I file offline nella cache lato client (CSC) sono indicizzati in locale da Windows Search.
-   Windows Search supporta la raccolta di indirizzi di avvio dei file nei volumi NTFS e FAT32. NTFS supporta l'indicizzazione basata sulle notifiche e FAT32 supporta una ricerca per indicizzazione incrementale all'avvio e quindi risponde alle notifiche.
-   Windows Vista e versioni successive continuano a esporre una proprietà per ogni cartella/file per abilitare l'indicizzazione: l'opzione "**per la ricerca rapida, consentendo al servizio di indicizzazione di indicizzare questa cartella**" nella finestra di dialogo delle **Proprietà** . Se si imposta il flag di bit, si garantisce che le proprietà di base del protocollo, ad esempio URL, filename e size, siano indicizzate, ma che non vengano eseguiti né gestori di filtro né gestori di proprietà.
-   Il contenuto di testo è indicizzato ma la punteggiatura non lo è.

## <a name="file-formats-supported"></a>Formati di file supportati

Windows Search dispone di gestori di protocollo, gestori di proprietà e gestori di filtri per indicizzare automaticamente i formati seguenti:

-   File multimediali: tutti i tipi di file multimediali
-   **HTML** (nlhtml.dll):. ascx,. asp,. aspx,. CSS,. hhc,. htm,. html,. htt,. htw,. htx,. odc,. stm
-   **HTML MIME** (mimefilt.dll):. mht,. MHTML
-   **Office** (offfilt.dll):. doc,. dot,. pot,. PPS,. ppt,. xlb,. xlc,. xls,. xlt
-   **Testo** (query.dll):. asm,. asx,. bat,. c,. cmd,. cpp,. cxx,. def,. dic,. h,. hpp,. HXX,. idl,. idq,. inf,. ini,. INX,. js,. log,. m3u,. RC,. reg,. RTF,. txt,. URL,. vbs,. WTX
-   **XML** (xmlfilt.dll): XML, XSL
-   **OneNote**:. uno
-   **Journal Tablet** (jntfiltr.dll):. JNT

Le proprietà vengono indicizzate per tutti i file ad eccezione dell'archiviazione strutturata. In Windows Vista e versioni successive, vengono indicizzate molte proprietà dei file multimediali. Tuttavia, il contenuto non viene indicizzato se i file sono protetti da Digital Rights Management (DRM).

> [!Note]  
> Il filtro HTML non indicizza i commenti HTML.

 

## <a name="file-exclusions"></a>Esclusioni di file

Quando un tipo di file non dispone di un filtro associato o quando un file non dispone di un'estensione, le proprietà di sistema per i file di quel tipo sono indicizzate, ma il contenuto del file non viene indicizzato.

Inoltre, Windows Search non indicizza il contenuto dei file in Information Rights Management (IRM) o Digital Rights Management (DRM).

In Windows Vista (solo), per impostazione predefinita i file seguenti vengono esclusi dall'indicizzazione:

-   File contrassegnati come nascosti o System.
-   File con le seguenti estensioni:

    .386,. APS,. AudioCD,. bin,. BK1,. Bk2,. bkf,. BSC,. BTR,. chk,. ci,. crwl,. dbg,. DCT,. DeskLink, dir,. dl \_ ,. dll,. drv,. DVD,. evt,. ex \_ ,. exe,. exp,. EYB,. fnd,. fnt,. Cartella,. fon,. ghi,. gthr,. hqx,. ICM,. IDB,. idx,. ilk,. IMC,. in \_ ,. ini,. inv,. JBF,. latex,. lib,. local,. M14,. Mac,. manifest,. map,. MAPIMail,. mmf,. Movie,. MV,. docs,. BCN,. obj,. OC \_ ,. ocx,. pch,. pdb,. PF,. PMA,. PMC,. PML,. PMR,. res,. RMP,. RPC,. rsp,. SBR,. sc2,. sit,. SR \_ ,. sy,. sym,. \_ sys,. tlb,. trc,. TTC,. ttf,. VBX,. vxd,. wll,. WLT,. XIX,. Z96,. ZFSendToTarget.

## <a name="folder-exclusions"></a>Esclusioni di cartelle

> [!TIP]
> I nomi delle cartelle non fanno distinzione tra maiuscole e minuscole.

 

Per impostazione predefinita, le cartelle seguenti sono escluse dall'indicizzazione:



| Modello di esclusione di cartelle                                                              | Effetto in Windows 7 | Effetto in Windows Vista | Descrizione                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------|---------------------|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *% Sistema%* \\ ProgramData \\ \\ \\ i dati di Microsoft Search\\                                    | **Esclusione**        | Nessun effetto               | Dati dell'indicizzatore sull'unità di sistema.                                                                                                                                                                                          |
| *% Sistema%* \\ \\*Nome utente nome utente* \\ AppData\\                                              | **Esclusione**        | Nessun effetto               | I dati dell'applicazione dell'utente (inclusi i dati temporanei) nell'unità di sistema.<br/> Per ogni utente che accede al sistema, viene aggiunto un modello di esclusione specifico che esclude i dati dell'applicazione dall'indice.<br/> |
| *% Sistema%* \\ Utenti \\ \* \\ AppData \\ locale \\ \\ \\ file Internet temporanei di Microsoft Windows\\ | **Esclusione**        | Nessun effetto               | Percorso predefinito dei file Internet temporanei di Windows Internet Explorer nell'unità di sistema.<br/> Se il percorso dei file Internet temporanei di Internet Explorer viene modificato, è possibile indicizzare tali file.<br/>    |
| *% Sistema%* \\ Windows \\ CSC\\                                                            | **Esclusione**        | Nessun effetto               | Se l'indicizzazione è attivata per la directory di sistema di Windows, la cartella CSC (sull'unità di sistema) viene ancora esclusa dall'indicizzazione.                                                                                           |
| *% Sistema%* \\ Temp di Windows \\ \* \\\\                                                       | **Esclusione**        | Nessun effetto               | Dati temporanei di Windows nell'unità di sistema.                                                                                                                                                                                     |
| *% Sistema%* \\ Windows.\*\\                                                              | **Esclusione**        | Nessun effetto               | Installazioni precedenti di Windows nell'unità di sistema.                                                                                                                                                                             |
| *% Sistema%* \\ ProgramData\\                                                             | **Esclusione**        | **Esclusione**            | Si noti che la sottocartella del menu Start condiviso è indicizzata.                                                                                                                                                                     |
| *% Sistema%* \\ \\ \* \\ AppData utenti\\                                                      | **Esclusione**        | **Esclusione**            | Dati dell'applicazione degli utenti (inclusi i dati temporanei).                                                                                                                                                                              |
| *% Sistema%* \\ \\ \* \\ \\ Temp locale utenti \\ AppData\\                                         | **Esclusione**        | **Esclusione**            | Dati temporanei degli utenti. Se l'indicizzazione viene attivata per i dati dell'applicazione utente, i dati temporanei dell'utente sono ancora esclusi dall'indicizzazione per impostazione predefinita.                                                                                           |
| *% Sistema%* \\ Windows\\                                                                 | **Esclusione**        | **Esclusione**            | File del sistema operativo nell'unità di sistema.                                                                                                                                                                                |
| *% Sistema%* \\ $Recycle bin\\                                                            | **Esclusione**        | **Esclusione**            | Percorso dei file nel Cestino.                                                                                                                                                                                      |
| *% Sistema%* \\ Compilazione\\                                                                   | Nessun effetto           | **Esclusione**            | Nell'unità di sistema.                                                                                                                                                                                                       |
| *% Sistema%* \\ Repository installato\\                                                    | Nessun effetto           | **Esclusione**            | Nell'unità di sistema.                                                                                                                                                                                                       |
| *% Sistema%* \\ File di programma\\                                                           | Nessun effetto           | **Esclusione**            | Nell'unità di sistema.                                                                                                                                                                                                       |
| *% Sistema%* \\ Programmi (x86)\\                                                     | Nessun effetto           | **Esclusione**            | Nell'unità di sistema.                                                                                                                                                                                                       |
| \*\\Temp\\\*                                                                          | Nessun effetto           | **Esclusione**            | Dati temporanei di Windows e altre cartelle con il nome "Temp".                                                                                                                                                                  |
| *% Sistema%* \\ Utenti \\ predefiniti\\                                                          | Nessun effetto           | **Esclusione**            | Posizione dei dati del profilo utente predefiniti nell'unità di sistema.                                                                                                                                                             |
| \*\\Windows.\*\\                                                                      | Nessun effetto           | **Esclusione**            | Installazioni precedenti di Windows e altre cartelle con nomi che iniziano con "Windows".                                                                                                                                         |



 

## <a name="drive-exclusions"></a>Esclusioni delle unità

In Windows 7 e Windows Vista, le unità rimovibili non vengono indicizzate per impostazione predefinita.

> [!Note]  
> Se le unità rimovibili si segnalano come unità fisse, è possibile aggiungerle per l'indicizzazione anche se sono effettivamente rimovibili. Le informazioni rimarranno nell'indice e Windows Search effettuerà una ricerca per indicizzazione incrementale per riconciliare i risultati dell'indicizzazione quando il disco rimovibile viene collegato di nuovo. Poiché le unità flash USB si segnalano come rimovibili, non possono essere indicizzate.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Indicizzazione, query e notifiche in Windows Search](-search-3x-wds-included-in-index.md)
</dt> <dt>

[Processo di indicizzazione in Windows Search](-search-indexing-process-overview.md)
</dt> <dt>

[Esecuzione di query sul processo in Windows Search](querying-process--windows-search-.md)
</dt> <dt>

[Processo di notifica in Windows Search](-search-3x-wds-support.md)
</dt> <dt>

[Requisiti per la formattazione degli URL](url-formatting-requirements.md)
</dt> </dl>

 

 




