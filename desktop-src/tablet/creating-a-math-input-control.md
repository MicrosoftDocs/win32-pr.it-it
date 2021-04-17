---
description: Viene illustrato come creare un controllo di input matematico.
ms.assetid: 59976b01-9032-4226-a160-e9b2d4b8b23b
title: Creazione di un controllo di input matematico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5084f29943395bc6781fe20598f86bdc08c6c61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104568292"
---
# <a name="creating-a-math-input-control"></a>Creazione di un controllo di input matematico

Per creare il controllo di input matematico, è necessario:

-   [Includi intestazioni e librerie per il controllo di input matematico](#include-headers-and-libraries-for-the-math-input-control)
-   [Dichiarare il puntatore di controllo e chiamare CoInitialize sull'indicatore di misura del controllo](#declare-the-control-pointer-and-call-coinitialize-on-the-control-pointer)
-   [Mostra il controllo](#show-the-control)

## <a name="include-headers-and-libraries-for-the-math-input-control"></a>Includi intestazioni e librerie per il controllo di input matematico

Il codice seguente deve essere inserito all'inizio del codice in cui verrà usato il controllo di input matematico.


```
   // includes for implementation
   #include "micaut.h"
   #include "micaut_i.c"
   
```



Questo codice consente di aggiungere il supporto per il controllo di input matematico all'applicazione.

## <a name="declare-the-control-pointer-and-call-coinitialize-on-the-control-pointer"></a>Dichiarare il puntatore di controllo e chiamare CoInitialize sull'indicatore di misura del controllo

Dopo aver incluso le intestazioni per il controllo, è possibile dichiarare il puntatore di controllo e chiamare CoInitialize su di esso per creare un handle per l'interfaccia di controllo di input matematico. Il codice seguente può essere inserito in una classe o come variabile globale nell'implementazione dell'applicazione:


```
   CComPtr<IMathInputControl> g_spMIC; // Math Input Control
   
```



Nel codice seguente viene illustrato come è possibile chiamare CoInitialize sull'indicatore di misura del controllo.


```
   HRESULT hr = CoInitialize(NULL);
   hr = g_spMIC.CoCreateInstance(CLSID_MathInputControl);
   
```



Dopo la chiamata di CoInitialize sul puntatore di controllo, si dispone di un riferimento al controllo e può accedere ai metodi del controllo. Ad esempio, è possibile abilitare il set esteso di controlli, come illustrato nell'esempio seguente.


```
   hr = g_spMIC->EnableExtendedButtons(VARIANT_TRUE);
   
```



## <a name="show-the-control"></a>Mostra il controllo

Il controllo non verrà visualizzato automaticamente dopo averlo creato. Per visualizzare il controllo, chiamare il metodo [**show**](/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-show) sul riferimento al controllo creato nel passaggio precedente. Nel codice seguente viene illustrato come è possibile chiamare il metodo [**show**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) .


```
   hr = g_spMIC->Show();
   
```



Una volta visualizzato, il controllo sarà simile all'illustrazione seguente.

![screenshot che mostra il controllo di input matematico](images/mic.png)

Si noti che è stato abilitato il set esteso di pulsanti in modo da rendere disponibili le operazioni di **rollforward** e **rollback** .

 

 
