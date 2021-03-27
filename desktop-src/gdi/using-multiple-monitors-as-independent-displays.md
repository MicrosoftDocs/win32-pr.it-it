---
description: Quando si usano più monitor come visualizzazioni indipendenti, il desktop contiene una visualizzazione o un set di visualizzazioni.
ms.assetid: fbc88c91-3209-4b59-bdbb-0f5ba009a312
title: Uso di più monitor come visualizzazioni indipendenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4761e0e04ae1adaa197b06f04fa36c61ccda3083
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980506"
---
# <a name="using-multiple-monitors-as-independent-displays"></a>Uso di più monitor come visualizzazioni indipendenti

Quando si usano più monitor come visualizzazioni indipendenti, il desktop contiene una visualizzazione o un set di visualizzazioni. Questo set di visualizzazioni include sempre il monitoraggio primario e si comporta come indicato nelle altre sezioni di questo argomento. Un'applicazione può utilizzare qualsiasi altro monitor come display indipendente.

> [!Note]  
> L'utilizzo di altri monitoraggi come visualizzazioni indipendenti non è supportato nei driver implementati per Windows Display Driver Model (WDDM).

 

Windows Manager non è in grado di riconoscere le visualizzazioni indipendenti. Sono completamente controllati dall'applicazione e non sono disponibili funzioni di gestione finestre per l'applicazione. tutte le chiamate di Window Manager passano automaticamente alla visualizzazione principale. Ogni visualizzazione indipendente ha una propria origine e coordinate orizzontali e verticali ed è accessibile tramite le funzioni GDI, ad esempio [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) , o le funzioni DirectX, ad esempio **DirectDrawCreate**.

Per individuare gli schermi indipendenti, chiamare [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) e cercare le visualizzazioni che non dispongono \_ di un dispositivo \_ di visualizzazione collegato \_ al flag del \_ desktop nella struttura del [**\_ dispositivo di visualizzazione**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea) .

Un'applicazione può aprire una visualizzazione chiamando


```C++
hdc = CreateDC(lpszDisplayName, NULL, NULL, lpDevMode);
```



In questa chiamata il parametro *lpszDisplayName* è uno dei nomi di dispositivo restituiti da [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) e *lpDevMode* è una descrizione della modalità grafica per questo dispositivo. L'HDC risultante può essere usato per eseguire qualsiasi operazione grafica sul dispositivo.

 

 



