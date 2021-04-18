---
description: Mostra la relazione tra i parametri di funzione che puntano a strutture o matrici e i relativi dati inizializzati.
ms.assetid: 89caf4d3-727f-472b-9a09-e81b4ff4d127
title: Procedura per la firma dei dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba289928ab39c690e1c44bdbf65c77c18b7edab3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312797"
---
# <a name="procedure-for-signing-data"></a>Procedura per la firma dei dati

Una singola funzione, [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage), esegue tutte le attività elencate in [creazione di un messaggio firmato](creating-a-signed-message.md). Tuttavia, l'inizializzazione di strutture e altri dati è ancora necessaria. Nella figura seguente viene illustrata la relazione tra i parametri di funzione che puntano a strutture o matrici e i relativi dati inizializzati. Nell'illustrazione vengono mostrati solo i parametri di funzione e i membri della struttura derivati da altre strutture o funzioni. Gli altri parametri sono semplici inizializzazioni.

![Mappa di inizializzazione per una chiamata a CryptSignMessage](images/crypsign.png)

**Per firmare i dati tramite CryptSignMessage**

1.  Ottenere un puntatore ai dati che devono essere firmati.
2.  Assegnare il puntatore ai dati per indicizzare zero di una matrice "data da firmare".
3.  Ottenere un handle per il provider del crittografico.
4.  Aprire un [*archivio certificati*](../secgloss/c-gly.md) che contiene il certificato del firmatario.
5.  Ottenere un indirizzo per il certificato del firmatario.
6.  Assegnare l'indirizzo del certificato all'indice zero della matrice *MsgCert* .
7.  Assegnare gli indirizzi di tutti gli altri certificati da includere nel messaggio alla matrice *MsgCert* .
8.  Inizializzare la struttura dell' [**\_ \_ identificatore dell'algoritmo di crittografia**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier) , inizializzando il membro **pszObjId** nell'algoritmo hash desiderato e gli altri membri in base alle esigenze.
9.  Inizializzare la struttura del messaggio di firma della crittografia, inizializzando il membro **pSigningCert** nell'indirizzo del certificato del firmatario, il membro della matrice **MsgCert** all'indirizzo del firmatario e altri certificati, il membro **HashAlgorithm** all'indirizzo della struttura dell' [**identificatore dell' \_ algoritmo \_ crypt**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier) e gli altri membri in base alle esigenze. [**\_ \_ \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_sign_message_para)
10. Chiamare la funzione [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage) , passando la struttura del [**\_ \_ messaggio \_ di firma del Crypt**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_sign_message_para) per il parametro *pSignPara* , l'indirizzo della matrice "data da firmare" per il parametro *rgpbToBeSigned* , un indirizzo per il parametro di output *pbSignedBlob* e i valori per gli altri parametri nel modo appropriato.

 

 
