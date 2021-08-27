---
description: I dati in un contesto di certificato, elenco di revoche di certificati (CRL) o elenco di certificati attendibili (CTL), incluse eventuali estensioni, sono di sola lettura e non possono essere modificati.
ms.assetid: a9958c59-dc89-4d59-8ad3-6651ea4a1e56
title: Proprietà estese del certificato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c37eaf192d4c236a4f12898ece2bded86d467404c5eceedd98f1deb976b8857
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127091"
---
# <a name="certificate-extended-properties"></a>Proprietà estese del certificato

I dati in un contesto di [*certificato,*](../secgloss/c-gly.md)elenco di [*revoche*](../secgloss/c-gly.md) di certificati [](../secgloss/c-gly.md) (CRL) [](../secgloss/c-gly.md)o elenco di certificati attendibili (CTL), incluse eventuali estensioni, sono di sola lettura e non possono essere modificati. Tuttavia, nelle piattaforme Microsoft i certificati CryptoAPI hanno anche proprietà estese dinamiche che possono essere aggiunte e modificate.

> [!Note]  
> Le proprietà estese sono associate a un certificato e non fanno parte di un certificato rilasciato da [*un'autorità di certificazione*](../secgloss/c-gly.md) (CA). Le proprietà estese non sono disponibili in un certificato quando viene usato in una piattaforma non Microsoft.

 

Queste proprietà includono i dati che:

-   Si riferiscono alla chiave privata da usare con il certificato.
-   Indica il tipo di hash da eseguire sul certificato.
-   Fornisce informazioni definite dall'utente associate al certificato.

Nelle piattaforme Microsoft, i valori per queste proprietà vengono associati e spostati con il certificato. Le proprietà attualmente predefinite identificate con ID proprietà includono le proprietà seguenti:

-   Queste proprietà collegano un certificato a un CSP specifico e, all'interno di tale CSP, a una chiave privata specifica:
    -   CERT \_ KEY \_ PROV \_ HANDLE \_ PROP \_ ID
    -   CERT \_ KEY \_ PROV \_ INFO \_ PROP \_ ID
    -   CERT \_ KEY \_ CONTEXT \_ PROP \_ ID
-   Queste proprietà indicano l'algoritmo hash da usare quando viene eseguita un'operazione di hashing:
    -   CERT \_ SHA1 \_ HASH \_ PROP \_ ID
    -   CERT \_ MD5 \_ HASH \_ PROP \_ ID

Per elenchi completi delle proprietà del certificato esteso attualmente definite e descrizioni del significato e dell'uso di ogni proprietà, vedere [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) e [**CertSetCertificateContextProperty.**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextproperty)

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

 

 
