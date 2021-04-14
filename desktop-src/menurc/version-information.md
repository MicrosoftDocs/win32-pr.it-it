---
title: Informazioni sulla versione
description: In questa sezione viene illustrata la risorsa di informazioni sulla versione.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\versioninformation.htm
keywords:
- risorse, informazioni sulla versione
- informazioni sulla versione
- numeri di versione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78e43de27f18f89a5f240242b63ade057f57ec92
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330127"
---
# <a name="version-information"></a>Informazioni sulla versione

Le informazioni sulla versione rendono più semplice l'installazione corretta dei file e consente ai programmi di installazione di analizzare i file attualmente installati. La risorsa di informazioni sulla versione contiene il numero di versione del file, il sistema operativo previsto e il nome del file originale.

### <a name="in-this-section"></a>Contenuto della sezione



| Nome                                                               | Descrizione                                                        |
|--------------------------------------------------------------------|--------------------------------------------------------------------|
| [Informazioni sulle versioni](about-version-information.md)         | Vengono illustrate le funzioni delle informazioni sulla versione.<br/>            |
| [Utilizzo delle informazioni sulla versione](using-version-information.md)         | Viene illustrato come utilizzare le funzioni di informazioni sulla versione.<br/> |
| [Informazioni di riferimento sulla versione](version-information-reference.md) | Contiene il riferimento all'API.<br/>                             |



 

### <a name="version-information-functions"></a>Funzioni di informazioni sulla versione



| Nome                                                         | Descrizione                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetFileVersionInfo**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa)             | Recupera le informazioni sulla versione per il file specificato. <br/>                                                                                                                                                                                                                                                                                                     |
| [**GetFileVersionInfoEx**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoexa)         | Recupera le informazioni sulla versione per il file specificato.<br/>                                                                                                                                                                                                                                                                                                      |
| [**Impossibile eseguire GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea)     | Determina se il sistema operativo è in grado di recuperare le informazioni sulla versione per un file specificato. Se sono disponibili informazioni sulla versione, [**Impossibile eseguire GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea) restituisce le dimensioni, in byte, di tali informazioni. <br/>                                                                                                             |
| [**GetFileVersionInfoSizeEx**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizeexa) | Determina se il sistema operativo è in grado di recuperare le informazioni sulla versione per un file specificato. Se sono disponibili informazioni sulla versione, [**GetFileVersionInfoSizeEx**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizeexa) restituisce le dimensioni, in byte, di tali informazioni.<br/>                                                                                                          |
| [**VerFindFile**](/windows/desktop/api/Winver/nf-winver-verfindfilea)                           | Determina la posizione in cui installare un file a seconda che venga individuata un'altra versione del file nel sistema. I valori restituiti da [**VerFindFile**](/windows/desktop/api/Winver/nf-winver-verfindfilea) nei buffer specificati vengono utilizzati in una chiamata successiva alla funzione [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) . <br/>                                                                          |
| [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea)                     | Installa il file specificato in base alle informazioni restituite dalla funzione [**VerFindFile**](/windows/desktop/api/Winver/nf-winver-verfindfilea) . [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) decomprime il file, se necessario, assegna un nome file univoco e verifica la presenza di errori, ad esempio file obsoleti. <br/>                                                                                   |
| [**VerLanguageName**](/windows/desktop/api/Winver/nf-winver-verlanguagenamea)                   | Recupera una stringa di descrizione per la lingua associata a un identificatore di lingua Microsoft binario specificato.<br/>                                                                                                                                                                                                                                          |
| [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea)                       | Recupera le informazioni sulla versione specificate dalla risorsa di informazioni sulla versione specificata. Per recuperare la risorsa appropriata, prima di chiamare [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea), è necessario chiamare prima la funzione [**Impossibile eseguire GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea) e quindi la funzione [**GetFileVersionInfo**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa) . <br/> |



 

### <a name="version-information-structures"></a>Strutture di informazioni sulla versione



| Nome                                          | Descrizione                                                                                                                                                                                                                      |
|-----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Stringa**](string-str.md)                  | Descrive l'organizzazione dei dati in una risorsa di versione file. Contiene una stringa che descrive un aspetto specifico di un file, ad esempio la versione di un file, le notifiche sul copyright o i relativi marchi.<br/>                |
| [**StringFileInfo**](stringfileinfo.md)      | Descrive l'organizzazione dei dati in una risorsa di versione file. Contiene informazioni sulla versione che possono essere visualizzate per una lingua e una tabella codici particolari.<br/>                                                           |
| [**Un'STRINGTABLE**](stringtable.md)            | Descrive l'organizzazione dei dati in una risorsa di versione file. Contiene informazioni sulla formattazione della lingua e della tabella codici per le stringhe specificate dal membro **figlio** . Una tabella codici è un set di caratteri ordinato.<br/> |
| [**Var**](var-str.md)                        | Descrive l'organizzazione dei dati in una risorsa di versione file. Contiene in genere un elenco di coppie di identificatori di tabella codici e lingue supportate dalla versione dell'applicazione o dalla DLL.<br/>                             |
| [**VarFileInfo**](varfileinfo.md)            | Descrive l'organizzazione dei dati in una risorsa di versione file. Contiene informazioni sulla versione che non dipendono da una determinata combinazione di lingua e tabella codici.<br/>                                                        |
| [**VS \_ informazione FixedFileInfo**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) | Contiene informazioni sulla versione di un file. Queste informazioni sono indipendenti dalla lingua e dalla tabella codici. <br/>                                                                                                                   |
| [**VS \_ VERSIONINFO**](vs-versioninfo.md)     | Descrive l'organizzazione dei dati in una risorsa di versione file. Si tratta della struttura radice che contiene tutte le altre strutture di informazioni sulla versione del file.<br/>                                                                    |



 

 

 





