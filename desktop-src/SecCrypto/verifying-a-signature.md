---
description: Per verificare una firma, creare un oggetto hash usando CryptCreateHash. Questo oggetto hash accumula i dati da verificare. I dati vengono quindi aggiunti all'oggetto hash con la funzione CryptHashData.
ms.assetid: 3779f83b-0d87-4f47-949b-9eb39690adfb
title: Verifica di una firma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9a416dc2c3f7523af781e68fe78b066accbe6d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130226"
---
# <a name="verifying-a-signature"></a>Verifica di una firma

Per verificare una firma, creare un [*oggetto hash*](../secgloss/h-gly.md) usando [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash). Questo oggetto hash accumula i dati da verificare. I dati vengono quindi aggiunti all'oggetto hash con la funzione [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) .

Dopo l'aggiunta dell'ultimo blocco di dati all'hash, utilizzare [**CryptVerifySignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea) per verificare la firma. L'indirizzo dei dati della firma, un handle per l'oggetto hash e l'handle delle chiavi pubbliche vengono passati a **CryptVerifySignature**.

Dopo che la firma è stata verificata (o non ha superato la verifica), eliminare definitivamente l'oggetto hash usando la funzione [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) .

 

 
