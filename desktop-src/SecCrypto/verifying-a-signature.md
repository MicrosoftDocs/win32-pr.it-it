---
description: Per verificare una firma, creare un oggetto hash usando CryptCreateHash. Questo oggetto hash accumula i dati da verificare. I dati vengono quindi aggiunti all'oggetto hash con la funzione CryptHashData.
ms.assetid: 3779f83b-0d87-4f47-949b-9eb39690adfb
title: Verifica di una firma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26b3ea56533a9e04a53d847c80b1172ff155e847b8c9d5cf9b0f2ab3e24c8ba0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118896247"
---
# <a name="verifying-a-signature"></a>Verifica di una firma

Per verificare una firma, creare un [*oggetto hash*](../secgloss/h-gly.md) [**usando CryptCreateHash.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) Questo oggetto hash accumula i dati da verificare. I dati vengono quindi aggiunti all'oggetto hash con la [**funzione CryptHashData.**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata)

Dopo aver aggiunto l'ultimo blocco di dati all'hash, [**usare CryptVerifySignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea) per verificare la firma. L'indirizzo dei dati della firma, un handle per l'oggetto hash e l'handle delle chiavi pubbliche vengono passati a **CryptVerifySignature.**

Dopo che la firma è stata verificata (o non ha superato la verifica), eliminare l'oggetto hash usando la [**funzione CryptDestroyHash.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash)

 

 
