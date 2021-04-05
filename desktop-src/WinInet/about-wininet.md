---
title: Informazioni su WinINet
description: Windows Internet (WinINet) Application Programming Interface (API) consente all'applicazione di interagire con i protocolli FTP e HTTP per accedere alle risorse Internet.
ms.assetid: 0a06f2af-957a-4dff-a8cc-187370181b5c
keywords:
- Informazioni su WinINet WinINet
- WinINet WinINet, informazioni
- WinInet WinINet, pagina iniziale
- Windows Internet WinINet
- Internet, Windows Internet WinINet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4513e5c3912a483fd4dbef96f452c5712717c8a5
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "103956226"
---
# <a name="about-wininet"></a>Informazioni su WinINet

> [!NOTE]
> Per i contenitori di app a partire da Windows 10, versione 1709, HTTP/2 (vedere [RFC7540](https://tools.ietf.org/html/rfc7540)) è attiva per impostazione predefinita.

Windows Internet (WinINet) Application Programming Interface (API) consente all'applicazione di interagire con i protocolli FTP e HTTP per accedere alle risorse Internet. Con l'evolversi degli standard, queste funzioni gestiscono le modifiche apportate ai protocolli sottostanti, consentendo loro di mantenere un comportamento coerente.

**Windows XP e Windows Server 2003 R2 e versioni precedenti:** Inoltre, le applicazioni sono abilitate per interagire con gopher.

Per altre informazioni, vedere:

-   [WinINet rispetto a WinHTTP](wininet-vs-winhttp.md)
-   [Handle HINTERNET](appendix-a-hinternet-handles.md)
-   [Supporto IP versione 6](ip-version-6-support.md)
-   [Codifica del contenuto \_](content-encoding.md)
-   [Memorizzazione nella cache](caching.md)
-   [Funzioni comuni](common-functions.md)
-   [Sessioni FTP](ftp-sessions.md)
-   [Sessioni HTTP](http-sessions.md)
-   [Cookie HTTP](http-cookies.md)
-   [Operazione asincrona](asynchronous-operation.md)
-   [Gestione dell'autenticazione](handling-authentication.md)
-   [Gestione di localizzatori di risorse uniformi](handling-uniform-resource-locators.md)
-   [\_Linee guida sulla sicurezza](security-guidelines.md)

## <a name="internet-protocols"></a>Protocolli Internet

I due protocolli Internet primari sono FTP e HTTP. Per ulteriori informazioni su questi protocolli, vedere i documenti RFC (Request for Comments) per FTP e HTTP:

-   [RFC 959](https://www.ietf.org/rfc/rfc0959.txt), *File Transfer Protocol (FTP)*.
-   [RFC 1945](ftp://ftp.isi.edu/in-notes/rfc1945.txt), *Hypertext Transfer Protocol-HTTP/1.0*.
-   [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt), *Hypertext Transfer Protocol-HTTP/1.1*.

> [!NOTE]  
> Queste risorse potrebbero non essere disponibili in alcune lingue e paesi.

**Windows XP e Windows Server 2003 R2 e versioni precedenti:** È stato inoltre supportato il protocollo gopher. Vedere [RFC 1436](https://www.ietf.org/rfc/rfc1436.txt), *il protocollo Internet Gopher*.
