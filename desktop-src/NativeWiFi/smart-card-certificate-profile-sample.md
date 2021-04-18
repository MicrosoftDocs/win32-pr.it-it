---
description: Utilizzato per connettersi a una rete che utilizza certificati EAP-TLS (Extensible Authentication Protocol Transport Level Security) archiviati in una smart card per l'autenticazione 802.1 X.
ms.assetid: cb6758fc-1cce-4e62-adf7-0976957a49b0
title: Esempio di profilo certificato smart card
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13373ea66a7ed93ad527715de9f32d4f72705be5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318972"
---
# <a name="smart-card-certificate-profile-sample"></a><span data-ttu-id="3680b-103">Esempio di profilo certificato smart card</span><span class="sxs-lookup"><span data-stu-id="3680b-103">Smart Card Certificate Profile Sample</span></span>

<span data-ttu-id="3680b-104">Questo esempio di profilo mostra un profilo di rete cablato usato per connettersi a una rete che usa certificati EAP-TLS (Extensible Authentication Protocol Transport Level Security) archiviati in una smart card per l'autenticazione 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="3680b-104">This profile sample shows a wired network profile used to connect to a network that uses Extensible Authentication Protocol Transport Level Security (EAP-TLS) certificates stored on a smart card for 802.1X authentication.</span></span> <span data-ttu-id="3680b-105">Per visualizzare un profilo che usa i certificati EAP-TLS archiviati nel computer locale, vedere l' [esempio relativo al profilo certificato del computer](machine-certificate-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="3680b-105">To see a profile that uses EAP-TLS certificates stored on the local machine, see [Machine Certificate Profile Sample](machine-certificate-profile-sample.md).</span></span>

<span data-ttu-id="3680b-106">La configurazione EAPHost usata in questo esempio di profilo wireless è stata derivata dall'esempio delle [proprietà di connessione EAP-TLS](../eaphost/eap-tls-connection-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="3680b-106">The EAPHost configuration used in this wireless profile sample was derived from the [EAP-TLS Connection Properties](../eaphost/eap-tls-connection-properties.md) sample.</span></span>

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
                                        <eapTls:SmartCard />
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

## <a name="related-topics"></a><span data-ttu-id="3680b-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3680b-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3680b-108">Esempi di profili cablati</span><span class="sxs-lookup"><span data-stu-id="3680b-108">Wired Profile Samples</span></span>](wired-profile-samples.md)
</dt> </dl>

 

 
