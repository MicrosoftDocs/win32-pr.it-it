---
title: Recupero del nome utente
description: Per recuperare il nome dell'utente associato a un dispositivo locale connesso a una risorsa di rete o al nome di una rete, un'applicazione può chiamare la funzione WNetGetUser.
ms.assetid: aed410af-d5f0-4389-882b-5b4338b5f900
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98aeafc849e1a66b373fcb81af46ec47b49644c4b9c753fad480876180a5592a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118566479"
---
# <a name="retrieving-the-user-name"></a>Recupero del nome utente

Per recuperare il nome dell'utente associato a un dispositivo locale connesso a una risorsa di rete o al nome di una rete, un'applicazione può chiamare la [**funzione WNetGetUser.**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera)

Nell'esempio seguente viene utilizzato il nome del dispositivo per recuperare il nome dell'utente. Nell'esempio viene chiamato un gestore degli errori definito dall'applicazione per elaborare gli errori e la [**funzione TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) per la stampa.


```C++
CHAR szUserName[80]; 
DWORD dwResult, cchBuff = 80; 
 
// Call the WNetGetUser function.
//
dwResult = WNetGetUser("z:", 
    (LPSTR) szUserName, 
    &cchBuff); 
 
// If the call succeeds, print the user name.
//
if(dwResult == NO_ERROR) 
    printf("User name: %s\n", szUserName); 
 
// Handle the error.
//
else 
{ 
    printf("WNetGetUser failed.\n"); 
}
```



Per altre informazioni sull'uso di un gestore degli errori definito dall'applicazione, vedere [Recupero di errori di rete.](retrieving-network-errors.md)

 

 