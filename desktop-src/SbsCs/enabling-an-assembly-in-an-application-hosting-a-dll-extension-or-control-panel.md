---
description: Se l'applicazione ospita una DLL di terze parti, un'estensione, un plug-in o un pannello di controllo, potrebbe essere necessario abilitare un assembly nell'applicazione&\# 8212; senza abilitare anche questo assembly per i componenti ospitati.
ms.assetid: 832957ca-82fc-4600-b469-512621dde921
title: Abilitazione di un assembly in un'applicazione che ospita una DLL, un'estensione o un pannello di controllo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b04dd19b18c2cdce4783be47333b9afe53dd1ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313307"
---
# <a name="enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel"></a><span data-ttu-id="b0ad0-103">Abilitazione di un assembly in un'applicazione che ospita una DLL, un'estensione o un pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="b0ad0-103">Enabling an Assembly in an Application Hosting a DLL, Extension, or Control Panel</span></span>

<span data-ttu-id="b0ad0-104">Se l'applicazione ospita una DLL di terze parti, un'estensione, un plug-in o un pannello di controllo, è possibile abilitare un assembly nell'applicazione, senza abilitare anche questo assembly per i componenti ospitati.</span><span class="sxs-lookup"><span data-stu-id="b0ad0-104">If your application hosts a third-party DLL, extension, plug-in, or control panel, you may want to enable an assembly in your application—without also enabling this assembly for the hosted components.</span></span> <span data-ttu-id="b0ad0-105">Questo può essere il caso in cui un componente ospitato richiede modifiche al codice per usare l'assembly.</span><span class="sxs-lookup"><span data-stu-id="b0ad0-105">This can be the case when a hosted component requires code changes to use the assembly.</span></span> <span data-ttu-id="b0ad0-106">Lo sviluppatore dell'applicazione potrebbe non essere in grado di apportare modifiche a questi componenti di terze parti.</span><span class="sxs-lookup"><span data-stu-id="b0ad0-106">As the application developer, you may be unable to make changes to these third-party components.</span></span> <span data-ttu-id="b0ad0-107">In questo caso, è necessario seguire la procedura descritta in questa sezione in modo che l'applicazione possa usare l'assembly senza influire sui componenti ospitati.</span><span class="sxs-lookup"><span data-stu-id="b0ad0-107">In this case, you should follow the procedure described in this section so that your application can use the assembly without affecting the hosted components.</span></span>

-   <span data-ttu-id="b0ad0-108">Per abilitare un assembly in un'applicazione senza influire sulle dll, le estensioni, i plug-in o i pannelli di controllo ospitati, un manifesto che descrive la dipendenza dell'applicazione dall'assembly deve essere incluso nell'applicazione come risorsa.</span><span class="sxs-lookup"><span data-stu-id="b0ad0-108">To enable an assembly in an application without affecting any hosted DLLs, extensions, plug-ins, or control panels, a manifest that describes the application's dependence on the assembly should be included in the application as a resource.</span></span> <span data-ttu-id="b0ad0-109">I componenti ospitati che non sono abilitati con l'assembly non devono includere manifesti che descrivono questa dipendenza.</span><span class="sxs-lookup"><span data-stu-id="b0ad0-109">The hosted components that are not being enabled with the assembly should not include manifests describing this dependency.</span></span>
-   <span data-ttu-id="b0ad0-110">Per abilitare un assembly in un'applicazione e le relative dll, estensioni, plug-in o pannelli di controllo ospitati, includere i manifesti come risorse nell'applicazione e nei relativi componenti ospitati.</span><span class="sxs-lookup"><span data-stu-id="b0ad0-110">To enable an assembly in an application and its hosted DLLs, extensions, plug-ins, or control panels, include manifests as resources in both the application and its hosted components.</span></span> <span data-ttu-id="b0ad0-111">I manifesti inclusi nell'applicazione e nei componenti ospitati dovrebbero descrivere una dipendenza dall'assembly.</span><span class="sxs-lookup"><span data-stu-id="b0ad0-111">The manifests included in the application and in the hosted components should each describe a dependence on the assembly.</span></span> <span data-ttu-id="b0ad0-112">In genere, lo sviluppatore dell'applicazione aggiunge un manifesto all'applicazione e lo sviluppatore di componenti ospitati aggiunge un manifesto alla DLL, all'estensione, al plug-in o al pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="b0ad0-112">Typically, the application developer adds a manifest to the application and the hosted component developer adds a manifest to the DLL, extension, plug-in, or control panel.</span></span>

<span data-ttu-id="b0ad0-113">Il metodo seguente può essere usato per aggiungere un manifesto a un'applicazione o a un componente ospitato che è una DLL, un'estensione, un plug-in o un pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="b0ad0-113">The following method can be used to add a manifest to an application or a hosted component that is a DLL, extension, plug-in, or control panel.</span></span>

