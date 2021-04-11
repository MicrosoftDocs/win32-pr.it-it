---
description: 'I metodi IWbemServices:: ExecMethod o ExecMethodAsync richiedono la \_ \_ classe di sistema Parameters come contenitore in pInParams se il metodo in esecuzione contiene argomenti di input.'
ms.assetid: 17b72ceb-e730-4176-aa4d-189d0b6acc8b
ms.tgt_platform: multiple
title: Creazione di oggetti Parameters in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c200958f4ad00ced5455462e7a2909ac6a58cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226953"
---
# <a name="creating-parameters-objects-in-c"></a><span data-ttu-id="bf750-103">Creazione di oggetti Parameters in C++</span><span class="sxs-lookup"><span data-stu-id="bf750-103">Creating Parameters Objects in C++</span></span>

<span data-ttu-id="bf750-104">I metodi [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) o [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) richiedono la classe di sistema [**\_ \_ Parameters**](--parameters.md) come contenitore in *pInParams* se il metodo in esecuzione contiene argomenti di input.</span><span class="sxs-lookup"><span data-stu-id="bf750-104">The [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) or [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) methods require the [**\_\_PARAMETERS**](--parameters.md) system class as a container in *pInParams* if the method they are executing has any input arguments.</span></span>

<span data-ttu-id="bf750-105">Nella procedura seguente viene descritto come creare un'istanza della classe di sistema [**\_ \_ Parameters**](--parameters.md) per mantenere le informazioni sui parametri.</span><span class="sxs-lookup"><span data-stu-id="bf750-105">The following procedure describes how to create an instance of the [**\_\_PARAMETERS**](--parameters.md) system class to hold parameter information.</span></span>

<span data-ttu-id="bf750-106">**Per creare un'istanza di \_ \_ Parameters**</span><span class="sxs-lookup"><span data-stu-id="bf750-106">**To create an instance of \_\_PARAMETERS**</span></span>

1.  <span data-ttu-id="bf750-107">Determinare il percorso della classe per la classe che contiene la definizione del metodo.</span><span class="sxs-lookup"><span data-stu-id="bf750-107">Determine the class path for the class containing the method definition.</span></span>
2.  <span data-ttu-id="bf750-108">Utilizzando il percorso della classe e il puntatore [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) passati da [**IWbemProviderInit:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize), chiamare [**IWbemClassObject:: GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) per recuperare le classi di parametri di input e output.</span><span class="sxs-lookup"><span data-stu-id="bf750-108">Using the class path and the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer passed in from [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize), call [**IWbemClassObject::GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) to retrieve the input and output parameter classes.</span></span>

    <span data-ttu-id="bf750-109">Il metodo [**GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) restituisce un puntatore [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) per l'accesso a ognuna di queste classi.</span><span class="sxs-lookup"><span data-stu-id="bf750-109">The [**GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) method returns an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer for accessing each of these classes.</span></span>

3.  <span data-ttu-id="bf750-110">Utilizzando il puntatore [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) per la classe output, chiamare [**IWbemClassObject:: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) per creare un'istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="bf750-110">Using the [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer for the output class, call [**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) to create an instance of the class.</span></span>
4.  <span data-ttu-id="bf750-111">Popolare l'istanza della classe impostando le proprietà che corrispondono ai valori di output e, se è presente un valore restituito per il metodo, la proprietà [returnValue](creating-a-method.md) .</span><span class="sxs-lookup"><span data-stu-id="bf750-111">Populate the class instance by setting the properties that correspond to the output values and, if there is a return value for the method, the [ReturnValue](creating-a-method.md) property.</span></span>
5.  <span data-ttu-id="bf750-112">Passare di nuovo l'istanza dei [**\_ \_ parametri**](--parameters.md) al chiamante tramite il metodo [**IWbemObjectSink:: indica**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) .</span><span class="sxs-lookup"><span data-stu-id="bf750-112">Pass the [**\_\_PARAMETERS**](--parameters.md) instance back to the caller through the [**IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) method.</span></span>

<span data-ttu-id="bf750-113">Dopo che un provider di metodi ha determinato che i parametri di input sono corretti, il metodo a cui fa riferimento *strMethodName* potrebbe comunque essere superato o non riuscito.</span><span class="sxs-lookup"><span data-stu-id="bf750-113">After a method provider determines that the input parameters are correct, the method pointed to by *strMethodName* might still pass or fail.</span></span> <span data-ttu-id="bf750-114">Alcuni provider di metodi generano un secondo thread per implementare il metodo in modo che l'esito positivo o negativo effettivo del metodo venga segnalato al chiamante tramite [**IWbemObjectSink:: sestatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus).</span><span class="sxs-lookup"><span data-stu-id="bf750-114">Some method providers spawn a second thread to implement the method so that the method's actual success or failure ends up being reported to the caller through [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus).</span></span> <span data-ttu-id="bf750-115">Si noti che **IWbemObjectSink::** SetValue non riceve il codice restituito del metodo del provider.</span><span class="sxs-lookup"><span data-stu-id="bf750-115">Note that **IWbemObjectSink::SetStatus** does not receive the return code of the provider method.</span></span> <span data-ttu-id="bf750-116">Tuttavia, riceve il codice restituito del meccanismo effettivo di restituzione della chiamata ed è utile solo per verificare se la chiamata si è verificata o se non è riuscita per motivi meccanici.</span><span class="sxs-lookup"><span data-stu-id="bf750-116">However, it receives the return code of the actual call-return mechanism, and is only useful for verifying that the call occurred or that it failed for mechanical reasons.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf750-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bf750-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf750-118">Chiamata a un metodo</span><span class="sxs-lookup"><span data-stu-id="bf750-118">Calling a Method</span></span>](calling-a-method.md)
</dt> <dt>

[<span data-ttu-id="bf750-119">**IWbemCallResult::GetResultObject**</span><span class="sxs-lookup"><span data-stu-id="bf750-119">**IWbemCallResult::GetResultObject**</span></span>](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getresultobject)
</dt> <dt>

[<span data-ttu-id="bf750-120">**IWbemServices:: ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="bf750-120">**IWbemServices::ExecMethodAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
</dt> <dt>

[<span data-ttu-id="bf750-121">**IWbemServices:: ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="bf750-121">**IWbemServices::ExecMethod**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod)
</dt> </dl>

 

 



