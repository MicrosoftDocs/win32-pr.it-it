---
title: ServiceMonikerSample
description: Questo esempio illustra un client che può essere usato con l'esempio MetadataExchange TCP. Usa il moniker del servizio WCF.
ms.assetid: cfcff5ee-c0e1-4694-831e-fed0bd0e9855
keywords:
- ServiceMonikerSample Windows Web Services API
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dffac8b7eb4c9bdb92d4622452c15d56f53a514ba94fa908d38e1232dfec95f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026169"
---
# <a name="servicemonikersample"></a>ServiceMonikerSample

Questo esempio illustra un client che può essere usato con l'esempio MetadataExchange TCP. Usa il moniker del servizio WCF.

-   [PurchaseOrderClient.vbs](#purchaseorderclientvbs)

## <a name="purchaseorderclientvbs"></a>PurchaseOrderClient.vbs


```VB
set obj = GetObject("service:mexAddress='net.tcp://localhost/example/mex', address='net.tcp://localhost/example', contract='IPurchaseOrder', contractNamespace='http://example.org', binding=PurchaseOrderBinding, bindingNamespace='http://example.org'")
for i = 1 to 100
 orderId = obj.Order(i,"Pencil", date)
 Wscript.Echo orderId, date
Next 


```



 

 




