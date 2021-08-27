---
title: Intestazione dell'interfaccia IDL
description: L'intestazione dell'interfaccia IDL specifica le informazioni sull'intera interfaccia. A differenza di ACF, l'intestazione dell'interfaccia contiene attributi indipendenti dalla piattaforma.
ms.assetid: 667e5228-3ea7-4910-90b9-999e6fd705e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33c176078c370819331405b070ffa832384584a944b65fae771b9a2044a178e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924270"
---
# <a name="the-idl-interface-header"></a>Intestazione dell'interfaccia IDL

L'intestazione dell'interfaccia IDL specifica le informazioni sull'intera interfaccia. A differenza di ACF, l'intestazione dell'interfaccia contiene attributi indipendenti dalla piattaforma.

Gli attributi nell'intestazione dell'interfaccia sono globali per l'intera interfaccia. In altre informazioni, si applicano all'interfaccia e a tutte le relative parti. Questi attributi sono racchiusi tra parentesi quadre all'inizio della definizione dell'interfaccia. Un esempio è illustrato nella definizione dell'interfaccia seguente:

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface INTERFACENAME
{

}
```

Si noti che l'intestazione dell'interfaccia contiene **\[** [**gli attributi uuid**](/windows/desktop/Midl/uuid) **\]** e **\[** [**version.**](/windows/desktop/Midl/version) **\]** Poiché rappresentano rispettivamente L'UUID e il numero di versione dell'interfaccia, sono attributi dell'intera interfaccia.

Anche il corpo dell'interfaccia può contenere attributi. Tuttavia, non sono applicabili all'intera interfaccia. Fanno riferimento a elementi specifici nell'interfaccia, ad esempio parametri di procedura remota.

Per una descrizione completa degli attributi dell'intestazione IDL, vedere [midl Language Reference](/windows/desktop/Midl/midl-language-reference).

 

 