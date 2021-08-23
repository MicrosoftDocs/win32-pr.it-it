---
description: A partire dal formato del certificato X.509 versione 3, un certificato può contenere estensioni del certificato.
ms.assetid: fb106cab-8a61-4a83-8fb4-7c045d905575
title: Gestori di estensioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cba61c5896887471038325eba0dbed75f43061cff81452727933a3013c37f8aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006929"
---
# <a name="extension-handlers"></a>Gestori di estensioni

A partire [*dal formato del certificato X.509*](../secgloss/x-gly.md) versione 3, un certificato può contenere estensioni del certificato. Per il contenuto di un certificato X.509, vedere [Proprietà certificato.](certificate-properties.md) Queste estensioni indicano informazioni aggiuntive. Ad esempio, un'estensione può indicare informazioni aggiuntive sull'identificazione del soggetto oppure può indicare informazioni sull'utilizzo della chiave, che specifica le attività (ad esempio firma o crittografia) per le quali è possibile usare una chiave. Un set di estensioni standard è definito per l'uso dell'applicazione e le estensioni possono anche essere personalizzate.

A ogni estensione è associata una stringa di identificatore di oggetto che identifica il tipo di informazioni aggiuntive e una struttura di dati che contiene queste informazioni. Ad esempio, l'identificatore dell'oggetto di utilizzo della chiave è "2.5.29.15", che indica le informazioni sull'utilizzo della chiave. La struttura dei dati associata è [**un \_ \_ BLOB BIT CRYPT**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_bit_blob) (bitfield) che specifica come usare la chiave.

Un'estensione può essere aggiunta a un certificato prima dell'emissione. Quando il certificato viene emesso, tutte le estensioni abilitate fanno parte del certificato. Se un'estensione è contrassegnata come critica, il relativo utilizzo deve essere noto dall'applicazione using e l'applicazione deve rispettare la finalità o il valore dell'estensione. Servizi certificati consente di impostare le estensioni in un certificato non emesso tramite i metodi forniti da [**ICertAdmin**](/windows/desktop/api/Certadm/nn-certadm-icertadmin) e [**ICertServerPolicy.**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) Per informazioni dettagliate sulle estensioni certificato, vedere [**CERT \_ EXTENSION**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) nella documentazione di CryptoAPI. Per informazioni sulle strutture di dati comuni dell'estensione del certificato, vedere Strutture delle estensioni certificato [X.509](cryptography-structures.md).

Il gestore dell'estensione è un oggetto COM che fornisce routine per codificare le estensioni e i tipi di dati più complessi, ma comunemente usati, ad esempio IA5String o PrintableString.

Le estensioni con i tipi di dati **DATE**, **LONG** e **BSTR** non richiedono un gestore di estensione. Il modulo dei criteri chiama [**semplicemente ICertServerPolicy::SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) con il parametro *Type* impostato su un valore che rappresenta il tipo di dati dell'estensione: PROPTYPE \_ DATE, PROPTYPE LONG o \_ PROPTYPE \_ STRING. Passa quindi l'estensione al motore del server. Il motore del server, a sua volta, esegue la codifica ASN.1 [*(Abstract Syntax Notation One)*](../secgloss/a-gly.md) prima di archiviare l'estensione nel certificato.

Tuttavia, le estensioni con tipi di dati diversi da questi tipi predefiniti devono essere codificate come ASN.1 da un gestore di estensioni prima che il modulo criteri li passi al motore del server. Quando il modulo dei criteri chiama [**ICertServerPolicy::SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) per passare un'estensione con codifica ASN.1 al motore del server, deve impostare il parametro *Type* su PROPTYPE \_ BINARY. Il motore del server archivia quindi semplicemente questa estensione codificata nel certificato.

Il gestore di estensioni predefinito, Certenc.dll, esporta una serie di **interfacce ICertEncodeXXX** e può essere chiamato dal modulo dei criteri. Le informazioni sul tipo necessarie sono contenute anche in Certencl.dll forniti in Platform Software Development Kit (SDK). Ogni interfaccia fornisce un **metodo Encode** che restituisce un'estensione del certificato con codifica ASN.1 al modulo dei criteri in formato binario. Il modulo dei criteri può quindi impostare l'estensione in un certificato chiamando il [**metodo ICertServerPolicy::SetCertificateExtension.**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension)

Per altre informazioni, vedere [Scrittura di gestori di estensioni personalizzati.](writing-custom-extension-handlers.md)

 

 
