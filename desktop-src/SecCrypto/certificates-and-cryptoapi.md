---
description: Un certificato X. 509 standard, contiene la versione, il numero di serie, l'identificatore dell'algoritmo, il nome dell'autorità emittente, l'intervallo di date valido, il nome del soggetto, l'algoritmo e le informazioni sulla chiave pubblica dell'oggetto e, facoltativamente, ID univoco dell'autorità di certificazione, ID univoco del soggetto ed estensioni.
ms.assetid: 91425185-2a06-4040-b83d-c42ee080d55f
title: Certificati e CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 325086ab0dd46ace85745ca292bcab9bcd5324e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309984"
---
# <a name="certificates-and-cryptoapi"></a>Certificati e CryptoAPI

[*CryptoAPI*](../secgloss/c-gly.md) supporta l'uso di certificati X. 509, come definito in [IETF RFC 3280](https://www.ietf.org/rfc/rfc3280.txt). In questa documentazione si presuppone l'utilizzo di un [*certificato digitale*](../secgloss/c-gly.md)X. 509 o analogo.

Un certificato X. 509 standard contiene le informazioni seguenti.



| Campo                | Descrizione                                                                                                                                                                                                                |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione              | Numero di versione del certificato.                                                                                                                                                                                         |
| Numero di serie        | Numero di serie del certificato.                                                                                                                                                                                          |
| Identificatore dell'algoritmo | Algoritmo di firma usato dal firmatario del certificato.                                                                                                                                                                        |
| Nome dell'autorità di certificazione          | Nome dell'emittente del certificato.                                                                                                                                                                                     |
| Non prima           | Data prima della quale il certificato non è valido.                                                                                                                                                                            |
| Non dopo            | Data dopo la quale il certificato non è valido.                                                                                                                                                                             |
| Nome soggetto         | Nome della persona o dell'entità a cui viene emesso il certificato.                                                                                                                                                      |
| Algoritmo            | Algoritmo utilizzato per la chiave pubblica.                                                                                                                                                                                         |
| Chiave pubblica del soggetto   | Chiave pubblica effettiva (stringa di bit).                                                                                                                                                                                          |
| ID univoco dell'autorità di certificazione     | Campo facoltativo. Se presente, la versione deve essere la versione 2.                                                                                                                                                                     |
| ID oggetto univoco    | Campo facoltativo. Se presente, la versione deve essere la versione 2.                                                                                                                                                                     |
| Estensioni           | Campo facoltativo. Rappresenta dati aggiuntivi che un emittente può voler aggiungere a un certificato, ad esempio l'indirizzo di posta elettronica o l'autorizzazione per emettere certificati. Se sono presenti estensioni, la versione deve essere la versione 3.<br/> |



 

 

 
