---
description: La dimensione di una richiesta di accesso digest deve essere inferiore a 2048 byte.
ms.assetid: 16c6728a-966b-436f-902d-3e12368986b6
title: Contenuto di una richiesta digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97f90dd78ae28536f6e2d07882f69335975df14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128315"
---
# <a name="contents-of-a-digest-challenge"></a>Contenuto di una richiesta digest

La dimensione di una richiesta di accesso digest deve essere inferiore a 2048 byte. Nell'esempio seguente viene illustrata una richiesta di verifica assegnata alla stringa di caratteri szChallenge.


```C++
szChallenge = "realm=\"Microsoft_Example_Forest\",";
algorithm = "MD5-sess\", qop=\"auth\", nonce=\"0123456789abcdef\"";
```



> [!Note]  
> La stringa di verifica è racchiusa tra virgolette doppie e contiene virgolette doppie incorporate. Le virgolette doppie incorporate devono essere precedute (con caratteri di escape) con una barra rovesciata ( \\ ).

 

Una richiesta digest può contenere le direttive seguenti.



| Direttiva         | Descrizione                                                                                                                                                                                                                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| realm             | Hint definito dall'implementazione per il client su cui sono richieste le [*credenziali*](/windows/desktop/SecGloss/c-gly) . Se vengono richieste le credenziali, il client deve visualizzare queste informazioni all'utente.                                                  |
| algoritmo         | Microsoft Digest supporta MD5 e MD5-sess. Per ottenere prestazioni ottimali, usare MD5-sess.                                                                                                                                                                                                                     |
| qop               | Questa direttiva può essere impostata su auth, auth-int o auth-conf. Per ulteriori informazioni, vedere la pagina relativa alla [qualità della protezione e alle crittografie](quality-of-protection-and-ciphers.md).                                                                                                                                       |
| nonce             | Valore codificato univoco generato dal server per ogni richiesta di verifica. Il valore non deve essere modificato dal client.                                                                                                                                                                                       |
| opaco            | Contiene un riferimento per il [*contesto di sicurezza*](/windows/desktop/SecGloss/s-gly) che si sta stabilendo. Per ulteriori informazioni, vedere [gestione del contesto di sicurezza tra le connessioni](maintaining-the-security-context-between-connections.md). |
| Cipher (solo SASL) | Elenco di crittografie supportate dal server. Questo elemento può essere presente in una richiesta di autenticazione SASL digest solo se la direttiva qop specifica auth-conf. Per ulteriori informazioni, vedere la pagina relativa alla [qualità della protezione e alle crittografie](quality-of-protection-and-ciphers.md).                                              |
| charset           | Questa direttiva può essere impostata su UTF-8 se il server è in grado di elaborare i nomi utente e le aree di autenticazione con codifica UTF-8. Se il client riconosce la direttiva charset, può rispondere usando valori con codifica UTF-8.                                                                                                       |



 

Microsoft Digest genera la stringa di verifica del digest per le applicazioni server. Per informazioni dettagliate, vedere [generazione della richiesta digest](generating-the-digest-challenge.md).

 

 
