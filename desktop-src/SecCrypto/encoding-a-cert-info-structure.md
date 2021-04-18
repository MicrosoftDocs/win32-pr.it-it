---
description: Il processo di codifica è il contrario del processo di decodifica descritto in decodifica di una struttura di informazioni del certificato \_ .
ms.assetid: 5d3311e5-a2fb-46f7-aa76-f232b39b34fd
title: Codifica di una struttura di CERT_INFO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645a1d3054546a7b11c57d4f515dc7d3e26b5fe0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318940"
---
# <a name="encoding-a-cert_info-structure"></a>Codifica di una \_ struttura di informazioni del certificato

Il processo di codifica è il contrario del processo di decodifica descritto in [decodifica di una \_ struttura di informazioni del certificato](decoding-a-cert-info-structure.md). Ad esempio, la procedura seguente consente di aggiungere un' **autorità emittente** codificata a una struttura di [**\_ informazioni del certificato**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) . Vedere anche l'illustrazione che segue la procedura.

**Per aggiungere un'autorità emittente codificata a una struttura di \_ informazioni sul certificato**

1.  Creare una stringa contenente il nome dell'autorità emittente da utilizzare.
2.  Creare una matrice di [**strutture \_ RDN \_ del certificato**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn_attr) , che verrà inizializzata in modo da contenere le informazioni appropriate sulla stringa del nome dell'autorità emittente appena creata.
3.  Creare una matrice di [**strutture \_ RDN del certificato**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn) , una delle quali contiene le informazioni sulla matrice di [**strutture \_ RDN \_ del certificato**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn_attr) appena inizializzate.
4.  Creare una struttura di [**\_ \_ informazioni sul nome del certificato**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_name_info) che disponga di un puntatore alla matrice di strutture [**\_ RDN CERT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn) appena create.
5.  Chiamare [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) per ottenere la dimensione del BLOB codificato di output e passargli l'indirizzo della struttura di [**\_ \_ informazioni sul nome del certificato**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_name_info) appena creato.
6.  Allocare memoria per il BLOB codificato di output.
7.  Chiamare di nuovo [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) , passandogli le stesse informazioni, ma passando ora l'indirizzo della memoria appena allocata.
8.  Impostare il membro **Issuer. cbData** della struttura [**CERT \_ info**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) sulla dimensione restituita nel passaggio 5 e il membro **Issuer. pbData** per l'indirizzo ottenuto nel passaggio 6. Il BLOB dell' **emittente** codificato si trova ora qui.

![Aggiunta di un'autorità emittente codificata a una struttura di informazioni sul certificato \-](images/encflow.png)

Per inizializzare e codificare alcune informazioni sull'estensione del certificato, attenersi alla procedura riportata di seguito. Vedere anche l'illustrazione che segue la procedura.

**Per aggiungere informazioni sull'estensione codificata a una struttura di informazioni sul certificato \_**

1.  Creare e inizializzare una struttura di informazioni sull'estensione: per questo esempio si tratta di una struttura di [**informazioni sui vincoli di base del certificato \_ \_ \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_basic_constraints_info) .
2.  Chiamare [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject), passandogli l'indirizzo della struttura appena creata, per ottenere la dimensione del BLOB codificato di output.
3.  Allocare memoria per il BLOB codificato di output.
4.  Chiamare di nuovo [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) , passando le stesse informazioni, eccetto ora passare l'indirizzo della memoria allocata.
5.  Creare una matrice di strutture di [**\_ estensione del certificato**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) .
6.  Inizializzare una delle strutture di [**\_ estensione del certificato**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) in modo che **pszObjId** sia la stringa corretta per i dati contenuti nel **valore** e tale **valore** contenga il BLOB di dati crittografato restituito dalla chiamata a [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject).
7.  Inizializzare il membro **rgExtension** della struttura di [**\_ informazioni sul certificato**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) in modo che punti alla matrice di strutture di [**\_ estensione del certificato**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) .

![Aggiunta di informazioni sull'estensione codificata a una \- struttura di informazioni sul certificato](images/xtenflow.png)

 

 



