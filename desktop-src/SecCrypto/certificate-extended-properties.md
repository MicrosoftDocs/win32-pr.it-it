---
description: I dati in un certificato, un elenco di revoche di certificati (CRL) o un contesto elenco certificati attendibili (CTL), incluse eventuali estensioni, sono di sola lettura e non possono essere modificati.
ms.assetid: a9958c59-dc89-4d59-8ad3-6651ea4a1e56
title: Proprietà estese del certificato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f29853736433cb143a201ca352fceff0141cc96f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131051"
---
# <a name="certificate-extended-properties"></a>Proprietà estese del certificato

I dati in un [*certificato*](../secgloss/c-gly.md), un [*elenco di revoche di certificati*](../secgloss/c-gly.md) (CRL) o un [*contesto*](../secgloss/c-gly.md) [*elenco certificati attendibili*](../secgloss/c-gly.md) (CTL), incluse eventuali estensioni, sono di sola lettura e non possono essere modificati. Tuttavia, sulle piattaforme Microsoft, i certificati CryptoAPI hanno anche proprietà estese dinamiche che possono essere aggiunte e modificate.

> [!Note]  
> Le proprietà estese sono associate a un certificato e non fanno parte di un certificato emesso da un' [*autorità di certificazione*](../secgloss/c-gly.md) (CA). Le proprietà estese non sono disponibili in un certificato quando viene usato in una piattaforma non Microsoft.

 

Queste proprietà includono i dati che:

-   Si riferisce alla chiave privata da usare con il certificato.
-   Indica il tipo di hash da eseguire sul certificato.
-   Fornisce informazioni definite dall'utente associate al certificato.

Sulle piattaforme Microsoft, i valori di queste proprietà vengono collegati e spostati con il certificato. Le proprietà attualmente predefinite identificate con ID proprietà includono le proprietà seguenti:

-   Queste proprietà legano un certificato a un particolare CSP e, all'interno di tale CSP, a una chiave privata specifica:
    -   \_ \_ \_ ID Prop dell'handle \_ della chiave CERT \_
    -   \_ID di \_ attestazione della chiave \_ CERT \_ \_
    -   \_ \_ ID Prop del contesto della chiave CERT \_ \_
-   Queste proprietà indicano l'algoritmo hash da usare quando viene eseguita un'operazione di hashing:
    -   \_ID proprietà \_ hash \_ SHA1 \_ CERT
    -   \_ID della \_ prop di hash MD5 \_ CERT \_

Per gli elenchi completi delle proprietà del certificato esteso attualmente definite e delle descrizioni del significato e dell'uso di ogni proprietà, vedere [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) e [**CertSetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextproperty).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**CertGetCRLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcrlcontextproperty)
</dt> <dt>

[**CertGetCTLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetctlcontextproperty)
</dt> <dt>

[**CertSetCRLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcrlcontextproperty)
</dt> <dt>

[**CertSetCTLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetctlcontextproperty)
</dt> </dl>

 

 
