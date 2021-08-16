---
description: Viene illustrato come creare una richiesta di certificato e ricevere e archiviare il certificato restituito in un archivio certificati.
ms.assetid: 4ca3d6cb-6ce7-4408-9258-6e40c8219dc0
title: Uso del controllo registrazione certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d489edb7ed288ffc0b51d039c6c32df90631b833d491567729f075c1cee9cae0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117971758"
---
# <a name="using-certificate-enrollment-control"></a>Uso del controllo registrazione certificati

Il controllo registrazione certificati è un singolo oggetto con molte proprietà e diversi metodi che possono essere usati per determinare il modo in cui il controllo registrazione certificati elabora le informazioni utente, il tipo di certificato da richiedere, la modalità di generazione delle chiavi, la posizione in cui deve essere archiviato il certificato e i processi correlati. Esistono due usi principali del controllo registrazione [](../secgloss/c-gly.md) certificati: per creare una richiesta di certificato (PKCS 10) e per ricevere il certificato restituito e archiviarlo in un \# [*archivio certificati*](../secgloss/c-gly.md). Per informazioni dettagliate e sintassi per la creazione di un'istanza dell'oggetto Certificate Enrollment Control, l'impostazione delle proprietà e l'uso dei relativi metodi, vedere gli argomenti seguenti.



| Informazioni                                                                                                                                                                                           | Argomento                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| Creazione di un'istanza dell'oggetto Certificate Enrollment Control in linguaggi di programmazione diversi                                                                                                  | [Creazione di un'istanza dell'oggetto controllo registrazione certificati](creating-an-instance-of-the-certificate-enrollment-control-object.md) |
| Uso delle proprietà del controllo registrazione certificati in linguaggi di programmazione diversi                                                                                                                    | [Uso delle proprietà del controllo registrazione certificati](using-the-certificate-enrollment-control-properties.md)                             |
| Raccolta delle informazioni necessarie e invio di una [*richiesta di certificato*](../secgloss/c-gly.md) in linguaggi di programmazione diversi. | [Creazione della richiesta di certificato](creating-the-certificate-request.md)                                                                   |
| Estrazione e archiviazione del certificato completato                                                                                                                                                      | [Ricezione del certificato restituito](receiving-the-returned-certificate.md)                                                               |
| Recupero di informazioni dai valori restituiti in lingue diverse                                                                                                                                      | [Valori restituiti dal metodo](method-return-values.md)                                                                                           |
| Controllo degli errori                                                                                                                                                                                   | [Controllo degli errori](error-checking.md)                                                                                                       |



 

 

 
