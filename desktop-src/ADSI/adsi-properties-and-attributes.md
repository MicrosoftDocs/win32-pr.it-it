---
title: Proprietà e attributi ADSI
description: Gli attributi vengono talvolta indicati come proprietà. Questo può causare confusione. In questa documentazione vengono utilizzate le seguenti definizioni per proprietà e attributi.
ms.assetid: 8e391d36-5a8d-4960-805a-0caf281cab80
ms.tgt_platform: multiple
keywords:
- Proprietà ADSI e attributi ADSI
- ADSI ADSI, uso, accesso e manipolazione di dati, proprietà e attributi
- Proprietà ADSI
- attributi ADSI
- Proprietà ADSI, defined
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10c7b1dca9882f53b7fa746121ed431ace7f9af7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297701"
---
# <a name="adsi-properties-and-attributes"></a>Proprietà e attributi ADSI

Gli attributi vengono talvolta indicati come proprietà. Questo può causare confusione. In questa documentazione vengono utilizzate le seguenti definizioni per proprietà e attributi.

Le proprietà sono valori denominati associati a un oggetto di programmazione. Ad esempio, l'interfaccia [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) espone proprietà quali la [**classe**](iads-property-methods.md) e il **nome**.

Gli attributi sono i dati associati agli oggetti in un servizio directory. Ad esempio, un oggetto utente avrà un attributo denominato **CN** che contiene una stringa che rappresenta il nome distinto comune o relativo dell'oggetto. Gli attributi sono accessibili tramite metodi di interfaccia ADSI, ad esempio [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) e [**IADs. Put**](/windows/desktop/api/Iads/nf-iads-iads-put).

Per ulteriori informazioni sulle proprietà e sugli attributi ADSI, vedere:

-   [Cache degli attributi ADSI](the-adsi-attribute-cache.md)
-   [Attributi singolo e più valori](single-vs--multiple-value-attributes.md)
-   [Active Directory gli attributi operativi](active-directory-operational-attributes.md)

 

 




