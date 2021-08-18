---
title: Proprietà e attributi ADSI
description: Gli attributi vengono talvolta definiti proprietà. Ciò può causare confusione. Questa documentazione usa le definizioni seguenti per proprietà e attributi.
ms.assetid: 8e391d36-5a8d-4960-805a-0caf281cab80
ms.tgt_platform: multiple
keywords:
- Proprietà e attributi ADSI ADSI
- ADSI ADSI , uso, accesso e modifica di dati, proprietà e attributi
- proprietà ADSI
- attributi ADSI
- proprietà ADSI , definite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b05637cada9a62cee129e9645385233b4700cbf2762b9446ba9a871d1897d440
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082795"
---
# <a name="adsi-properties-and-attributes"></a>Proprietà e attributi ADSI

Gli attributi vengono talvolta definiti proprietà. Ciò può causare confusione. Questa documentazione usa le definizioni seguenti per proprietà e attributi.

Le proprietà sono valori denominati associati a un oggetto di programmazione. Ad esempio, [**l'interfaccia IADs**](/windows/desktop/api/Iads/nn-iads-iads) espone proprietà come [**Class**](iads-property-methods.md) e **Name.**

Gli attributi sono i dati associati agli oggetti in un servizio directory. Ad esempio, un oggetto utente avrà un attributo denominato **cn** che contiene una stringa che rappresenta il nome distinto comune o relativo dell'oggetto. Gli attributi sono accessibili tramite metodi di interfaccia ADSI, ad esempio [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) e [**IADs.Put.**](/windows/desktop/api/Iads/nf-iads-iads-put)

Per altre informazioni sulle proprietà e sugli attributi ADSI, vedere:

-   [Cache degli attributi ADSI](the-adsi-attribute-cache.md)
-   [Attributi a valore singolo e multiplo](single-vs--multiple-value-attributes.md)
-   [Attributi operativi di Active Directory](active-directory-operational-attributes.md)

 

 




