---
description: Viene illustrato come controfirmare un messaggio utilizzando CryptMsgCountersign.
ms.assetid: e1969b43-f50e-4c7d-a7e5-b22db4e05be2
title: Controfirma un messaggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02091d25e7ee22f986a26b8f07abff68ebb8c11c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314138"
---
# <a name="countersigning-a-message"></a>Controfirma un messaggio

**Per controfirmare un messaggio firmato tramite CryptMsgCountersign**

1.  Chiamare [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) per ottenere un handle per il messaggio firmato.
2.  Inizializzare una struttura di [**\_ informazioni di \_ codifica \_ del firmatario CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) per countersigner.
3.  Aggiungere la struttura delle [**\_ informazioni di \_ codifica \_ del firmatario CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) a una matrice di countersigners (attualmente è supportato un solo countersigner).
4.  Chiamare [**CryptMsgCountersign**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersign) per aggiungere controfirma o controfirme.

Se tutte le chiamate di funzione hanno esito positivo, il messaggio originale dispone ora di un [*controfirma*](../secgloss/c-gly.md) incluso come attributo non autenticato.

**Per controfirmare un messaggio firmato tramite CryptMsgCountersignEncoded**

1.  Chiamare [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) per ottenere un handle per il messaggio firmato.
2.  Chiamare [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) per recuperare le informazioni sul firmatario codificato del messaggio firmato.
3.  Inizializzare una struttura di [**\_ informazioni di \_ codifica \_ del firmatario CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) per countersigner.
4.  Aggiungere la struttura delle [**\_ informazioni di \_ codifica \_ del firmatario CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) a una matrice di countersigners (attualmente è supportato un solo countersigner).
5.  Chiamare [**CryptMsgCountersignEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersignencoded) per creare l'attributo controfirma codificato.
6.  Chiamare [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol) per aggiungere l'attributo controfirma al messaggio originale come attributo non autenticato.

Se tutte le chiamate di funzione hanno esito positivo, al messaggio originale viene aggiunto un attributo [*controfirma*](../secgloss/c-gly.md) .

 

 
