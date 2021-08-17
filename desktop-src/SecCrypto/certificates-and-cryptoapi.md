---
description: Un certificato X.509 standard, contiene versione, numero di serie, identificatore dell'algoritmo, nome dell'autorità emittente, intervallo di date valido, nome soggetto, algoritmo e informazioni sulla chiave pubblica del soggetto e, facoltativamente, ID univoco dell'autorità di certificazione, ID univoco del soggetto ed estensioni.
ms.assetid: 91425185-2a06-4040-b83d-c42ee080d55f
title: Certificati e CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8af32073cc3f42bbee07d1702fd1e6044c424ac236cf05ed8374c33757c1408
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770742"
---
# <a name="certificates-and-cryptoapi"></a>Certificati e CryptoAPI

[*CryptoAPI*](../secgloss/c-gly.md) supporta l'uso di certificati X.509 come definito in [IETF RFC 3280.](https://www.ietf.org/rfc/rfc3280.txt) Questa documentazione presuppone l'uso di un certificato digitale X.509 o [*comparabile.*](../secgloss/c-gly.md)

Un certificato X.509 standard contiene le informazioni seguenti.



| Campo                | Descrizione                                                                                                                                                                                                                |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione              | Numero di versione del certificato.                                                                                                                                                                                         |
| Numero di serie        | Numero di serie del certificato.                                                                                                                                                                                          |
| Identificatore dell'algoritmo | Algoritmo di firma usato dal firmatario del certificato.                                                                                                                                                                        |
| Nome dell'autorità di certificazione          | Nome dell'autorità emittente del certificato.                                                                                                                                                                                     |
| Non prima           | Data prima della quale il certificato non è valido.                                                                                                                                                                            |
| Non dopo            | Data dopo la quale il certificato non è valido.                                                                                                                                                                             |
| Nome soggetto         | Nome della persona o dell'entità a cui viene emesso il certificato.                                                                                                                                                      |
| Algoritmo            | Algoritmo usato per la chiave pubblica.                                                                                                                                                                                         |
| Chiave pubblica dell'oggetto   | Chiave pubblica effettiva (una stringa di bit).                                                                                                                                                                                          |
| ID univoco dell'autorità di emittente     | Campo facoltativo. Se presente, la versione deve essere la versione 2.                                                                                                                                                                     |
| ID univoco del soggetto    | Campo facoltativo. Se presente, la versione deve essere la versione 2.                                                                                                                                                                     |
| Estensioni           | Campo facoltativo. Rappresenta dati aggiuntivi che un'autorità di certificazione può aggiungere a un certificato, ad esempio l'indirizzo di posta elettronica o l'autorizzazione per rilasciare certificati. Se sono presenti estensioni, la versione deve essere la versione 3.<br/> |



 

 

 
