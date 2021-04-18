---
description: Individuazione di risorse PE non Win32
ms.assetid: 12f0b78e-ca85-443a-94ea-6bec5aa40c06
title: Individuazione di risorse PE non Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 079288cd6200eb64289f474636cbc8dc046c1e47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308703"
---
# <a name="locating-non-win32-pe-resources"></a>Individuazione di risorse PE non Win32

Per individuare le risorse PE non Win32, l'applicazione deve prima chiamare la funzione [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) per individuare il file di risorse specifico della lingua da cui caricare le risorse. Se l'applicazione segue le impostazioni della lingua di sistema, deve chiamare la funzione con il \_ nome del linguaggio MUI \_ \| MUI \_ utente \_ preferenza lingue dell'interfaccia utente \_ \_ specificata per *dwFlags* e **null** specificato per *pwszLanguage*. Se l'applicazione segue le impostazioni della lingua specifica dell'applicazione, USA **GetFileMUIPath** per determinare se esiste un file specifico della lingua specificando la lingua nel parametro *pwszLanguage* .

Dopo la chiamata a [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath), l'applicazione deve definire funzionalità personalizzate per caricare il modulo della risorsa e caricare risorse specifiche. Se, ad esempio, si utilizza un file di risorse con estensione txt o XML, l'applicazione deve utilizzare un parser TXT o XML per caricare il file e quindi analizzare il contenuto del file per ogni risorsa richiesta.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dell'interfaccia utente multilingue](using-multilingual-user-interface.md)
</dt> <dt>

[**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath)
</dt> </dl>

 

 



