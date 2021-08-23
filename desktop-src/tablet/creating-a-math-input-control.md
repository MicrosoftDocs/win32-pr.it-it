---
description: Viene illustrato come creare un controllo di input matematico.
ms.assetid: 59976b01-9032-4226-a160-e9b2d4b8b23b
title: Creazione di un Controllo input penna espressioni matematiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ee8cca2a799bd44e79ef2f32691614bb3f22c933b40aa23dc4aa0cd6cfb6fb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967720"
---
# <a name="creating-a-math-input-control"></a>Creazione di un Controllo input penna espressioni matematiche

Per creare il controllo di input matematico, è necessario:

-   [Includere intestazioni e librerie per il Controllo input penna espressioni matematiche](#include-headers-and-libraries-for-the-math-input-control)
-   [Dichiarare il puntatore di controllo e chiamare CoInitialize sul puntatore di controllo](#declare-the-control-pointer-and-call-coinitialize-on-the-control-pointer)
-   [Visualizzare il controllo](#show-the-control)

## <a name="include-headers-and-libraries-for-the-math-input-control"></a>Includere intestazioni e librerie per il Controllo input penna espressioni matematiche

Il codice seguente deve essere inserito all'inizio del codice in cui verrà utilizzato il controllo di input matematico.


```
   // includes for implementation
   #include "micaut.h"
   #include "micaut_i.c"
   
```



Questo codice aggiungerà il supporto per il controllo di input matematico all'applicazione.

## <a name="declare-the-control-pointer-and-call-coinitialize-on-the-control-pointer"></a>Dichiarare il puntatore di controllo e chiamare CoInitialize sul puntatore di controllo

Dopo aver incluso le intestazioni per il controllo, è possibile dichiarare il puntatore di controllo e chiamare CoInitialize su di esso per creare un handle per l'interfaccia del controllo di input matematico. Il codice seguente può essere inserito in una classe o come variabile globale nell'implementazione dell'applicazione:


```
   CComPtr<IMathInputControl> g_spMIC; // Math Input Control
   
```



Nel codice seguente viene illustrato come chiamare CoInitialize sul puntatore di controllo.


```
   HRESULT hr = CoInitialize(NULL);
   hr = g_spMIC.CoCreateInstance(CLSID_MathInputControl);
   
```



Dopo aver chiamato CoInitialize sul puntatore di controllo, si ha un riferimento al controllo e si può accedere ai metodi del controllo. Ad esempio, è possibile abilitare il set esteso di controlli come illustrato nell'esempio seguente.


```
   hr = g_spMIC->EnableExtendedButtons(VARIANT_TRUE);
   
```



## <a name="show-the-control"></a>Visualizzare il controllo

Il controllo non verrà visualizzato automaticamente dopo la creazione. Per visualizzare il controllo, chiamare [**il metodo Show**](/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-show) sul riferimento al controllo creato nel passaggio precedente. Nel codice seguente viene illustrato [**come**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) chiamare il metodo Show.


```
   hr = g_spMIC->Show();
   
```



Dopo che il controllo è stato visualizzato, avrà un aspetto simile all'illustrazione seguente.

![Screenshot che mostra il controllo di input matematico](images/mic.png)

Si noti che è stato abilitato il set esteso di pulsanti in modo che **i pulsanti Ripristina** **e** Annulla siano disponibili.

 

 
