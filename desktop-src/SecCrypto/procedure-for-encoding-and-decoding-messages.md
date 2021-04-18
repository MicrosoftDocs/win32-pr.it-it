---
description: Descrive la procedura per la codifica di un messaggio generale.
ms.assetid: 554cab0d-cfa2-46a7-80d9-f41430eb4b47
title: Procedura per la codifica e la decodifica dei messaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49da09c2318fffd3d1c92d6012055172709609a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310750"
---
# <a name="procedure-for-encoding-and-decoding-messages"></a>Procedura per la codifica e la decodifica dei messaggi

La procedura per la codifica di un messaggio generale è la seguente:

**Per codificare un messaggio**

1.  Inizializzare le strutture di dati appropriate per il tipo di dati desiderato.
2.  Chiamare [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode), passando gli argomenti necessari. Quando si chiama **CryptMsgOpenToEncode**, se i dati da fornire a [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) sono già stati codificati come messaggi, passare l'identificatore di oggetto appropriato in *pszInnerContentObjID* (ad esempio, "1.2.840.113549.1.7.2" per szOID \_ RSA \_ SignedData). Se *pszInnerContentObjID* è **null**, si presuppone che il tipo di [*contenuto interno*](../secgloss/i-gly.md) non sia stato codificato in precedenza e venga elaborato in modo appropriato.
3.  Chiamare [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) il numero di volte necessario per completare il messaggio. Nell'ultima chiamata, impostare il parametro *fFinal* su **true**. Per informazioni dettagliate, vedere **CryptMsgUpdate**.
4.  Chiamare [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) per ottenere un puntatore ai parametri desiderati, ad esempio il contenuto. Per la codifica di dati generali semplici, usare \_ \_ il parametro di contenuto CMSG per *dwParamtype*.
5.  Chiudere il messaggio chiamando [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose).

Questa procedura restituisce un messaggio codificato di un tipo specificato nelle chiamate di funzione.

Di seguito è riportata la procedura per la decodifica di un messaggio generale.

**Per decodificare un messaggio**

1.  Determinare la lunghezza necessaria per il buffer per memorizzare i dati codificati utilizzando [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength).
2.  Chiamare [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), passando gli argomenti necessari. Per mantenere la compatibilità con Internet Explorer versione 3,0, viene fornito il parametro *dwMsgType* . I dati firmati creati in Internet Explorer 3,0 non contengono informazioni di intestazione. Pertanto, se un messaggio di questo tipo viene estratto dalle firme del file, il tipo di messaggio deve essere passato nella funzione. Se viene passato zero al parametro *dwMsgType* , la funzione leggerà il tipo di messaggio dall'intestazione del messaggio. Se l'intestazione non è presente, la chiamata di funzione avrà esito negativo. In caso di esito positivo, viene restituito un handle per il messaggio aperto.
3.  Chiamare [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) una volta. In questo modo vengono eseguite le azioni appropriate per il messaggio, a seconda del tipo di messaggio.
4.  Per un'ulteriore elaborazione del messaggio, ad esempio la decrittografia aggiuntiva o la verifica della firma, chiamare [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), passando l'azione desiderata in *dwCtrlType*.
5.  Chiamare [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) per ottenere un puntatore ai parametri desiderati, ad esempio il contenuto. Per decodificare i dati generali semplici, \_ usare \_ il parametro CMSG Content per il parametro *dwParamtype* .
6.  Chiamare [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) per chiudere il messaggio.

Per un esempio in cui vengono implementati questi passaggi, vedere il [programma C di esempio: codifica e decodifica dei dati](example-c-program-encoding-and-decoding-data.md). Per le procedure e un esempio che illustra il processo di codifica, decodifica e verifica della firma di un messaggio firmato, vedere il [programma C di esempio: firma, codifica, decodifica e verifica di un messaggio](example-c-program-signing-encoding-decoding-and-verifying-a-message.md).

 

 
