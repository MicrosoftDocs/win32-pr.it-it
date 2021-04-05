---
title: Programmazione di ADSI con Java/COM
description: Utilizzando Microsoft Virtual Machine per Java (Microsoft VM) e il compilatore Java Microsoft, è possibile accedere a tutte le funzionalità ADSI esposte tramite i componenti COM ADSI, da un'applicazione Java/COM.
ms.assetid: eda516b6-0f89-464f-a9d2-9bb4ca70fda5
ms.tgt_platform: multiple
keywords:
- Programmazione di ADSI con AD Java/COM
- ADSI ADSI, uso, programmazione Java/COM per
- ADSI ADSI, codice di esempio Java
- ADSI ADSI, esempio di codice Java, associazione a un oggetto ADSI e richiamo di metodi su tale oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6899804208f9899823f266bc941bcf3c2dec372
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855266"
---
# <a name="programming-adsi-with-javacom"></a><span data-ttu-id="da6f3-107">Programmazione di ADSI con Java/COM</span><span class="sxs-lookup"><span data-stu-id="da6f3-107">Programming ADSI with Java/COM</span></span>

<span data-ttu-id="da6f3-108">Utilizzando Microsoft Virtual Machine per Java (Microsoft VM) e il compilatore Java Microsoft, è possibile accedere a tutte le funzionalità ADSI esposte tramite i componenti COM ADSI, da un'applicazione Java/COM.</span><span class="sxs-lookup"><span data-stu-id="da6f3-108">Using the Microsoft virtual machine for Java (Microsoft VM) and Microsoft Java Compiler, you have access to all the ADSI features exposed through any ADSI COM components, from a Java/COM application.</span></span> <span data-ttu-id="da6f3-109">Nell'esempio di codice Java riportato di seguito vengono illustrati gli elementi necessari per eseguire l'associazione a un oggetto ADSI e richiamare metodi su tale oggetto.</span><span class="sxs-lookup"><span data-stu-id="da6f3-109">The following Java code example shows the elements necessary to bind to an ADSI object and invoke methods on that object.</span></span> <span data-ttu-id="da6f3-110">Le funzioni e i metodi degli oggetti dell'API ADSI richiesti vengono esposti tramite Activeds.dll.</span><span class="sxs-lookup"><span data-stu-id="da6f3-110">The required ADSI API functions and object methods are exposed through Activeds.dll.</span></span>


```C++
import activeds.*;       // ADSI COM Wrapper classes
import com.ms.com.*;     // to use _Guid data type in COM.

public Class SimpleADSI 
{
    IADs obj;
    String path = "WinNT://domain/machine,computer";
    _Guid riid = IADs.iid;
    public static void main(String args[]) 
    {
        try 
        {
            obj = (IADs)ADsGetObject(path, riid);
            System.out.println( "Object name:  " + obj.getName() );
            System.out.println( "      class:  " + obj.getSchema() );
            System.out.println( "    ADsPath:  " + obj.getADsPath() );
            System.out.println( "     parent:  " + obj.getParent() );
        }
        catch (Exception e) 
        {
            System.out.println( "SimpleADSI Error: " + e.toString() );
        }
    }

    /** @dll.import("activeds", ole) */
    private static native IUnknown ADsGetObject(String path, _Guid riid);
}
```



<span data-ttu-id="da6f3-111">L'argomento nella prima istruzione **Import** fa riferimento alle classi wrapper Java incluse in Activeds.dll.</span><span class="sxs-lookup"><span data-stu-id="da6f3-111">The argument in the first **import** statement refers to Java Wrapper classes packaged in Activeds.dll.</span></span> <span data-ttu-id="da6f3-112">Utilizzare Visual J++ per creare le classi wrapper e includerle nel progetto, attenendosi alla procedura riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="da6f3-112">Use Visual J++ to create the wrapper classes and include them in your project, following the procedure below.</span></span>

<span data-ttu-id="da6f3-113">**Per creare classi wrapper e includerle nel progetto**</span><span class="sxs-lookup"><span data-stu-id="da6f3-113">**To create wrapper classes and include them in your project**</span></span>

1.  <span data-ttu-id="da6f3-114">In un progetto Visual J++ selezionare **Aggiungi wrapper com...** dal menu **progetto** .</span><span class="sxs-lookup"><span data-stu-id="da6f3-114">In a Visual J++ project, select **Add Com Wrapper...** from the **Project** menu.</span></span>
2.  <span data-ttu-id="da6f3-115">Selezionare "Active DS Type Library" dalla finestra di dialogo **componenti installati:** dalla finestra di dialogo wrapper com.</span><span class="sxs-lookup"><span data-stu-id="da6f3-115">Select "Active DS Type Library" from the **Installed Components:** from the COM Wrappers dialog.</span></span> <span data-ttu-id="da6f3-116">Se la libreria dei tipi non è visualizzata nella casella di riepilogo, fare clic sul pulsante **Sfoglia** , passare alla directory in cui è archiviato activeds. tlb, quindi selezionare la libreria dei tipi.</span><span class="sxs-lookup"><span data-stu-id="da6f3-116">If the type library is not shown in the list box, click the **Browse...** button, navigate to the directory where Activeds.tlb is stored, and then select the type library.</span></span>

