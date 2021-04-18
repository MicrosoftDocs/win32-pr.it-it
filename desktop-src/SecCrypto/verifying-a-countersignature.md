---
description: Viene illustrato come verificare un controfirma usando CryptMsgVerifyCountersignatureEncoded.
ms.assetid: b7be0d4c-338f-4319-bd82-5cf3d158d6fe
title: Verifica di un controfirma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711e15388144fbf674cbb0c42ff41883edbb5af0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308625"
---
# <a name="verifying-a-countersignature"></a>Verifica di un controfirma

**Per verificare un controfirma**

1.  Chiamare [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) per ottenere un handle per il messaggio firmato.
2.  Ottenere un puntatore al certificato di countersigner ( [**\_ informazioni**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info)sul certificato).
3.  Chiamare [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) per recuperare le informazioni sul firmatario dal messaggio.
4.  Chiamare [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) per recuperare [*controfirma*](../secgloss/c-gly.md) dal messaggio.
5.  Chiamare [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) per verificare il controfirma.

Se la chiamata alla funzione [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) ha esito positivo, viene verificata la [*controfirma*](../secgloss/c-gly.md) .

 

 
