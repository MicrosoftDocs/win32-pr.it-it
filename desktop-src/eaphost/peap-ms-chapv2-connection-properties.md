---
title: Proprietà connessione MS-CHAPv2 PEAP
description: Informazioni sulle proprietà di connessione MS-CHAPv2 PEAP. Vedere un esempio che è un'istanza dello schema legacy mschapv2connectionpropertiesv1.
ms.assetid: a289343a-b702-4be2-baf5-2d004a8a8fea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f55ce0f6b561fe32169768452d409cb7d51084589b0f3a3dca49ff9022fffb45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983911"
---
# <a name="peap-ms-chapv2-connection-properties"></a>Proprietà connessione MS-CHAPv2 PEAP

Questo esempio è un'istanza dello schema legacy [mschapv2connectionpropertiesv1.](mschapv2connectionpropertiesv1schema-schema.md)

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

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà connessione](connection-profiles.md)
</dt> <dt>

[Schema EAPHost e legacy](eaphost-schemas.md)
</dt> </dl>

 

 




