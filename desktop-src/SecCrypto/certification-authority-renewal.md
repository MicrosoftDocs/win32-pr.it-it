---
description: Servizi certificati supporta il rinnovo di un'autorità di certificazione (CA).
ms.assetid: b6c76642-9a23-471e-af08-58e91d778f09
title: Rinnovo dell'autorità di certificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de57cd16ae6fc4c90bfeea411a06efcb14d028b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966962"
---
# <a name="certification-authority-renewal"></a>Rinnovo dell'autorità di certificazione

[*Servizi certificati*](../secgloss/c-gly.md) supporta il rinnovo di un' [*autorità di certificazione*](../secgloss/c-gly.md) (CA). Il rinnovo è l'emissione di un nuovo certificato per la CA per estendere la durata della CA oltre la data di fine del certificato originale. È possibile rinnovare una CA come attività nello snap-in MMC dell'autorità di certificazione o utilizzando lo strumento Certutil.exe (con il comando **-renewCert** ).

Ogni rinnovo restituisce un nuovo certificato CA; Tuttavia, l'amministratore può generare una nuova coppia di chiavi pubblica/privata oppure riutilizzare la coppia di chiavi pubblica/privata esistente per il certificato della CA. Per coerenza e integrità, i certificati della CA e gli [*elenchi di revoche di certificati*](../secgloss/c-gly.md) (CRL) emessi dalla CA prima del rinnovo saranno disponibili dopo che l'autorità di certificazione è stata rinnovata. Per renderle disponibili, Servizi certificati mantiene un indice di certificati, CRL e chiavi della CA.

Gli indici e i nomi dei suffissi dei certificati della CA e dei CRL durante le varie operazioni di rinnovo della CA sono i seguenti.



| Operazione                | Indice certificato CA | Suffisso del nome file del certificato CA | CRL e indice chiave | Suffisso CRL e nome contenitore di chiavi |
|--------------------------|----------------------|---------------------------------|-------------------|-----------------------------------|
| Installazione della CA originale | 0                    | ""                              | 0                 | ""                                |
| Rinnovo con nuova chiave     | 1                    | "(1)"                           | 1                 | "(1)"                             |
| Rinnovo chiave riutilizzo      | 2                    | "(2)"                           | 1                 | "(1)"                             |
| Rinnovo chiave riutilizzo      | 3                    | "(3)"                           | 1                 | "(1)"                             |
| Rinnovo con nuova chiave     | 4                    | "(4)"                           | 4                 | "(4)"                             |
| Rinnovo chiave riutilizzo      | 5                    | "(5)"                           | 4                 | "(4)"                             |
| Rinnovo con nuova chiave     | 6                    | "(6)"                           | 6                 | "(6)"                             |
| Rinnovo chiave riutilizzo      | 7                    | "(7)"                           | 6                 | "(6)"                             |



 

Quando viene installata un'autorità di certificazione, l'indice del certificato è zero e il suffisso del certificato è "" (una stringa vuota). Ogni volta che il certificato viene rinnovato (indipendentemente dal fatto che le chiavi vengano riutilizzate), l'indice del certificato viene incrementato di uno e il suffisso del nome del file del certificato diventa una stringa nel formato "(*n*)", dove *n* rappresenta il numero di volte in cui il certificato della CA è stato rinnovato. Dopo il primo rinnovo, l'indice del certificato è 1 e il suffisso del nome del file del certificato è "(1)". Dopo il secondo rinnovo, l'indice del certificato è 2 e il suffisso del nome del file del certificato è "(2)" e così via.

Anche se l'indice e il suffisso del certificato della CA vengono incrementati di uno ogni volta che l'autorità di certificazione viene rinnovata, il CRL e gli indici delle chiavi e i suffissi dei nomi di file vengono impostati sull'indice del certificato CA solo se il processo di rinnovo include una nuova coppia di chiavi pubblica/privata. In caso contrario, i valori di questi indici e suffissi rimangono invariati per l'ultimo indice. Durante il rinnovo, un amministratore specifica se viene generata una nuova coppia di chiavi o se viene utilizzata la coppia di chiavi esistente. Nello snap-in MMC dell'autorità di certificazione, un'opzione nell'interfaccia utente specifica una coppia di chiavi nuova o esistente. nello strumento Certutil.exe il comando **certutil-renewCert** rinnova la CA con una nuova coppia di chiavi, mentre il comando **certutil-renewCert REUSEKEYS** rinnova la CA con la coppia di chiavi esistente.

L'indice CRL è direttamente associato all'indice della chiave, che è impostato sull'indice del certificato della CA solo quando per il rinnovo viene utilizzata una nuova coppia di chiavi. Dopo il primo rinnovo (che usava una nuova coppia di chiavi), l'indice del CRL e della chiave è impostato su 1, mentre il suffisso CRL e il suffisso del nome del contenitore di chiavi sono "(1)". Dopo il secondo rinnovo, tuttavia, l'indice del CRL e della chiave rimane 1 e anche il suffisso CRL e il suffisso del nome del contenitore di chiavi rimangono "(1)"; Questo perché il secondo rinnovo usava la coppia di chiavi esistente e viene emesso un solo CRL per ogni coppia di chiavi della CA.

È possibile recuperare i certificati e i CRL della CA indicizzata chiamando il metodo **GetCertificateProperty** (in entrambe le interfacce [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) e [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) ). Quando si recuperano determinate proprietà correlate al certificato della CA o al CRL, è possibile aggiungere l'indice in base zero del certificato CA ai nomi delle proprietà. Ad esempio, per recuperare l'indice CRL che corrisponde al terzo certificato della CA, passare la proprietà "CRLIndex. 2" a [**ICertServerPolicy:: GetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-getcertificateproperty); per la tabella, il valore della proprietà "CRLIndex. 2" recuperato sarà 1. Una proprietà denominata "CertCount" può essere usata per determinare il numero di volte in cui l'autorità di certificazione ha emesso un certificato CA.

I certificati della CA e i CRL contengono un'estensione che fornisce informazioni sul certificato e sull'indice della chiave. L'estensione è definita in WinCrypt. h come szOID \_ CERTSRV \_ CA \_ Version con un valore di "1.3.6.1.4.1.311.21.1". I dati dell'estensione sono un valore **DWORD** (codificato come X509 \_ Integer nell'estensione), i 16 bit bassi sono l'indice del certificato e i 16 bit alti sono l'indice della chiave.

L'installazione iniziale di una CA produce un indice del certificato pari a zero e un indice chiave pari a zero. Il rinnovo di un certificato della CA provocherà l'incremento dell'indice del certificato. Se la chiave viene riutilizzata nel rinnovo, l'indice chiave sarà lo stesso dell'indice chiave precedente. Se la chiave non viene riutilizzata, l'indice della chiave corrisponderà al nuovo indice del certificato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ICertServerPolicy::GetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-getcertificateproperty)
</dt> <dt>

[**ICertServerExit::GetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverexit-getcertificateproperty)
</dt> </dl>

 

 
