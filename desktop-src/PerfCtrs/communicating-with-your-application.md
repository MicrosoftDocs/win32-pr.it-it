---
description: In genere, un provider fornisce dati per conto di un'applicazione.
ms.assetid: 65ea6099-79df-4baa-9752-7df032ccc9a0
title: Comunicazione con l'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6def58d3e03676f3b1b46ba3ebd756eb3adc6196
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881774"
---
# <a name="communicating-with-your-application"></a><span data-ttu-id="0bb9b-103">Comunicazione con l'applicazione</span><span class="sxs-lookup"><span data-stu-id="0bb9b-103">Communicating With Your Application</span></span>

<span data-ttu-id="0bb9b-104">In genere, un provider fornisce dati per conto di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0bb9b-104">Typically, a provider provides data on behalf of an application.</span></span> <span data-ttu-id="0bb9b-105">Ad esempio, un server potrebbe creare una DLL di prestazioni per fornire i dati del contatore.</span><span class="sxs-lookup"><span data-stu-id="0bb9b-105">For example, a server might create a performance DLL to provide its counter data.</span></span> <span data-ttu-id="0bb9b-106">La comunicazione tra un'applicazione e il relativo provider differisce per le applicazioni in modalità utente e kernel.</span><span class="sxs-lookup"><span data-stu-id="0bb9b-106">Communication between an application and its provider differs for user-mode and kernel-mode applications.</span></span> <span data-ttu-id="0bb9b-107">I provider vengono eseguiti in modalità utente.</span><span class="sxs-lookup"><span data-stu-id="0bb9b-107">Providers execute in user mode.</span></span> <span data-ttu-id="0bb9b-108">Per questo motivo, le applicazioni in modalità utente, ad esempio le applicazioni di stampa e visualizzazione, possono utilizzare qualsiasi tecnica per la comunicazione interprocesso, ad esempio le named pipe, il mapping dei file o la RPC.</span><span class="sxs-lookup"><span data-stu-id="0bb9b-108">Because of this, user-mode applications, such as print and display applications, can use any technique for interprocess communication, such as named pipes, file mapping, or RPC.</span></span> <span data-ttu-id="0bb9b-109">Tuttavia, le applicazioni in modalità kernel devono fornire un'interfaccia IOCTL che restituisca i dati sulle prestazioni al provider.</span><span class="sxs-lookup"><span data-stu-id="0bb9b-109">However, kernel-mode applications must provide an IOCTL interface that returns the performance data to the provider.</span></span>

> [!WARNING]
> <span data-ttu-id="0bb9b-110">Non usare COM come meccanismo IPC.</span><span class="sxs-lookup"><span data-stu-id="0bb9b-110">Do not use COM as the IPC mechanism.</span></span> <span data-ttu-id="0bb9b-111">Il sistema non è in grado di garantire lo stato di inizializzazione COM del thread che chiama l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="0bb9b-111">The system cannot guarantee the COM initialization state of the thread calling the interface.</span></span> <span data-ttu-id="0bb9b-112">Pertanto, la DLL potrebbe non essere in grado di inizializzare COM e raccogliere i dati.</span><span class="sxs-lookup"><span data-stu-id="0bb9b-112">Therefore, the DLL may not be able to successfully initialize COM and collect the data.</span></span>

 

 

 



