---
description: Come accedere alle variabili del firmware di Unified Extensible Firmware Interface (UEFI) da un'app di Windows universale.
ms.assetid: 4131CCED-3B76-4569-B0A7-111E4E9215EF
title: Accedere alle variabili del firmware UEFI da un'app di Windows universale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 738b7042b4c650c74115760e6dcd2e93131d6780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313269"
---
# <a name="access-uefi-firmware-variables-from-a-universal-windows-app"></a><span data-ttu-id="0321e-103">Accedere alle variabili del firmware UEFI da un'app di Windows universale</span><span class="sxs-lookup"><span data-stu-id="0321e-103">Access UEFI firmware variables from a Universal Windows App</span></span>

<span data-ttu-id="0321e-104">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="0321e-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0321e-105">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="0321e-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0321e-106">Come accedere alle variabili del firmware di Unified Extensible Firmware Interface (UEFI) da un'app di Windows universale.</span><span class="sxs-lookup"><span data-stu-id="0321e-106">How to access Unified Extensible Firmware Interface (UEFI) firmware variables from a Universal Windows app.</span></span>

<span data-ttu-id="0321e-107">A partire da Windows 10, versione 1803, le app di Windows universale possono usare [**GetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariablea) e [**SetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariablea) (e le relative varianti "ex") per accedere alle variabili del firmware UEFI eseguendo le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="0321e-107">Starting with Windows 10, version 1803, Universal Windows apps can use [**GetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariablea) and [**SetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariablea) (and their 'ex' variants) to access UEFI firmware variables by doing the following:</span></span>

-   <span data-ttu-id="0321e-108">Dichiarare la funzionalità personalizzata **Microsoft. firmwareRead \_ cw5n1h2txyewy** nel manifesto per leggere una variabile del firmware e/o la funzionalità **Microsoft. firmwareWrite \_ cw5n1h2txyewy** per scrivere una variabile del firmware.</span><span class="sxs-lookup"><span data-stu-id="0321e-108">Declare the **Microsoft.firmwareRead\_cw5n1h2txyewy** custom capability in the manifest to read a firmware variable, and/or the **Microsoft.firmwareWrite\_cw5n1h2txyewy** capability to write a firmware variable.</span></span>
-   <span data-ttu-id="0321e-109">Dichiarare inoltre la funzionalità limitata **protectedApp** nel manifesto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0321e-109">Also declare the **protectedApp** restricted capability in the app manifest.</span></span>
-   <span data-ttu-id="0321e-110">Ad esempio, le aggiunte del manifesto dell'app seguenti consentono all'app di Windows universale di leggere le variabili del firmware:</span><span class="sxs-lookup"><span data-stu-id="0321e-110">For example, the following app manifest additions allow the Universal Windows app to read firmware variables:</span></span>

    ``` syntax
    <Package
      ...
      xmlns:uap4=http://schemas.microsoft.com/appx/manifest/uap/windows10/4
      xmlns:rescap="http://schemas.microsoft.com/appx/manifest/foundation/windows10/restrictedcapabilities"
      IgnorableNamespaces="uap mp uap4 rescap">  
      ...
      <Capabilities>
        <rescap:Capability Name="protectedApp"/>
        <uap4:CustomCapability Name="microsoft.firmwareRead_cw5n1h2txyewy" />
      </Capabilities>
    </Package>
    ```

<!-- -->

