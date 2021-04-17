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
# <a name="creating-a-math-input-control"></a><span data-ttu-id="2b2d9-103">Creazione di un controllo di input matematico</span><span class="sxs-lookup"><span data-stu-id="2b2d9-103">Creating a Math Input Control</span></span>

<span data-ttu-id="2b2d9-104">Per creare il controllo di input matematico, è necessario:</span><span class="sxs-lookup"><span data-stu-id="2b2d9-104">To create the math input control, you must:</span></span>

-   [<span data-ttu-id="2b2d9-105">Includi intestazioni e librerie per il controllo di input matematico</span><span class="sxs-lookup"><span data-stu-id="2b2d9-105">Include Headers and Libraries for the Math Input Control</span></span>](#include-headers-and-libraries-for-the-math-input-control)
-   [<span data-ttu-id="2b2d9-106">Dichiarare il puntatore di controllo e chiamare CoInitialize sull'indicatore di misura del controllo</span><span class="sxs-lookup"><span data-stu-id="2b2d9-106">Declare the Control Pointer and Call CoInitialize on the Control Pointer</span></span>](#declare-the-control-pointer-and-call-coinitialize-on-the-control-pointer)
-   [<span data-ttu-id="2b2d9-107">Mostra il controllo</span><span class="sxs-lookup"><span data-stu-id="2b2d9-107">Show the Control</span></span>](#show-the-control)

## <a name="include-headers-and-libraries-for-the-math-input-control"></a><span data-ttu-id="2b2d9-108">Includi intestazioni e librerie per il controllo di input matematico</span><span class="sxs-lookup"><span data-stu-id="2b2d9-108">Include Headers and Libraries for the Math Input Control</span></span>

<span data-ttu-id="2b2d9-109">Il codice seguente deve essere inserito all'inizio del codice in cui verrà usato il controllo di input matematico.</span><span class="sxs-lookup"><span data-stu-id="2b2d9-109">The following code should be placed at the top of your code where you will be using the math input control.</span></span>


```
   // includes for implementation
   #include "micaut.h"
   #include "micaut_i.c"
   
```



<span data-ttu-id="2b2d9-110">Questo codice consente di aggiungere il supporto per il controllo di input matematico all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2b2d9-110">This code will add support for the math input control to your application.</span></span>

## <a name="declare-the-control-pointer-and-call-coinitialize-on-the-control-pointer"></a><span data-ttu-id="2b2d9-111">Dichiarare il puntatore di controllo e chiamare CoInitialize sull'indicatore di misura del controllo</span><span class="sxs-lookup"><span data-stu-id="2b2d9-111">Declare the Control Pointer and Call CoInitialize on the Control Pointer</span></span>

<span data-ttu-id="2b2d9-112">Dopo aver incluso le intestazioni per il controllo, è possibile dichiarare il puntatore di controllo e chiamare CoInitialize su di esso per creare un handle per l'interfaccia di controllo di input matematico.</span><span class="sxs-lookup"><span data-stu-id="2b2d9-112">After you have included the headers for your control, you can declare the control pointer and can call CoInitialize on it to create a handle to the math input control interface.</span></span> <span data-ttu-id="2b2d9-113">Il codice seguente può essere inserito in una classe o come variabile globale nell'implementazione dell'applicazione:</span><span class="sxs-lookup"><span data-stu-id="2b2d9-113">The following code can be placed in a class or as a global variable in your application's implementation:</span></span>


```
   CComPtr<IMathInputControl> g_spMIC; // Math Input Control
   
```



<span data-ttu-id="2b2d9-114">Nel codice seguente viene illustrato come è possibile chiamare CoInitialize sull'indicatore di misura del controllo.</span><span class="sxs-lookup"><span data-stu-id="2b2d9-114">The following code shows how you can call CoInitialize on the control pointer.</span></span>


```
   HRESULT hr = CoInitialize(NULL);
   hr = g_spMIC.CoCreateInstance(CLSID_MathInputControl);
   
```



<span data-ttu-id="2b2d9-115">Dopo la chiamata di CoInitialize sul puntatore di controllo, si dispone di un riferimento al controllo e può accedere ai metodi del controllo.</span><span class="sxs-lookup"><span data-stu-id="2b2d9-115">After calling CoInitialize on the control pointer, you have a reference to the control and can access the control's methods.</span></span> <span data-ttu-id="2b2d9-116">Ad esempio, è possibile abilitare il set esteso di controlli, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="2b2d9-116">For example, you could enable the extended set of controls as shown in the following example.</span></span>


```
   hr = g_spMIC->EnableExtendedButtons(VARIANT_TRUE);
   
```



## <a name="show-the-control"></a><span data-ttu-id="2b2d9-117">Mostra il controllo</span><span class="sxs-lookup"><span data-stu-id="2b2d9-117">Show the Control</span></span>

<span data-ttu-id="2b2d9-118">Il controllo non verrà visualizzato automaticamente dopo averlo creato.</span><span class="sxs-lookup"><span data-stu-id="2b2d9-118">The control will not automatically appear after you create it.</span></span> <span data-ttu-id="2b2d9-119">Per visualizzare il controllo, chiamare il metodo [**show**](/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-show) sul riferimento al controllo creato nel passaggio precedente.</span><span class="sxs-lookup"><span data-stu-id="2b2d9-119">To show the control, call the [**Show**](/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-show) method on the control reference that you created in the previous step.</span></span> <span data-ttu-id="2b2d9-120">Nel codice seguente viene illustrato come è possibile chiamare il metodo [**show**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) .</span><span class="sxs-lookup"><span data-stu-id="2b2d9-120">The following code demonstrates how the [**Show**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) method can be called.</span></span>


```
   hr = g_spMIC->Show();
   
```



<span data-ttu-id="2b2d9-121">Una volta visualizzato, il controllo sarà simile all'illustrazione seguente.</span><span class="sxs-lookup"><span data-stu-id="2b2d9-121">After the control shows, it will look something like the following illustration.</span></span>

![screenshot che mostra il controllo di input matematico](images/mic.png)

<span data-ttu-id="2b2d9-123">Si noti che è stato abilitato il set esteso di pulsanti in modo da rendere disponibili le operazioni di **rollforward** e **rollback** .</span><span class="sxs-lookup"><span data-stu-id="2b2d9-123">Note that I have enabled the extended set of buttons so that **Redo** and **Undo** are available.</span></span>

 

 
