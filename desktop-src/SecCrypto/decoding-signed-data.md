---
description: Processo per decodificare i dati firmati.
ms.assetid: 803220d0-7963-4fc4-8451-a979e54a9cc3
title: Decodifica dei dati firmati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdfd327746c5d0ba8e7089e1c273817b76c16370
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306443"
---
# <a name="decoding-signed-data"></a>Decodifica dei dati firmati

Il processo generale seguente decodifica un tipo di [*dati con segno*](../secgloss/s-gly.md) .

**Per decodificare un messaggio firmato**

1.  Ottenere un puntatore al BLOB codificato.
2.  Chiamare [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), passando gli argomenti necessari.
3.  Chiamare [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) una volta, passando l'handle recuperato nel passaggio 2 e un puntatore ai dati che devono essere decodificati. In questo modo vengono eseguite le azioni appropriate per il messaggio, a seconda del tipo di messaggio.
4.  Chiamare [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passando l'handle recuperato nel passaggio 2 e i tipi di parametro appropriati per accedere ai dati decodificati. Ad esempio, passare CMSG \_ Content \_ param per ottenere un puntatore al contenuto decodificato.

Nel processo generale seguente viene verificata la firma di un messaggio firmato decodificato.

**Per verificare la firma di un messaggio firmato decodificato**

1.  Chiamare [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passando le informazioni sul certificato del firmatario e sull'handle del messaggio CMSG \_ \_ \_ \_ per ottenere le [**\_ informazioni sul certificato**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) del firmatario dal messaggio.
2.  Chiamare [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) per aprire un archivio temporaneo inizializzato con i certificati del messaggio.
3.  Chiamare [**CertGetSubjectCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore) per ottenere le [**\_ informazioni sul certificato**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) del firmatario dai certificati inclusi nel messaggio.
4.  Chiamare [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), passando il CMSG \_ CTRL \_ Verify \_ Signature per verificare le firme.
5.  Chiamare [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) per chiudere il messaggio.

Il risultato di queste procedure è che la firma viene verificata e un puntatore viene recuperato al contenuto del messaggio decodificato ottenuto nel passaggio 4 della procedura per la decodifica di un messaggio firmato.

Per informazioni sul codice C, vedere [esempio di programma c: firma, codifica, decodifica e verifica di un messaggio](example-c-program-signing-encoding-decoding-and-verifying-a-message.md).

 

 
