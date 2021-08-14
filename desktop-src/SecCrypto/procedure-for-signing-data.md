---
description: Mostra la relazione tra i parametri della funzione che puntano a strutture o matrici e i relativi dati inizializzati.
ms.assetid: 89caf4d3-727f-472b-9a09-e81b4ff4d127
title: Procedura per la firma dei dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10bae09c97fa42086f853d43b2a5a9dc02f0cbdbe2dd946fefe5d39e28a32104
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117977551"
---
# <a name="procedure-for-signing-data"></a>Procedura per la firma dei dati

Una singola funzione, [**CryptSignMessage,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage)esegue tutte le attività elencate in [Creazione di un messaggio firmato.](creating-a-signed-message.md) Tuttavia, l'inizializzazione di strutture e altri dati è ancora necessaria. Nella figura seguente viene illustrata la relazione tra i parametri della funzione che puntano a strutture o matrici e i relativi dati inizializzati. La figura mostra solo i parametri della funzione e i membri della struttura derivati da altre strutture o funzioni. Gli altri parametri sono inizializzazioni semplici.

![mappa di inizializzazione per una chiamata a cryptsignmessage](images/crypsign.png)

**Per firmare i dati usando CryptSignMessage**

1.  Ottenere un puntatore ai dati da firmare.
2.  Assegnare il puntatore ai dati per indicizzare zero di una matrice "data da firmare".
3.  Ottenere un handle per il provider del servizio di crittografia.
4.  Aprire un [*archivio certificati*](../secgloss/c-gly.md) contenente il certificato del firmatario.
5.  Ottenere un indirizzo per il certificato del firmatario.
6.  Assegnare l'indirizzo del certificato all'indice zero della *matrice MsgCert.*
7.  Assegnare gli indirizzi di qualsiasi altro certificato da includere nel messaggio alla *matrice MsgCert.*
8.  Inizializzare [**la struttura CRYPT ALGORITHM \_ \_ IDENTIFIER**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier) inizializzando il membro **pszObjId** sull'algoritmo hash desiderato e gli altri membri in base alle esigenze.
9.  Inizializzare la struttura [**CRYPT \_ SIGN MESSAGE \_ \_ PARA,**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_sign_message_para) inizializzando il membro **pSigningCert** sull'indirizzo del certificato del firmatario, il membro della matrice **MsgCert** all'indirizzo dei certificati del firmatario e di altri, il membro **HashAlgorithm** all'indirizzo della struttura [**CRYPT ALGORITHM \_ \_ IDENTIFIER**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier) e gli altri membri in base alle esigenze.
10. Chiamare la funzione [**CryptSignMessage,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage) passando la struttura [**CRYPT \_ SIGN MESSAGE \_ \_ PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_sign_message_para) per il parametro *pSignPara,* l'indirizzo della matrice "data da firmare" per il parametro *rgpbToBeSigned,* un indirizzo per il parametro di output *pbSignedBlob* e i valori per gli altri parametri in base alle esigenze.

 

 
