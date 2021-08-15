---
title: Linee guida per l'estensione metafile
description: Linee guida per l'estensione metafile
ms.assetid: 079fac31-7a6f-4775-a337-870ad25a56a0
keywords:
- Windows metafile multimediali, estensioni
- Windows metafile multimediali, estensioni di file
- metafile, estensioni
- metafile, estensioni di file
- Windows Supporti, metafile
- Estensioni dei nomi di file Windows metafile multimediali
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4aaa31f1364271b1b968244494586ba5006e7c292ca2d9a207cdd1c758b5e432
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118836969"
---
# <a name="metafile-extension-guidelines"></a>Linee guida per l'estensione metafile

Un'estensione di file fornisce a un fornitore di software indipendente (ISV) informazioni sui requisiti di rendering di un'applicazione che usa l'estensione e consente agli autori di contenuto di scegliere come destinazione tipi generali di lettori.

Windows Le estensioni dei nomi dei metafile multimediali vengono usate per identificare il formato Windows file multimediali a cui fa riferimento un metafile. Windows I metafile multimediali con estensioni .tutto, wvx o asx fanno riferimento rispettivamente ai file con estensione wma, wmv e asf. Tutti i metafile, indipendentemente dall'estensione di file usata, hanno il tag **dell'elemento ASX** all'inizio del file con l'attributo version specificato. 

La tabella seguente illustra i tipi di file multimediali a cui fa riferimento ogni tipo di estensione di file metafile. Le colonne elencano le estensioni dei nomi di file multimediali, le righe elencano le estensioni dei nomi dei metafile. Una X in una colonna indica un tipo di file multimediale a cui può fare riferimento una determinata estensione di file metafile.



| Estensione | .asf | wma | wmv |
|-----------|------|------|------|
| WVX      | X    | X    | X    |
| .tutto      | X    | X    |      |
| .asx      | X    |      |      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Estensioni di file**](file-name-extensions.md)
</dt> <dt>

[**Playlist metafile**](metafile-playlists.md)
</dt> <dt>

[**Windows Guida ai metafile multimediali**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




