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
# <a name="access-uefi-firmware-variables-from-a-universal-windows-app"></a>Accedere alle variabili del firmware UEFI da un'app di Windows universale

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Come accedere alle variabili del firmware di Unified Extensible Firmware Interface (UEFI) da un'app di Windows universale.

A partire da Windows 10, versione 1803, le app di Windows universale possono usare [**GetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariablea) e [**SetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariablea) (e le relative varianti "ex") per accedere alle variabili del firmware UEFI eseguendo le operazioni seguenti:

-   Dichiarare la funzionalità personalizzata **Microsoft. firmwareRead \_ cw5n1h2txyewy** nel manifesto per leggere una variabile del firmware e/o la funzionalità **Microsoft. firmwareWrite \_ cw5n1h2txyewy** per scrivere una variabile del firmware.
-   Dichiarare inoltre la funzionalità limitata **protectedApp** nel manifesto dell'applicazione.
-   Ad esempio, le aggiunte del manifesto dell'app seguenti consentono all'app di Windows universale di leggere le variabili del firmware:

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

-   Impostare l'opzione del linker **/INTEGRITYCHECK**, per tutte le configurazioni del progetto, prima di inviare l'app al Microsoft Store. Ciò garantisce che l'app venga avviata come app protetta. Per informazioni dettagliate, vedere [/INTEGRITYCHECK (Richiedi controllo della firma)](/cpp/build/reference/integritycheck-require-signature-check) .
-   Ottenere un file [descrittore di funzionalità personalizzato](/windows-hardware/drivers/devapps/creating-a-custom-capability-to-pair-driver-with-hsa#preparing-the-signed-custom-capability-descriptor-sccd-file) (SCCD) firmato da Microsoft. Vedere [creazione di una funzionalità personalizzata per associare un driver a un'app di supporto hardware (HSA)](/windows-hardware/drivers/devapps/creating-a-custom-capability-to-pair-driver-with-hsa) e [usare una funzionalità personalizzata per associare un'app di supporto hardware (HSA) a un driver](/windows-hardware/drivers/devapps/using-a-custom-capability-to-pair-hsa-with-driver) per informazioni su come ottenere un file SCCD firmato da Microsoft, come creare un pacchetto con l'app e come abilitare la modalità sviluppatore. Di seguito è riportato un esempio di file SSCD dell' [esempio CustomCapability](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/CustomCapability):
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

    

-   Inviare l'app al Microsoft Store per ottenerne la firma. Per finalità di sviluppo, è possibile ignorare la firma abilitando la firma di test nel database di configurazione di avvio. Per informazioni dettagliate, vedere [l'opzione di configurazione di avvio TESTSIGNING](/windows-hardware/drivers/install/the-testsigning-boot-configuration-option) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzionalità speciali e con restrizioni](/windows/uwp/packaging/app-capability-declarations#special-and-restricted-capabilities)
</dt> <dt>

[**GetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariablea)
</dt> <dt>

[**GetFirmwareEnvironmentVariableEx**](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariableexa)
</dt> <dt>

[**SetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariablea)
</dt> <dt>

[**SetFirmwareEnvironmentVariableEx**](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariableexa)
</dt> <dt>

[Accedere alle informazioni di SMBIOS da un'app di Windows universale](access-smbios-information-from-a-universal-windows-app.md)
</dt> </dl>

 

 
