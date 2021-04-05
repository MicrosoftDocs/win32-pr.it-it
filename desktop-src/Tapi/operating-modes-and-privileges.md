---
description: Quando si apre un dispositivo telefonico, l'applicazione può richiedere una delle due modalità operative.
ms.assetid: 2bb16fbe-883e-4734-a071-f14f5e5737e3
title: Modalità operative e privilegi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ba1cc01ed0552762ac3bc97449b1ae5a923cb10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755119"
---
# <a name="operating-modes-and-privileges"></a><span data-ttu-id="bb328-103">Modalità operative e privilegi</span><span class="sxs-lookup"><span data-stu-id="bb328-103">Operating Modes and Privileges</span></span>

<span data-ttu-id="bb328-104">Quando si apre un dispositivo telefonico, l'applicazione può richiedere una delle due modalità operative.</span><span class="sxs-lookup"><span data-stu-id="bb328-104">The application can request one of two operating modes when opening a phone device.</span></span> <span data-ttu-id="bb328-105">Queste modalità riflettono i privilegi richiesti dall'applicazione per il dispositivo:</span><span class="sxs-lookup"><span data-stu-id="bb328-105">These modes reflect the privileges the application requests for the device:</span></span>

-   <span data-ttu-id="bb328-106">L'apertura di un telefono per i privilegi di monitoraggio consente all'applicazione di determinare lo stato del dispositivo telefonico.</span><span class="sxs-lookup"><span data-stu-id="bb328-106">Opening a phone for monitor privileges lets the application determine the status of the phone device.</span></span> <span data-ttu-id="bb328-107">I messaggi vengono inviati all'applicazione quando vengono rilevate modifiche allo stato sul dispositivo telefonico.</span><span class="sxs-lookup"><span data-stu-id="bb328-107">Messages are sent to the application when status changes on the phone device are detected.</span></span>
-   <span data-ttu-id="bb328-108">Un'applicazione che apre un dispositivo telefonico per i privilegi proprietario può utilizzare operazioni che modificano lo stato del dispositivo telefonico.</span><span class="sxs-lookup"><span data-stu-id="bb328-108">An application that opens a phone device for owner privileges can use operations that modify the state of the phone device.</span></span> <span data-ttu-id="bb328-109">Il privilegio proprietario include automaticamente anche i privilegi di monitoraggio completo.</span><span class="sxs-lookup"><span data-stu-id="bb328-109">Owner privilege automatically includes full monitor privileges as well.</span></span> <span data-ttu-id="bb328-110">In qualsiasi momento, è possibile aprire un determinato dispositivo telefonico solo una volta per i privilegi di proprietario, ma più volte per i privilegi di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="bb328-110">At any time, a given phone device can be open only once for owner privileges, but multiple times for monitor privileges.</span></span> <span data-ttu-id="bb328-111">Tutte le operazioni di **telefonia** richiedono privilegi di proprietario, mentre tutte le operazioni **phoneGet** richiedono solo privilegi di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="bb328-111">All **phoneSet** operations require owner privileges, while all **phoneGet** operations require only monitor privileges.</span></span>

 

 



