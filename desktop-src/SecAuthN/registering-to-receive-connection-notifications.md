---
description: Dopo aver creato una DLL per ricevere le notifiche di connessione, è necessario registrarla nel sistema.
ms.assetid: 1a389de1-367d-4b07-a420-4af431d48b7f
title: Registrazione per la ricezione delle notifiche di connessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 812c47ba43fe13e4908a1812f7c67f38a94bce5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756422"
---
# <a name="registering-to-receive-connection-notifications"></a><span data-ttu-id="6d298-103">Registrazione per la ricezione delle notifiche di connessione</span><span class="sxs-lookup"><span data-stu-id="6d298-103">Registering to Receive Connection Notifications</span></span>

<span data-ttu-id="6d298-104">Dopo aver creato una DLL per ricevere le notifiche di connessione, è necessario registrarla nel sistema.</span><span class="sxs-lookup"><span data-stu-id="6d298-104">After you have created a DLL to receive connection notifications, you must register it with the system.</span></span> <span data-ttu-id="6d298-105">A tale scopo, aggiungere un valore **reg \_ expand \_ SZ** sotto il</span><span class="sxs-lookup"><span data-stu-id="6d298-105">You do this by adding a **REG\_EXPAND\_SZ** value under the</span></span>

<span data-ttu-id="6d298-106">**HKEY \_ \_** \\  \\  \\  \\  \\ **Avvisi** NetworkProvider del controllo CurrentControlSet del computer locale</span><span class="sxs-lookup"><span data-stu-id="6d298-106">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**NetworkProvider**\\**Notifyees**</span></span>

<span data-ttu-id="6d298-107">disponga di una chiave.</span><span class="sxs-lookup"><span data-stu-id="6d298-107">key.</span></span> <span data-ttu-id="6d298-108">Questo valore specifica il percorso della DLL che implementa l' [API di notifica della connessione](connection-notification-api.md).</span><span class="sxs-lookup"><span data-stu-id="6d298-108">This value specifies the path to the DLL that implements the [Connection Notification API](connection-notification-api.md).</span></span>

<span data-ttu-id="6d298-109">Il valore può avere qualsiasi nome.</span><span class="sxs-lookup"><span data-stu-id="6d298-109">The value can have any name.</span></span> <span data-ttu-id="6d298-110">Tutti i valori della chiave **notifyd** vengono trattati come percorsi per le dll che ricevono notifiche di eventi di connessione.</span><span class="sxs-lookup"><span data-stu-id="6d298-110">All values under the **Notifyees** key are treated as paths to DLLs that are notified of connection events.</span></span> <span data-ttu-id="6d298-111">Si consiglia di usare un nome che identifichi la DLL.</span><span class="sxs-lookup"><span data-stu-id="6d298-111">It is recommended that you use a name that identifies your DLL.</span></span> <span data-ttu-id="6d298-112">In questo modo si riduce la probabilità che si verifichi un conflitto di nomi con altre applicazioni di notifica della connessione.</span><span class="sxs-lookup"><span data-stu-id="6d298-112">This lessens the chance of a name conflict with other connection notification applications.</span></span>

<span data-ttu-id="6d298-113">Per ulteriori informazioni sulla creazione di un'applicazione che riceve le notifiche di connessione, vedere [ricezione di notifiche di connessione](receiving-connection-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="6d298-113">For more information about how to create an application that receives connection notifications, see [Receiving Connection Notifications](receiving-connection-notifications.md).</span></span>

 

 



