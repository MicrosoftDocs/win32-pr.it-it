---
title: Sicurezza del client durante una chiamata asincrona
description: Sicurezza del client durante una chiamata asincrona
ms.assetid: 26d1f2c2-cb08-49f1-8beb-b99b029f0d8c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bea2f83bf6341704dd0265a37ec2f64b79e9b2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712937"
---
# <a name="client-security-during-an-asynchronous-call"></a>Sicurezza del client durante una chiamata asincrona

La gestione proxy creata da MIDL per gli oggetti che usano il marshalling standard implementa l'interfaccia [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) . I client possono gestire la sicurezza delle chiamate con marshalling eseguendo una query per **IClientSecurity** sull'oggetto chiamata e ottenendo o modificando le impostazioni di sicurezza.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esecuzione di una chiamata asincrona](making-an-asynchronous-call.md)
</dt> </dl>

 

 




