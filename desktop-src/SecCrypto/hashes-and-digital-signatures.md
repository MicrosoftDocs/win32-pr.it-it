---
description: Con le funzioni hash e firma digitale, un utente può firmare digitalmente i dati in modo che qualsiasi altro utente possa verificare che i dati non siano stati modificati dopo la firma. È anche possibile verificare l'identità dell'utente che ha firmato i dati.
ms.assetid: dbe70506-f0d9-4239-a3af-8494fd6d4149
title: Hash e firme digitali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dc2894cbf53834551afef375fb5056df89675a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316164"
---
# <a name="hashes-and-digital-signatures"></a>Hash e firme digitali

Con le [funzioni hash e firma digitale](cryptography-functions.md), un utente può firmare digitalmente i dati in modo che qualsiasi altro utente possa verificare che i dati non siano stati modificati dopo la firma. È anche possibile verificare l'identità dell'utente che ha firmato i dati.

Una [*firma digitale*](../secgloss/d-gly.md) è costituita da una piccola quantità di dati binari, in genere inferiore a 256 byte. Questa firma può essere inclusa nel messaggio firmato o archiviata separatamente, a seconda della modalità di implementazione di una particolare applicazione.

Microsoft Strong Cryptographic Provider crea firme digitali conformi a RSA [*Public Key Cryptography Standards*](../secgloss/p-gly.md) (PKCS) \# 1.

 

 
