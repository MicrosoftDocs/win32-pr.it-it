---
description: "Per creare un'applicazione per WMI mediante C++: è necessario inizializzare COM, accedere e impostare i protocolli WMI ed eseguire una pulizia manuale."
ms.assetid: 0b9b7990-6982-4ba9-8dba-7470990405f7
ms.tgt_platform: multiple
title: Creazione di un'applicazione WMI con C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baaa4f7e79828b2cb6cb496254d906182ff611ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348406"
---
# <a name="creating-a-wmi-application-using-c"></a><span data-ttu-id="6e0a9-103">Creazione di un'applicazione WMI con C++</span><span class="sxs-lookup"><span data-stu-id="6e0a9-103">Creating a WMI Application Using C++</span></span>

<span data-ttu-id="6e0a9-104">Per creare un'applicazione per WMI mediante C++: è necessario inizializzare COM, accedere e impostare i protocolli WMI ed eseguire una pulizia manuale.</span><span class="sxs-lookup"><span data-stu-id="6e0a9-104">To create an application for WMI using C++: you must initialize COM, access and set WMI protocols, and perform a manual cleanup.</span></span> <span data-ttu-id="6e0a9-105">Tuttavia, C++ ha il vantaggio di flessibilità e potenza.</span><span class="sxs-lookup"><span data-stu-id="6e0a9-105">However, C++ does have the advantage of flexibility and power.</span></span> <span data-ttu-id="6e0a9-106">Pertanto, anche se è meglio utilizzare Visual Basic Scripting Edition (VBScript) o Windows PowerShell per semplici processi, C++ funziona meglio per applicazioni più sofisticate ed è necessario per la scrittura di [provider](providing-data-to-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="6e0a9-106">Therefore, while you are better served in using Visual Basic Scripting Edition (VBScript) or Windows PowerShell for simple processes, C++ works better for more sophisticated applications and is required for writing [providers](providing-data-to-wmi.md).</span></span>

<span data-ttu-id="6e0a9-107">Nella procedura riportata di seguito viene descritto come creare un'applicazione WMI.</span><span class="sxs-lookup"><span data-stu-id="6e0a9-107">The following procedure describes how to create a WMI application.</span></span>

<span data-ttu-id="6e0a9-108">**Per creare un'applicazione WMI**</span><span class="sxs-lookup"><span data-stu-id="6e0a9-108">**To create a WMI application**</span></span>

1.  <span data-ttu-id="6e0a9-109">[Inizializzare com](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="6e0a9-109">[Initialize COM](initializing-com-for-a-wmi-application.md).</span></span>

    <span data-ttu-id="6e0a9-110">Poiché WMI è basato sulla tecnologia COM, è necessario eseguire chiamate alle funzioni [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) e [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) per accedere a WMI.</span><span class="sxs-lookup"><span data-stu-id="6e0a9-110">Because WMI is based on COM technology, you must perform calls to the [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) functions to access WMI.</span></span>

2.  <span data-ttu-id="6e0a9-111">[Creare una connessione a uno spazio dei nomi WMI](creating-a-connection-to-a-wmi-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="6e0a9-111">[Create a connection to a WMI namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

    <span data-ttu-id="6e0a9-112">Per definizione, WMI viene eseguito in un processo diverso rispetto all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6e0a9-112">By definition, WMI runs in a different process than your application.</span></span> <span data-ttu-id="6e0a9-113">Pertanto, è necessario creare una connessione tra l'applicazione e WMI.</span><span class="sxs-lookup"><span data-stu-id="6e0a9-113">Therefore, you must create a connection between your application and WMI.</span></span>

3.  <span data-ttu-id="6e0a9-114">[Impostare i livelli di sicurezza per la connessione WMI](setting-the-security-levels-on-a-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="6e0a9-114">[Set the security levels on the WMI connection](setting-the-security-levels-on-a-wmi-connection.md).</span></span>

    <span data-ttu-id="6e0a9-115">Per utilizzare la connessione creata a WMI, è necessario impostare i livelli di autenticazione e di rappresentazione per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6e0a9-115">To use the connection you create to WMI, you must set the impersonation and authentication levels for your application.</span></span>

4.  <span data-ttu-id="6e0a9-116">Implementare lo scopo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6e0a9-116">Implement the purpose of your application.</span></span>

    <span data-ttu-id="6e0a9-117">WMI espone un'ampia gamma di interfacce COM che consentono di accedere e modificare i dati nell'azienda.</span><span class="sxs-lookup"><span data-stu-id="6e0a9-117">WMI exposes a variety of COM interfaces use to access and manipulate data across your enterprise.</span></span> <span data-ttu-id="6e0a9-118">Per ulteriori informazioni, vedere [modifica delle informazioni di classe e istanza](manipulating-class-and-instance-information.md), [ricezione di un evento WMI](receiving-a-wmi-event.md)e [API com per WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="6e0a9-118">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md), [Receiving a WMI Event](receiving-a-wmi-event.md), and [COM API for WMI](com-api-for-wmi.md).</span></span>

    <span data-ttu-id="6e0a9-119">Questo è il punto in cui deve esistere la maggior parte dell'applicazione client WMI, ad esempio l'accesso agli oggetti WMI o la manipolazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="6e0a9-119">This is where the bulk of your WMI client application should exist, such as accessing WMI objects or manipulating data.</span></span>

5.  <span data-ttu-id="6e0a9-120">[Pulire e arrestare l'applicazione](cleaning-up-and-shutting-down-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="6e0a9-120">[Cleanup and shut down your application](cleaning-up-and-shutting-down-a-wmi-application.md).</span></span>

    <span data-ttu-id="6e0a9-121">Dopo aver completato le query in WMI, è necessario eliminare tutti i puntatori COM e arrestare correttamente l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6e0a9-121">After you complete your queries to WMI, you should destroy all COM pointers and shut down your application correctly.</span></span>

<span data-ttu-id="6e0a9-122">Per ulteriori informazioni e un esempio di codice su come creare un'applicazione WMI, vedere [esempio: creazione di un'applicazione WMI](example-creating-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="6e0a9-122">For more information and a code example about how to create a WMI application, see [Example: Creating a WMI Application](example-creating-a-wmi-application.md).</span></span>

 

 
