---
title: Utilizzo delle librerie dei tipi da parte degli strumenti di sviluppo
description: Utilizzo delle librerie dei tipi da parte degli strumenti di sviluppo
ms.assetid: 260aa694-1055-4a43-93aa-69a9d7359881
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0cc0f5249075aa861a1301466f86a0f769b8bf3
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/03/2021
ms.locfileid: "106320196"
---
# <a name="how-developer-tools-use-type-libraries"></a><span data-ttu-id="72cbe-103">Utilizzo delle librerie dei tipi da parte degli strumenti di sviluppo</span><span class="sxs-lookup"><span data-stu-id="72cbe-103">How Developer Tools Use Type Libraries</span></span>

<span data-ttu-id="72cbe-104">Il diagramma seguente illustra il modo in cui i vari strumenti di sviluppo interagiscono con la libreria dei tipi di un oggetto COM.</span><span class="sxs-lookup"><span data-stu-id="72cbe-104">The following diagram illustrates how the various development tools interact with a COM object's type library.</span></span> <span data-ttu-id="72cbe-105">Ogni libreria dei tipi espone interfacce programmatiche standard che possono essere chiamate da strumenti per ottenere informazioni sugli elementi descritti nella libreria dei tipi.</span><span class="sxs-lookup"><span data-stu-id="72cbe-105">Each type library exposes standard programmatic interfaces that tools can call to get information about the elements described in that type library.</span></span> <span data-ttu-id="72cbe-106">In questo diagramma GUID rappresenta l'identificatore univoco globale e la RPC per la chiamata di procedura remota.</span><span class="sxs-lookup"><span data-stu-id="72cbe-106">In this diagram, GUID stands for globally unique identifier and RPC for remote procedure call.</span></span>

![Diagramma che illustra il modo in cui lo strumento di sviluppo interagisce con la libreria dei tipi di un oggetto C O M.](images/09983c96-3f01-4ad5-8d3e-12b8ed28c35d.png)

<span data-ttu-id="72cbe-108">Nel diagramma precedente, gli strumenti di conversione C++, ad esempio il compilatore MIDL e le procedure guidate fornite dal sistema di sviluppo Microsoft Visual C++, generano file di intestazione e stub.</span><span class="sxs-lookup"><span data-stu-id="72cbe-108">In the preceding diagram, the C++ conversion tools, such as the MIDL compiler and the wizards provided by the Microsoft Visual C++ development system, generate header and stub files.</span></span> <span data-ttu-id="72cbe-109">È possibile aggiungere questi file al progetto per utilizzare l'oggetto COM descritto dalla libreria dei tipi.</span><span class="sxs-lookup"><span data-stu-id="72cbe-109">You can add these files to your project in order to use the COM object described by the type library.</span></span>

<span data-ttu-id="72cbe-110">Analogamente, in Java gli strumenti di sviluppo generano file di classe e di origine Java che è quindi possibile importare nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="72cbe-110">Similarly, in Java the developer tools generate Java class and source files, which you can then import into your application.</span></span>

<span data-ttu-id="72cbe-111">In Visual Basic, lo scenario è piuttosto più semplice.</span><span class="sxs-lookup"><span data-stu-id="72cbe-111">In Visual Basic, the scenario is somewhat simpler.</span></span> <span data-ttu-id="72cbe-112">Non è necessario generare file aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="72cbe-112">You do not need to generate additional files.</span></span> <span data-ttu-id="72cbe-113">Nell'ambiente Visual Basic sono disponibili finestre di dialogo che elencano gli oggetti COM attualmente installati nel computer.</span><span class="sxs-lookup"><span data-stu-id="72cbe-113">The Visual Basic environment provides dialog boxes listing the COM objects currently installed on your computer.</span></span> <span data-ttu-id="72cbe-114">Si seleziona il componente che si desidera chiamare dall'applicazione e questo viene aggiunto al progetto, come un componente o un riferimento.</span><span class="sxs-lookup"><span data-stu-id="72cbe-114">You select the component you want to call from your application, and it is added to your project, either as a component or a reference.</span></span>

<span data-ttu-id="72cbe-115">Il Visualizzatore OLE-COM legge una libreria dei tipi, genera un file IDL temporaneo basato sulla libreria dei tipi e lo visualizza agli utenti.</span><span class="sxs-lookup"><span data-stu-id="72cbe-115">The OLE-COM viewer reads a type library, generates a temporary IDL file based on the type library, and displays it to users.</span></span> <span data-ttu-id="72cbe-116">Nel Visualizzatore OLE-COM viene inoltre visualizzata la sintassi C++ per gli elementi COM elencati nella libreria dei tipi.</span><span class="sxs-lookup"><span data-stu-id="72cbe-116">The OLE-COM viewer also displays the C++ syntax for the COM elements listed in the type library.</span></span>

<span data-ttu-id="72cbe-117">Per ulteriori informazioni sulle librerie dei tipi, vedere [librerie dei tipi e il Object Description Language](/previous-versions/windows/desktop/automat/type-libraries-and-the-object-description-language).</span><span class="sxs-lookup"><span data-stu-id="72cbe-117">For more information about type libraries, see [Type Libraries and the Object Description Language](/previous-versions/windows/desktop/automat/type-libraries-and-the-object-description-language).</span></span>

 

 