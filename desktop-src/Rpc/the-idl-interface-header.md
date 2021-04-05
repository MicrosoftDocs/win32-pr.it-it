---
title: Intestazione dell'interfaccia IDL
description: L'intestazione dell'interfaccia IDL specifica le informazioni sull'interfaccia nel suo complesso. A differenza di ACF, l'intestazione dell'interfaccia contiene attributi indipendenti dalla piattaforma.
ms.assetid: 667e5228-3ea7-4910-90b9-999e6fd705e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8abce6204fdc09ed74a63a85e9366125dbef8e35
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118391"
---
# <a name="the-idl-interface-header"></a>Intestazione dell'interfaccia IDL

L'intestazione dell'interfaccia IDL specifica le informazioni sull'interfaccia nel suo complesso. A differenza di ACF, l'intestazione dell'interfaccia contiene attributi indipendenti dalla piattaforma.

Gli attributi nell'intestazione dell'interfaccia sono globali per l'intera interfaccia. Ovvero si applicano all'interfaccia e a tutte le relative parti. Questi attributi sono racchiusi tra parentesi quadre all'inizio della definizione dell'interfaccia. Un esempio è illustrato nella definizione di interfaccia seguente:

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface INTERFACENAME
{

}
```

Si noti che l'intestazione dell'interfaccia contiene gli **\[** attributi [**UUID**](/windows/desktop/Midl/uuid) **\]** e **\[** [**Version**](/windows/desktop/Midl/version) **\]** . Poiché rappresentano rispettivamente l'UUID e il numero di versione dell'interfaccia, sono attributi dell'intera interfaccia.

Il corpo dell'interfaccia può contenere anche attributi. Tuttavia, non sono applicabili all'intera interfaccia. Si riferiscono a elementi specifici nell'interfaccia, ad esempio i parametri di procedura remota.

Per una descrizione completa degli attributi dell'intestazione IDL, vedere la Guida di [riferimento al linguaggio MIDL](/windows/desktop/Midl/midl-language-reference).

 

 