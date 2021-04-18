---
description: Per compilare applicazioni per Tablet PC in C \# e Visual Basic .NET, il progetto in Microsoft Visual Studio .NET deve includere un riferimento agli assembly di librerie gestite da Tablet PC. Consente di accedere al modello a oggetti gestito e ai controlli.
ms.assetid: d9c491c9-d341-4189-9a41-45c4d78322fa
title: Libreria e controlli gestiti (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7299a1df0cc1b64d650ec748eb2de01ad4b776f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316822"
---
# <a name="managed-library-and-controls-tablet-pc"></a><span data-ttu-id="d1f60-104">Libreria e controlli gestiti (Tablet PC)</span><span class="sxs-lookup"><span data-stu-id="d1f60-104">Managed Library and Controls (Tablet PC)</span></span>

<span data-ttu-id="d1f60-105">Per compilare applicazioni per Tablet PC in C \# e Visual Basic .NET, il progetto in Microsoft Visual Studio .NET deve includere un riferimento agli assembly di librerie gestite da Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="d1f60-105">To build Tablet PC applications in C\# and Visual Basic .NET, your project in Microsoft Visual Studio .NET must include a reference to the Tablet PC managed library assemblies.</span></span> <span data-ttu-id="d1f60-106">Consente di accedere al modello a oggetti gestito e ai controlli.</span><span class="sxs-lookup"><span data-stu-id="d1f60-106">This provides access to the managed object model and controls.</span></span>

## <a name="microsoft-visual-c-and-visual-basicnet"></a><span data-ttu-id="d1f60-107">Microsoft Visual C \# e visual Basic.NET</span><span class="sxs-lookup"><span data-stu-id="d1f60-107">Microsoft Visual C\# and Visual Basic.NET</span></span>

<span data-ttu-id="d1f60-108">In Windows Vista, gli assembly della libreria gestita di Tablet PC vengono installati per impostazione predefinita in due directory:</span><span class="sxs-lookup"><span data-stu-id="d1f60-108">In Windows Vista, the Tablet PC managed library assemblies are installed by default in two directories:</span></span>

-   <span data-ttu-id="d1f60-109"><systemdrive>: \\ Programmi file \\ comuni \\ Microsoft Shared \\ Ink directory</span><span class="sxs-lookup"><span data-stu-id="d1f60-109"><systemdrive>:\\Program Files\\Common Files\\Microsoft Shared\\Ink directory</span></span>
-   <span data-ttu-id="d1f60-110"><systemdrive>: \\ Programmi \\ Microsoft SDK \\ Windows \\ v 6.0 \\ bin</span><span class="sxs-lookup"><span data-stu-id="d1f60-110"><systemdrive>:\\Program Files\\Microsoft SDKs\\Windows\\v6.0\\Bin</span></span>

<span data-ttu-id="d1f60-111">Per aggiungere un riferimento alle librerie gestite dalla piattaforma Tablet PC in Microsoft Visual Studio .NET:</span><span class="sxs-lookup"><span data-stu-id="d1f60-111">To add a reference to the Tablet PC platform managed libraries in Microsoft Visual Studio .NET:</span></span>

1.  <span data-ttu-id="d1f60-112">Aprire il progetto Visual Studio .NET.</span><span class="sxs-lookup"><span data-stu-id="d1f60-112">Open your Visual Studio .NET project.</span></span>
2.  <span data-ttu-id="d1f60-113">Scegliere **Aggiungi riferimento** dal menu **Progetto**.</span><span class="sxs-lookup"><span data-stu-id="d1f60-113">On the **Project** menu, click **Add Reference**.</span></span>
3.  <span data-ttu-id="d1f60-114">Nella scheda **.NET** della finestra di dialogo **Aggiungi riferimento** selezionare l' **API Microsoft Tablet PC** nell'elenco componenti.</span><span class="sxs-lookup"><span data-stu-id="d1f60-114">On the **.NET** tab in the **Add Reference** dialog box, on the components list, select **Microsoft Tablet PC API**.</span></span>
4.  <span data-ttu-id="d1f60-115">Fare clic su **Seleziona** e quindi su **OK**.</span><span class="sxs-lookup"><span data-stu-id="d1f60-115">Click **Select**, and then click **OK**.</span></span>

<span data-ttu-id="d1f60-116">Per aggiungere un riferimento alle API di analisi dell'input penna in Visual Studio .NET:</span><span class="sxs-lookup"><span data-stu-id="d1f60-116">To add a reference to the ink analysis APIs in Visual Studio .NET:</span></span>

1.  <span data-ttu-id="d1f60-117">Aprire il progetto Microsoft Visual Studio .NET.</span><span class="sxs-lookup"><span data-stu-id="d1f60-117">Open your Microsoft Visual Studio .NET project.</span></span>
2.  <span data-ttu-id="d1f60-118">Scegliere **Aggiungi riferimento** dal menu **Progetto**.</span><span class="sxs-lookup"><span data-stu-id="d1f60-118">On the **Project** menu, click **Add Reference**.</span></span>
3.  <span data-ttu-id="d1f60-119">Nella scheda **.NET** della finestra di dialogo **Aggiungi riferimento** , nell'elenco componenti selezionare **libreria gestita di analisi dell'input penna Microsoft Tablet PC**.</span><span class="sxs-lookup"><span data-stu-id="d1f60-119">On the **.NET** tab in the **Add Reference** dialog box, on the components list, select **Microsoft Tablet PC Ink Analysis Managed Library**.</span></span>
4.  <span data-ttu-id="d1f60-120">Fare clic su **Seleziona** e quindi su **OK**.</span><span class="sxs-lookup"><span data-stu-id="d1f60-120">Click **Select**, and then click **OK**.</span></span>

> [!Note]  
> <span data-ttu-id="d1f60-121">Quando si compilano applicazioni che usano Microsoft. Ink in Visual Studio 2005, è necessario selezionare **progetto**, selezionare **Proprietà**, selezionare **Compila** e impostare target piattaforma = x86.</span><span class="sxs-lookup"><span data-stu-id="d1f60-121">When compiling applications that use Microsoft.Ink on Visual Studio 2005, you must select **Project**, select **Properties**, select **Build** and set Platform target=x86.</span></span> <span data-ttu-id="d1f60-122">Questa opzione non è disponibile nei prodotti Microsoft Visual Studio Express.</span><span class="sxs-lookup"><span data-stu-id="d1f60-122">This option is not available in Microsoft Visual Studio Express products.</span></span>

 

 

 



