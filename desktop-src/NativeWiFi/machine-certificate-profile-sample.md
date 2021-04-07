---
description: Usato per connettersi a una rete che usa certificati EAP-TLS (Extensible Authentication Protocol Transport Level Security) archiviati nel computer locale per l'autenticazione 802.1 X.
ms.assetid: 4cc4cbb7-963f-4771-8a3d-2a37058c9011
title: Esempio di profilo certificato del computer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad892d26a3ec401364fba79132db82c3fa6c4157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881462"
---
# <a name="machine-certificate-profile-sample"></a><span data-ttu-id="5f900-103">Esempio di profilo certificato del computer</span><span class="sxs-lookup"><span data-stu-id="5f900-103">Machine Certificate Profile Sample</span></span>

<span data-ttu-id="5f900-104">Questo esempio di profilo mostra un profilo di rete cablato usato per connettersi a una rete che usa certificati EAP-TLS (Extensible Authentication Protocol Transport Level Security) archiviati nel computer locale per l'autenticazione 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="5f900-104">This profile sample shows a wired network profile used to connect to a network that uses Extensible Authentication Protocol Transport Level Security (EAP-TLS) certificates stored on the local machine for 802.1X authentication.</span></span> <span data-ttu-id="5f900-105">Per visualizzare un profilo che usa i certificati EAP-TLS archiviati in una smart card, vedere [profilo di esempio del certificato della smart card](smart-card-certificate-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="5f900-105">To see a profile that uses EAP-TLS certificates stored on a smart card, see [Smart Card Certificate Sample Profile](smart-card-certificate-profile-sample.md).</span></span>

<span data-ttu-id="5f900-106">La configurazione EAPHost usata in questo esempio di profilo wireless è stata derivata dall'esempio delle [proprietà di connessione EAP-TLS](../eaphost/eap-tls-connection-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="5f900-106">The EAPHost configuration used in this wireless profile sample was derived from the [EAP-TLS Connection Properties](../eaphost/eap-tls-connection-properties.md) sample.</span></span>

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<LANProfile xmlns="https://www.microsoft.com/networking/LAN/profile/v1">
    <MSM>
        <security>
            <OneXEnforced>false</OneXEnforced>
            <OneXEnabled>true</OneXEnabled>
            <OneX xmlns="https://www.microsoft.com/networking/OneX/v1">
                <EAPConfig>
                    <EapHostConfig xmlns="https://www.microsoft.com/provisioning/EapHostConfig" 
                                   xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon" 
                                   xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodConfig">
 
                        <EapMethod>
                            <eapCommon:Type>13</eapCommon:Type> 
                            <eapCommon:AuthorId>0</eapCommon:AuthorId> 
                        </EapMethod>
                        <Config xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapConnectionPropertiesV1" 
                                xmlns:eapTls="https://www.microsoft.com/provisioning/EapTlsConnectionPropertiesV1">

                            <baseEap:Eap>
                                <baseEap:Type>13</baseEap:Type> 
                                <eapTls:EapType>
                                    <eapTls:CredentialsSource>
                                        <eapTls:CertificateStore />
                                    </eapTls:CredentialsSource>
                                    <eapTls:ServerValidation>
                                        <eapTls:DisableUserPromptForServerValidation>false</eapTls:DisableUserPromptForServerValidation> 
                                        <eapTls:ServerNames /> 
                                    </eapTls:ServerValidation> 
                                   <eapTls:DifferentUsername>false</eapTls:DifferentUsername> 
                               </eapTls:EapType>
                           </baseEap:Eap>
                       </Config>
                   </EapHostConfig>
                </EAPConfig>
            </OneX>
        </security>
    </MSM>
</LANProfile>
```

## <a name="related-topics"></a><span data-ttu-id="5f900-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5f900-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f900-108">Esempi di profili cablati</span><span class="sxs-lookup"><span data-stu-id="5f900-108">Wired Profile Samples</span></span>](wired-profile-samples.md)
</dt> </dl>

 

 
