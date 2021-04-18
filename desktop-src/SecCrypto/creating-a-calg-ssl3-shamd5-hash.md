---
description: Viene illustrato come creare un \_ hash CALG SSL3 \_ SHAMD5.
ms.assetid: dad6fc7f-8abd-4f90-b3e4-8d0169e95087
title: Creazione di un hash di CALG_SSL3_SHAMD5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2f38b5939dc64467ef813b354f33a90f009619f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314134"
---
# <a name="creating-a-calg_ssl3_shamd5-hash"></a>Creazione di un \_ hash CALG SSL3 \_ SHAMD5

**Per creare un \_ hash CALG SSL3 \_ SHAMD5**

1.  Usando la metodologia CryptoAPI standard, creare sia un MD5 che un [*hash*](../secgloss/h-gly.md) [*Sha*](../secgloss/s-gly.md) dei dati di destinazione.
2.  Concatena i due hash, con il valore MD5 più a sinistra e il valore SHA a destra. Il risultato è un valore di 36 byte (16 byte + 20 byte).
3.  Ottenere un handle per un [*oggetto hash*](../secgloss/h-gly.md) chiamando [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) con CALG \_ SSL3 \_ SHAMD5 passato nel parametro *algido* .
4.  Impostare il valore hash con una chiamata a [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam). I valori hash concatenati vengono passati come **byte** \* nel parametro *PBDATA* e il \_ valore HP HASHVAL deve essere passato nel parametro *dwParam* . La chiamata di [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) con l'handle restituito da [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) nel passaggio 3 avrà esito negativo.
5.  Chiamare [**CryptSignHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha) per generare la firma.
6.  Chiamare [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) per eliminare definitivamente l'oggetto hash.

 

 
