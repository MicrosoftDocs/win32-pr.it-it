---
title: Utilizzo della finestra di dialogo connessioni
description: La funzione WNetConnectionDialog crea una finestra di dialogo che consente all'utente di esplorare e connettersi alle risorse di rete.
ms.assetid: ef375004-e426-4dee-b318-b470721116fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f69d0f32772e614d60598853af620ae3c6452f5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338206"
---
# <a name="using-the-connections-dialog-box"></a>Utilizzo della finestra di dialogo connessioni

La funzione [**WNetConnectionDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog) crea una finestra di dialogo che consente all'utente di esplorare e connettersi alle risorse di rete. È inoltre possibile chiamare la funzione [**WNetConnectionDialog1**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog1a) per creare una finestra di dialogo connessioni. **WNetConnectionDialog1** richiede una struttura [**CONNECTDLGSTRUCT**](/windows/win32/api/winnetwk/ns-winnetwk-connectdlgstructa) .

La funzione [**WNetDisconnectDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetdisconnectdialog) crea una finestra di dialogo che consente all'utente di disconnettersi dalle risorse di rete.

Nell'esempio di codice seguente viene illustrato come chiamare la funzione **WNetConnectionDialog** per creare una finestra di dialogo in cui vengono visualizzate le risorse disco. Se la chiamata ha esito negativo, l'esempio chiama un gestore degli errori definito dall'applicazione.


```C++
DWORD dwResult; 
//
// Call the WNetConnectionDialog function.
//
dwResult = WNetConnectionDialog(hwnd, RESOURCETYPE_DISK);
//
// Call an application-defined error handler 
//  to process errors.
//
if(dwResult != NO_ERROR) 
{
    NetErrorHandler(hwnd, dwResult, (LPSTR)"WNetConnectionDialog"); 
    return FALSE; 
}
```



Per ulteriori informazioni sull'utilizzo di un gestore degli errori definito dall'applicazione, vedere [recupero degli errori di rete](retrieving-network-errors.md).

 

 