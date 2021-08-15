---
title: Proprietà connessione MS-CHAPv2 EAP
description: Informazioni sulle proprietà di connessione MS-CHAPv2 EAP. Vedere un esempio che è un'istanza dello schema legacy mschapv2connectionpropertiesv1.
ms.assetid: d6a057e0-56f6-4a31-9391-fde631ac2898
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28ec894f8e95aa08e68aae418ed2b194c02a90cd008b9ac8d810d3c497e76f9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984261"
---
# <a name="eap-ms-chapv2-connection-properties"></a>Proprietà connessione MS-CHAPv2 EAP

Questo esempio è un'istanza dello schema legacy [mschapv2connectionpropertiesv1.](mschapv2connectionpropertiesv1schema-schema.md)

``` syntax
  <?xml version="1.0" ?> 
  <EapHostConfig xmlns="https://www.microsoft.com/provisioning/EapHostConfig" 
    xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon" 
    xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodConfig">
    <EapMethod>
      <eapCommon:Type>26</eapCommon:Type> 
      <eapCommon:AuthorId>0</eapCommon:AuthorId> 
    </EapMethod>
    <Config xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapConnectionPropertiesV1" 
      xmlns:msPeap="https://www.microsoft.com/provisioning/MsPeapConnectionPropertiesV1" 
      xmlns:msChapV2="https://www.microsoft.com/provisioning/MsChapV2ConnectionPropertiesV1">
      <baseEap:Eap>
        <baseEap:Type>26</baseEap:Type> 
        <msChapV2:EapType>
        <msChapV2:UseWinLogonCredentials>false</msChapV2:UseWinLogonCredentials> 
        </msChapV2:EapType>
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

 

 




