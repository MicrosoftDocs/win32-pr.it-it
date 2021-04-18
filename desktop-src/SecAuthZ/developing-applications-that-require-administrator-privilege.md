---
description: È possibile sviluppare un'applicazione che esegua operazioni che richiedono un privilegio di amministratore ancora eseguito come utente standard.
ms.assetid: 78099b59-b09b-43c0-91f5-adb5c9e0e191
title: Sviluppo di applicazioni che richiedono privilegi di amministratore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d22687dad0a8914c5dcaebe8ea85a525529a34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315838"
---
# <a name="developing-applications-that-require-administrator-privilege"></a><span data-ttu-id="2f350-103">Sviluppo di applicazioni che richiedono privilegi di amministratore</span><span class="sxs-lookup"><span data-stu-id="2f350-103">Developing Applications that Require Administrator Privilege</span></span>

<span data-ttu-id="2f350-104">È possibile sviluppare un'applicazione che esegua operazioni che richiedono un privilegio di amministratore ancora eseguito come utente standard.</span><span class="sxs-lookup"><span data-stu-id="2f350-104">It is possible to develop an application that performs operations that require administrator privilege yet runs as a standard user.</span></span>

<span data-ttu-id="2f350-105">Sono disponibili diversi modelli per eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="2f350-105">There are several models for accomplishing this.</span></span>



| <span data-ttu-id="2f350-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="2f350-106">Topic</span></span>                                                                | <span data-ttu-id="2f350-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2f350-107">Description</span></span>                                                                                                                                                                                          |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2f350-108">Modello di attività con privilegi elevati</span><span class="sxs-lookup"><span data-stu-id="2f350-108">Elevated Task Model</span></span>](elevated-task-model.md)                       | <span data-ttu-id="2f350-109">Un'applicazione in esecuzione come utente standard esegue operazioni che richiedono privilegi di amministratore avviando un'attività pianificata.</span><span class="sxs-lookup"><span data-stu-id="2f350-109">An application running as a standard user performs operations that require administrator privilege by starting a scheduled task.</span></span>                                                                     |
| [<span data-ttu-id="2f350-110">Modello di servizio del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="2f350-110">Operating System Service Model</span></span>](operating-system-service-model.md) | <span data-ttu-id="2f350-111">Un'applicazione in esecuzione come utente standard comunica con un servizio eseguito come **sistema** utilizzando RPC ( [Remote Procedure Call](/windows/desktop/Rpc/rpc-start-page) ).</span><span class="sxs-lookup"><span data-stu-id="2f350-111">An application running as a standard user communicates with a service running as **SYSTEM** by using [Remote Procedure Call](/windows/desktop/Rpc/rpc-start-page) (RPC).</span></span>                                              |
| [<span data-ttu-id="2f350-112">Modello di broker amministratore</span><span class="sxs-lookup"><span data-stu-id="2f350-112">Administrator Broker Model</span></span>](administrator-broker-model.md)         | <span data-ttu-id="2f350-113">L'applicazione è divisa in due programmi.</span><span class="sxs-lookup"><span data-stu-id="2f350-113">The application is divided into two programs.</span></span> <span data-ttu-id="2f350-114">Uno dei programmi viene eseguito come utente standard e l'altro viene eseguito con privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="2f350-114">One of the programs runs as a standard user, and the other runs with administrator privilege.</span></span>                                                          |
| [<span data-ttu-id="2f350-115">Modello a oggetti COM dell'amministratore</span><span class="sxs-lookup"><span data-stu-id="2f350-115">Administrator COM Object Model</span></span>](administrator-com-object-model.md) | <span data-ttu-id="2f350-116">Un'applicazione in esecuzione come utente standard esegue operazioni che richiedono privilegi di amministratore creando un oggetto [Component Object Model](/windows/desktop/com/component-object-model--com--portal) con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="2f350-116">An application running as a standard user performs operations that require administrator privilege by creating an elevated [Component Object Model](/windows/desktop/com/component-object-model--com--portal) object.</span></span> |



 

 

 
