---
description: Microsoft Enhanced DSS and Diffie-Hellman Cryptographic Provider supporta lo scambio di chiavi Diffie-Hellman, l'hash SHA, la firma e la verifica dei dati DSA (FIPS 186-2) e gli algoritmi di crittografia simmetrica RC4.
ms.assetid: 90eca1e0-960f-4355-aef7-6e923100a6d8
title: Microsoft Enhanced DSS & Diffie-Hellman Cryptographic Provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3eb3e70d90224b2d97612c5d63380171d3239e11915da4cdd8a38a0faea0b8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119425441"
---
# <a name="microsoft-enhanced-dss--diffie-hellman-cryptographic-provider"></a>Microsoft Enhanced DSS & Diffie-Hellman Cryptographic Provider

Microsoft Enhanced DSS and [*Diffie-Hellman*](../secgloss/d-gly.md) Cryptographic Provider supporta lo scambio di chiavi *Diffie-Hellman,* l'hash SHA, la firma e la verifica dei dati DSA (FIPS 186-2) e gli algoritmi di crittografia simmetrica RC4.

<dl> Tipo di provider: **PROV \_ DSS \_ DH**  
Nome provider: **MS \_ ENH \_ DSS \_ DH \_ PROV**  
</dl>

Questo provider del servizio di crittografia supporta gli algoritmi seguenti.

| ID algoritmo          | Tipo di algoritmo  | Dimensioni predefinite (bit) | Descrizione                                                                                                                                                |
|-----------------------|-----------------|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CALG \_ CYLINK \_ MEK** | Crittografia dei dati | 40                  | Algoritmo di crittografia del messaggio CYLINK.                                                                                                                       |
| **CALG \_ RC2**         | Crittografia dei dati | 128                 | RSA RC2.                                                                                                                                                   |
| **CALG \_ RC4**         | Crittografia dei dati | 128                 | RSA RC4.                                                                                                                                                   |
| **CALG \_ DES**         | Crittografia dei dati | 56                  | Data Encryption Standard (DES).                                                                                                                            |
| **CALG \_ 3DES \_ 112**   | Crittografia dei dati | 112                 | DES triplo a due chiavi.                                                                                                                                        |
| **CALG \_ 3DES**        | Crittografia dei dati | 168                 | DES triplo a tre chiavi.                                                                                                                                      |
| **CALG \_ SHA1**        | Hash            | 160                 | Secure Hash Algorithm 1 (SHA-1).                                                                                                                           |
| **CALG \_ MD5**         | Hash            | 128                 | Message Digest 5 (MD5).                                                                                                                                    |
| **CALG \_ DSS \_ SIGN**   | Firma       | 1024                | Digital Signature Algorithm (DSA).                                                                                                                         |
| **CALG \_ DH \_ SF**      | Scambio di chiave    | 1024                | Archiviare e inoltrare l'algoritmo di scambio delle chiavi [*Diffie-Hellman.*](../secgloss/d-gly.md) |
| **CALG \_ DH \_ EPHEM**   | Scambio di chiave    | 1024                | [*Algoritmo phemeral Diffie-Hellman.*](../secgloss/d-gly.md)                      |



 

 

 
