---
title: Informazioni su WinINet
description: L Windows'API (Application Programming Interface) di WinINet consente all'applicazione di interagire con i protocolli FTP e HTTP per accedere alle risorse Internet.
ms.assetid: 0a06f2af-957a-4dff-a8cc-187370181b5c
keywords:
- Informazioni su WinINet WinINet
- WinINet WinINet , informazioni su
- WinINet WinINet , pagina iniziale
- Windows Internet WinINet
- Internet, Windows Internet WinINet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be38840c33735a1e064e9bdc5e044651130d6e15a6fe22d004a2e8d7c29bf140
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051869"
---
# <a name="about-wininet"></a>Informazioni su WinINet

> [!NOTE]
> Per i contenitori di app Windows 10 versione 1709, HTTP/2 (vedere [RFC7540)](https://tools.ietf.org/html/rfc7540)è on per impostazione predefinita.

L Windows'API (Application Programming Interface) di WinINet consente all'applicazione di interagire con i protocolli FTP e HTTP per accedere alle risorse Internet. Con l'evolversi degli standard, queste funzioni gestiscono le modifiche nei protocolli sottostanti, consentendo loro di mantenere un comportamento coerente.

**Windows XP e Windows Server 2003 R2 e versioni precedenti:** Le applicazioni sono anche abilitate per l'interazione con Gopher.

Per altre informazioni, vedere:

-   [Confronto tra WinINet e WinHTTP](wininet-vs-winhttp.md)
-   [Handle HINTERNET](appendix-a-hinternet-handles.md)
-   [Supporto ip versione 6](ip-version-6-support.md)
-   [Codifica \_ del contenuto](content-encoding.md)
-   [Memorizzazione nella cache](caching.md)
-   [Funzioni comuni](common-functions.md)
-   [Sessioni FTP](ftp-sessions.md)
-   [Sessioni HTTP](http-sessions.md)
-   [Cookie HTTP](http-cookies.md)
-   [Operazione asincrona](asynchronous-operation.md)
-   [Gestione dell'autenticazione](handling-authentication.md)
-   [Gestione dei localizzatori di risorse uniformi](handling-uniform-resource-locators.md)
-   [Linee \_ guida sulla sicurezza](security-guidelines.md)

## <a name="internet-protocols"></a>Protocolli Internet

I due protocolli Internet principali sono FTP e HTTP. Per altre informazioni su questi protocolli, vedere i documenti Request For Comments (RFC) per FTP e HTTP:

-   [RFC 959](https://www.ietf.org/rfc/rfc0959.txt), *File Transfer Protocol (FTP)*.
-   [RFC 1945](ftp://ftp.isi.edu/in-notes/rfc1945.txt), *Hypertext Transfer Protocol - HTTP/1.0*.
-   [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt), *Hypertext Transfer Protocol - HTTP/1.1*.

> [!NOTE]  
> Queste risorse potrebbero non essere disponibili in alcune lingue e paesi.

**Windows XP e Windows Server 2003 R2 e versioni precedenti:** È stato supportato anche il protocollo Gopher. Vedere [RFC 1436](https://www.ietf.org/rfc/rfc1436.txt), *Internet Gopher Protocol*.
