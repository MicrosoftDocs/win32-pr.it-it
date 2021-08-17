---
description: Quando si usano più monitor come schermi indipendenti, il desktop contiene un solo schermo o un set di schermi.
ms.assetid: fbc88c91-3209-4b59-bdbb-0f5ba009a312
title: Uso di più monitor come schermi indipendenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710672e02e8ea7244e09c21b876197033e5f17144433b8f530ad8e52cd6806e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119468251"
---
# <a name="using-multiple-monitors-as-independent-displays"></a>Uso di più monitor come schermi indipendenti

Quando si usano più monitor come schermi indipendenti, il desktop contiene un solo schermo o un set di schermi. Questo set di schermi include sempre il monitoraggio principale e si comporta come indicato nelle altre sezioni di questo argomento. Un'applicazione può usare qualsiasi altro monitoraggio come visualizzazione indipendente.

> [!Note]  
> L'uso di altri monitor come schermi indipendenti non è supportato nei driver implementati nel modello WDDM (Windows Display Driver Model).

 

Il gestore finestre non sa nulla sugli schermi indipendenti. Sono completamente controllati dall'applicazione e non sono disponibili funzioni di gestione finestre per l'applicazione (tutte le chiamate di gestione finestre passano automaticamente alla visualizzazione primaria). Ogni visualizzazione indipendente ha la propria origine e coordinate orizzontali e verticali ed è accessibile tramite le funzioni GDI, ad esempio [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) o le funzioni DirectX, ad esempio **DirectDrawCreate**.

Per individuare gli schermi indipendenti, chiamare [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) e cercare gli schermi che non hanno il flag DISPLAY \_ DEVICE \_ ATTACHED \_ TO DESKTOP nella struttura DISPLAY \_ [**\_ DEVICE.**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea)

Un'applicazione può aprire una visualizzazione chiamando


```C++
hdc = CreateDC(lpszDisplayName, NULL, NULL, lpDevMode);
```



In questa chiamata, il *parametro lpszDisplayName* è uno dei nomi di dispositivo restituiti da [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) e *lpDevMode* è una descrizione della modalità grafica per questo dispositivo. L'hdc risultante può essere usato per eseguire qualsiasi operazione grafica sul dispositivo.

 

 



