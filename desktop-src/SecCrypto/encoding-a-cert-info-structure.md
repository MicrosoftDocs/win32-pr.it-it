---
description: Il processo di codifica è il contrario del processo di decodifica descritto in Decodifica di una struttura CERT \_ INFO.
ms.assetid: 5d3311e5-a2fb-46f7-aa76-f232b39b34fd
title: Codifica di una CERT_INFO struttura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b469ae0bdf02ffd8f30f8b0c2dd44051239a5702ff32704d58de8b60f1ca9701
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766788"
---
# <a name="encoding-a-cert_info-structure"></a>Codifica di una struttura CERT \_ INFO

Il processo di codifica è il contrario del processo di decodifica descritto in [Decodifica di una struttura CERT \_ INFO](decoding-a-cert-info-structure.md). Ad esempio, la procedura seguente aggiunge **un'autorità** di certificazione codificata a una [**struttura CERT \_ INFO.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) Vedere anche l'illustrazione che segue la procedura.

**Per aggiungere un'autorità di certificazione codificata a una struttura CERT \_ INFO**

1.  Creare una stringa contenente il nome dell'autorità di emittente da usare.
2.  Creare una matrice di [**strutture \_ CERT RDN \_ ATTR,**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn_attr) che verranno inizializzate in modo da contenere le informazioni appropriate sulla stringa del nome dell'autorità di certificazione appena creata.
3.  Creare una matrice di [**strutture \_ RDN CERT,**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn) una delle quali contiene le informazioni sulla matrice di [**strutture \_ CERT RDN \_ ATTR**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn_attr) appena inizializzate.
4.  Creare una [**struttura CERT \_ NAME \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_name_info) con un puntatore alla matrice di [**strutture \_ RDN CERT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn) appena create.
5.  Chiamare [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) per ottenere le dimensioni del BLOB con codifica di output, passando l'indirizzo della struttura [**CERT \_ NAME \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_name_info) appena creata.
6.  Allocare memoria per il BLOB con codifica di output.
7.  Chiamare [**di nuovo CryptEncodeObject,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) passando le stesse informazioni, ma ora passando l'indirizzo della memoria appena allocata.
8.  Impostare il membro **Issuer.cbData** della struttura [**CERT \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) sulle dimensioni restituite nel passaggio 5 e il membro **Issuer.pbData** sull'indirizzo ottenuto nel passaggio 6. Il BLOB **dell'autorità di emittente** codificato si trova ora in questa cartella.

![aggiunta di un'autorità di certificazione codificata a una struttura di \- informazioni sul certificato](images/encflow.png)

Per inizializzare e codificare alcune informazioni sull'estensione del certificato, usare la procedura seguente. Vedere anche l'illustrazione che segue la procedura.

**Per aggiungere informazioni sull'estensione codificata a una struttura CERT \_ INFO**

1.  Creare e inizializzare una struttura di informazioni sull'estensione. Per questo esempio si tratta di una [**struttura CERT \_ BASIC CONSTRAINTS \_ \_ INFO.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_basic_constraints_info)
2.  Chiamare [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject), passando l'indirizzo della struttura appena creata, per ottenere le dimensioni del BLOB codificato in output.
3.  Allocare memoria per il BLOB con codifica di output.
4.  Chiamare [**di nuovo CryptEncodeObject,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) passando le stesse informazioni, ad eccezione del passaggio dell'indirizzo della memoria allocata.
5.  Creare una matrice di [**strutture CERT \_ EXTENSION.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension)
6.  Inizializzare una delle strutture [**CERT \_ EXTENSION**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) in modo che **pszObjId** sia la stringa appropriata per i dati contenuti in **Value** e **che Value** contenga il BLOB di dati crittografati restituito dalla chiamata a [**CryptEncodeObject.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)
7.  Inizializzare **il membro rgExtension** della struttura [**CERT \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) in modo che punti alla matrice di [**strutture CERT \_ EXTENSION.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension)

![aggiunta di informazioni sull'estensione codificata a una struttura di \- informazioni sul certificato](images/xtenflow.png)

 

 



