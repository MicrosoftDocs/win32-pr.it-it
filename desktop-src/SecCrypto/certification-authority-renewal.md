---
description: Servizi certificati supporta il rinnovo di un'autorità di certificazione (CA).
ms.assetid: b6c76642-9a23-471e-af08-58e91d778f09
title: Rinnovo dell'autorità di certificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49f486e877e2ce1645cddf0099599e120776194dfd71e4e8b131d936c85e1f45
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993111"
---
# <a name="certification-authority-renewal"></a>Rinnovo dell'autorità di certificazione

[*Servizi certificati*](../secgloss/c-gly.md) supporta il rinnovo di un'autorità [*di certificazione*](../secgloss/c-gly.md) (CA). Il rinnovo è l'emissione di un nuovo certificato per l'autorità di certificazione per estendere la durata della CA oltre la data di fine del certificato originale. È possibile rinnovare una CA come attività nello snap-in MMC autorità di certificazione o usando lo strumento Certutil.exe (con il **comando -renewCert).**

Ogni rinnovo comporta un nuovo certificato DELLA CA. Tuttavia, l'amministratore può generare una nuova coppia di chiavi pubblica/privata o riutilizzare la coppia di chiavi pubblica/privata esistente per il certificato della CA. Per coerenza e integrità, i certificati CA e gli elenchi di [*revoche*](../secgloss/c-gly.md) di certificati (CRL) rilasciati dalla CA prima del rinnovo saranno disponibili dopo il rinnovo della CA. Per renderli disponibili, Servizi certificati gestisce un indice di certificati CA, CRL e chiavi.

Gli indici e i nomi dei suffissi dei certificati CA e dei CRL durante varie operazioni di rinnovo della CA sono i seguenti.



| Operazione                | Indice dei certificati CA | Suffisso del nome file del certificato CA | CRL e indice delle chiavi | CRL e suffisso del nome del contenitore di chiavi |
|--------------------------|----------------------|---------------------------------|-------------------|-----------------------------------|
| Installazione della CA originale | 0                    | ""                              | 0                 | ""                                |
| Rinnovo con nuova chiave     | 1                    | "(1)"                           | 1                 | "(1)"                             |
| Rinnovo della chiave di riutilizzo      | 2                    | "(2)"                           | 1                 | "(1)"                             |
| Rinnovo della chiave di riutilizzo      | 3                    | "(3)"                           | 1                 | "(1)"                             |
| Rinnovo con nuova chiave     | 4                    | "(4)"                           | 4                 | "(4)"                             |
| Rinnovo della chiave di riutilizzo      | 5                    | "(5)"                           | 4                 | "(4)"                             |
| Rinnovo con nuova chiave     | 6                    | "(6)"                           | 6                 | "(6)"                             |
| Rinnovo della chiave di riutilizzo      | 7                    | "(7)"                           | 6                 | "(6)"                             |



 

Quando viene installata una CA, l'indice del certificato è zero e il suffisso del certificato è "" (una stringa vuota). Ogni volta che il certificato viene rinnovato (indipendentemente dal fatto che le chiavi siano riutilizzate), l'indice del certificato viene incrementato di uno e il suffisso del nome file del certificato diventa una stringa nel formato "(*n*)", dove *n* rappresenta il numero di volte in cui il certificato CA è stato rinnovato. Dopo il primo rinnovo, l'indice del certificato è 1 e il suffisso del nome file del certificato è "(1)". Dopo il secondo rinnovo, l'indice del certificato è 2 e il suffisso del nome file del certificato è "(2)" e così via.

Anche se l'indice e il suffisso del certificato CA vengono incrementati di uno ogni volta che la CA viene rinnovata, gli indici CRL e chiave e i suffissi dei nomi file vengono impostati sull'indice del certificato ca solo se il processo di rinnovo include una nuova coppia di chiavi pubblica/privata. In caso contrario, i valori di questi indici e suffissi rimangono gli stessi dell'ultimo indice. Durante il rinnovo, un amministratore specifica se viene generata una nuova coppia di chiavi o se viene usata la coppia di chiavi esistente. Nello snap-in MMC Autorità di certificazione un'opzione nell'interfaccia utente specifica una coppia di chiavi nuova o esistente. Nello strumento Certutil.exe il comando **certutil -renewCert** rinnova la CA con una nuova coppia di chiavi, mentre il comando **certutil -renewCert ReuseKeys** rinnova la CA con la coppia di chiavi esistente.

L'indice CRL è direttamente associato all'indice delle chiavi, che viene impostato sull'indice del certificato CA solo quando per il rinnovo viene usata una nuova coppia di chiavi. Dopo il primo rinnovo (che ha usato una nuova coppia di chiavi), l'indice del CRL e della chiave viene impostato su 1 e il suffisso del nome del contenitore di chiavi e CRL è "(1)". Dopo il secondo rinnovo, tuttavia, l'indice del CRL e della chiave rimane 1 e anche il suffisso CRL e il nome del contenitore di chiavi rimangono "(1)"; ciò è dovuto al fatto che il secondo rinnovo ha usato la coppia di chiavi esistente e viene emesso un solo CRL per ogni coppia di chiavi ca.

È possibile recuperare i certificati ca indicizzati e i CRL chiamando il **metodo GetCertificateProperty** (in entrambe [**le interfacce ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) e [**ICertServerPolicy).**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) Quando si recuperano determinate proprietà correlate al certificato ca o al CRL, è possibile aggiungere l'indice in base zero del certificato CA ai nomi delle proprietà. Ad esempio, per recuperare l'indice CRL corrispondente al terzo certificato della CA, passare la proprietà "CRLIndex.2" a [**ICertServerPolicy::GetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-getcertificateproperty); per la tabella, il valore della proprietà "CRLIndex.2" recuperato sarà 1. Una proprietà denominata "CertCount" può essere usata per determinare il numero di volte in cui la CA ha rilasciato un certificato CA.

I certificati CA e i CRL contengono un'estensione che fornisce informazioni sul certificato e sull'indice delle chiavi. L'estensione è definita in Wincrypt.h come szOID CERTSRV CA VERSION con valore \_ \_ \_ "1.3.6.1.4.1.311.21.1". I dati dell'estensione sono un valore **DWORD** (codificato come X509 INTEGER nell'estensione); i 16 bit bassi sono l'indice del certificato e i 16 bit alti sono l'indice della \_ chiave.

L'installazione iniziale di una CA produce un indice del certificato pari a zero e un indice di chiave pari a zero. Il rinnovo di un certificato CA causerà l'incremento dell'indice del certificato. Se la chiave viene riutilizzata nel rinnovo, l'indice della chiave sarà lo stesso dell'indice di chiave precedente. Se la chiave non viene riutilizzata, l'indice della chiave corrisponderà al nuovo indice del certificato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ICertServerPolicy::GetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-getcertificateproperty)
</dt> <dt>

[**ICertServerExit::GetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverexit-getcertificateproperty)
</dt> </dl>

 

 