<span data-ttu-id="b0ad0-114">**Per abilitare un assembly in un'applicazione o in un componente ospitato.**</span><span class="sxs-lookup"><span data-stu-id="b0ad0-114">**To enable an assembly in an application or hosted component.**</span></span>

1.  <span data-ttu-id="b0ad0-115">Creare un manifesto che descriva la dipendenza dell'applicazione o dell'estensione nell'assembly.</span><span class="sxs-lookup"><span data-stu-id="b0ad0-115">Author a manifest that describes the dependence of the application or extension on the assembly.</span></span>

    <span data-ttu-id="b0ad0-116">È ad esempio possibile creare il manifesto per "YourApplication" copiando il manifesto di esempio seguente e sostituendo i valori corretti per **assemblyIdentity**, **processorArchitecture** e **Description**.</span><span class="sxs-lookup"><span data-stu-id="b0ad0-116">For example, the manifest for "YourApplication" can be created by copying the following sample manifest and substituting correct values for **assemblyIdentity**, **processorArchitecture**, and **description**.</span></span> <span data-ttu-id="b0ad0-117">Impostare il valore di **processorArchitecture** su x86 se si compila su una piattaforma a 32 bit e su ia64 se si compila su una piattaforma a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="b0ad0-117">Set the value of **processorArchitecture** to x86 if building on a 32-bit platform and to ia64 if building on a 64-bit platform.</span></span> <span data-ttu-id="b0ad0-118">L'elemento **Description** contiene una descrizione dell'opzione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b0ad0-118">The **description** element contains an option description of the application.</span></span> <span data-ttu-id="b0ad0-119">Per ulteriori informazioni sul formato del manifesto, vedere [manifesti dell'applicazione](application-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="b0ad0-119">For more information about the manifest format, see [application manifests](application-manifests.md).</span></span>

    ``` syntax
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="x86"
        name="YourCompanyName.YourDivision.YourApp"
        type="win32"
    />
    <description>Your app description here</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Proseware.Research.SampleAssembly"
                version="6.0.0.0"
                processorArchitecture="X86"
                publicKeyToken="0000000000000000"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

2.  <span data-ttu-id="b0ad0-120">Creare una risorsa nell'applicazione o nell'estensione di tipo RT \_ manifest ID 2.</span><span class="sxs-lookup"><span data-stu-id="b0ad0-120">Create a resource in the application or extension of type RT\_MANIFEST id 2.</span></span>

    <span data-ttu-id="b0ad0-121">Ad esempio, se il nome dell'applicazione è YourApp, l'applicazione deve contenere quanto segue:</span><span class="sxs-lookup"><span data-stu-id="b0ad0-121">For example, if the application's name is YourApp, the application should contain the following:</span></span>

    ``` syntax
    #define MANIFEST_RESOURCE_ID 2
    MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.manifest"
    ```

3.  <span data-ttu-id="b0ad0-122">Compilare l'applicazione con il flag di \_ Abilitazione di-DISOLATION \_ o inserire questa istruzione prima dell' \# istruzione include "Windows. h".</span><span class="sxs-lookup"><span data-stu-id="b0ad0-122">Compile the application with the -DISOLATION\_AWARE\_ENABLED flag, or insert this statement before the \#include "Windows.h" statement.</span></span> <span data-ttu-id="b0ad0-123">Nel caso di un'applicazione con più moduli, il flag-DISOLATION \_ Aware \_ Enabled è obbligatorio in tutti i moduli.</span><span class="sxs-lookup"><span data-stu-id="b0ad0-123">In the case of an application with multiple modules, the -DISOLATION\_AWARE\_ENABLED flag is required on all modules.</span></span>

    ``` syntax
    #define ISOLATION_AWARE_ENABLED 1
    ```

4.  <span data-ttu-id="b0ad0-124">Eseguire un test per assicurarsi che gli assembly usati dall'applicazione funzionino correttamente nell'applicazione e nel componente ospitato.</span><span class="sxs-lookup"><span data-stu-id="b0ad0-124">Test to ensure that assemblies that are used by the application work correctly in the application and hosted component.</span></span>

<span data-ttu-id="b0ad0-125">Per ulteriori informazioni sull'aggiunta di un assembly alle applicazioni senza estensioni, vedere [Abilitazione di un assembly in un'applicazione senza estensioni](enabling-an-assembly-in-an-application-without-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="b0ad0-125">For more information about adding an assembly to applications without extensions, see [Enabling an Assembly in an Application Without Extensions](enabling-an-assembly-in-an-application-without-extensions.md).</span></span>

 

 



