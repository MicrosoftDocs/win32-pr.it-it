---
description: Lo scopo dell'algoritmo Diffie-Hellman consiste nel consentire a due o più host di creare e condividere una chiave di crittografia segreta identica, condividendo semplicemente le informazioni su una rete non sicura.
ms.assetid: f89a1268-e364-41ec-a6a8-1f6331dbb787
title: Algoritmi del provider Diffie-Hellman/SChannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e4fb88e3a50e15a6690340ab3fbcee91da1193a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350141"
---
# <a name="diffie-hellmanschannel-provider-algorithms"></a>Algoritmi del provider Diffie-Hellman/SChannel

Lo scopo dell'algoritmo Diffie-Hellman consiste nel consentire a due o più host di creare e condividere una chiave di crittografia segreta identica, condividendo semplicemente le informazioni su una rete non sicura. Le informazioni che vengono condivise sulla rete sono sotto forma di un paio di valori costanti e una chiave pubblica D-H.

Il provider di crittografia Microsoft [*Diffie-Hellman*](../secgloss/d-gly.md) / [*Schannel*](../secgloss/s-gly.md) supporta gli algoritmi seguenti.



| ID algoritmo                  | Descrizione                                                                                                                                           | Commenti                                                                                                   |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| CALG \_ DH \_ SF                  | Algoritmo di scambio delle [ *chiavi* in Diffie-Hellman Store e in futuro](../secgloss/k-gly.md) | Lunghezza della chiave: è possibile impostare 384 bit su 512 bit in incrementi di 8 bit. Lunghezza chiave predefinita: 512 bit.<br/> |
| \_MD5 CALG                     | Algoritmo di hash MD5.                                                                                                                                | Fornito solo per l'hashing.                                                                                 |
| CALG \_ DH \_ EPHEM               | Scambio di chiavi temporaneo D-H.                                                                                                                           | Lunghezza della chiave: è possibile impostare 384 bit su 512 bit in incrementi di 8 bit. Lunghezza chiave predefinita: 512 bit.<br/> |
| \_Sha CALG                     | Algoritmo di hash SHA.                                                                                                                                | Deve essere usato per le firme DSS.                                                                           |
| CALG \_ RC2                     | Algoritmo di crittografia a blocchi RC2                                                                                                                        | Lunghezza della chiave: da 40 a 88 bit.                                                                                 |
| CALG \_ RC4                     | Algoritmo di crittografia del flusso RC4                                                                                                                       | Lunghezza della chiave: da 40 a 88 bit.                                                                                 |
| CALG \_ CYLINK \_ MEK<br/> | Algoritmo di crittografia DES Variant                                                                                                                      | Lunghezza della chiave: 40 bit.                                                                                       |



 

 

 
