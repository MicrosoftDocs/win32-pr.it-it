---
description: Costante numerica che specifica il numero massimo di caratteri che alcuni provider di crittografia Microsoft utilizzeranno per ottenere l'ID utente.
ms.assetid: cc15a166-9a0c-41ce-9cb1-ecdc922565c0
title: MAXUIDLEN (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 199d8e697deba86ffe48d4f76501f2d9d3a6d4e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307691"
---
# <a name="maxuidlen"></a>MAXUIDLEN

MAXUIDLEN è una costante numerica che specifica il numero massimo di caratteri che alcuni provider di crittografia Microsoft utilizzeranno per ottenere l'ID utente. MAXUIDLEN è definito in WinCrypt. h.



| Costante/valore                                                                                                                                                                                                  | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MAXUIDLEN"></span><span id="maxuidlen"></span><dl> <dt>**MAXUIDLEN**</dt> <dt>64 (0x40)</dt> </dl> | Quando il parametro *pszContainer* della funzione [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) è **null**, alcuni provider di servizi di crittografia Microsoft usano il nome di accesso dell'utente attualmente connesso come nome del contenitore di chiavi. MAXUIDLEN specifica il numero massimo di caratteri, incluso il carattere **null** di terminazione, che questi provider utilizzeranno per il nome utente.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Wincrypt. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta)
</dt> <dt>

[**CPAcquireContext**](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> </dl>

 

 




