---
description: Il provider di crittografia Microsoft Enhanced DSS e Diffie-Hellman supporta Diffie-Hellman scambio di chiave, hash SHA, firma e verifica dei dati DSA (FIPS 186-2) e algoritmi di crittografia simmetrica RC4.
ms.assetid: 90eca1e0-960f-4355-aef7-6e923100a6d8
title: Microsoft Enhanced DSS & Diffie-Hellman provider di crittografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c42b4e504c1e5d4cb8ccfea7405580e37362f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307671"
---
# <a name="microsoft-enhanced-dss--diffie-hellman-cryptographic-provider"></a>Microsoft Enhanced DSS & Diffie-Hellman provider di crittografia

Il provider di crittografia Microsoft Enhanced DSS e [*Diffie-Hellman*](../secgloss/d-gly.md) supporta lo scambio di chiavi *Diffie-Hellman* , l'hashing Sha, la firma e la verifica dei dati DSA (FIPS 186-2) e gli algoritmi di crittografia simmetrica RC4.

<dl> Tipo di provider: **prova \_ DSS \_ DH**  
Nome provider: **MS \_ Enh \_ DSS \_ DH \_ prov**  
</dl>

Questo provider di crittografia supporta gli algoritmi seguenti.

| ID algoritmo          | Tipo di algoritmo  | Dimensioni predefinite (BITS) | Descrizione                                                                                                                                                |
|-----------------------|-----------------|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CALG \_ CYLINK \_ MEK** | Crittografia dei dati | 40                  | Algoritmo di crittografia del messaggio CYLINK.                                                                                                                       |
| **CALG \_ RC2**         | Crittografia dei dati | 128                 | RSA RC2.                                                                                                                                                   |
| **CALG \_ RC4**         | Crittografia dei dati | 128                 | RSA RC4.                                                                                                                                                   |
| **CALG \_ des**         | Crittografia dei dati | 56                  | Data Encryption Standard (DES).                                                                                                                            |
| **CALG \_ 3des \_ 112**   | Crittografia dei dati | 112                 | Due triple DES chiave.                                                                                                                                        |
| **\_3DES CALG**        | Crittografia dei dati | 168                 | Tre chiavi Triple DES.                                                                                                                                      |
| **CALG \_ SHA1**        | Hash            | 160                 | Secure Hash Algorithm 1 (SHA-1).                                                                                                                           |
| **\_MD5 CALG**         | Hash            | 128                 | Messaggio digest 5 (MD5).                                                                                                                                    |
| **\_firma CALG DSS \_**   | Firma       | 1024                | Algoritmo di firma digitale (DSA).                                                                                                                         |
| **CALG \_ DH \_ SF**      | Scambio di chiave    | 1024                | Archiviare e inviare l'algoritmo di scambio delle chiavi [*Diffie-Hellman*](../secgloss/d-gly.md) . |
| **CALG \_ DH \_ EPHEM**   | Scambio di chiave    | 1024                | Algoritmo temporaneo [*Diffie-Hellman*](../secgloss/d-gly.md) .                      |



 

 

 
