---
description: CryptoAPI fornisce funzioni per l'utilizzo di certificati, elenchi di revoche di certificati (CRL) ed elenchi di certificati attendibili (scopi consentiti).
ms.assetid: 23460329-44ed-4bcb-9727-5c841070f093
title: Operazioni con certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab2f9f5d6d541b452741f2e4634752b979f26107
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884041"
---
# <a name="operations-with-certificates"></a>Operazioni con certificati

[*CryptoAPI*](../secgloss/c-gly.md) fornisce funzioni per l'utilizzo di [*certificati*](../secgloss/c-gly.md), [*elenchi di revoche di certificati*](../secgloss/c-gly.md) (CRL) ed elenchi di certificati [*attendibili*](../secgloss/c-gly.md) (scopi consentiti). Queste includono funzioni per la conversione di tipi codificati in tipi di contesto, funzioni che duplicano oggetti e funzioni che liberano questi oggetti. Queste funzioni codificano le informazioni in contesti, ma non aggiungono questo contesto a nessun archivio. Queste funzioni sono [**CertCreateCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecertificatecontext), [**CertCreateCRLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecrlcontext)e [**CertCreateCTLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatectlcontext). Usare la funzione CertFree appropriata per liberare i contesti creati da una di queste funzioni.

Le funzioni CryptoAPI per duplicare i certificati, i CRL e scopi consentiti incrementano il [*contatore dei riferimenti*](../secgloss/r-gly.md) nel contesto specificato e restituiscono un puntatore al contesto. Le funzioni di duplicazione non allocano spazio aggiuntivo o copiano i dati da un contesto in una nuova posizione di memoria. Queste funzioni sono [**CertDuplicateCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecertificatecontext), [**CertDuplicateCRLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecrlcontext)e [**CertDuplicateCTLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatectlcontext). I contesti creati con una di queste funzioni devono essere liberati utilizzando la funzione CertFree appropriata.

Le funzioni CryptoAPI che liberano certificati, CRL e scopi consentiti sono [**CertFreeCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext), [**CertFreeCRLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecrlcontext)e [**CertFreeCTLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreectlcontext). Ognuna di queste funzioni riduce il [*conteggio dei riferimenti*](../secgloss/r-gly.md) in un contesto. Se il conteggio dei riferimenti raggiunge zero, la memoria allocata per il contesto viene rilasciata.

Per elenchi completi di funzioni per l'utilizzo di certificati, CRL e scopi consentiti, vedere funzioni di [manutenzione dell'archivio certificati e](cryptography-functions.md)certificati, funzioni di [certificato](cryptography-functions.md), funzioni dell'elenco di [revoche di certificati](cryptography-functions.md)e [funzioni elenco certificati attendibili](cryptography-functions.md).

 

 
