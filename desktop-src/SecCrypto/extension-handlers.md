---
description: A partire dal formato del certificato X. 509 versione 3, un certificato può contenere estensioni di certificato.
ms.assetid: fb106cab-8a61-4a83-8fb4-7c045d905575
title: Gestori estensioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfcf1b47fcc97b87f5956f4584aee07acce04222
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318234"
---
# <a name="extension-handlers"></a>Gestori estensioni

A partire dal formato del certificato [*X. 509*](../secgloss/x-gly.md) versione 3, un certificato può contenere estensioni di certificato. Per il contenuto di un certificato X. 509, vedere [proprietà del certificato](certificate-properties.md). Queste estensioni indicano informazioni aggiuntive. Un'estensione può, ad esempio, indicare informazioni aggiuntive sull'identificazione del soggetto o indicare le informazioni sull'utilizzo della chiave, che specificano le attività, ad esempio la firma o la crittografia, per le quali è possibile utilizzare una chiave. Un set di estensioni standard viene definito per l'uso dell'applicazione ed è anche possibile personalizzare le estensioni.

A ogni estensione è associata una stringa dell'identificatore di oggetto che identifica il tipo di informazioni aggiuntive e una struttura di dati che contiene queste informazioni. Ad esempio, l'identificatore dell'oggetto utilizzo chiave è "2.5.29.15", che indica le informazioni sull'utilizzo della chiave. La struttura dei dati associata è [**un \_ \_ BLOB di bit Crypt**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_bit_blob) (bit) che specifica come è possibile usare la chiave.

Un'estensione può essere aggiunta a un certificato prima dell'emissione. Quando il certificato viene emesso, le estensioni abilitate fanno parte del certificato. Se un'estensione è contrassegnata come critica, il suo utilizzo deve essere noto all'applicazione using e l'applicazione deve rispettare lo scopo o il valore dell'estensione. Servizi certificati consente di impostare le estensioni per un certificato non emesso tramite i metodi forniti da [**ICertAdmin**](/windows/desktop/api/Certadm/nn-certadm-icertadmin) e [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy). Per informazioni dettagliate sulle estensioni dei certificati, vedere [**\_ estensione CERT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) nella documentazione di CryptoAPI. Per informazioni sulle strutture dei dati di estensione del certificato comuni, vedere [strutture di estensione del certificato X. 509](cryptography-structures.md).

Il gestore dell'estensione è un oggetto COM che fornisce routine per la codifica dei tipi di dati e delle estensioni più complessi, ma usati di frequente, ad esempio IA5String o PrintableString.

Le estensioni con tipi di dati **date**, **Long** e **BSTR** non richiedono un gestore di estensione. Il modulo criteri chiama semplicemente [**ICertServerPolicy:: SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) con il parametro di *tipo* impostato su un valore che rappresenta il tipo di dati dell'estensione: PROPTYPE \_ date, PROPTYPE \_ Long o PROPTYPE \_ String. Passa quindi l'estensione al motore del server. Il motore di server, a sua volta, esegue la codifica ASN. 1 ( [*Abstract Syntax Notation One*](../secgloss/a-gly.md) ) prima di archiviare l'estensione nel certificato.

Tuttavia, le estensioni con tipi di dati diversi da questi tipi predefiniti devono essere ASN. 1 codificate da un gestore di estensione prima che il modulo criteri le passi al motore del server. Quando il modulo criteri chiama [**ICertServerPolicy:: SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) per passare un'estensione con codifica ASN. 1 al motore del server, è necessario impostare il parametro di *tipo* su PROPTYPE \_ Binary. Il motore Server archivia semplicemente questa estensione codificata nel certificato.

Il gestore dell'estensione predefinito, Certenc.dll, esporta un numero di interfacce **ICertEncodeXXX** e può essere chiamato dal modulo criteri. Le informazioni sul tipo necessarie sono contenute anche in Certencl.dll fornito in Platform Software Development Kit (SDK). Ogni interfaccia fornisce un metodo **Encode** che restituisce un'estensione di certificato con codifica ASN. 1 al modulo criteri in formato binario. Il modulo criteri può quindi impostare l'estensione in un certificato chiamando il metodo [**ICertServerPolicy:: SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) .

Per altre informazioni, vedere [scrittura di gestori estensioni personalizzati](writing-custom-extension-handlers.md).

 

 
