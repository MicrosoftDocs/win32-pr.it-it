---
description: L'API CNG fornisce un set di funzioni che eseguono operazioni di crittografia di base, ad esempio la creazione di hash o la crittografia e la decrittografia di dati. Per altre informazioni su queste funzioni, vedere funzioni primitive di crittografia CNG.
ms.assetid: 925848ae-9f4f-444a-81ff-14a1997434b2
title: Primitive di crittografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0f390b36bc500bf80b5b2ef0065651cf99f5e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524865"
---
# <a name="cryptographic-primitives"></a>Primitive di crittografia

L'API CNG fornisce un set di funzioni che eseguono operazioni di crittografia di base, ad esempio la creazione di hash o la crittografia e la decrittografia di dati. Per altre informazioni su queste funzioni, vedere [funzioni primitive di crittografia CNG](cng-cryptographic-primitive-functions.md).

CNG implementa numerosi algoritmi di crittografia. Ogni algoritmo o classe di algoritmi espone una propria API primitiva. È possibile installare contemporaneamente più implementazioni di un determinato algoritmo; Tuttavia, solo un'implementazione sarà quella predefinita in un determinato momento.

Ogni classe Algorithm in CNG è rappresentata da un router primitivo. Le applicazioni che usano le funzioni primitive CNG si collegano al file binario del router Bcrypt.dll in modalità utente o Ksecdd.sys in modalità kernel prima di chiamare le funzioni. Diverse routine del router gestiscono tutte le primitive dell'algoritmo. Questi router tengono traccia di ogni implementazione dell'algoritmo installata nel sistema e indirizzano ogni chiamata di funzione al modulo del provider primitivo appropriato.

CNG fornisce primitive per le classi di algoritmi seguenti.



| Classe Algorithm                                                                                                                                                  | Descrizione                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span id="Random_number_generator"></span><span id="random_number_generator"></span><span id="RANDOM_NUMBER_GENERATOR"></span>Generatore di numeri casuali<br/> | Generazione di numeri casuali innestabili (RNG).<br/>                                                         |
| <span id="Hashing"></span><span id="hashing"></span><span id="HASHING"></span>Hash<br/>                                                                 | Algoritmi utilizzati per l'hashing, ad esempio SHA1 e SHA2.<br/>                                               |
| <span id="Symmetric_encryption"></span><span id="symmetric_encryption"></span><span id="SYMMETRIC_ENCRYPTION"></span>Crittografia simmetrica<br/>             | Algoritmi utilizzati per la crittografia simmetrica, ad esempio AES, 3DES e RC4.<br/>                             |
| <span id="Asymmetric_encryption"></span><span id="asymmetric_encryption"></span><span id="ASYMMETRIC_ENCRYPTION"></span>Crittografia asimmetrica<br/>         | Algoritmi asimmetrici (chiave pubblica) che supportano la crittografia, ad esempio RSA.<br/>                          |
| <span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Firma<br/>                                                         | Algoritmi di firma, ad esempio DSA e ECDSA. Questa classe può essere usata anche con RSA.<br/>                 |
| <span id="Secret_agreement"></span><span id="secret_agreement"></span><span id="SECRET_AGREEMENT"></span>Contratto segreto<br/>                             | Algoritmi di accordo segreto, ad esempio Diffie-Hellman (DH) e curva ellittica Diffie-Hellman (ECDH).<br/> |



 

Nella figura seguente viene illustrata la progettazione e la funzione delle primitive di crittografia CNG.

![progettazione e funzione delle primitive di crittografia CNG](images/ssdk-cng1c.png)

Il file di intestazione bcrypt. h definisce la costante del **\_ \_ provider MS primitiva** come "Microsoft primitive provider". Per usare il provider primitivo Microsoft, passare questo valore a [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider).

 

 




