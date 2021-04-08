---
title: Proprietà di connessione SDK
description: Informazioni sulle proprietà di connessione dell'SDK. Vedere un esempio che è un'istanza dello schema nativo eaphostconfig.
ms.assetid: 34c9b423-4f4c-484e-86d7-4594566cd396
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edbd404246055a3c94daff4c029a94f16adfe51b
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "103734599"
---
# <a name="sdk-connection-properties"></a>Proprietà di connessione SDK

Questo esempio è un'istanza dello schema nativo [eaphostconfig](eaphostconfigschema-schema.md) .

``` syntax
  <?xml version="1.0" ?> 
  <EapHostConfig xmlns="https://www.microsoft.com/provisioning/EapHostConfig" 
    xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon" 
    xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodConfig">
    <EapMethod>
      <eapCommon:Type>40</eapCommon:Type> 
      <eapCommon:AuthorId>100</eapCommon:AuthorId> 
    </EapMethod>
    <Config>
      <EapType>40</EapType> 
      <ConfigData>seatac.bingo.com</ConfigData> 
    </Config>
  </EapHostConfig>
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà di connessione](connection-profiles.md)
</dt> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> </dl>

 

 




