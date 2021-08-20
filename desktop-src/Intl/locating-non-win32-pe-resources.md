---
description: Individuazione di risorse PE non Win32
ms.assetid: 12f0b78e-ca85-443a-94ea-6bec5aa40c06
title: Individuazione di risorse PE non Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf706712b2e1be2dd8fb1598c1404a829251bb24db83db7c7d6deaa87a13d24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147174"
---
# <a name="locating-non-win32-pe-resources"></a>Individuazione di risorse PE non Win32

Per individuare risorse PE non Win32, l'applicazione deve prima chiamare la funzione [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) per individuare il file di risorse specifico della lingua da cui caricare le risorse. Se l'applicazione segue le impostazioni della lingua di sistema, deve chiamare la funzione con MUI LANGUAGE NAME MUI USER PREFERRED UI LANGUAGES specificati per \_ \_ \| \_ \_ \_ \_ *dwFlags*  e NULL specificati per pwszLanguage . Se l'applicazione segue le impostazioni della lingua specifiche dell'applicazione, usa **GetFileMUIPath** per determinare se esiste un file specifico della lingua specificando la lingua nel *parametro pwszLanguage.*

Dopo la chiamata a [**GetFileMUIPath,**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath)l'applicazione deve definire funzionalità personalizzate per caricare il modulo di risorse e caricare risorse specifiche da esso. Ad esempio, se si usa un file di risorse .txt o .xml, l'applicazione deve usare un parser TXT o XML per caricare il file e quindi analizzare il contenuto del file per ogni risorsa richiesta.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di interfaccia utente multilingue](using-multilingual-user-interface.md)
</dt> <dt>

[**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath)
</dt> </dl>

 

 



