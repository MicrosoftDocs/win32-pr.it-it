---
description: Con Funzioni hash e firma digitale, un utente può firmare digitalmente i dati in modo che qualsiasi altro utente possa verificare che i dati non siano stati modificati dopo la firma. È anche possibile verificare l'identità dell'utente che ha firmato i dati.
ms.assetid: dbe70506-f0d9-4239-a3af-8494fd6d4149
title: Hash e firme digitali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdd6367217343a067bbdd0d5a4ad5e9f4f47e9b744ee9f159046259ec2e26185
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006489"
---
# <a name="hashes-and-digital-signatures"></a>Hash e firme digitali

Con [Funzioni hash e firma](cryptography-functions.md)digitale , un utente può firmare digitalmente i dati in modo che qualsiasi altro utente possa verificare che i dati non siano stati modificati dopo la firma. È anche possibile verificare l'identità dell'utente che ha firmato i dati.

Una [*firma digitale*](../secgloss/d-gly.md) è costituita da una piccola quantità di dati binari, in genere inferiori a 256 byte. Questa firma può essere in bundle con il messaggio firmato o archiviata separatamente, a seconda di come è stata implementata una particolare applicazione.

Microsoft Strong Cryptographic Provider crea firme digitali conformi a RSA [*Public Key Cryptography Standards*](../secgloss/p-gly.md) (PKCS) \# 1.

 

 