<span data-ttu-id="da6f3-117">Visual J++ crea il pacchetto activeds per le classi wrapper Java e include il pacchetto nel percorso predefinito del progetto.</span><span class="sxs-lookup"><span data-stu-id="da6f3-117">Visual J++ creates the activeds package for the Java Wrapper classes and include the package into the project's default path.</span></span> <span data-ttu-id="da6f3-118">Per ulteriori informazioni, vedere il pacchetto activeds nel riquadro **Esplora progetti** della finestra Visual J++.</span><span class="sxs-lookup"><span data-stu-id="da6f3-118">For more information, see the activeds package in the **Project Explore** pane on the Visual J++ window.</span></span>

<span data-ttu-id="da6f3-119">Per ottenere un oggetto ADSI che non può essere cocreato, usare una delle funzioni dell'API ADSI esposte, ad esempio, [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) o [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject), che vengono anche assemblate in Activeds.dll.</span><span class="sxs-lookup"><span data-stu-id="da6f3-119">To get an ADSI object that cannot be cocreated, use one of the exposed ADSI API functions, for example, [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) or [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject), which are also packaged in Activeds.dll.</span></span> <span data-ttu-id="da6f3-120">Microsoft J/Direct fornisce l'accesso a queste e ad altre API native.</span><span class="sxs-lookup"><span data-stu-id="da6f3-120">Microsoft J/Direct provides access to these and other native APIs.</span></span> <span data-ttu-id="da6f3-121">Questa operazione è illustrata nelle ultime due righe dell'esempio di codice, sopra.</span><span class="sxs-lookup"><span data-stu-id="da6f3-121">This is illustrated by the last two lines of the code example, above.</span></span>

<span data-ttu-id="da6f3-122">Quando si esegue la compilazione, assicurarsi che l'estensione del linguaggio Microsoft sia abilitata.</span><span class="sxs-lookup"><span data-stu-id="da6f3-122">When compiling, ensure that Microsoft Language Extension is enabled.</span></span> <span data-ttu-id="da6f3-123">A tale scopo, selezionare **<project> Proprietà** dal menu **progetto** nella finestra del progetto Visual J++.</span><span class="sxs-lookup"><span data-stu-id="da6f3-123">To do this, select **<project> Properties...** from the **Project** menu in the Visual J++ project window.</span></span> <span data-ttu-id="da6f3-124">Quindi, fare clic sulla scheda **Compila** nella finestra di dialogo **<project> proprietà** .</span><span class="sxs-lookup"><span data-stu-id="da6f3-124">Then, click the **Compile** tab in the **<project> Properties** dialog.</span></span> <span data-ttu-id="da6f3-125">Deselezionare la casella di controllo **Disabilita estensioni Microsoft Language** .</span><span class="sxs-lookup"><span data-stu-id="da6f3-125">Clear the **Disable Microsoft Language Extensions** check box.</span></span> <span data-ttu-id="da6f3-126">Se si esegue la compilazione dalla riga di comando, usare l'opzione "/x-", ad esempio:</span><span class="sxs-lookup"><span data-stu-id="da6f3-126">If compiling from the command line, use "/x-" switch, for example:</span></span>

<span data-ttu-id="da6f3-127">**JVC/x-SimpleADSI. Java**</span><span class="sxs-lookup"><span data-stu-id="da6f3-127">**jvc /x- SimpleADSI.java**</span></span>

<span data-ttu-id="da6f3-128">Infine, per consentire alla macchina virtuale di caricare il componente COM, la libreria di collegamento dinamico (DLL) deve essere visibile sul percorso di sistema.</span><span class="sxs-lookup"><span data-stu-id="da6f3-128">Finally, in order for the virtual machine to load the COM component, the dynamic-link library (DLL) must be visible on the system path.</span></span> <span data-ttu-id="da6f3-129">Se viene restituito un errore "Java. lang. UnsatisfiedLinkError", impostare il percorso in modo da includere il percorso che contiene la DLL richiesta.</span><span class="sxs-lookup"><span data-stu-id="da6f3-129">If a "java.lang.UnsatisfiedLinkError" error is returned, set the PATH to include the path that contains the required DLL.</span></span> <span data-ttu-id="da6f3-130">Se ad esempio Activeds.dll è stato installato in c: \\ ADSI \\ lib, eseguire il comando seguente dalla riga di comando:</span><span class="sxs-lookup"><span data-stu-id="da6f3-130">For example, if Activeds.dll has been installed in c:\\adsi\\lib, issue the following command from the command line:</span></span>

<span data-ttu-id="da6f3-131">**Imposta percorso =% PATH%; c: \\ ADSI \\ lib**</span><span class="sxs-lookup"><span data-stu-id="da6f3-131">**set PATH = %PATH%; c:\\adsi\\lib**</span></span>

 

 




