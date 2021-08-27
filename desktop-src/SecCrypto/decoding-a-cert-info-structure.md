---
description: Dato un certificato, il primo passaggio per decodificare il BLOB del certificato consiste nel chiamare CertCreateCertificateContext, passando un puntatore al certificato codificato (BLOB).
ms.assetid: b50530e2-15a0-4215-bf18-300cf67d1611
title: Decodifica di una CERT_INFO struttura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8eab5a75c2a5906ac875f925845f83f3c411c12a31aeea4825efd795b78eaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100883"
---
# <a name="decoding-a-cert_info-structure"></a>Decodifica di una struttura CERT \_ INFO

Dato un certificato, il primo passaggio per decodificare il [*BLOB*](../secgloss/b-gly.md) del certificato consiste nel chiamare [**CertCreateCertificateContext,**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecertificatecontext)passando un puntatore al certificato codificato (*BLOB*). Quando questa funzione viene chiamata, crea un duplicato del certificato codificato, crea una struttura di tipo [**CERT \_ CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)e crea una struttura di tipo [**CERT \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info). Come illustrato nella figura [](../secgloss/c-gly.md) seguente, un contesto del certificato include il *BLOB* del certificato originale, una struttura C di tipo **CERT \_ CONTEXT** e una struttura C di tipo **CERT \_ INFO.** Uno dei membri della struttura **CERT \_ CONTEXT** punta alla struttura **CERT \_ INFO** e un altro al BLOB del certificato codificato.

![contesto del certificato](images/certcntx.png)

L'oggetto codificato (membro dati) viene sempre fornito come input per la funzione [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) e l'output è una struttura C che può o meno avere membri codificati, a seconda della distanza nel processo.

Esiste un altro membro che richiede una decodifica, che è il **membro extension.** Anche se non è codificato a livello [**di CERT \_ INFO,**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) contiene alcune informazioni codificate. Per decodificare queste informazioni, procedere come illustrato nella figura seguente.

![decodifica di informazioni](images/xtension.png)

Nella struttura [**CERT \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) il membro **rgExtension** è un puntatore a una matrice di [**strutture CERT \_ EXTENSION.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) Ogni **struttura CERT \_ EXTENSION** ha un **membro Value** in formato codificato e deve essere decodificato. Il **membro Value** viene passato alla funzione [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) e quindi l'output della funzione dipende dal valore del membro **pszObjId.** Si noti che nella figura vengono prodotte due strutture diverse, una di tipo [**CERT \_ BASIC CONSTRAINTS \_ \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_basic_constraints_info) e una di tipo [**CERT AUTHORITY KEY ID \_ \_ \_ \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_authority_key_id_info), a seconda del valore di **pszObjId**.

 

 
