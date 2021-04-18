---
description: Dato un certificato, il primo passaggio nella decodifica del BLOB del certificato consiste nel chiamare CertCreateCertificateContext, passandogli un puntatore al certificato codificato (BLOB).
ms.assetid: b50530e2-15a0-4215-bf18-300cf67d1611
title: Decodifica di una struttura di CERT_INFO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7178c9a5bcfc95a8e2945a6e381f0c2c29cf3b4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104552558"
---
# <a name="decoding-a-cert_info-structure"></a>Decodifica di una \_ struttura di informazioni CERT

Dato un certificato, il primo passaggio nella decodifica del [*BLOB*](../secgloss/b-gly.md) del certificato consiste nel chiamare [**CertCreateCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecertificatecontext), passandogli un puntatore al certificato codificato (*BLOB*). Quando questa funzione viene chiamata, viene creato un duplicato del certificato codificato, viene creata una struttura di tipo [**CERT \_ context**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)e viene creata una struttura di tipo [**CERT \_ info**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info). Come illustrato nella figura seguente, un [*contesto del certificato*](../secgloss/c-gly.md) include il *BLOB* del certificato originale, una struttura c di tipo **CERT \_ context** e una struttura c di tipo **CERT \_ info**. Uno dei membri della struttura del **\_ contesto** del certificato punta alla struttura **delle \_ informazioni** del certificato e un altro al BLOB del certificato codificato.

![contesto del certificato](images/certcntx.png)

L'oggetto codificato (membro dati) viene sempre fornito come input per la funzione [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) e l'output è una struttura C che può contenere o meno membri codificati, a seconda della distanza nel processo.

È presente un altro membro che richiede una decodifica e che è il membro di **estensione** . Sebbene non sia codificato a livello di [**\_ informazioni del certificato**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) , contiene alcune informazioni codificate. Per decodificare queste informazioni, procedere come illustrato nella figura seguente.

![decodifica di informazioni](images/xtension.png)

Nella struttura [**delle \_ informazioni del certificato**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) , il membro **rgExtension** è un puntatore a una matrice di strutture di [**\_ estensione CERT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) . Ogni struttura di **\_ estensione del certificato** ha un membro del **valore** in formato codificato e deve essere decodificato. Il membro **value** viene passato alla funzione [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) e quindi l'output della funzione dipende dal valore del membro **pszObjId** . Si noti che nell'illustrazione vengono generate due strutture diverse, una di tipo [**CERT \_ Basic \_ Constraints \_ info**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_basic_constraints_info) e una di tipo [**CERT \_ Authority \_ Key \_ ID \_ info**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_authority_key_id_info), a seconda del valore di **pszObjId**.

 

 
