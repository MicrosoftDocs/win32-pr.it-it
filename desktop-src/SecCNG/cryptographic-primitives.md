---
description: L'API CNG fornisce un set di funzioni che eseguono operazioni crittografiche di base, ad esempio la creazione di hash o la crittografia e la decrittografia dei dati. Per altre informazioni su queste funzioni, vedere Funzioni primitive crittografiche CNG.
ms.assetid: 925848ae-9f4f-444a-81ff-14a1997434b2
title: Primitive di crittografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d65b37193ccf2f37a06dea0a994c40ea472c6041b451a1d2c31dd19b259b843
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907805"
---
# <a name="cryptographic-primitives"></a>Primitive di crittografia

L'API CNG fornisce un set di funzioni che eseguono operazioni crittografiche di base, ad esempio la creazione di hash o la crittografia e la decrittografia dei dati. Per altre informazioni su queste funzioni, vedere [Funzioni primitive crittografiche CNG.](cng-cryptographic-primitive-functions.md)

CNG implementa numerosi algoritmi di crittografia. Ogni algoritmo o classe di algoritmi espone la propria API primitiva. È possibile installare contemporaneamente più implementazioni di un determinato algoritmo. Tuttavia, solo un'implementazione sarà l'impostazione predefinita in un determinato momento.

Ogni classe di algoritmo in CNG è rappresentata da un router primitivo. Le applicazioni che usano le funzioni primitive CNG verranno collegate al file binario del router Bcrypt.dll in modalità utente o Ksecdd.sys in modalità kernel prima di chiamare le funzioni. Varie routine del router gestiscono tutte le primitive dell'algoritmo. Questi router tiene traccia di ogni implementazione dell'algoritmo installata nel sistema e instradare ogni chiamata di funzione al modulo del provider primitivo appropriato.

CNG fornisce primitive per le classi di algoritmi seguenti.



| Classe algorithm                                                                                                                                                  | Descrizione                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span id="Random_number_generator"></span><span id="random_number_generator"></span><span id="RANDOM_NUMBER_GENERATOR"></span>Generatore di numeri casuali<br/> | Generazione di numeri casuali collegabili (RNG).<br/>                                                         |
| <span id="Hashing"></span><span id="hashing"></span><span id="HASHING"></span>Hash<br/>                                                                 | Algoritmi usati per l'hashing, ad esempio SHA1 e SHA2.<br/>                                               |
| <span id="Symmetric_encryption"></span><span id="symmetric_encryption"></span><span id="SYMMETRIC_ENCRYPTION"></span>Crittografia simmetrica<br/>             | Algoritmi utilizzati per la crittografia simmetrica, ad esempio AES, 3DES e RC4.<br/>                             |
| <span id="Asymmetric_encryption"></span><span id="asymmetric_encryption"></span><span id="ASYMMETRIC_ENCRYPTION"></span>Crittografia asimmetrica<br/>         | Algoritmi asimmetrici (chiave pubblica) che supportano la crittografia, ad esempio RSA.<br/>                          |
| <span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Firma<br/>                                                         | Algoritmi di firma come DSA e ECDSA. Questa classe può essere usata anche con RSA.<br/>                 |
| <span id="Secret_agreement"></span><span id="secret_agreement"></span><span id="SECRET_AGREEMENT"></span>Contratto segreto<br/>                             | Algoritmi di accordo segreto, ad esempio Diffie-Hellman (DH) e ECDH (elliptic curve Diffie-Hellman).<br/> |



 

La figura seguente illustra la progettazione e la funzione delle primitive di crittografia CNG.

![progettazione e funzione delle primitive crittografiche cng](images/ssdk-cng1c.png)

Il file di intestazione Bcrypt.h definisce la costante **MS \_ PRIMITIVE \_ PROVIDER** come "Microsoft Primitive Provider". Per usare il provider primitivo Microsoft, passare questo valore a [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider).

 

 