-   <span data-ttu-id="0321e-111">Impostare l'opzione del linker **/INTEGRITYCHECK**, per tutte le configurazioni del progetto, prima di inviare l'app al Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="0321e-111">Set the linker option **/INTEGRITYCHECK**, for all project configurations, before submitting the app to the Microsoft Store.</span></span> <span data-ttu-id="0321e-112">Ciò garantisce che l'app venga avviata come app protetta.</span><span class="sxs-lookup"><span data-stu-id="0321e-112">This ensures that the app will be launched as a protected app.</span></span> <span data-ttu-id="0321e-113">Per informazioni dettagliate, vedere [/INTEGRITYCHECK (Richiedi controllo della firma)](/cpp/build/reference/integritycheck-require-signature-check) .</span><span class="sxs-lookup"><span data-stu-id="0321e-113">See [/INTEGRITYCHECK (Require Signature Check)](/cpp/build/reference/integritycheck-require-signature-check) for details.</span></span>
-   <span data-ttu-id="0321e-114">Ottenere un file [descrittore di funzionalità personalizzato](/windows-hardware/drivers/devapps/creating-a-custom-capability-to-pair-driver-with-hsa#preparing-the-signed-custom-capability-descriptor-sccd-file) (SCCD) firmato da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0321e-114">Obtain a [Signed Custom Capability Descriptor](/windows-hardware/drivers/devapps/creating-a-custom-capability-to-pair-driver-with-hsa#preparing-the-signed-custom-capability-descriptor-sccd-file) (SCCD) file from Microsoft.</span></span> <span data-ttu-id="0321e-115">Vedere [creazione di una funzionalità personalizzata per associare un driver a un'app di supporto hardware (HSA)](/windows-hardware/drivers/devapps/creating-a-custom-capability-to-pair-driver-with-hsa) e [usare una funzionalità personalizzata per associare un'app di supporto hardware (HSA) a un driver](/windows-hardware/drivers/devapps/using-a-custom-capability-to-pair-hsa-with-driver) per informazioni su come ottenere un file SCCD firmato da Microsoft, come creare un pacchetto con l'app e come abilitare la modalità sviluppatore.</span><span class="sxs-lookup"><span data-stu-id="0321e-115">See [Creating a custom capability to pair a driver with a Hardware Support App (HSA)](/windows-hardware/drivers/devapps/creating-a-custom-capability-to-pair-driver-with-hsa) and [Using a custom capability to pair a Hardware Support App (HSA) with a driver](/windows-hardware/drivers/devapps/using-a-custom-capability-to-pair-hsa-with-driver) for information about how to obtain signed SCCD file from Microsoft, how to package it with your app, and how to enable developer mode.</span></span> <span data-ttu-id="0321e-116">Di seguito è riportato un esempio di file SSCD dell' [esempio CustomCapability](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/CustomCapability):</span><span class="sxs-lookup"><span data-stu-id="0321e-116">Here is an example SSCD file from the [CustomCapability sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/CustomCapability):</span></span>
    ```XML
    <?xml version="1.0" encoding="utf-8"?>
    <CustomCapabilityDescriptor xmlns="http://schemas.microsoft.com/appx/2016/sccd" xmlns:s="http://schemas.microsoft.com/appx/2016/sccd">
      <CustomCapabilities>
        <CustomCapability Name="microsoft.hsaTestCustomCapability_q536wpkpf5cy2"></CustomCapability>
        <CustomCapability Name="microsoft.firmwareRead_cw5n1h2txyewy"></CustomCapability>
      </CustomCapabilities>
      <AuthorizedEntities>
        <AuthorizedEntity AppPackageFamilyName="Microsoft.SDKSamples.CustomCapability.CPP_8wekyb3d8bbwe" CertificateSignatureHash="ca9fc964db7e0c2938778f4559946833e7a8cfde0f3eaa07650766d4764e86c4"></AuthorizedEntity>
        <AuthorizedEntity AppPackageFamilyName="Microsoft.SDKSamples.CustomCapability.CPP_8wekyb3d8bbwe" CertificateSignatureHash="279cd652c4e252bfbe5217ac722205d7729ba409148cfa9e6d9e5b1cb94eaff1"></AuthorizedEntity>
      </AuthorizedEntities>
      <Catalog>xxxx</Catalog>
    </CustomCapabilityDescriptor>
    ```

    

-   <span data-ttu-id="0321e-117">Inviare l'app al Microsoft Store per ottenerne la firma.</span><span class="sxs-lookup"><span data-stu-id="0321e-117">Submit the app to the Microsoft Store to get it signed.</span></span> <span data-ttu-id="0321e-118">Per finalità di sviluppo, è possibile ignorare la firma abilitando la firma di test nel database di configurazione di avvio.</span><span class="sxs-lookup"><span data-stu-id="0321e-118">For development purposes, you can skip signing by enabling test-signing in the boot configuration database (bcd).</span></span> <span data-ttu-id="0321e-119">Per informazioni dettagliate, vedere [l'opzione di configurazione di avvio TESTSIGNING](/windows-hardware/drivers/install/the-testsigning-boot-configuration-option) .</span><span class="sxs-lookup"><span data-stu-id="0321e-119">See [The TESTSIGNING Boot Configuration Option](/windows-hardware/drivers/install/the-testsigning-boot-configuration-option) for details.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0321e-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0321e-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0321e-121">Funzionalità speciali e con restrizioni</span><span class="sxs-lookup"><span data-stu-id="0321e-121">Special and restricted capabilities</span></span>](/windows/uwp/packaging/app-capability-declarations#special-and-restricted-capabilities)
</dt> <dt>

[<span data-ttu-id="0321e-122">**GetFirmwareEnvironmentVariable**</span><span class="sxs-lookup"><span data-stu-id="0321e-122">**GetFirmwareEnvironmentVariable**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariablea)
</dt> <dt>

[<span data-ttu-id="0321e-123">**GetFirmwareEnvironmentVariableEx**</span><span class="sxs-lookup"><span data-stu-id="0321e-123">**GetFirmwareEnvironmentVariableEx**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariableexa)
</dt> <dt>

[<span data-ttu-id="0321e-124">**SetFirmwareEnvironmentVariable**</span><span class="sxs-lookup"><span data-stu-id="0321e-124">**SetFirmwareEnvironmentVariable**</span></span>](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariablea)
</dt> <dt>

[<span data-ttu-id="0321e-125">**SetFirmwareEnvironmentVariableEx**</span><span class="sxs-lookup"><span data-stu-id="0321e-125">**SetFirmwareEnvironmentVariableEx**</span></span>](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariableexa)
</dt> <dt>

[<span data-ttu-id="0321e-126">Accedere alle informazioni di SMBIOS da un'app di Windows universale</span><span class="sxs-lookup"><span data-stu-id="0321e-126">Access SMBIOS information from a Universal Windows App</span></span>](access-smbios-information-from-a-universal-windows-app.md)
</dt> </dl>

 

 
