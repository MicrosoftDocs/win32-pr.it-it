---
description: Viene illustrato come creare una richiesta di certificato e come ricevere e archiviare il certificato restituito in un archivio certificati.
ms.assetid: 4ca3d6cb-6ce7-4408-9258-6e40c8219dc0
title: Uso del controllo di registrazione certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ac3da319571b164fe66eb5bb3ac647c2978fff7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308644"
---
# <a name="using-certificate-enrollment-control"></a>Uso del controllo di registrazione certificati

Il controllo di registrazione dei certificati è un singolo oggetto con molte proprietà e diversi metodi che possono essere usati per determinare il modo in cui il controllo di registrazione certificati elabora le informazioni utente, il tipo di certificato da richiedere, il modo in cui devono essere generate le chiavi, il certificato da archiviare e i processi correlati. Il controllo di registrazione dei certificati prevede due utilizzi principali: per creare una richiesta di [*certificato*](../secgloss/c-gly.md) (PKCS \# 10) e per ricevere il certificato restituito e archiviarlo in un [*archivio certificati*](../secgloss/c-gly.md). Per informazioni dettagliate e la sintassi per la creazione di un'istanza dell'oggetto controllo di registrazione certificati, l'impostazione delle relative proprietà e l'utilizzo dei relativi metodi, vedere gli argomenti seguenti.



| Informazioni                                                                                                                                                                                           | Argomento                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| Creazione di un'istanza dell'oggetto controllo registrazione certificati in diversi linguaggi di programmazione                                                                                                  | [Creazione di un'istanza dell'oggetto controllo di registrazione certificati](creating-an-instance-of-the-certificate-enrollment-control-object.md) |
| Uso delle proprietà del controllo di registrazione certificati in diversi linguaggi di programmazione                                                                                                                    | [Uso delle proprietà del controllo di registrazione certificati](using-the-certificate-enrollment-control-properties.md)                             |
| Raccolta delle informazioni necessarie e invio di una [*richiesta di certificato*](../secgloss/c-gly.md) in diversi linguaggi di programmazione. | [Creazione della richiesta di certificato](creating-the-certificate-request.md)                                                                   |
| Estrazione e archiviazione del certificato completato                                                                                                                                                      | [Ricezione del certificato restituito](receiving-the-returned-certificate.md)                                                               |
| Recupero di informazioni dai valori restituiti in lingue diverse                                                                                                                                      | [Valori restituiti dal metodo](method-return-values.md)                                                                                           |
| Verifica degli errori                                                                                                                                                                                   | [Controllo errori](error-checking.md)                                                                                                       |



 

 

 
