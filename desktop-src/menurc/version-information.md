---
title: Informazioni sulla versione
description: In questa sezione viene illustrata la risorsa version-information.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\versioninformation.htm
keywords:
- risorse,informazioni sulla versione
- informazioni sulla versione
- numeri di versione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac69601c593c51a5a15a0af0706a019f135d855875f6e1ecabdb414a8a100045
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118733096"
---
# <a name="version-information"></a>Informazioni sulla versione

Le informazioni sulla versione semplificano l'installazione corretta dei file da parte delle applicazioni e consentono ai programmi di installazione di analizzare i file attualmente installati. La risorsa version-information contiene il numero di versione del file, il sistema operativo previsto e il nome del file originale.

### <a name="in-this-section"></a>Contenuto della sezione



| Nome                                                               | Descrizione                                                        |
|--------------------------------------------------------------------|--------------------------------------------------------------------|
| [Informazioni sulla versione](about-version-information.md)         | Vengono illustrate le funzioni relative alle informazioni sulla versione.<br/>            |
| [Uso delle informazioni sulla versione](using-version-information.md)         | Viene illustrato come usare le funzioni di informazioni sulla versione.<br/> |
| [Informazioni di riferimento sulle informazioni sulla versione](version-information-reference.md) | Contiene il riferimento all'API.<br/>                             |



 

### <a name="version-information-functions"></a>Funzioni relative alle informazioni sulla versione



| Nome                                                         | Descrizione                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetFileVersionInfo**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa)             | Recupera le informazioni sulla versione per il file specificato. <br/>                                                                                                                                                                                                                                                                                                     |
| [**GetFileVersionInfoEx**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoexa)         | Recupera le informazioni sulla versione per il file specificato.<br/>                                                                                                                                                                                                                                                                                                      |
| [**GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea)     | Determina se il sistema operativo può recuperare le informazioni sulla versione per un file specificato. Se sono disponibili informazioni sulla versione, [**GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea) restituisce le dimensioni, in byte, di queste informazioni. <br/>                                                                                                             |
| [**GetFileVersionInfoSizeEx**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizeexa) | Determina se il sistema operativo può recuperare le informazioni sulla versione per un file specificato. Se sono disponibili informazioni sulla versione, [**GetFileVersionInfoSizeEx**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizeexa) restituisce le dimensioni, in byte, di queste informazioni.<br/>                                                                                                          |
| [**VerFindFile**](/windows/desktop/api/Winver/nf-winver-verfindfilea)                           | Determina dove installare un file in base al fatto che individua un'altra versione del file nel sistema. I valori [**restituiti da VerFindFile**](/windows/desktop/api/Winver/nf-winver-verfindfilea) nei buffer specificati vengono usati in una chiamata successiva alla [**funzione VerInstallFile.**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) <br/>                                                                          |
| [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea)                     | Installa il file specificato in base alle informazioni restituite dalla [**funzione VerFindFile.**](/windows/desktop/api/Winver/nf-winver-verfindfilea) [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) decomprime il file, se necessario, assegna un nome file univoco e verifica la presenza di errori, ad esempio file obsoleti. <br/>                                                                                   |
| [**VerLanguageName**](/windows/desktop/api/Winver/nf-winver-verlanguagenamea)                   | Recupera una stringa di descrizione per la lingua associata a un identificatore di lingua Microsoft binario specificato.<br/>                                                                                                                                                                                                                                          |
| [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea)                       | Recupera le informazioni sulla versione specificate dalla risorsa di informazioni sulla versione specificata. Per recuperare la risorsa appropriata, prima di chiamare [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea)è necessario chiamare prima la [**funzione GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea) e quindi la [**funzione GetFileVersionInfo.**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa) <br/> |



 

### <a name="version-information-structures"></a>Strutture delle informazioni sulla versione



| Nome                                          | Descrizione                                                                                                                                                                                                                      |
|-----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Stringa**](string-str.md)                  | Illustra l'organizzazione dei dati in una risorsa con versione file. Contiene una stringa che descrive un aspetto specifico di un file, ad esempio la versione di un file, le relative comunicazioni sul copyright o i relativi marchi.<br/>                |
| [**StringFileInfo**](stringfileinfo.md)      | Illustra l'organizzazione dei dati in una risorsa con versione file. Contiene informazioni sulla versione che possono essere visualizzate per una determinata lingua e tabella codici.<br/>                                                           |
| [**Stringtable**](stringtable.md)            | Illustra l'organizzazione dei dati in una risorsa con versione file. Contiene informazioni sulla lingua e sulla formattazione della tabella codici per le stringhe specificate dal **membro** Children. Una tabella codici è un set di caratteri ordinato.<br/> |
| [**Var**](var-str.md)                        | Illustra l'organizzazione dei dati in una risorsa con versione file. Contiene in genere un elenco di coppie di identificatori di linguaggio e tabella codici supportati dalla versione dell'applicazione o della DLL.<br/>                             |
| [**VarFileInfo**](varfileinfo.md)            | Illustra l'organizzazione dei dati in una risorsa con versione file. Contiene informazioni sulla versione non dipendenti da una determinata combinazione di lingua e tabella codici.<br/>                                                        |
| [**VS \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) | Contiene informazioni sulla versione di un file. Queste informazioni sono indipendenti dal linguaggio e dalla tabella codici. <br/>                                                                                                                   |
| [**VS \_ VERSIONINFO**](vs-versioninfo.md)     | Illustra l'organizzazione dei dati in una risorsa con versione file. È la struttura radice che contiene tutte le altre strutture di informazioni sulla versione del file.<br/>                                                                    |



 

 

 





