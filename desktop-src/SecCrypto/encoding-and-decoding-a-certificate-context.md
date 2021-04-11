---
description: Codifica e decodifica di un contesto di certificato tramite CryptoAPI.
ms.assetid: 149d1097-5f50-40ba-84f1-b815f54ba33d
title: Codifica e decodifica di un contesto del certificato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4168d15ad8db5d4711a18f2042106e7d6d46010
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226440"
---
# <a name="encoding-and-decoding-a-certificate-context"></a>Codifica e decodifica di un contesto del certificato

[*CryptoAPI*](../secgloss/c-gly.md) supporta la codifica e la decodifica dei [*certificati*](../secgloss/c-gly.md). CryptoAPI include un sistema completo e flessibile di funzioni e strutture C che consentono la codifica e la decodifica in diversi modi. CryptoAPI supporta la struttura di certificati [*X. 509*](../secgloss/x-gly.md) standard e la codifica ASN. 1 (standard [*Abstract Syntax Notation One*](../secgloss/a-gly.md) ) per garantire l'interoperabilità con altri sistemi.

Per una panoramica dei dati codificati, vedere [dati codificati e decodificati](encoded-and-decoded-data.md).

## <a name="certificate-contexts"></a>Contesti di certificato

Un [*contesto del certificato*](../secgloss/c-gly.md), un [**\_ contesto**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)del certificato, è una struttura C che contiene un membro codificato, un handle per un [*archivio certificati*](../secgloss/c-gly.md), un puntatore al [*BLOB del certificato*](../secgloss/c-gly.md)codificato originale e un puntatore a una struttura di [**\_ informazioni**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) del certificato.

La struttura delle [**\_ informazioni**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) sul certificato è il cuore del certificato. Contiene, in formato diretto e in formato codificato, tutte le informazioni di base del certificato. Nella figura seguente viene illustrata la struttura di **\_ info CERT** con tutti i membri codificati visualizzati come ombreggiati.

![\-struttura di informazioni CERT](images/certinf2.png)

I membri **IssuerUniqueID** e **SubjectUniqueID** fanno parte dell'implementazione del certificato [*X. 509*](../secgloss/x-gly.md) versione 2, ma vengono usati raramente. Le estensioni del certificato nella versione 3 sostituiscono la funzionalità di questi membri.

Se sono necessarie le informazioni contenute nell' **emittente** e nell' **oggetto** con codifica (ombreggiata), i membri devono essere decodificati. Usare [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) per decodificare questi membri. Nella figura seguente viene illustrato il processo di decodifica di uno di questi membri.

![decodifica con cryptdecodeobject](images/infoflow.png)

Nel caso illustrato, la funzione [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) crea una struttura [**di \_ \_ informazioni sul nome del certificato**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_name_info) , una matrice di strutture [**\_ RDN CERT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn) , una matrice corrispondente di strutture [**\_ RDN RDN \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn_attr) e una stringa che contiene il nome. I membri della struttura di **\_ RDN \_ RDN del certificato** determinano il contenuto della stringa. Se, ad esempio, il membro **pszObjId** è 2.5.4.3, la stringa contiene un nome comune. Se è 2.5.4.10, la stringa conterrà un nome di organizzazione. Per un elenco di questi [*identificatori di oggetto*](../secgloss/o-gly.md) (OID), vedere **CERT \_ RDN \_ attr**.

Il membro **dwValueType** contiene informazioni sul tipo di stringa. Se è \_ \_ una stringa stampabile di tipo RDN \_ , il membro del valore contiene una stringa di caratteri con terminazione di byte e di lunghezza zero. Se è una stringa \_ \_ Unicode del certificato RDN \_ , la stringa è una stringa di caratteri a larghezza doppia (con dimensione di Word).

Per un processo dettagliato per la codifica e la decodifica dei certificati, vedere [codifica di una \_ struttura di informazioni del certificato](encoding-a-cert-info-structure.md) e [decodifica di una \_ struttura di informazioni del certificato](decoding-a-cert-info-structure.md).

 

 
