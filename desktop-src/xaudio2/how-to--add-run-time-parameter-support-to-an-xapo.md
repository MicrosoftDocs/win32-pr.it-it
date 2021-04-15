---
description: È possibile aggiungere il supporto dei parametri della fase di esecuzione a un XAPO implementando l'interfaccia IXAPOParameters. Il supporto dei parametri in fase di esecuzione consente a un XAPO di modificare il comportamento in base ai parametri passati in fase di esecuzione.
ms.assetid: 13f974ec-fcf5-1749-e69d-88de79b7d82b
title: 'Procedura: Aggiungere supporto per i parametri di runtime a un oggetto di elaborazione audio di XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 582f51b3dfbdc6d31422494906d5f945f77ccb03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485180"
---
# <a name="how-to-add-run-time-parameter-support-to-an-xapo"></a><span data-ttu-id="764fc-104">Procedura: Aggiungere supporto per i parametri di runtime a un oggetto di elaborazione audio di XAudio2</span><span class="sxs-lookup"><span data-stu-id="764fc-104">How to: Add Run-time Parameter Support to an XAPO</span></span>

<span data-ttu-id="764fc-105">È possibile aggiungere il supporto dei parametri della fase di esecuzione a un XAPO implementando l'interfaccia [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) .</span><span class="sxs-lookup"><span data-stu-id="764fc-105">You can add run-time parameter support to an XAPO by implementing the [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) interface.</span></span> <span data-ttu-id="764fc-106">Il supporto dei parametri in fase di esecuzione consente a un XAPO di modificare il comportamento in base ai parametri passati in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="764fc-106">Run-time parameter support allows an XAPO to change its behavior based on the parameters passed to it at run time.</span></span>

1.  <span data-ttu-id="764fc-107">Seguire i passaggi in [procedura: creare un XAPO](how-to--create-an-xapo.md).</span><span class="sxs-lookup"><span data-stu-id="764fc-107">Follow the steps in [How to: Create an XAPO](how-to--create-an-xapo.md).</span></span>
2.  <span data-ttu-id="764fc-108">Modificare il XAPO in modo che derivi da [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) e [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase).</span><span class="sxs-lookup"><span data-stu-id="764fc-108">Change the XAPO to derive from [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) and [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase).</span></span>
3.  <span data-ttu-id="764fc-109">Aggiungere le chiamate ai metodi [**CXAPOParametersBase:: BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) e [**CXAPOParametersBase:: EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) all'implementazione di [**IXAPO::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process).</span><span class="sxs-lookup"><span data-stu-id="764fc-109">Add calls to the methods [**CXAPOParametersBase::BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) and [**CXAPOParametersBase::EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) to the implementation of [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process).</span></span>

    > [!Note]  
    > <span data-ttu-id="764fc-110">L'aggiunta di questi metodi a [IXAPO::P rocess](how-to--build-a-basic-audio-processing-graph.md) consente a [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) di preservare le copie dei parametri degli effetti in uno stato thread-safe.</span><span class="sxs-lookup"><span data-stu-id="764fc-110">Adding these methods to [IXAPO::Process](how-to--build-a-basic-audio-processing-graph.md) allows [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) to keep its copies of the effect parameters in a thread-safe state.</span></span> <span data-ttu-id="764fc-111">Chiamare [**CXAPOParametersBase:: BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) all'inizio di [**IXAPO::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process)e [**CXAPOParametersBase:: EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) alla fine di **IXAPO::P rocess**.</span><span class="sxs-lookup"><span data-stu-id="764fc-111">Call [**CXAPOParametersBase::BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) at the beginning of [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process), and [**CXAPOParametersBase::EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) at the end of **IXAPO::Process**.</span></span>

     

4.  <span data-ttu-id="764fc-112">Aggiungere altro codice all'implementazione [**IXAPO::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) per modificarne il comportamento in base ai valori archiviati dal metodo [**separameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) .</span><span class="sxs-lookup"><span data-stu-id="764fc-112">Add more code to the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) implementation to change its behavior according to values stored by the [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) method.</span></span>

    > [!Note]  
    > <span data-ttu-id="764fc-113">L'aggiunta di codice al metodo [**IXAPO::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) per usare i parametri specificati da [**separameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) consente di modificare il comportamento di XAPO per tutta la sua vita.</span><span class="sxs-lookup"><span data-stu-id="764fc-113">Adding code to the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method to use the parameters specified by [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) allows the XAPO's behavior to be changed throughout its life.</span></span>

     

5.  <span data-ttu-id="764fc-114">Quando si crea un'istanza dell'effetto, allocare un buffer di tre strutture che rappresenteranno i parametri dell'effetto e passarlo al costruttore [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) .</span><span class="sxs-lookup"><span data-stu-id="764fc-114">When you create an instance of the effect, allocate a buffer of three of the structures that will represent the effect's parameters, and pass it to the [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) constructor.</span></span>

    > [!Note]  
    > <span data-ttu-id="764fc-115">L'istanza di [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) usa internamente questo buffer per gestire i parametri degli effetti passati quando [**si chiamano i parametri.**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters)</span><span class="sxs-lookup"><span data-stu-id="764fc-115">The [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) instance internally uses this buffer to manage effect parameters passed to it when you call [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters).</span></span> <span data-ttu-id="764fc-116">È necessario inizializzare tutti i blocchi di parametri di processo in *pParameterBlocks* con lo stesso valore predefinito prima di chiamare uno dei metodi [**IXAPO::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process), [**IXAPOParameters:: GetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-getparameters)e **IXAPOParameters::** SetValue.</span><span class="sxs-lookup"><span data-stu-id="764fc-116">You must initialize all the process parameter blocks in *pParameterBlocks* to the same default value before you call any of the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process), [**IXAPOParameters::GetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-getparameters), and **IXAPOParameters::SetParameters** methods.</span></span> <span data-ttu-id="764fc-117">Questa inizializzazione viene in genere gestita in [**IXAPO:: Initialize**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) o in [**IXAPO:: LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess).</span><span class="sxs-lookup"><span data-stu-id="764fc-117">Usually this initialization is handled in [**IXAPO::Initialize**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) or in [**IXAPO::LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess).</span></span>

     

## <a name="related-topics"></a><span data-ttu-id="764fc-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="764fc-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="764fc-119">Effetti audio</span><span class="sxs-lookup"><span data-stu-id="764fc-119">Audio Effects</span></span>](audio-effects.md)
</dt> <dt>

[<span data-ttu-id="764fc-120">Panoramica di XAPO</span><span class="sxs-lookup"><span data-stu-id="764fc-120">XAPO Overview</span></span>](xapo-overview.md)
</dt> </dl>

 

 
