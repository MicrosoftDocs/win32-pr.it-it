---
description: Codifica e decodifica di un contesto di certificato tramite CryptoAPI.
ms.assetid: 149d1097-5f50-40ba-84f1-b815f54ba33d
title: Codifica e decodifica di un contesto di certificato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f640e12034ebf4ec84e0e71013197f043453b62e1102018dcfe9ea887d6ada
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874891"
---
# <a name="encoding-and-decoding-a-certificate-context"></a>Codifica e decodifica di un contesto di certificato

[*CryptoAPI*](../secgloss/c-gly.md) supporta la codifica e la decodifica dei [*certificati*](../secgloss/c-gly.md). CryptoAPI include un sistema esteso e flessibile di funzioni e strutture C che consentono la codifica e la decodifica in vari modi. CryptoAPI supporta la struttura del [*certificato X.509*](../secgloss/x-gly.md) standard e la codifica ASN.1 [*(Abstract Syntax Notation One)*](../secgloss/a-gly.md) standard per garantire l'interoperabilità con altri sistemi.

Per una panoramica dei dati codificati, vedere [Dati codificati e decodificati.](encoded-and-decoded-data.md)

## <a name="certificate-contexts"></a>Contesti di certificato

Un contesto [*del*](../secgloss/c-gly.md)certificato, [**CERT \_ CONTEXT,**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)è una struttura C che contiene un membro codificato, un handle a un archivio [*certificati,*](../secgloss/c-gly.md)un puntatore al [*BLOB*](../secgloss/c-gly.md)del certificato codificato originale e un puntatore a una [**struttura CERT \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) C.

La [**struttura CERT \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) è il centro del certificato. Contiene, in forma diretta e codificata, tutte le informazioni di base nel certificato. La figura seguente mostra la **struttura CERT \_ INFO** con tutti i membri codificati visualizzati come ombreggiati.

![Struttura delle \- informazioni sul certificato](images/certinf2.png)

I **membri IssuerUniqueID** e **SubjectUniqueID** fanno parte dell'implementazione del certificato [*X.509*](../secgloss/x-gly.md) versione 2, ma raramente vengono usati. Le estensioni del certificato nella versione 3 sostituiscono la funzionalità di questi membri.

Se le informazioni contenute nei membri codificati (ombreggiati) **Issuer** e **Subject** sono necessarie, tali membri devono essere decodificati. Usare [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) per decodificare questi membri. La figura seguente illustra il processo di decodifica di uno di questi membri.

![decodifica con cryptdecodeobject](images/infoflow.png)

Nel caso illustrato, la funzione [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) crea una struttura [**CERT \_ NAME \_ INFO,**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_name_info) una matrice di strutture [**\_ CERT RDN,**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn) una matrice corrispondente di strutture [**\_ CERT RDN \_ ATTR**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn_attr) e una stringa che contiene il nome. I membri della **struttura ATTR \_ RDN \_ CERT** determinano il contenuto della stringa. Ad esempio, se il **membro pszObjId** è 2.5.4.3, la stringa contiene un nome comune. Se è 2.5.4.10, la stringa conterrà il nome di un'organizzazione. Per un elenco di [*questi identificatori di oggetto*](../secgloss/o-gly.md) (OID), vedere **CERT \_ RDN \_ ATTR**.

Il **membro dwValueType** contiene informazioni sul tipo di stringa. Se è CERT RDN PRINTABLE STRING, il membro value contiene una stringa di caratteri a larghezza di \_ \_ byte con \_ terminazione zero. Se è CERT RDN UNICODE STRING, la stringa è una stringa di caratteri a larghezza doppia \_ \_ \_ (dimensioni della parola).

Per un processo dettagliato per la codifica e la decodifica dei certificati, vedere Codifica di una [struttura CERT \_ INFO](encoding-a-cert-info-structure.md) e [Decodifica di una struttura CERT \_ INFO.](decoding-a-cert-info-structure.md)

 

 
