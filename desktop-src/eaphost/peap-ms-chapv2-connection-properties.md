---
title: Proprietà di connessione MS-CHAPv2 PEAP
description: Informazioni sulle proprietà di connessione MS-CHAPv2 PEAP. Vedere un esempio che è un'istanza dello schema legacy mschapv2connectionpropertiesv1.
ms.assetid: a289343a-b702-4be2-baf5-2d004a8a8fea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcac1210eb0fb1606600366618b28c0a4276fa80
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "104474534"
---
# <a name="peap-ms-chapv2-connection-properties"></a><span data-ttu-id="1ef77-104">Proprietà di connessione MS-CHAPv2 PEAP</span><span class="sxs-lookup"><span data-stu-id="1ef77-104">PEAP MS-CHAPv2 Connection Properties</span></span>

<span data-ttu-id="1ef77-105">Questo esempio è un'istanza dello schema legacy [mschapv2connectionpropertiesv1](mschapv2connectionpropertiesv1schema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="1ef77-105">This sample is an instance of the [mschapv2connectionpropertiesv1](mschapv2connectionpropertiesv1schema-schema.md) legacy schema..</span></span>

``` syntax
  <?xml version="1.0" ?> 
  <EapHostConfig xmlns="https://www.microsoft.com/provisioning/EapHostConfig" 
    xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon" 
    xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodConfig">
    <EapMethod>
      <eapCommon:Type>25</eapCommon:Type> 
      <eapCommon:AuthorId>0</eapCommon:AuthorId> 
    </EapMethod>
    <Config xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapConnectionPropertiesV1"
      xmlns:msPeap="https://www.microsoft.com/provisioning/MsPeapConnectionPropertiesV1" 
      xmlns:msChapV2="https://www.microsoft.com/provisioning/MsChapV2ConnectionPropertiesV1">
      <baseEap:Eap>
        <baseEap:Type>25</baseEap:Type> 
        <msPeap:EapType>
          <msPeap:ServerValidation>
            <msPeap:DisableUserPromptForServerValidation>false</msPeap:DisableUserPromptForServerValidation> 
            <msPeap:TrustedRootCA /> 
          </msPeap:ServerValidation>
          <msPeap:FastReconnect>true</msPeap:FastReconnect> 
          <msPeap:InnerEapOptional>0</msPeap:InnerEapOptional> 
          <baseEap:Eap>
            <baseEap:Type>26</baseEap:Type> 
            <msChapV2:EapType>
              <msChapV2:UseWinLogonCredentials>false</msChapV2:UseWinLogonCredentials> 
            </msChapV2:EapType>
          </baseEap:Eap>
          <msPeap:EnableQuarantineChecks>false</msPeap:EnableQuarantineChecks> 
          <msPeap:RequireCryptoBinding>false</msPeap:RequireCryptoBinding> 
          <msPeap:PeapExtensions /> 
        </msPeap:EapType>
      </baseEap:Eap>
    </Config>
  </EapHostConfig>
```

## <a name="related-topics"></a><span data-ttu-id="1ef77-106">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1ef77-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ef77-107">Proprietà di connessione</span><span class="sxs-lookup"><span data-stu-id="1ef77-107">Connection Properties</span></span>](connection-profiles.md)
</dt> <dt>

[<span data-ttu-id="1ef77-108">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="1ef77-108">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> </dl>

 

 




