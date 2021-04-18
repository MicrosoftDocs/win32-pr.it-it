---
title: Uso di StoServe
description: StoServe è una DLL destinata principalmente a un server COM.
ms.assetid: 32cb284a-de78-4953-9d8e-5bb87d6d5a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d46dfd4070e9951223e0a498184b8db814c7a43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300206"
---
# <a name="using-stoserve"></a><span data-ttu-id="eb7d6-103">Uso di StoServe</span><span class="sxs-lookup"><span data-stu-id="eb7d6-103">Using StoServe</span></span>

<span data-ttu-id="eb7d6-104">**StoServe** è una dll destinata principalmente a un server com.</span><span class="sxs-lookup"><span data-stu-id="eb7d6-104">**StoServe** is a DLL that is intended primarily as a COM server.</span></span> <span data-ttu-id="eb7d6-105">Sebbene possa essere caricato in modo implicito tramite il collegamento al relativo oggetto associato. Il file LIB viene in genere usato dopo una chiamata LoadLibrary esplicita, in genere dalla funzione COM [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject).</span><span class="sxs-lookup"><span data-stu-id="eb7d6-105">Although it can be implicitly loaded by linking to its associated .LIB file, it is normally used after an explicit LoadLibrary call, usually from within the COM function [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject).</span></span> <span data-ttu-id="eb7d6-106">**StoServe** è un server in-process con registrazione automatica.</span><span class="sxs-lookup"><span data-stu-id="eb7d6-106">**StoServe** is a self-registering in-process server.</span></span>

<span data-ttu-id="eb7d6-107">Per usare **StoServe**, non è necessario che un programma client includa StoServe. H o collegamento a STOSERVE. LIB.</span><span class="sxs-lookup"><span data-stu-id="eb7d6-107">To use **StoServe**, a client program does not need to include STOSERVE.H or link to STOSERVE.LIB.</span></span> <span data-ttu-id="eb7d6-108">Un client COM di **StoServe** Ottiene l'accesso esclusivamente tramite il CLSID e i servizi com dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="eb7d6-108">A COM client of **StoServe** obtains access solely through its object's CLSID and COM services.</span></span> <span data-ttu-id="eb7d6-109">Per **StoServe**, il CLSID è CLSID \_ DllPaper (definito nel file PAPGUIDS. H nella \\ directory di pari livello Inc.</span><span class="sxs-lookup"><span data-stu-id="eb7d6-109">For **StoServe**, that CLSID is CLSID\_DllPaper (defined in file PAPGUIDS.H in the \\INC sibling directory).</span></span> <span data-ttu-id="eb7d6-110">L'esempio di codice [StoClien](structured-storage-client-sample--stoclien-.md) Mostra come il client ottiene questo accesso.</span><span class="sxs-lookup"><span data-stu-id="eb7d6-110">The [StoClien](structured-storage-client-sample--stoclien-.md) code sample shows how the client obtains this access.</span></span>

<span data-ttu-id="eb7d6-111">Il makefile che compila questo esempio registra automaticamente il server nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="eb7d6-111">The makefile that builds this sample automatically registers the server in the registry.</span></span> <span data-ttu-id="eb7d6-112">È possibile avviare manualmente la registrazione automatica eseguendo il comando seguente al prompt dei comandi nella directory **StoServe** :</span><span class="sxs-lookup"><span data-stu-id="eb7d6-112">You can manually initiate its self-registration by issuing the following command at the command prompt in the **StoServe** directory:</span></span>

<span data-ttu-id="eb7d6-113"> **Registro** NMAKE</span><span class="sxs-lookup"><span data-stu-id="eb7d6-113">**nmake** **register**</span></span>

<span data-ttu-id="eb7d6-114">Si presuppone che sia configurato un ambiente di compilazione.</span><span class="sxs-lookup"><span data-stu-id="eb7d6-114">This assumes that you have a compilation environment set up.</span></span> <span data-ttu-id="eb7d6-115">In caso contrario, è anche possibile richiamare direttamente il REGISTER.EXE comando al prompt dei comandi, mentre si trovi nella directory **StoServe**</span><span class="sxs-lookup"><span data-stu-id="eb7d6-115">If not, you can also directly invoke the REGISTER.EXE command at the command prompt while in the **StoServe** directory.</span></span>

<span data-ttu-id="eb7d6-116">**..\\ Registra \\register.exe** **stoserve.dll**</span><span class="sxs-lookup"><span data-stu-id="eb7d6-116">**..\\register\\register.exe** **stoserve.dll**</span></span>

<span data-ttu-id="eb7d6-117">Questi comandi di registrazione richiedono una compilazione precedente dell'esempio di registrazione in questa serie, oltre a una build precedente di STOSERVE.DLL.</span><span class="sxs-lookup"><span data-stu-id="eb7d6-117">These registration commands require a prior build of the REGISTER sample in this series, as well as a prior build of STOSERVE.DLL.</span></span>

<span data-ttu-id="eb7d6-118">In questa serie i makefile usano l'utilità REGISTER.EXE dall'esempio REGISTER.</span><span class="sxs-lookup"><span data-stu-id="eb7d6-118">In this series, the makefiles use the REGISTER.EXE utility from the REGISTER sample.</span></span> <span data-ttu-id="eb7d6-119">Le versioni recenti di Platform Software Development Kit (SDK) e Visual C++ includono un'utilità, REGSVR32.EXE, che può essere usata in modo analogo per registrare i server in-process e il marshalling delle dll.</span><span class="sxs-lookup"><span data-stu-id="eb7d6-119">Recent releases of the Platform Software Development Kit (SDK) and Visual C++ include a utility, REGSVR32.EXE, which can be used in a similar fashion to register in-process servers and marshaling DLLs.</span></span>

<span data-ttu-id="eb7d6-120">**StoServe** usa molte delle classi e dei servizi di utilità forniti da APPUTIL.</span><span class="sxs-lookup"><span data-stu-id="eb7d6-120">**StoServe** uses many of the utility classes and services provided by APPUTIL.</span></span> <span data-ttu-id="eb7d6-121">Per altri dettagli su APPUTIL, studiare il codice sorgente della libreria APPUTIL nella directory di pari livello APPUTIL e APPUTIL.HTM nella directory principale dell'esercitazione.</span><span class="sxs-lookup"><span data-stu-id="eb7d6-121">For more details on APPUTIL, study the APPUTIL library's source code in the sibling APPUTIL directory and APPUTIL.HTM in the main tutorial directory.</span></span>

 

 