---
title: Risoluzione di più componenti di aggregazione che supportano la stessa interfaccia
description: Non è raro che due estensioni espongano la stessa interfaccia a ADSI.
ms.assetid: 87cb1a17-04f7-4ad0-989a-a9506dfdca05
ms.tgt_platform: multiple
keywords:
- Risoluzione di più componenti di aggregazione che supportano la stessa interfaccia ADSI
- risoluzione di più componenti di aggregazione che supportano la stessa interfaccia ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f58b7b606a05543444a172e2f76b436f6048431
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297659"
---
# <a name="resolution-of-multiple-aggregation-components-supporting-the-same-interface"></a>Risoluzione di più componenti di aggregazione che supportano la stessa interfaccia

Non è raro che due estensioni espongano la stessa interfaccia a ADSI. In tal caso, si applicano le regole seguenti:

-   Se un'interfaccia, ad esempio **IMyInterface**, è supportata da entrambi gli oggetti Aggregator (ADSI) ed any Extension, **QueryInterface** restituisce sempre il **IMyInterface** per ADSI.
-   Se un'interfaccia, ad esempio **IMyInterface**, non è supportata da Aggregator (ADSI), ma è supportata da più di un oggetto di estensione, **QueryInterface** restituisce il **IMyInterface** del primo oggetto di estensione elencato nel registro di sistema che supporta l'interfaccia.

Tenere presente che l'ordine dei componenti nel registro di sistema influiscono anche sulla risoluzione dei conflitti di nome in automazione. Per altre informazioni, vedere [risoluzione dei conflitti di nome di funzione/proprietà in automazione nelle estensioni](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md).

 

 




